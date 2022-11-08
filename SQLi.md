# <p align="center"> Understanding SQL Injection, Identification and Prevention

* First it is important to understand that not just because SQL injection can be achieved by simply providing some characters as an input it doesn't constitute a crime. Unlawful access to a computer system is not a game and there are many resources dedicated to practice these skills.
* SQL stands for Standardized query language and is still the best way to communicate with a database. No matter the size of a site, numerous SQL queries will be run and this creates the opportunity for actors to exploit them.

### SQL and Sysadmins 
*  First, it is important to understand that SQL is a language with numerous powerful commands that can be exploited and not just a querier for data.   
* Even though SQL is mostly used to query data from databases, Sysadmins need to have knowledge about how SQL can manipulate data and its raw commands, in order to safely implement communications between a SQL database and a web application.

### Database Tables and its commands
* Tables are simply lists of information, like sheets in a spreadsheet. Each sheet is the list and the columns are attributes of the item.
* The basic SQL commands for a table are (CRUD), create, read, update and Delete. It is important to understand how they work because SQL injection attacks use them as aid. A common convention for SQL statements is that commands are capitalized and lowercase the ones that change statements to statements.  

### CRDU
* In order to load data into a table, “INSERT” is used in the following format, and the same command is used to add new values(products) in to the table

![Screenshot (43)](https://user-images.githubusercontent.com/97658998/200479492-4fefa8fb-24b1-484b-8f4c-aaca64539a29.png)
  
* UPDATE works similarly 

![Screenshot (45)](https://user-images.githubusercontent.com/97658998/200479780-f5ce1760-34bd-4fa1-a144-3b8c5ce2c15e.png)

* In order to read data one can use SELECT, to return the desire data from a table.

![Screenshot (49)](https://user-images.githubusercontent.com/97658998/200481628-b2dbb818-57b7-4a5b-9dad-f12ae112453d.png)

* Finally DELETE, the “Name = name” will delete everything in the “Products” table.

![Screenshot (46)](https://user-images.githubusercontent.com/97658998/200480028-25fa0472-c3e5-4137-87e0-538d990728e6.png)

* SELECT is also commonly used to retrieve specific data, providing a WHERE clause.

![Screenshot (47)](https://user-images.githubusercontent.com/97658998/200480089-7b10443a-da37-4414-9656-3dc8c14d81f9.png)
    

### String Concatenation
This is basically a bunch of strings put together to build an SQL statement, the ID value of an item gets passed with a command. In the next example the “sql_string” value gets passed to the database to display the information desired. The problem with this concept is that String Concatenation query the information disregarding what is being asked, actors use this tool to get a hold and mess with anything inside the code, like switching prices as shown below. 

![Screenshot (50)](https://user-images.githubusercontent.com/97658998/200481836-92bc884a-7e36-4353-94d2-163992a5ec1a.png)

### Frameworks as Prevention
* Basically, frameworks provide an alternative for string concatenation, making it easier to query and eliminating its abuse; more importantly, they offer input sanitization and syntax declaration.
*  Input sanitation will allow the framework to strip NULL characters and other malicious input normally used to piggyback SQL commands. Using the syntax shows how the statement looks before executing it to see if it is safe to run.
* These are some of the frameworks
	* Rails
	* NodeJS/Express
	* Python/SQL Alchemy
	* Django
	* Laravel
	* ASP.Net

### Targets
* Traditionally SQL attacks were directed mainly to Web Applications, however with the development of SQLite things changed. This library is a free portable database suitable for use in any IOTD that uses poorly formatted text files as storage. Some examples of elements that can be compromise are:
	* Smart Home Hubs
	* Network equipment
	* Electric Cars
	* Android Apps
	* iOS Apps

### Web Servers
* Web servers can help in this area by using ModSecurity which provides a default core set of rules that file basic SQL injection attacks.
* Web application firewalls that function as a 3rd party module to block tale characteristics of SQL injection attacks, like Naxsi
* Internet information server (ISS) to filter inbound http requests.

### NoSQL
This is a term that covers all different varieties of storage technologies that are not related with SQL queries. They are also referred to as document databases, these solutions have a different style than SQL so they reduce the possible area of attack. A clear example is “mongoDB” that queries data in a binary JSON mode, so no string can be passed, however it is exposed to BSON query objects.

### Checklist for SQL Injection
Like anything in technology, there are always vulnerabilities to exploit, so one way to reduce exposure is multiple layers of protection. So the following is a list to identify where to add security layers:
* Database
	* sufficient and appropriate database user permission set
	* Extraneous or unused database features disabled
	* Database logging enabled
	* Database backup/restore procedure
	* Database connection filtering procedures enabled(Prevent execution of multiple SQL statements in a single query)
	* Database drivers up to date

* Application
	* Using filtering options
	* Using parameterization options
	* Using DB calls only when needed?(Static site generator)
	* Code lint/checks for potential SQL injection points
	* Manual check for SQL Injection prone points
	* Application logging

* Web Server/Web Firewall
	* Use WAF SQL Injection pre-filters
	* Rate limit to prevent mass SQL Injection attempts
	* Alert on SQL Injection pattern attempts

