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
{% raw %}
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
{% endraw %}
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

**Date: 2-March-2022**

## Import Data through csv file

Today I learnt to import data in bulk through csv files. I insert students in bulk with the following steps:

1. First of all, go to the student list.
2. Click on Import then Add Data Import.
3. Then the New Data Import form will open. Here, add the doctype "Student Applicant" in the Document Type field, and select "Insert New Record" in Import Type. Then save it.
4. Then download the template with required fields like First name, Middle name, Last name, Email etc.
5. Create the csv file of all students according to the fields in the downloaded template.
6. Then Attach csv file in "Import File". Then click on "Save" then "Start Import".
7. Here, if you find any error in fields then you can export the failed error logs, change it and upload it again.
8. Now all students will be visible in the Student List.
<br>

**Date: 3-March-2022**

## Mentor-Mentee Application on Frappe

- We (I and Amandeep) have to create a new app in frappe framework i.e. Mentor-Mentee. 
- In this, there should be some mentees and mentors. 
- Details of mentees and mentors should be stored there. 
- Each mentee should have a mentor. 
- We should be able to assign mentors to the mentees. 
- List of mentors and mentees should be visible on the webpage.
- After clicking, webpage of their details should be opened.
<br>

**Date: 4-March-2022**

## Create DocType and Enter Data

We decided a flow of Mentor-Mentee application. First of all we created a new site in frappe with bench command. Then we create a new app named mentor_mentee. After creating successfully, we install the app on the site. 
Then we decided to create following three doctypes :

Mentor Doctype

- Create a Mentor Doctype, details of mentors will be visible there. 
- Go to doctype list, click on Add DocType. 
- Enter name of Doctype as Mentor then select mentor_mentee in module field.
- Enable Quick Entry check box.
- Add the following fields in fields table:
  - First Name: (Data, Mandatory) For first name of the mentor.
  - Last Name: (Data) For last name of the mentor.
  - Full Name: (Data, Read Only) We will define the function to compute full name from first and last name. So keep it read only.
  - Address: (Data) For address of mentor.
  - Phone: (Data) For phone number of mentor.
  - Email: (Data, Unique) For email of mentor. Email should be unique.
  - Code: (Data, Mandatory) This is code of teachers. It should also be unique.
          
- To compute full name, edit the mentor.py file as following:
from frappe.website.website_generator import WebsiteGenerator
```py
class Mentor(WebsiteGenerator):
	def before_save(self):
		self.full_name=f'{self.first_name} {self.last_name or ""}'	
```
- Go to the mentor list and add data of some mentors.
<br>

**Date: 5-March-2022**

## Mentee Doctype

- Create a Mentee DocType in which details of students will be stored.
- Go to doctype list and click on Add DocType.
- Enable Quick Entry check box.
- Add the following fields in fields table:
	- First Name: (Data, Mandatory) For first name of the student.
	- Last Name: (Data) For last name of the student.
	- Full Name: (Data, Read Only) We will define the function to compute full name from first and last name. So keep it read only.
	- Roll No: (Int, Mandatory) For roll numbers of students. It will be integer.
	- Address: (Data) For address of mentee.
	- Phone: (Data) For phone number of mentee.
	- Email: (Data, Unique) For email of mentee. Email should be unique.
	- Image: (Data, Mandatory) This is for the image of students. It should also be unique.

- To compute full name, edit the mentee.py file as following:
from frappe.website.website_generator import WebsiteGenerator
```py
class Mentee(WebsiteGenerator):
	def before_save(self):
		self.full_name=f'{self.first_name} {self.last_name or ""}'
```				
- Go to the mentee list and add data of some mentees.
<br>

**Date: 7-March-2022**

## Meeting App

Today, Vishal and Pawandeep gave us presentation to all of us on Meeting App.

- They showed us the structure of Meeting App.
- They showed us how to create custom apps in erp and how to install it onto the site. 
- I learned how to create parent and child doctypes and how to link child doctypes with parent doctypes.
- We can plan meetings, and add details like meeting agenda, meeting
time and its users and we can invite users by sending mails.
<br>

**Date: 8-March-2022**

## Relation Doctype

- We decided to create a more doctype which is for relation of mentors and mentees.
- We want to select the mentor name from mentor list and mentee name from mentee list and create a relation of both.
- Follow same steps to create doctype named Relation.
- Add the following fields:
	- Mentor: (Link, Mandatory) As we want to select mentors from mentor doctype so we will link this. Write Mentor in Options.
	- Mentee: (Link, Mandatory) Here also we want to select mentees from mentee doctype so we will link this. Write Mentee in Options.
- Go to Relation list and some relations of the mentor and mentees.
- In Mentee and Mentor Doctype, write full_name in title field in View Settings. With this, when we select mentor and students, their full name will also be visible with their code or roll no.
<br>

**Date: 9-March-2022**

## Webpage for list of Mentor and Mentee 

- Now, we want to see the list of mentors and mentees on webpage.
- After clicking a mentor or mentee, their detailed information should also be visible. 
- To create webpage, go to the Mentor doctype then web view. 
- Enable check boxes Has Web View and Allow Guest to View.
- Add the Route field in the fields table and save the doctype.
- Now two html files mentor.html and mentor_row.html will created in the templates directory of doctype.
- Follow same steps for mentee doctype also.
- In mentor_row.html and mentee_row.html files, replace code and roll_no with full_name respectively.
- Now list will be visible on webpage.
<br>

