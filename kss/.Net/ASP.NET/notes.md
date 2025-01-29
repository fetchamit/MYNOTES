# What is ASP.NET

## ASP .NET web controls / ASP .NET Controls / ASP.NET Form Controls:

syntax:

    <asp:ControlName ID="Id_Of_Control" runat="Server"/>
    OR
    <asp:ControlName ID="id_of_control" runat="Server"></asp:ControlName>

Ex:

    <asp:Button ID="BtnSave" runat="Server" Text="Save"/>
    <asp:TextBox ID="TxtName" runat="Server"/>

Note: ASP.NET controls are server side controls and all controls are defined in form of class.

### Some Common properties of ASP.NET Controls:
1. Text: Used to get/set the content of a tag.
2. BackColor:
3. ForeColor:
4. runat:
5. ID: Used to identify a tab uniquely.
6. CssClass:
7. Width:
8. Height:

* Note: ASP.NET uses concept of code behind. It means in ASP.NET there is always a backend page having same name as frontend page.
* Ex: Front End Page :`Login.aspx`
*   Backend Page: `Login.aspx.cs`
* Use below form tag in ASP.NEE:

       <form runat="server">

        </form>

















    
