# bootcamp-Net-Core-web-application

Bootcamo Week 3 Bonus Project: .Net Core Web Application

Creating a .NET core web application
1.	Open visual studio
2.	Select create a new project in which you have to select "ASP .net core web app" template. 
	  If it is not visible then download the template.
3.	Give project name, path on computer, you can also check the option to have the solution and the project in the same directory and click on Next.
4.	Click on next and select the framework and click on Create. The web application will be created in the selected directory.
	  To check if the application is running, open the terminal and run the command, "dotnet run".
	  The application will start running on designated ports. 
5.	Installing Newtonsoft.Json using nuget package manager: open the terminal and run the command: 
	  dotnet add package Newtonsoft.Json --version 13.0.1
	  This will add the package in the created project.
6.	Publishing Application 
	a) Right click on project in solution explorer window and select publish 
	b) Target - Select Folder option (there are many other publishing options but we are going with folder). Next 
	c) Location - Select folder where you want to publish your web application.
	
Hosting Created .Net Web Application
a)	Open IIS
b)	Sites > Add Website > Add website window will appear
	Site Name = web app or the name of your choice
	This will create application pool with name same as your site name, or you can also select existing app pool.
	Physical path = disk location where your application executables are.
	Binding
	    - Type : http
		- Ip Address : All Unassinged
		- Port : 5001
		- Host name : blank
c) You will see created new web app in sutes section and new app pool in Application Pools section
d) Open your created app pool and open it, change .NET CLR version to "No Manged Code" and save it.
e) Copy your application executables in directory which you specified in physical path while adding website section.

- By following above steps the application can be accessed at http://localhost:5001
- if application is not accessible usign localhost:5001 address and shows an .net runtime core issue, 
  then install .net runtime core from below link:
  [.net Core runtime](https://download.visualstudio.microsoft.com/download/pr/1c12a7f4-1e3b-4d0c-a0f8-a03950187940/15abf24d5330aca4429b6212892ca2ae/dotnet-hosting-3.1.25-win.exe)
- Application is accessible inside server using internal ip or localhost and port number, 
  but not externally using external ip then open port 5001 in firewall by creating new inbound rule.
  This will allow your hosted application accessible through internet using external ip.
