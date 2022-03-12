Date : 1-Feb-2022
Introduction to Linux & Installing Ubuntu

Linux is an open-source operating system like other operating systems such as Microsoft Windows, Apple Mac OS, iOS, Google android, etc. An operating system is a software that enables the communication between computer hardware and software. It conveys input to get processed by the processor and brings output to the hardware to display it. This is the basic function of an operating system.

    Download the linux distribution of your choice.
    Creating Boot pendrive using rufus.exe in windows.
    Restart the system and open boot menu using boot key. (Eg.- F8, F2 etc.)
    Select your boot device in boot menu.
    Select Install Ubuntu then Click Noraml Installation.
    Select where to install alongside window or Erase disk or something else.
    Then Click next and start ubuntu installation.
    For More detail about Installation Guide Click here


Date : 2-Feb-2022
Introduction to LAMP Stack

The LAMP stack is a popular open-source solution stack used primarily in web development.LAMP consists of four components necessary to establish a fully functional web development environment. The first letters of the components' names make up the LAMP acronym:

    Linux is an operating system used to run the rest of the components.
    Apache HTTP Server is a web server software used to serve static web pages.
    MySQL is a relational database management system used for creating and managing web databases, but also for data warehousing, application logging, e-commerce, etc.
    PHP, Perl, and Python are programming languages are used to create web applications.
    Installing lamp on Ubuntu System.
    Verifying by run LAMP on localhost.


Date : 3-Feb-2022
Run Cgi Script

CGI stands for Common Gateway Interface. CGI defines a standard way in which information may be passed to and from the browser and server. Any program or script that can process information according to the CGI specification can, in theory, be used to code a CGI script.

    Create a cgi scirpt.
    Run it on Localhost using Apache Server.


Date : 4-Feb-2022
Image to video

    Create a python Script.
    install pip,Image-MagicK on your system.
    goto ---- /etc/ImageMagick-6/policy.xml file.
    Comment out line "policy domain="path" rights="none" pattern="@*"
    Run the script by using python3 filename.py.


Date : 5-Feb-2022
Introduction to frappe

Frappe, pronounced fra-pay, is a full stack, batteries-included, web framework written in Python and Javascript with MariaDB as the database. It is the framework which powers ERPNext, is pretty generic and can be used to build database driven apps.
#### Why Frappe?

The key difference in Frappe compared to other frameworks is that meta-data is also treated as data. This enables you to build front-ends very easily. We believe in a monolithic architecture, so Frappe comes with almost everything you need to build a modern web application. It has a full featured Admin UI called the Desk that handles forms, navigation, lists, menus, permissions, file attachment and much more out of the box.

    Install Frappe-bench and its required tool. For more info Click here.


Date : 7-Feb-2022
Creating App and Site & run on local server in Frappe

    Start Bench in one Terminal.
    In Second Terminal.
    Creating App by using bench new-app library_management inside Frappe-bench Directory.
    Creating site by using bench new-site library.test inside Frappe-bench Directory.
    Run Site on Localhost by using library.test custom port name.


Date : 8-Feb-2022
Introduction to Github Pages

    Getting Information What is GitHub Pages.
    Create a New Repository on GitHub.
    Setting Repository as the main branch and setting a theme for GitHub pages. "policy domain="path" rights="none" pattern="@*"- Learning about Personal access tokens for push Local Repository on GitHub.
    Learning Syntax of Markdown Language in GitHub.


Date : 9-Feb-2022
Introduction to Reveal.JS, Pandoc, Use of Markdown in Reveal.js

    What is Reveal.JS, Pandoc, Use Markdown in Reveal.js.
    Creating Presentation in Reveal.JS using Markdown only.
    Learn how to show presentation on Local machine.
    Converting .md file into .pdf file using Pandoc.


Date : 10-Feb-2022
Introduction to Docker, Virtual Machine and ERPNext

What is Docker?

Docker is popular virtualization software that helps its users in developing, deploying, monitoring, and running applications in a Docker Container with all their dependencies (frameworks, libraries, etc.) to run an application in an efficient and bug-free manner.Docker Containers are Light-weight, Applications run in isolation,Occupies less space, Easily portable and highly secure, Short boot-up time.
- It can run multiple containers on a system. - It can start multiple containers at a time on the Docker engine.

What is Virtual Machine?