**Date: 11-March-2022**

## Introduction to Jinja Template

Jinja is a fast, expressive, extensible templating engine. Special placeholders in the template allow writing code similar to Python syntax. Then the template is passed data to render the final document.

A Jinja template is simply a text file. Jinja can generate any text-based format (HTML, XML, CSV, LaTeX, etc.). A Jinja template doesn’t need to have a specific extension: .html, .xml, or any other extension is just fine.

A template contains variables and/or expressions, which get replaced with values when a template is rendered; and tags, which control the logic of the template. The template syntax is heavily inspired by Django and Python.

Delimiters
Here are some delimiters that are used in the Jinja syntax:
<br>

**Date: 12-March-2022**

## Fetching Data from another doctype on webpage

- Now, we have to show the details of students and mentors on webpage.
- We have to write the jinja code for this.
- Add the following code in mentee.html file:

```html
{% raw %}
{% block page_content %}

<div class="py-20 row">
    <div class="col-sm-2">
        <img alt="{{ title }}" src="{{ image }}">
    </div>

    <div class="col">
        <div><strong>Roll No: </strong>{{roll_no}}</div>
        <div><strong>First Name: </strong>{{first_name}}</div>
        <div><strong>Last Name: </strong>{{last_name}}</div>
        <div><strong>Full Name: </strong>{{full_name}}</div>
        <div><strong>Email: </strong>{{email}}</div>
        <div><strong>Phone No: </strong>{{phone}}</div>
        <div><strong>Address: </strong>{{address}}</div>
        
    </div>
</div>

{% endblock %}
{% endraw %}
```

- Now students details will be visible on Mentee webpage.
- We want to show the details of mentors on webpage and also there should be a table of menees that are assigned to the mentor.
- To do this, we have to fetch data from mentee doctype on mentor’s webpage. 
- We can use set query.
- But it didn’t meet our requirements. So, we are finding another way.
<br>

**Date: 14-March-2022**

## Detailed View of Mentor

- After exploring, we found that there is no need of Relation DocType.
- We can select mentor from when we entering details of student.
- So, we delete the Relation Doctype. And add field Mentor name in the Mentee DocType.
- To show details of mentor and table of their mentees, write the following code in mentor.html file:

```html
{% raw %}
{% block page_content %}
<div class="col">
    
    <div><strong>First Name: </strong>{{first_name}}</div>
    <div><strong>Last Name: </strong>{{last_name}}</div>
    <div><strong>Full Name: </strong>{{full_name}}</div>
    <div><strong>Email: </strong>{{email}}</div>
    <div><strong>Phone No: </strong>{{phone}}</div>
    <div><strong>Code: </strong>{{code}}</div>
    <div><strong>Students List:</strong></div>
</div>
<table class="table table-condensed table-hover table-bordered">
    <tr>
    <th class="text-center">Roll No</th>
    <th class="text-center">Full Name</th>
    <th class="text-center">Address</th>
    <th class="text-center">Email</th>
    <th class="text-center">Phone</th>
    </tr>
{% set students=frappe.get_all
    ('Mentee',fields=['roll_no','full_name','mentor_name','mentor'], order_by='roll_no asc') %}

{% for student in students %}

{% if student.mentor==code %}

<tr>
<td style="width:10%; text-align:center;">{{student.roll_no}}</td>
<td style="width:10%; text-align:center;">{{student.full_name}}</td>
<td style="width:10%; text-align:center;">{{student.address}}</td>
<td style="width:10%; text-align:center;">{{student.email}}</td>
<td style="width:10%; text-align:center;">{{student.phone}}</td>
</tr>

{% endif %}
{% endfor %}

</table>

{% endblock %}
{% endraw %}
```

- Now, we created the links of Student and Mentor list on navigation bar of website.
<br>

**Date: 15-March-2022**

## Mentor-Mentee Table on Webpage

- Now we have to create a table of mentees and their assigned mentors on webpage.
- For this we create a new html file in the www folder.
- Then write the following code :

```html
{% raw %}
{% block page_content %}

{% set u2=frappe.get_all('Mentee',fields=['roll_no','name','full_name','mentor_name'], order_by='roll_no asc') %}
{% set u3=frappe.get_all('Mentor',fields=['full_name','code']) %}

<table class="table table-condensed table-hover table-bordered">
<tr>
    <th>Roll No</th>
    <th>Mentee Name</th>
    <th>Mentor Name</th>
</tr>

{% for i in u2 %}

<tr>
    <td>{{i.roll_no}}</td>
    <td>{{i.full_name}}</td>
    <td>{{i.mentor_name}}</td>

</tr>
{% endfor %}


{% endblock %}
{% endraw %}
```

- With this, table will created on webpage. Roll no, Mentee Name and Mentor Name will be fetched in the table. Check screenshot below:
<br>

**Date: 16-March-2022**

## Notice Board App

Today, we create a notice board app in frappe. NoticeBoard for an institute regarding the important information provided by the Institute.

