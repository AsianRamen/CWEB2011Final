<%@ Page Title="" Language="C#" MasterPageFile="~/MasterPage.Master" AutoEventWireup="true" CodeBehind="HomePage.aspx.cs" Inherits="TheProject.HomePage" %>

<asp:Content ID="Content1" ContentPlaceHolderID="head" runat="server">
</asp:Content>

<asp:Content ID="Content2" ContentPlaceHolderID="ContentPlaceHolder1" runat="server">
    <div id="Navigation">
        <div id="navs">
            <asp:Button runat="server" ID="HButton" Text="Home" OnClick="HButton_Click"/>
            <asp:Button runat="server" ID="Contact" Text="Contact" OnClick="Contact_Click"/>
            <asp:Button runat="server" ID="About" Text="About" OnClick="About_Click"/>
        </div>
        <div id="pageTitle">
            <asp:Label runat="server"><u>Welcome to our Products page</u></asp:Label><br /><br />
        </div>

        <div id="creds">
            <asp:Button runat="server" ID="Reg" Text="Register" OnClick="Reg_Click"/>
            <asp:Button runat="server" ID="Login" Text="Login" OnClick="Login_Click"/>
        </div>
        
    </div>
    <div id="Search">
        <div id="productSearch">
            <asp:Label runat="server" ID="Select" Text="Please select a product: "/>
            &nbsp;&nbsp;
            <asp:DropDownList runat="server" ID="CategoryDDL" AutoPostBack="true" OnSelectedIndexChanged="CategoryDDL_SelectedIndexChanged" />
            <asp:DropDownList runat="server" ID="SubDDL"  AutoPostBack="true" Visible="false" OnSelectedIndexChanged="SubDDL_SelectedIndexChanged">
            </asp:DropDownList>
            <asp:DropDownList runat="server" ID="ProductDDL" AutoPostBack="true" Visible="false">
            </asp:DropDownList>
            <asp:Button runat="server" ID="Add2Cart" Text="Add to Cart" />
        </div>
    </div>
    <div id="MainContent">
        <div id="product">
            <asp:Label runat="server" ID="productInfo" />
        </div>
    </div>
    <div id="Error">
        <asp:Label runat="server" ID="ErrorLabel" Visible="false" />
    </div>
</asp:Content>