A Virtual Machine (VM) is a compute resource that uses software instead of a physical computer to run programs and deploy apps. One or more virtual “guest” machines run on a physical “host” machine. Each virtual machine runs its own operating system and functions separately from the other VMs, even when they are all running on the same host. This means that, for example, a virtual MacOS virtual machine can run on a physical PC.
- It can start only a single VM on a VMX. - It can run only a limited number of VMs on a system.

What is ERPNext?

ERPNext is a full-featured business management solution that helps SMEs to record all their business transactions in a single system. With ERPNext, SMEs can make informed, fact-based, timely decisions to remain ahead in the competition. It serves as the backbone of a business adding strength, transparency, and control to your growing enterprise.

Date : 11-Feb-2022
Installing ERPNext in Frappe-bench

    If Frappe-bench installed in system follow second method otherwise you will get error.
    Installion done with two manner
    By Adduser in linux
    And create Erpnext app and site in frappe-bench Diretory.
    For installation steps Click here.


Date : 12-Feb-2022
Introduction to Selenium, Budibase, Coding standard for program
- Selenium is browser automation tool by which you can create a script which automatically done task like fill credential and click for search. - Budibase is a development platform designed for speed and productivity. -

With Budibase, developers no-longer experience repetition, long-dev cycles, and frustration. Instead, developers are more productive, happier, and can deliver applications they're proud of in minutes.
-

How to write code in Any script so that it can easily read by other programmer who contribute to your project, take variable name which should be relevant with its function.

Date : 14-Feb-2022
Try to Solve error redis-server during Installation
**error while loading shared libraries: libatomic.so.1: cannot open shared object file: No such file or directory** - sudo apt purge libatomic1. - install houncho if file is missing.

Date : 15-Feb-2022
Introduction to Education module in Erpnext

The Education domain in ERPNext is designed to meet requirements of any organization which imparts knowledge and believe in doing so in an organized fashion. It has already been used at schools, colleges and even in private firms. It helps you to effectively manage administration and allows you to focus on what is most important for your institute, to educate!

Date : 17-Feb-2022
Introduction to Jinja Templating

Jinja is a fast, expressive, extensible templating engine. Special placeholders in the template allow writing code similar to Python syntax. Then the template is passed data to render the final document.

Date : 18-Feb-2022
Trying to fetch data from database using Jinja Templating
- Write a Python Script for establish connection with Mariadb. - Still it gives permission error try to solve it.

Date : 19-Feb-2022
Working with server
- Resetting the password of server. - Trying to install Erpnext on server.

Date : 21-Feb-2022
Mysql Administration, Converting pdf to md file
- Today I created a new doctype in erpnext with different options - then learned about the administration concept of database - Converting pdf file to md and applying changes using markdown.

Date : 22-Feb-2022
Add new user in ubuntu
- Add new user in ubuntu. - trying to give access of database to other user.

Date : 23-Feb-2022
How to use ssh
- Login to Server, Try to help other member to install ldap on server. - Apply different permission related queries on database for different user.

Date : 24-Feb-2022
Learning about how to import data in erpnext from csv file
- Try to import data in erpnext app throught csv file. - Apply pagination in erpnext webpage.

Date : 25-Feb-2022
Import Data in Mysql
- Try to import data in MariaDB throught csv file. - Learning the concept of permission on Server.

Date : 28-Feb-2022
Creating Web page in ErpNext
- Creating Static Webpage on Erpnext. - Learning Frappe School Module.

Date : 2-Mar-2022
Learn Module from Frappe School
- Creating new site with new app. - Creating Doctype and linking doctype with other. - Learn Jinja Script for frappe doctypes.

Date : 3-Mar-2022
Learn Meeting App
- Understand the structure of meeting app. - Understand the javascript code and python code of meeting app.

Date : 4-Mar-2022
Presentation and discussion of meeting app
- Telling about the importance of doctype in Frappe-Framework. - Discuss with all team how it works and how we create new custom app.

Date : 5-Mar-2022
Creating own Noticeboard app
- First create App and install it on website. - Create Doctype according to structure discussed in team. - Provide it web view.

Date : 7-Mar-2022
Customize Noticeboard app
- Writing code to show correct date format eg. March 7, 2022. - Writing code to show the name of user who upload the notice. - Making its view user friendly in form and webpage both. 
