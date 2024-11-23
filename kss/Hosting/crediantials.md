Internship123@KSS
--------------------
React Hosting
----------------

Step 1:
	Find your destination url where your website will be hosted on
	Ex : http://thecodekings.eprogrammers.in/Amit/react/
	Add an attribute on package.json file:
	"homepage":"http://thecodekings.eprogrammers.in/Amit/react/"

Step 2:
	If you are usign <BrowserRouter> then replace this by
		import { BrowserRouter, Routes, Route } from "react-router-dom"; 
			To -> import { HashRouter as Router, Routes, Route } from "react-router-dom";
	and <BrowserRouter> To -> <Router>
	
Step 3:
	Then run command 
	-> npm run build

Step 4: 
	After build look into build directory and add an .htaccess file(it's an file name not any extension please do not write anyting before '.'). Copy and paste below code in .htaccess file :
		RewriteEngine On
		RewriteCond %{REQUEST_FILENAME} !-f
		RewriteCond %{REQUEST_FILENAME} !-d
		RewriteRule ^ /index.html [L]
		
Step 5:
	Upload your files(Located in build directory) in your hosting server.
	
