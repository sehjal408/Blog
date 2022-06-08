**Date: 1-Feb-2022**

## Introduction to Linux and Installing Ubuntu

Linux is an open-source operating system like other operating systems such as Microsoft Windows, Apple Mac OS, iOS, Google android, etc. An operating system is a software that enables the communication between computer hardware and software. It conveys input to get processed by the processor and brings output to the hardware to display it. This is the basic function of an operating system. Its main benefits are –
- Being open-source, anyone with programming knowledge can modify it. 
- The Linux operating systems now offer millions of programs/applications and Linux softwares to choose from, most of them are free! 
- Once you have Linux installed you no longer need an antivirus! Linux is a highly secure system. More so, there is a global development community constantly looking at ways to enhance its security. With each upgrade, the OS becomes more secure and robust 
- Linux freeware is the OS of choice for Server environments due to its stability and reliability (Mega-companies like Amazon, Facebook, and Google use Linux for their Servers). A Linux based server could run non-stop without a reboot for years on end. 
<br>

**Date: 2-Feb-2022**

## Download the linux distribution of your choice. 

- Creating Boot pendrive using rufus.exe in windows. 
- Restart the system and open boot menu using boot key. (Eg.- F8, F2 etc.) 
- Select your boot device in boot menu. 
- Select Install Ubuntu then Click Noraml Installation. 
- Select where to install alongside window or Erase disk or something else. 
- Then Click next and start ubuntu installation. 
- For More detail about Installation Guide [Click here](https://phoenixnap.com/kb/install-ubuntu-20-04)
<br>

**Date: 3-Feb-2022**

## Introduction to LAMP Stack

A “LAMP” stack is a group of open-source software that is typically installed together to enable a server to host dynamic websites and web apps. LAMP consists of four components necessary to establish a fully functional web development environment. The first letters of the components' names make up the LAMP acronym:

- Linux is an operating system used to run the rest of the components. 
- Apache HTTP Server is a web server software used to serve static web pages. 
- MySQL is a relational database management system used for creating and managing web databases, but also for data warehousing, application logging, e-commerce, etc. 
- PHP, Perl, and Python are programming languages are used to create web applications. 
- Installing lamp on Ubuntu System. 
- Verifying by run LAMP on localhost. 
<br>

**Date: 4-Feb-2022**

## Run Cgi Script

A CGI script is any program that runs on a web server. CGI stands for Common Gateway Interface. CGI defines a standard way in which information may be passed to and from the browser and server. Any program or script that can process information according to the CGI specification can, in theory, be used to code a CGI script.
- Create a cgi scirpt. 
- Run it on Localhost using Apache Server. 
<br>

**Date: 5-Feb-2022**

## Introduction to Frappe

Frappe, pronounced fra-pay, is a full stack, batteries-included, web framework written in Python and Javascript with MariaDB as the database. It is the framework which powers erpnext, is pretty generic and can be used to build database driven apps.

The key difference in Frappe compared to other frameworks is that meta-data is also treated as data. This enables you to build front-ends very easily. We believe in a monolithic architecture, so Frappe comes with almost everything you need to build a modern web application. It has a full featured Admin UI called the Desk that handles forms, navigation, lists, menus, permissions, file attachment and much more out of the box.
<br>
<br>

**Date: 7-Feb-2022**

## Installation of Frappe FrameWork on linux based System:

Installed frappe from https://github.com/D-codE-Hub/ERPNext-installation-Guide/blob/main/README.md documentation till step 13.<br>
Pre-requisites for frappe framework:<br>
  Python 3.6+<br>
  Node.js 14+<br>
  Redis 5                                      
  MariaDB 10.3.x / Postgres 9.5.x            
  yarn 1.12+                            
  pip 20+          
<br>

**Date: 8-Feb-2022**

## Create a site on frappe and run on local server.

- First, Go in bench folder. 
- Then, Start bench
- Create a site using following command: 
                                             `bench new-site <site-name>`
- This command will create a new database, so you need to enter your MySQL root password. It will also ask to set the password for the Administrator user, just set a password that you won't forget.
- Access the site on localhost in the browser. 
(However, bench allows you to create multiple sites and access them separately in the browser on the same port. This is what we call multi-tenancy support in bench. So to access another site we can use the command: 
                                              `bench use <site-name> `
This command will set the current site.)

- Enter Administrator as the user and password that you set while creating the site. After successful login, complete the wizard by selecting language etc. Then you will able to see the desk.
<br>

**Date: 9-Feb-2022**

## Create an app and install on site in frappe

Create an app with command:`bench new-app <app-name>`
This will ask for App’s Title, Description, Publisher, Email, Icon etc.
Fill all details and an app with name  of your app will be created in the apps folder.

Now install this app on the site that we created earlier with the following command: ` bench –site <site-name> install-app <app-name>`
With this the app will installed on site. To check if app installed, Go on site, login with username and password and click on about.
Here, two apps were installed, first is Frappe (it is automatically installed when we create site), second is the app we created.

I created an app named library_management

The app will create certains file in the app folder the whole structure is:
- library_management: This directory will contain all the source code for your app 
- public: Store static files that will be served from Nginx in production 
- templates: Jinja templates used to render web views 
- www: Web pages that are served based on their directory path 
- library_management: Default Module bootstrapped with app 
- modules.txt: List of modules defined in the app 
- patches.txt: Patch entries for database migrations 
- hooks.py: Hooks used to extend or intercept standard functionality provided by the framework 
- requirements.txt: List of Python packages that will be installed when you install this app 
<br>

**Date: 10-Feb-2022**

## Create Library Management System in frappe.

I learned some new commands of bench that are as following:

`bench –version`: To check the version of bench.

`bench –site <site-name> list-apps`: This will give the list of all apps that are installed on site.

`bench –site <site-name> console`: To access the python console.

`bench –site <site-name> mariadb`: To access the mariadb console.

`bench backup`: Ceate a backup of the default site.

`bench –site <site-name> set-admin-password <password>`: This will reset the administrator password.

`bench remove-app <app-name>`: This will remove app from bench.

I started building a simple Library Management System in which the Librarian can log in and manage Articles and Memberships. This will include:
1. Article: A Book or similar item that can be rented. 
2. Library Member: A user who is subscribed to a membership. 
3. Library Transaction: An Issue or Return of an article. 
4. Library Membership: A document that represents an active membership of a Library Member. 
5. Library Settings: Settings that define values like Loan Period and the maximum number of articles that can be issued at a time. 
<br>

**Date: 11-Feb-2022**

## Introduction to Doc Types in Frappe

I follow https://frappe.school/courses/frappe-framework-tutorial tutorial for creating LMS. 

A DocType is the core building block of any application based on the Frappe Framework. It describes the Model and the View of your data. It contains what fields are stored for your data, and how they behave with respect to each other. It contains information about how your data is named.
When you create a DocType, a JSON object is created which in turn creates a database table.
To enable rapid application development, Frappe Framework follows some standard conventions.
1. DocType is always singular. If you want to store a list of articles in the database, you should name the doctype Article. 
2. Table names are prefixed with tab. So the table name for Article doctype is tabArticle. 
3. The standard way to create a DocType is by typing new doctype in the search bar in the Desk. 

A DocType not only stores fields, but also other information about how your data behaves in the system. We call this Meta. Since this meta-data is also stored in a database table, it makes it easy to change meta-data on the fly without writing much code.

Before we can create DocTypes, we need to enable developer mode on with command: `bench set-config -g developer_mode true`. This will enable boilerplate creation when we create doctypes and we can track them into version control with our app.
<br>

**Date: 12-Feb-2022**

## Creating Article DocType for LMS

Go to the doctype list using the Awesomebar. This list will include Doc Types bundled with the framework.
 
- Enter the Name for the DocType 
- Then select a Module Named LMS which we have created earlier or we can create a new module. 
- We require fileds for the doctype. We created the required below fields in the doctype: 
  - Article Name (Data, Mandatory) 
  - Image (Attach Image) 
  - Author (Data) 
  - Description (Text Editor) 
  - ISBN (Data) 
  - Status (Select, here we can add a drodown with options Issued and Available) 
  - Publisher (Data) 

- After adding the fields, click on Save. 

Our doctype is created and we can now Add data to our doctype. Now We can go to the article list and create " Article ". As we created new article the data wiil be pushed to the database in the form of tables and we can also check its data by giving command in the terminal
`bench --site library.test mariadb `

Here it will show all the database of a perticluar site. And we can check and update our data using differnet sql commands by selecting differnet databasea and tables.
<br>

**Date: 14-Feb-2022**

## Creating Different DocTypes in LMS

### Library Member

Create “Library Member” Doctype with following fields.

- First Name (Data, Mandatory)
- Last Name ( Data ) 
- Full Name (Data, Read Only) 
- Email Address (Data) 
- Phone (Data) 

Write code in python controller class such that Full Name is computed automatically from First Name and Last Name. Make the following changes in library_member.py :

```
class LibraryMember(Document):
     #this method will run every time a document is saved
       def before_save(self):
          self.full_name = f'{self.first_name} {self.last_name or ""}'
          
```
### Library Membership

Create “Library Membership” Doctype with the following fields:

- Library Member (Link, Mandatory)
- Full Name (Data, Read Only) 
- From Date (Date) 
- To Date (Date) 
- Paid (Check) 

Make this doctype a Submittable doctype. A Submittable doctype can have 3 states: Draft, Submitted, Cancelled. A document in the Draft state can be changed like any document, however once it is in Submitted state, the value of any field in the document cannot be changed. A Submitted document can be Cancelled, which makes the document invalid. 

Write the following code in library_membership.py that will make sure whenever a Library Membership is created, there is no active membership for the Member.

```
from __future__ import unicode_literals

import frappe
from frappe.model.document import Document

class LibraryMembership(Document):
    # check before submitting this document
    def before_submit(self):
        exists = frappe.db.exists(
            "Library Membership",
            {
                "library_member": self.library_member,
                # check for submitted documents
                "docstatus": 1,
                # check if the membership's end date is later than this membership's start date
                "to_date": (">", self.from_date),
            },
        )
        if exists:
            frappe.throw("There is an active membership for this member")
```
<br>

<!----------------------------------------------------------------------------------------------------------------------------->
**Date : 15-Feb-2022** 
<h3 align='center'>Introduction to Education module in Erpnext</h3>
<p align="justify">The Education domain in ERPNext is designed to meet requirements of any organization which imparts knowledge and believe in doing so in an organized fashion. It has already been used at schools, colleges and even in private firms.
It helps you to effectively manage administration and allows you to focus on what is most important for your institute, to educate!</p>
<br>

<!----------------------------------------------------------------------------------------------------------------------------->
**Date : 17-Feb-2022** 
<h3 align='center'>Introduction to Jinja Templating</h3>
<p align='justify'>Jinja is a fast, expressive, extensible templating engine. Special placeholders in the template allow writing code similar to Python syntax. Then the template is passed data to render the final document.</p>

<br>

<!----------------------------------------------------------------------------------------------------------------------------->
**Date : 18-Feb-2022** 
<h3 align='center'>Trying to fetch data from database using Jinja Templating</h3>
- Write a Python Script for establish connection with Mariadb.
- Still it gives permission error try to solve it.

<br>

<!----------------------------------------------------------------------------------------------------------------------------->
**Date : 19-Feb-2022** 
<h3 align='center'>Working with server</h3>
- Resetting the password of server.
- Trying to install Erpnext on server.

<br>



<!----------------------------------------------------------------------------------------------------------------------------->
**Date : 23-Feb-2022** 
<h3 align='center'>How to use ssh</h3>
- Login to Server, Try to help other member to install ldap on server.
- Apply different permission related queries on database for different user.

<br>



<!----------------------------------------------------------------------------------------------------------------------------->
**Date : 07-Apr-2022** 
<h3 align='center'>Pagination on webpage in Library Management System</h3>
Firstly, i had created a library management system which had 5 doctypes. I gave web view to Article doctype. Then two files article_row.html and article.html were automatically generated in doctype folder. On webpageof Article doctype, whole list of articles was visible. But we wanted to apply pagination on the webpage. So i tried from a video (url: https://youtu.be/rDC-5ZJTmOU ). 
I created a file utils.py in library_management folder where i write the function of pagination for showing 4 articles on single page. 
Then in video, two files python and html were created in www > Article folder. I did the same but it didn't worked for me. After trying many ways, i created these files directly in www folder, then it worked. In python file, pagination function was called. And in html file i write jinja code to display the list on webpage and applied "previous" and "next" buttons. 
Now 4 articles are visible on webpage and previous, next buttons are working fine.

<br>
