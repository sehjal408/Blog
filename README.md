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

```py
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

```py
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

**Date: 15-Feb-2022**

## Library Transaction

Create another doctype named “Library Transaction” with following fields:

- Article (Link to Article)
- Library Member (Link to Library Member) 
- Type (Select with two options- Issue and Return) 
- Date (Date of Transaction) 

### Adding Validation for Transaction

When an Article is issued, we should verify whether the Library Member has an active membership. We should also check whether the Article is available for Issue. Let's write the code for these validations.
```py
from __future__ import unicode_literals

import frappe
from frappe.model.document import Document

class LibraryTransaction(Document):
    def before_submit(self):
        if self.type == "Issue":
            self.validate_issue()
            # set the article status to be Issued
            article = frappe.get_doc("Article", self.article)
            article.status = "Issued"
            article.save()

        elif self.type == "Return":
            self.validate_return()
            # set the article status to be Available
            article = frappe.get_doc("Article", self.article)
            article.status = "Available"
            article.save()

    def validate_issue(self):
        self.validate_membership()
        article = frappe.get_doc("Article", self.article)
        # article cannot be issued if it is already issued
        if article.status == "Issued":
            frappe.throw("Article is already issued by another member")

    def validate_return(self):
        article = frappe.get_doc("Article", self.article)
        # article cannot be returned if it is not issued first
        if article.status == "Available":
            frappe.throw("Article cannot be returned without being issued first")

    def validate_membership(self):
        # check if a valid membership exist for this library member
        valid_membership = frappe.db.exists(
            "Library Membership",
            {
                "library_member": self.library_member,
                "docstatus": 1,
                "from_date": ("<", self.date),
                "to_date": (">", self.date),
            },
        )
        if not valid_membership:
            frappe.throw("The member does not have a valid membership")
```
<br>

**Date: 16-Feb-2022**

## Library Settings

Create the last doctype for our app: Library Settings. It will have the following fields:

- Loan Period - Will define the loan period in number of days 
- Maximum Number of Issued Articles - Restrict the maximum number of articles that can be issued by a single member 

Since we don't need to have multiple records for these settings, we will enable Is Single for this doctype. After creating the doctype, click on Go to Library Settings, to go to the form and set the values for Loan Period and Maximum Number of Issued Articles.
Make the change in Library Membership such that, the To Date automatically computed based on the Loan Period and the From Date.
```py
# get loan period and compute to_date by adding loan_period to from_date
        loan_period = frappe.db.get_single_value("Library Settings", "loan_period")
        self.to_date = frappe.utils.add_days(self.from_date, loan_period or 30)
```

Now, make the change in Library Transaction such that when an Article is Issued, it checks whether the maximum limit is reached.
```py
    def validate_maximum_limit(self):
        max_articles = frappe.db.get_single_value("Library Settings", "max_articles")
        count = frappe.db.count(
            "Library Transaction",
            {"library_member": self.library_member, "type": "Issue", "docstatus": 1},
        )
        if count >= max_articles:
            frappe.throw("Maximum limit reached for issuing articles")
```


### Web View Pages

Web View Pages are server rendered pages for website visitors. To see available articles on website, we can create webpage for articles. To enable Web View:

Go to Article doctype, and scroll down to the Web View section.
1. Enable Has Web View and Allow Guest to View 
2. Enter articles in the Route field 
3. Add fields named Route and Published in the fields table 
4. Click on Save 
<br>

**Date: 17-Feb-2022**

## Web View Pages

When we made Article a web view, two html files were created namely: article.html and article_row.html. We can use Bootstrap 4 to style pages. We can write code in html files for styling of webpage. 

Write following code in article.html file:
```html

<div class="py-20 row">
    <div class="col-sm-2">
        <img alt="{{ title }}" src="{{ image }}">
    </div>
    <div class="col">
        <h1>{{ title }}</h1>
        <p class="lead">By {{ author }}</p>
        <div>
            {%- if status == 'Available' -%}
            <span class="badge badge-success">Available</span>
            {%- elif status == 'Issued' -%}
            <span class="badge badge-primary">Issued</span>
            {%- endif -%}
        </div>
        <div class="mt-4">
            <div>Publisher: <strong>{{ publisher }}</strong></div>
            <div>ISBN: <strong>{{ isbn }}</strong></div>
        </div>
        <p>{{ description }}</p>
    </div>
</div>

```
Edit the article_row.html and add the following HTML:
```html
<div class="py-8 row">
    <div class="col-sm-1">
        <img alt="{{ doc.name }}" src="{{ doc.image }}">
    </div>
    <div class="col">
        <a class="font-size-lg" href="{{ doc.route }}">{{ doc.name }}</a>
        <p class="text-muted">By {{ doc.author }}</p>
    </div>
</div>
```
Now following webpage will visible on the website:

Now, click on Article to view its details. Now the following webpage will visible :

<br>

**Date: 18-Feb-2022**

## Introduction to Selenium and Budibase

Selenium is an open-source tool that automates web browsers. Selenium is browser automation tool by which you can create a script which automatically done task like fill credential and click for search.

Budibase is a modern open-source development platform used for building, designing, automating, self-hosting, and shipping internal applications, including internal tools, admin panels, client portals, etc.

It is a no-code or low-code platform that eliminates all the extra repetition by involving the essential elements that are required for connecting different forms, tables, views, and data sources. 
<br>
<br>