- Create Doctype according to structure discussed in team.
- Add the fields like Title, Description, Signature of the uploader, Date and Attachment.
- Applied validations in python class.
- Also can see how many have seen the notice.
<br>

**Date: 17-March-2022**

## Create Program and Courses

I am reading the documentation of education module and implementing Program and Courses module.

**Course:-**

A course can be considered as a subject or a part of an educational program which is to be taught for a term. Corses are subjects in the school. A course will have a set of topics that are to be covered under it's scope. Steps to create course:

1. Go to Course List and click on New.
2. Enter the Course Name.
3. Select the Department under which this course is being made.
4. Add the Topics. You can also create the topics from here itself.
5. Add the Description for the course.
6. Save.

**Program:-**

A Program will have an educational curriculum defined by your institute to streamline the learning process and goals in each subject or course. Programs are classes in the school. Steps to create programs:

1. Go to the Program list and click on New.
2. Enter the Program Name and the Program Abbreviation.
3. Select the Department for the Program.
4. Select and add the courses within the Program.
5. Save.
<br>

**Date: 18-March-2022**

## Portal Settings for Program

- **Is Published:** For every program created in ERPNext, there is a check-box in the Portal settings, that allows the Program to be published on the portal. This can facilitate Self Enrollment and other settings for the program. Once this box is checked, the following options will be available for the user.
- **Allow Self Enroll:** Once this box is checked, the students/applicants would be able to enroll themselves for the program on the portal.
- **Is Featured:** Enabling this option would allow the program to be featured on the portal.
- **Intro Video:** Enter the link for the video that you wish to add an Introductory Video for the Program.
- **Description:** Add the description of the Program which you want to be visible on the portal.

**Student Attendance Module**

Sir assigned me the task of Attendance module and to explore how we can mark the attendance based on course, activity or batch.

Student Attendance allows you to track and manage the attendance of a student for a day. The Attendance module is designed to help teachers easily mark student attendance during class.
Attendance Records can be created against Students on a daily basis.
<br>

**Date: 19-March-2022**

## Gunicorn, Socket.io, Scaffhold

Gunicorn is a WSGI(Web Server Gateway Interface) server. Gunicorn is built so many different web servers can interact with it. It also does not really care what you used to build your web application - as long as it can be interacted with using the WSGI interface.Gunicorn takes care of everything which happens in-between the web server and your web application. 

Socket.IO is a library that enables low-latency, bidirectional and event-based communication between a client and a server. It is built on top of the WebSocket protocol and provides additional guarantees like fallback to HTTP long-polling or automatic reconnection. There are several Socket.IO server implementations available: JavaScript, Java, Python.

Just like a real scaffolding in a building construction site, scaffolding gives you some kind of a (fast, simplified, temporary) structure for your project, on which you can rely to build the real project. It can be (and is today) used to describe many things – from abstracting DB layers, to web apps folder structures, and to generating and managing project dependencies. It is not something that is specific to any language / technology, just like the term skeleton or boilerplate. You build some fast, simplified, (sometimes external, sometimes temporary) structure that will help you to build the real,
more complex, finalized structure under, above, inside or outside of that temporary structure . Scaffolding enables developers a tool to quickly create a running web-based environment for the Internet.
<br>

**Date: 21-March-2022**

## Student Attendance Module

I explored about Student Attendaance Module. We can mark attendance of students manually one by one or in bulk with Student Attendance Tool.

We will not mark attendance manually, we will use Tool to mark attendance in bulk.

In the Student Attendance Tool, We can mark attendance based on Student Group or Course Schedule.

- In Course Schedule, first we have to schedule the course with Instructor, Room and Time of lecture. After setting up the the course schedule, we can mark attendance of all students that belong to this course.
- If we mark attendance based on Student Group, then further there are three options i.e. Group based on: Batch, Course and Activity.
	- Based on Batch: We can mark attendance of all students of a group based on batch that is section A or section B.
	- Based on Course: Here, we can mark attendance of all students of the group i.e. based on course.
	- Based on Activity: Here, we can mark attendance based on the Activity group.
<br>

**Date: 22-March-2022**

## Create Academic Manager Role 

Sir assigned us the task to create an academic manager role that can add a studet group, assign instructors to the student group and create course schedule.

So we (I, Kiranjeet, Pooja) have created new role academic manager role. 

Create a new role with name Academic Manager in the Role list. Give desk access to this role. Then go to Role Permission Manager. Here select doctypes and add all permissions required for this role.
<br>

**Date: 23-March-2022**

## Learned Github 

So being a part of a developer team one must need to Know Github in order to have a seamless conversation, information and code can be shared easily. Some basic github commands are as following:-

