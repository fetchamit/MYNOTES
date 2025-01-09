#Integrating Google Recaptcha in .NET Core 8.0
---------------------------------------------

## What is reCAPTCHA ?
* reCAPTCHA is a free service from Google that helps protect websites from spam and abuse.

## Steps to integrate recaptcha:
1. Generate Site Key and secret key from official website of google recaptcha.
  * Open your borwser and sign in your gmail account.
  * Open recaptcha admin portal

        https://www.google.com/recaptcha/admin/create

  * Create a new captcha by specifying basic details. It will generate two keys - Site Key and Secrate Key.
      * Site Key : It is for client side integration of google recaptcha.
      * Secrate Key : It is for server side integration of google recaptcha.

2. Write Captcha key in secret key in your project
  * However you can directly write keys inside view page and controller but for security reason it is recommended to write that keys inside `appsettings.json` file of project.
  * Ex:

        "CaptchaKeys":
        {
           SiteKey:"dajldajldaj flajdljljaljdla a",
           SecretKey:"dajlkdjaldjaldjaldjaljdla lj akldjal"
        }   

3. Integrate client side part in your view page using HTML & JavaScript.
  * To perform recaptcha integration open below website-

        https://developers.google.com/recaptcha/docs/display

  * Add recaptcha div tag inside your web form just before the submit button.

        <div class="g-recaptcha" data-sitekey="your_site_key"></div>
  * In view page Read site key of `captcha` from your `appsetting.json` file by using `IConfiguration` interface and specify that key in `data-sitekey` attribute of above div tag.
  * Ex:

         @inject IConfiguration config
          @{
              var MySiteKey=config["CaptchaKeys:SiteKey"];
           }          

        <div class="g-recaptcha" data-sitekey="@MySiteKey"></div>

  * Add link of recaptcha api in view page as shown below:

        <script src="https://www.google.com/recaptcha/api.js" async defer></script>


4. Integrate server side part in your action method inside controller.
  * In recaptcha developer documentation you will get a link at left corner - "Verify the User Response". Click on this link.
  * Read a post parameter in your action method having name `g-recaptcha-response`.
  * Ex:

        string captcha=Request.Form["g-recaptcha-response"];

  * Request below recaptcha API to verify captcha response-

        https://www.google.com/recaptcha/api/siteverify

  * Note :
    * You must have to specify two parameters in above API- `secret` and `response`.
    * Secret will contains Secret Key of captcha  and response will contains user response of captcha that we have accepted by using `g-recaptcha-response` parameter.

  * Read Secret key from `appsettings.json` file inside your controller. For that we also have to create a constructor of controller to instantiate `IConfiguration` Interface.
  * Ex:

        private IConfiguration configure;
        public HomeController(IConfiguration conf)
        {
          configure=conf;
        }

  * Note: Write below line inside your post action method-
  * Ex:

        var SecretKey = configuration.GetSection("Captcha").GetSection("SecretKey").Value;

  * Now Create object of `WebClient` class that is used to open an URL from background services.
  * Ex:

        WebClient wc=new WebClient();
        string API_URL="https://www.google.com/recaptcha/api/siteverify?secret="+SecretKey+"&response="+resp;
        string result=wc.DownloadString(API_URL);

  * Now check if result variable contains `true/false` value and based on that show response to user.

5. Run and test the recaptcha integration.