**Date: 19-Feb-2022**

## ERPNext Installation

ERPNext is a free and open-source integrated Enterprise Resource Planning software developed by Frappe Technologies Pvt. Ltd. and is built on MariaDB database system using Frappe, a Python based server-side framework. ERPNext is a generic ERP software used by manufacturers, distributors and services companies.

To install ERPNext, first we have to install frappe in our system. 
After installing frappe, create a fresh site with the command: 

`bench new-site site_name`

This site will create new database so we have to give MySql Password here.

Then install app in the system with the following command:

`bench get-app erpnext --branch version-13`

OR

`bench get-app https://github.com/frappe/erpnext --branch version-13`

With this, ERPNext version 13 will visible in apps folder of frappe directory.

After creating site successfully, install the ERPNext on this site.
Use the following command:

`bench --site site_name install-app erpnext`
`bench start`


Now complete the setup wizard. Select your Region, Create first user etc.
There will be many domains like Distribution, Retail, Education, Services, Agriculture, Healthcare etc. We have to work with Education so select only “Education” domain and continue the process. Then provide a company name and abbreviation. On the last screen, ERPNext will ask you what your company does, its bank name, the type of charts of accounts, and the fiscal year period. Fill the details and complete setup.
<br>
<br>

**Date: 21-Feb-2022**

## Introduction to TMUX and MOSH

Today we got to know two new tools which are really very helpful for the coders which are TMUX and MOSH. 
- Mosh: Mosh is free and command-line software that is used to connect from a client computer to a server over the Internet to run a remote terminal. Mosh is more intelligent than SSH. While the SSH client waits for a TCP response from the server before showing your typing, Mosh will display your typing in real-time and even give underlined typing predictions. The mosh program will SSH to user@host to establish the connection. As you know, SSH may prompt the user for a password or use public-key authentication to log in. But mosh runs the mosh-server process (as the user) on the server machine. Mosh will run inside your Terminals such as xterm, gnome-terminal, urxvt, Terminal.app, iTerm, emacs, screen, or tmux. 
- Tmux: Tmux is a Linux application that allows multitasking in a terminal window. It stands for Terminal Multiplexing, and is based around sessions. Users can start a process, switch to a new one, detach from a running process, and reattach to a running process.
<br>

**Date: 22-Feb-2022**

## Introduction to Github Pages

- Create a New Repository on GitHub. 
- Setting Repository as the main branch and setting a theme for GitHub pages. 
- Learning about Personal access tokens for push Local Repository on GitHub. 
- Learning Syntax of Markdown Language in GitHub. 
<br>

**Date: 23-Feb-2022**

## Comparison between ERPNext Version 12 and Version 13

Install ERPNext Version 12 and 13. Then compare both the versions.
The major difference is the UI interaction. In ERPNext 13 the UI design is very user friendly as compared to ERPNext 12 version,

- In the 13 version , we have access to different themes well , this feature is not available in the 12 version. 
- In ERPnext 12 version we have to manually set up the domains which is time consuming while on the other hand in 13 version it give us pre-processed domains with very clean UI which makes it simpler. 
- In version 13 while setting up it automatically created a blog/webpage for the user and in version 12 this is missing or we can manually create it . 
<br>

**Date: 24-Feb-2022**

## Education Domain in ERPNext

Sir assigned the task to explore the Education Domain of ERPNext. So I am reading the documentation and trying to understand it and implementing it on my localhost. 

The ERPNext Education Module helps to organizing your entire set-up. You can have your entire Student Database, Fee Structure, Staffing Information, Courses, Curriculum Which we used for the Project Nanakana Sahib Public School and Guru Nanak Dev Engineering College Ludhiana.

Using Education module of ERPNext, you can effectively manage operations like:
- Managing Student 
- Program and Courses 
- Publishing Programs on the portal 
- Online Admissions 
- Student Attendance 
- Course Scheduling 
- Portal for Publishing Programs 
- Assessment Planning and Assessment Result 
- Fee Structure and Fee Receipt 
<br>

**Date: 25-Feb-2022**

## Modules in Education Domain

I am reading documentation of ERPNext Education Domain and understanding the concepts.

There are different modules under Education Domain. 

- **Student:** There is record of all the students like student detail, guardian detail, student group, batch etc.
- **Admission:** It keep track of admissions of students.
- **Fees:** It keep track of fees, due date, pending fee etc of student.
- **Learning Management System:** In this, the progress of individual students can be tracked through ERPNext as well as the portal.
- **Attendance:** There is record of attendance of all the students. 
- **Assessment:** It keep track of student progress, assessment result, schedule etc.
- **HR:** It keeps record of all employees and instrutors of school or college.
- **Website:** In this, we can make beautiful website, webpages, blog, themes, homepage etc for our school/college
<br>

**Date: 28-Feb-2022**

## Setting Up ErpNext for School

First we setup the parent Company with all the details and under that parent company we setup our school which further related to courses, program, room, student category etc. then our team divided the work for different modules.

I create Academic Year, Academic Term, students etc for school. 

To add students, 
1. Go to Education > Student.
2. Click on Add student.
3. Enter details of student.
4. If student is already user of erp then select User Id, otherwise enter the email of student.
5. A user of same email will be created in User list.
6. After saving, email will be sent to the provided email of student.
7. Now, student can set the password and login to the system.
<br>