- git init - to initialize a repository 
- git add . to add the whole files and folder 
- git add filename.extension to add the specific file 
- git commit -m "Your Message" to commit the changes 
- git remote add origin git URL 
- git push -u origin [branch name] 
- git stash clear -to clear all stashed enteries 
- git checkout branch_name move across beanches of specifi reporsitory 
- git status to check the curent status of the files 
- git pull origin [branch name] pull changes from the remote url 
- form Documentation [Click here ](https://github.com/joshnh/Git-Commands)
<br>

**Date: 24-March-2022**

## Installing New ERPNext on server

- First we install the new instance of frappe framework on the New Server then install erpnext with education domain. 
- After this we are collecting students around 5000 and teachers (114) data from Nankana Sahib Public School. 
- Arranging data according to doctype in erpnext. 
- Setting up the school. 
<br>

**Date: 25-March-2022**

## Explore Company’s Default Values

**Default Holiday List:**
Holiday List is a list which contains the dates of holidays. Most organizations have a standard Holiday List for their employees. However, some of them may have different holiday lists based on different Locations or Departments. In ERPNext, you can configure multiple Holiday Lists and assign them to your employees based on your requirements.

**Default Letter Head:**
A Letter Head contains your organization's name, logo, address, etc which appears at the top portion in documents. Every company has a default Letter Head. These Letter Head values are generally set as Header and Footer in the documents. In ERPNext, you can capture these details in the Letter Head master.

**Default Finance Book:**
A Finance Book is a book against which all the accounting entries are booked. You can have multiple finance books. For example, one book for tax authorities and another for stockholders. This is useful if you have to report depreciation and other values in different ways based on regulatory requirements.
<br>
<br>

**Date: 26-March-2022**

## Adding Students and Arranging CSV

Today, We got student, instructor, classes data from Nankana Sahib Pubic School. Then Sir assigned me the task to upload all students on server through csv files.

Before uploading students, we have to create programs and courses. So I helped Aman in creating Programs and Courses.

Then I start arranging data of students in csv file. All team members helped me in arranging data because there were arount 3000 students. 
<br>
<br>

**Date: 28-March-2022**

## Add Students on New Server

To add students in school, we have to upload student csv in Student Applicant. Then we will approve students and enroll in their classes. 

For Student Applicants,

1. First, Go to the Student Applicant. Then click on import then Add Data Import. 
2. Then the New Data Import form will open. Here, add the doctype "Student Applicant" in the Document Type field, and select "Insert New Record" in Import Type. Then save it.
3. Then download the template with required fields like First name, Middle name, Last name, Program, Application Status etc. Application Status of all students should be "Approved". Otherwise we have to Approve all manually.
4. Create the csv file of all students according to the fields in the downloaded template. Then Attach csv file in "Import File". Then click on "Save" then "Start Import".
5. Here, if you find any error in fields then you can export the failed error logs, change it and upload it again.
6. Now all students will be visible in the Student Applicant List.
<br>

**Date: 29-March-2022**

## Add User on New Server

After uploading students, we have to create users of all students. It means we have to create their login ids and passwords. So that students can login and check the content, quiz etc of their subjects.

For Students User,

1. First, go to Student Applicants. Click on Import, then Add Data Import.
2. Then the New Data Import form will open. Here, add the doctype "Student Applicant" in the Document Type field, and select "Update Existing Record" in Import Type. Then save it.
3. Then, click on "Download Template". Select "All Records" in Export Type. Select the First Name, Middle Name, Last Name, Student Email Address and download the template.
4. Then the csv file of all students will be downloaded. In this, add the field "Set New Password" and create passwords of all students.
5. Add column "Role (Roles Assigned)" and write "Student" for all students.
6. Then go to the User list, click on import then Add Data Import. Then the New Data Import form will open. Here, add the doctype "User" in the Document Type field, and select "Insert New Record" in Import Type. Then save it.
7. Then attach the file, click on "Save" and then "Start Import".
8. All students will become users with Student role.
<br>

**Date: 30-March-2022**

## Enroll Students in Programs

Now we have to enroll all students in their respective classes. So that their subjects and content of subjects will visible on their account.

For Enrollinng Students,

1. If you have already set the "Default Email" then go to step 3. Otherwise, In Settings, click on "Education Settings". Then the Education Setting page will open.
2. Then enable the option "Skip User creation for new Student".
3. In Tools, Click on Program Enrollment Tool, the new form will open.
4. Select "Student Applicant" in the field "Get Students From" and Select Program in which you want to enroll students. Select Academic Year and Academic Term.
5. Then click on "Get Students". Here, you will get all students from this Program.
6. Click on the "Enroll Students" button.
7. Repeat these steps for all Programs.
8. In Admission, click on Program Enrollment. Then all students will be visible here with status "Draft". You have to submit all then they will be in Submitted status and they automatically get enrolled in courses.
<br>

**Date: 31-March-2022**

## Enroll Students in Groups

We created Student Groups for all programs. 
For Creating Student Group,

1. Go to Education, then Studnet Group.
2. Click on New Student Group.
3. Select “Batch” in Group Based On field.
4. Enter other details like Academic Year, Term, Program, Group name etc.
5. Then Save it and click on Get Students.
6. All students of this program will visible there. Save it.
<br>

**Date: 1-April-2022**

## Student vs Instructor Enrollment

I have completed all my tasks that are assigned by sir. And Japreet was inserting instructors and employees. So I helped her in inserting instructors and users.

After completion, we compare the Enrollment of Students and Instructors in erp. It has been found that after adding students to the programs and courses, that only those programs and courses are visible to the students, in which the enrollment has been done. But in the case of Instructors all the courses are visible and he/she is able to create/delete the content in all the programs and courses. We need to find the way with which only those courses should visible to instructor to whom he/she belongs. 
<br>

**Date: 4-April-2022**

## User Permission for Instructors

We were finding the solution for the task that instructor can only see their own assigned programs and courses . We can do it by the user permission list in which we can assign them a specific program. But it is only applicable in desk. After this instructor is able to see his own assigned programs in desk but on the lms all the programs are visible to the instructor. 

For User Permission,

1. Go to User, then User Permission list.
2. Click on Add User Permission
3. Select Email Id of Instructor in User field. 
4. Select Program Doctype (for Program permission) or Course Doctype (for Course permission) in Allow field.
5. Select Class or Course in field For Value.
6. Click on Save.
<br>

**Date: 5-April-2022**

## User Permission for Instructors through csv

Now only those program and courses will visible to instructors for which we gave the user permissions. We can also create user permisisons in bulk for all instructors through csv file. 

For bulk permissions,
1. Go to User, then User Permission.
2. Click on Import then Add Data Import.
3. Then download template with all fields and create csv according to these fields.
4. Then Attach file in Import File. Then click on Save then Start Import.
<br>

**Date: 6-April-2022**

## Reading Files for Filters

My task was to add filters on a webpage so that we can search and sort the data on the webpage.
I am doing this task by reading the python files and understanding the concepts of desk filters.

After exploring I found that there is a global search which we have to enable for webpages. First go to Website, then Website Settings. Check Navbar Section, here we have to enable the checkbox “Include Search in Top Bar”. Now Search Filter will visible on our webpage.
<br>
<br>

**Date: 7-April-2022**

## Pagination on Webpage

When we give web view to a doctype, then list is visible on webpage. If there are more than 20 rows in the list then, firstly only 20 will visible on webpage and a “More” button at bottom will also show. Rest of the entries will visble after clicking on More button. 

But our need is to apply pagination with Previous and Next buttons. I am reading documentation of frappe and exploring a way to do this. 
<br>

**Date: 8-April-2022**

## Pagination on Webpage of LMS

- Firstly, I had created a library management system which had 5 doctypes. I gave web view to Article doctype. Then two files article_row.html and article.html were automatically generated in doctype folder. 
- On webpage of Article doctype, whole list of articles was visible. But we wanted to apply pagination on the webpage. So I tried from a video (url: https://youtu.be/rDC-5ZJTmOU ). 
- I created a file utils.py in library_management folder where I write the function of pagination for showing 4 articles on single page. Then in video, two files python and html were created in www > Article folder. I did the same but it didn't worked for me. 
- After trying many ways, i created these files directly in www folder, then it worked. In python file, pagination function was called. And in html file i write jinja code to display the list on webpage and applied "previous" and "next" buttons. 
- Now 4 articles are visible on webpage and previous, next buttons are working fine. 
<br>

**Date: 9-April-2022**

## Add LMS App in Github Repository

- First I go through the git documentation, so that every thing done properly. 
- In add on I'm finding a command how to add repositiory from terminal to github. 
- Then I upload my Library Management System application on my repository with some basic commands of github.
- To check Click here: https://github.com/sehjal408/LMS
<br>

**Date: 11-April-2022**

## Install Chat App on Server

We have installed Chat app and enabled it on server using following commands.

`bench get-app https://github.com/Software-Dechat --branch main`

`bench --site gne11.gndec.ac.in install-app chat`

Only System User are able to use chat app. It will not visible to the Website Users.
<br>
<br>

**Date: 12-April-2022**

## Learning Management System 

This allows institutes to publish their programs on their website. Programs can contain rich text articles, videos, and even quizzes. The progress of individual students can be tracked through the portal.

**Enabling LMS**

LMS is disabled by default and can be enabled from Education Settings.
To enable LMS we first go to education module then click the settings and open education settings. Here, there is a checkbox using which the LMS can be enabled. The portal is hosted on the /lms route. Here all the programs are shown in the form of cards. Each card is clickable and navigates to the corresponding program/course/topic/content. 
<br>
<br>

**Date: 13-April-2022**

## Setting Up Learning Management System for NSPS

- To make the Program accessible on the portal, tick the 'Is Published' checkbox in the Program form. You can also tick the 'Is Featured' checkbox, which will show it on the portal landing page. The portal will automatically fetch the courses from the course table in the program.

- On the portal, for students to be able to view the programs on the portal, a program has to be marked as Published. On the portal students will be able to see only those courses they are enrolled to or they are allowed to enroll into.

- If 'Allow Self Enroll' is checked, then the program will be visible to all students whether they are enrolled in the program or not. Students can enroll themselves in these programs and start learning, this way we can host private programs on your portal.

- For each of the courses in a particular program, we can set a course intro and a course hero image to be used on the portal. There is a table to add topics too, these topics will be displayed on the LMS to all enrolled students.

- Similar to the course, Topic has a table where we can add the content. We can add three different types of content viz. Video, Article and a Quiz.
<br>

**Date : 15-April-2022**

## Presentation of Nankana Sahib Public School Project

Today we had a meeting with Satinder Sir and a teacher from Nankana Sahib Public School. In today's meetings we all presented what we have done till now. We showed them the whole workflow to add a student. For which first we need to add a student applicant and explained that there are two methods for this one is online by using web form and another is offline.

After the application is accepted we can enroll them in the programs by single-2 enrollment of every student or by using the program enrollment tool and we showed them the lms interface of student how student is going to access the programs and courses and quizzes. 

After student section, we showed them the whole working of instructor how instructor can add content like articles, videos and quizzes in lms, mark the attendance of students etc. After Instructor we presented the HR module how to generate payrolls, salary slips, attendance of employees etc.
<br>
<br>

**Date: 16-April-2022**

## ERP User vs LDAP User

Sir assigned us the task to find the difference between ldap user and user created in erp.

First we (me, aman) tried it by exporting a csv file of users with some data to check if there any field related to ldap. But there was no such field.

Then In the meeting with Satinder sir, we tried to find the difference between a user created in erp and a user which is created by using ldap (Both users with same email) and we found that both are the same. So, we concluded that when we create any user with or without ldap, there is no difference.
<br>
<br>

**Date: 18-April-2022**

## CRM Module

CRM is Customer Relationsip Management. It helps us to track business Opportunities from Leads and Customers, send them Quotations, and book Sales Orders.

I created a lead and users with permissions Sales Manager and Sales User. Then I found that the lead is visible to all, not only to sales users. But it should be visible to only sales users. Now, I am reading the document again and implementing it by assigning the lead to a particular sales user.
<br>
<br>

**Date: 19-April-2022**

## Lead Management in CRM

A lead is a potential customer who might be interested in our products or services.

To get the customer through the door, we may be doing all or any of the following:

- Listing our product on directories. 
- Maintaining an updated and searchable website. 
- Meeting people at trade events. 
- Advertising our products or services. 

When we send out the word that we are around and have something valuable to offer, people will come in to check out our products. These are our Leads. They are called Leads because they may lead us to a sale.

To create lead,

1. Go to the Lead list and click on New. 
2. If the person represents an organization, check the 'Lead is an Organization' checkbox. If the person is an individual, leave the checkbox unchecked.
3. Enter the 'Email Address'. 
4. Status is the important field in the Lead. You can set the status manually and also it will be updated automatically based on your actions against the lead. 
5. You can set the Lead Source in Source field. 
6. Enter email ID for communication. 
7. Click on 'Save'. 
<br>

**Date: 20-April-2022**

## Adding Filters on doctype as per requirement
- As per requirement changes for achieve this we add filter in list-view like class-wise, subject-wise, date-wise filter. 
- For creating filters on desk we need to go to Doctype. 
- On click edit we need check option In List View, In Standard Filter. 
- Then on save changes filters are available on desk list-view of doctype. 
<br>

**Date: 21-April-2022**

## Introduction to Kimai
- Kimai is a free & open source timetracker. It tracks work time and prints out a summary of your activities on demand. Yearly, monthly, daily, by customer, by project 
- With Kimai, the boring process of feeding Excel spreadsheets with your working hours is simplified.
- Kimai does not have to run while recording, you can even quit your browser. Your time is still recording until you stop it from any web browser that has access to your installation. 
- It is designed to hold lots of users, but you can also use it for a single user if you want to. 
- Its simplicity is its strength. Due to Kimai’s browser based interface it runs cross-platform, even on your mobile device. 
- Kimai can be used by as many users as you want: each installation supports unlimited users with different roles.
- Teams can be created to group your users into logical groups like departments or project related peer-groups. Customers and projects can be assigned to those teams, which will limit visibility and access for other users.
<br>

**Date: 22-April-2022**

## Installation of Kimai

- I installed kimai from https://github.com/kevinpapst/kimai2.git
- Prerequisites for kimai are git, composer, apache2, php.
- First, I install all these then follow the steps to install kimai.
<br>

**Date: 23-April-2022**

## New Specifications for Notice Board App

Sir assigned us (Me, Vishal) the task to create Notice Board Application with following requirements:-

- Notice should be created by CLERK then it should be in the draft state. 
- Only CLERK and HOD should be able to create notice.
- Only CLERK and HOD can create notice for their department, no one else from other department should be able to create notice for their department.
- Another requirement when notice is created by clerk It will be in Draft state when Hod Submit Notice only then it would be published. 
- Naming Series of notice maintained department wise eg: Notice-CSE/2022/00001, Notice-CIVIL/2022/00001. 
- If HOD Cancel the notice then Clerk is able to make changes then again send it to HOD. 
<br>

**Date: 25-April-2022**

## Creating doctype for Notice Board App

- In First approach we decide to create doctype and apply workflow on it. 
- So we created a doctype with following fields: 
	- Title: (Data, Mandatory) This is for the title of the Notice.
	- Content: (Text Editor, Mandatory) This is for the content of the Notice.
	- Attachment: (Attach) This is to attach any pdf or image etc.
	- Signature: (Signature/Image) This is for signature of HOD. 
	- Status: (Select) There are options of status like Draft, Created by Clerk, Approved by HOD, Rejected, Pending, Published etc. This will be used in workflow.
	- Department: (Link) This is linked with department. Department of CLERK, who is creating notice will be fetched here.
	- Date: (Read Only) This is date of the day notice is created.
<br>

**Date: 26-April-2022**

## Workflow for Notice Board App

- As we want that Clerk will create notice and HOD will approve, reject or reassign it. 
- So we created two roles: HOD and Clerk in the Role list and gave them required permissions for Notices like to create, view, delete the notice.
- Then we created a workflow named “Notice” for the doctype.
- Here we define states like Draft, Approves, Pending etc. 
- Then we created Transition Rules like first Clerk will create a notice, after approved by clerk it will go to HOD then HOD will approve it or reassign it to Clerk.
- If HOD reassigns it then it will go to Clerk in Draft state, here clerk can edit it and resend it to HOD.
- If HOD wants to reject it, then first he needs to click on Pending then he can reject it, after rejecting by HOD it will go to the Clerk and the clerk can delete it.
- Every thing Works fine but when we apply some code then workflow states create problem. eg data is saved but changes apply with delay. 
- So we decide to work without workflow also learn new things from mistakes.
<br>

**Date: 27-April-2022**

## Department wise Naming Series

- Assigning department to Hod & Clerk to one department in User Permission List. 
- We use condition like cse = department_name. 
- Department_name is fetched from doctype use function self.fieldname. 
- After apply such condition we use make_autoname function. 
- self.name = make_autoname('NOTICE-'+'CSE'+'/'+'.YYYY.'+'/'+'.#####') 
- This function return series 'NOTICE-CSE/2022/00001' 
<br>

**Date: 28-April-2022**

## Fetching HOD by using variables in query

- First we use Simple Frappe query "frappe.db.get_value('User', 'hodcse@gmail.com', 'full_name')". 
- But this depends upon the email of hod if email will change in future then we need to change it. 
- Also we have to wrote this many times. 
- So we use another optimized version of query. 

```py
department = self.department
requiredRole = "Hod" 
                
                self.hod = frappe.db.sql(f""" select full_name 
                        from `tabUser` 
                        where `email` IN (select user 
                        from `tabUser Permission` 
                        where `for_value`="{department}" AND `user` IN (select parent 
                        from `tabHas Role` 
                        where `role`="{requiredRole}" )) """)
			
```
- By using this query with variable we are able to use this for all departments. 
<br>

**Date: 29-April-2022**

## Try to optimize Notice.py Code

- As we use department for naming series so for this we have to change code when department and its abbrivation changed. 
- To Remove this we add department abbrivation field in doctype. 
- With following query abbr depends upon the department abbrivation also we haven't make changes in code also code become more simple than previous code. 

```py
department=self.department
abbr=frappe.db.get_value( 'Department' , department ,'department_abbreviation' )
self.name=make_autoname( 'NOTICE-' + abbr + '/' + '.YYYY.' + '/' + '.#####' )
```
<br>

**Date: 30-April-2022**

## Hierarchy of Nankana Sahib Education Trust

Today we have discussed the hierarchy and structure of Nanakana Sahib Education Trust, GNDEC, NSPS.
- **Basic Structure:** First we have a parent company Nankana Sahib Education Trust and under these we have child companies Guru Nanak Dev Engineering College, Nankana Sahib Public School (21 branches), Guru Nanak Dev Polytechnic College, ITI.
- **Accounts Structure:** First we have a parent company NSET and it has a bank account which will take care of all the accounts of child companies. Under the parent company we have a child company GNDEC which also has a fee account and a salary account all the tuition fee of students will directly go to the fee bank account , and all the amount of fee bank account will be transferred to the salary account and all the employees will get their salaries from the salary account. All the development fee will be directly transferred to the development account. For the development, company will get the amount/fund from the development account.
- **Roles in NSET:** In the Nankana Sahib Education Trust we have president , director, managerial staff and under the president we have sub roles for other users, secretary, and trustees. And under the managerial staff we have clerks and accountant. Only the received amounts and all benefits should be visible to the instructor. Only the accounts part should be visible to the director. Clerk is responsible for all the inventories stocks. Clerk2 will be responsible for the hostellers fee. And they should be able to see only their assigned company details.
- **NSET:** In NSET company we have a director role which should have access to all the child companies. All the child companies GNDEC, NSPS have a principal. After that other staff is divided into two sections one is Non-teaching and other is teaching. Under the non-teaching staff we have clerks, accountants, assistants and other staff. Teaching section is further divided into Examination, student section(admissions etc), Establishment, Department. The examination staff will take care of examinations of companies, the student section will take care of the students admissions, fees etc.In the departments we have the role of HOD, section incharge, staff.
<br>

**Date: 2-May-2022**

## Hackathon day 1

**Roles and flow for Parent Comapany:-**

**Director:-** Director will have all permissions like fees, salary, accounts , total gain etc but with read only access.

**Accountant:-** will have permissions to see all the account information of Trust, NSPS, GNDEC. Accountant will have read, write access to create the fee and salaries of the employee and also can create the fee report and salary report.

**HR:-** HR will have permission to create the users and make them employees, leave allocation, holiday list, salary of employee.

**Principal:-** Will have only read only access to all the education domain related information and HR related information.

**Accountants:-** 1 For students fee and 1 for salaries of employees. 

**Teaching Incharge:-** Will do all the tasks of academic user like course scheduling etc.

**HR:-** will create employees and instructors only for Nankana sahib Public School, leave allocation, salary of employees etc. We need to show all the reports like employees attendance report, salary report, leave report etc to the HR..

**Instructors:-** will have access to student attendance, quiz, videos, article, Diary, Student list etc
<br>
<br>

**Date: 3-May-2022**

## Hackathon day 2

**Students:-** will have access of only LMS and on lms they will have access of programs, Courses, Quizzes, Videos, Articles, daily diary and attendance.

**Accountant:-** will create the salaries of employees and fees of students, will generate the balance sheet.

We need to generate all the reports and graphs for necessary information for each role.

**Inventory Management**
Today, We created Director user of NSET, Superintendent of NSET, Principal user of NSPS and HR user of NSPS on erp server and gave them all the required permissions. And same roles are created on gne11.GNE. Also we learn about Salary Structure and Salary Component of employees. In meeting with Harpreet sir, we learn about PF, Taxes, Funds, Earnings and Deductions etc. 
<br>
<br>

**Date: 4-May-2022**

## Creating Roles and permissions

- Creating Director Role and add permission for Viewing accounts, payroll, Employee details, all reports etc. 
- Customize Deskview for Director Role. 
- Creating Principal Role and add all academic views for Principal. 
- Creating Instructor Role and allow all permissions needed to do their tasks. 
- Creating Superintendent role and gave all permissions to this role.
- Creating HR role and add permissions for employee and instructors.
<br>

**Date: 5-May-2022**

## Creating Presentation with Other Team-mates in Reveal.JS

- Review all work which is done by us. 
- Creating presentation for the whole project so that we can present our work to the trusties of trust.
- Add all Salary Components required. 
- Add how Desk is visible for different Roles. 
- What is visible to all student. 
- What is visible to all instructors, director, principle etc.
- Explaing other modules like Accounts, Assets, Payroll, Human Resource, Education Domain. 
<br>

**Date: 6-May-2022**

## Working on Mentor-Mentee Task without erp

- Creating new database with three tables Mentor, Mentee & Relation. 
- Import data in these tables using csv files through terminal. 
- Make connection of database with python file. 
<br>

**Date : 7-May-2022**

## Install and use Flask

- As we need to show detail on webpage using jinja templating. 
- After few searches we decide to use flask as a framework which render jinja template for html file. 
- Again Make connection with database, but this time as adviced by teacher, we need to hide credential from public so that we push it on git. 
- For hiding credentials we load details from another python file. 
- Write basic hello world program and render it using jinja templating. 
<br>

**Date : 10-May-2022**

## Showing detail in html file using jinja

- Creating a templates folder inside flask app where all the html files put together.
- Make a funtion in which we put query select Mentor name from mentor table. 
- Then render template with data and file name in which template is shown.
```
@app.route('/')
def example():
    cur.execute("SELECT Name FROM Mentor")
    data = cur.fetchall()
    return render_template('index.html', output = data)
```
- cur.execute is used for query and cur.fetchall() fetch all names from mentor table. 
- And at the end funtion return render template in which filename, and assign data to output variable. 
<br>

**Date: 11-May-2022**

## Company NSPS in Student DocType

- There is a company(School name in our case) field in Student Applicant Doctype. 
- A user of same company can see the student applicants in the list.
- But there is no company field in the Student Doctype. So all students of other schools are also visible in student list.
- I tried by giving User Permission of company to users. But did not worked.
- After exploring, I found the solution. To view students school wise, we have to customize the company field in Student DocType.
-  With this, User of Child Company (like Nankana Sahib Public School or Guru Nanak Dev Engineering College) can see the students of this company only. And user of Parent Company (like Nankana Sahib Education Trust) can see the students of all child companies by applying filters.
<br>

**Date: 12-May-2022**

## Introduction to Stock 

The Stock or Inventory module in ERPNext helps us to:

- Maintain details of your products and warehouses. 
- Track receipt, transfer and delivery of the products. 
- Optimize stock levels by providing real-time information via reports. 
- Provide valuation of each product. 
    
The Stock module is tightly integrated with Purchase, Manufacturing and Accounting modules. Businesses have a large part of their financial resources invested in the stock items they trade. With ERP, we can always keep a bird's eye view on our stock availability, replenishment, procurement, sales, and much more.
<br>

**Date: 13-May-2022**

## Core Stock Transactions

There are three main types of entries:

- Purchase Receipt: Items received from Suppliers against Purchase Orders. 
- Stock Entry: Items transferred from one Warehouse to another. 
- Delivery Note: Items shipped to Customers. 

Apart from these core transactions, there are other documents available in ERPNext Stock module to manage Stock Reconciliation, Item Prices, deliveries, serial numbers, batch numbers, quality inspections, returns, etc.
<br>

**Date: 14-May-2022**

## Item and Item Group for Stock

First of all, Create Item Groups, Items, Warehouses, Suppliers etc.

**Item Group:**

An Item Group is a way to classify items based on types. Following are steps to create item group:

1. Go to the Item Group list, click on New. 
2. Select a group node under which you wish to create the Item Group, the default root is 'All Item Groups'. 
3. Select 'Add Child' or click on the New button. 
4. To make this child a category/group node, tick on Group Node. 
5. Click on Create New. 

**Item:**

An Item is a product or a service offered by the company. Following are the steps to create items:

1. Go to Stock -> Item. 
2. Click on Add Item. 
3. Keep the “Maintain Stock” field checked. 
4. Save (After saving, Stock Entry, Stock Ledger, Accounting Ledger will be created automatically.) 
<br>
