# Pet-Adoption-Website
**OBJECTIVE**

Each year, it&#39;s estimated that more than one million adoptable dogs and cats are euthanized in the United States, simply because too many pets come into shelters and too few people consider adoption when looking for a pet.

The number of euthanized animals could be reduced dramatically if more people adopted pets instead of buying them. When you adopt, you save a loving animal by making them part of your family and open up shelter space for another animal who might desperately need it.

The cost of adoption is free in contrast to the cost of purebred puppies or kittens sold for profit.

This website helps people find their perfect pet online and are connected to the owners/rescuers that are geographically spread at different locations.

**ER DIAGRAM**

![](RackMultipart20201201-4-o5vipc_html_f257efcbb4eda42c.png)

**RELATIONAL MODEL**

![](RackMultipart20201201-4-o5vipc_html_42067d5827336433.png)

**SOFTWARE USED**

**PHP**

PHP is a widely-used general-purpose scripting language that is especially suited for Web development and can be embedded into HTML. All server-side code was written in php. It is used to dynamically update the values on our webpage and help in querying the database and receiving the query results from the hosted database and get it to the webpage. The design was done in Windows in a WAMP environment.

**HTML**

HTML, or Hypertext Mark-up Language, is used to create web pages. Used for the basic front-end design of the websiteand it helps in giving structure to the page, to format text as titles and headings, to arrange graphics on a webpage, to link to different pages within a website, and to link to different websites.

**CSS**

Cascading Style Sheets is a style sheet languageused for describing the presentationof a document written in amarkup language which includes colors, layout, and fonts. It allows one to adapt the presentation to different types of devices, such as large screens, small screens, or printers.

Why did we use PHP and MySQL combination to build our site?

- _ **Easy** _: This server side scripting language is extremely easy to learn.
- _ **Cost efficient** _: PHP is open source, it is free of cost. You need
- not buy expensive software for it. Your website will be developed in the minimal cost.
- _ **Efficient** _: You can enhance the performance of the website built in PHP, as it is scalable when writing the code as well as reliable too when you need to deal with a lot of web pages.
- _ **Access to support** _: As PHP is being used by a huge number of people, a large community is formed. So, you need not worry if you get stuck somewhere.

**DATABASE CONNECTIVITY STEPS**

**STEP 1:** Create a database called  **registration**.

In the  **registration**  database, add following tables:

- users – stores the registered users
- pets – stores the pets that are up for adoption
- wishlist – stores the pets that are liked by the respective user

_ **USER** _

![](RackMultipart20201201-4-o5vipc_html_bec160430ab0f281.png)

_ **PETS** _ ![](RackMultipart20201201-4-o5vipc_html_7b987b5e63705788.png)

_ **WISHLIST** _

![](RackMultipart20201201-4-o5vipc_html_8958e3f13f593c46.png)

**STEP 2:** Connect to the database

![](RackMultipart20201201-4-o5vipc_html_bec59f238e307570.png)

- mysqli\_connect is the function for php database connection
- &quot;localhost&quot; is the name or IP address of the server hosting MySQL server.
- &quot;root&quot; is a valid user name in MySQL server.
- &quot;project&quot; is a valid password associated with a user name in MySQL server. (local in my case)
- &quot;registeration&quot; is the name of the database

**STEP 3:** Check the connection

![](RackMultipart20201201-4-o5vipc_html_19afb7fac8206f7e.png)

**STEP 4:** Close the connection

![](RackMultipart20201201-4-o5vipc_html_bea59ab1b15423ea.png)

**MODULES**

1. **Home Page**
2. **Registration**
3. **Login**
4. **View all the pets**
5. **Add a new pet**
6. **Delete a pet**
7. **Add to Wishlist**
8. **Logout**

_ **HOME PAGE** _ _ **-first.php** _

This is the initial page that leads you to the Login or Registration page. ![](RackMultipart20201201-4-o5vipc_html_b2ffc4fed9b5029e.png)

![](RackMultipart20201201-4-o5vipc_html_e9d97332061a8a96.png)

_ **SIGN UP/REGISTRATION PAGE** _ _ **-register.php** _

Enables one to register himself for the website. Only after being a registered user can one view/add the pets on the site.When a user is registered in the database, they are immediately logged in and redirected to the pet details page.

![](RackMultipart20201201-4-o5vipc_html_8ac8210d94fe89f.png) ![](RackMultipart20201201-4-o5vipc_html_1a9d3e4d33eb3115.png) ![](RackMultipart20201201-4-o5vipc_html_a35cc906eccec1a.png)

The form&#39;s  **action**  attribute is set to register.php. This means that when the form submit button is clicked, all the data in the form will be submitted to the same page (register.php).

All the data is received from the form and checked to make sure that the user correctly filled the form. Passwords are also compared to make sure they match. ![](RackMultipart20201201-4-o5vipc_html_cb834d3e25c595b3.png)

We include the **errors.php** file to display form errors. If no errors were encountered, the user is registered in the  **users**  table in the database with a hashed password. The hashed password is for security reasons. It ensures that even if a hacker manages to gain access to your database, they would not be able to read your password.

**VALIDATION**

- **If the username field is empty**

![](RackMultipart20201201-4-o5vipc_html_c75b6eaa673edded.png)

- **If the email id is in the wrong format**

![](RackMultipart20201201-4-o5vipc_html_5bac0237bd2f949e.png)

- **For the password to be strong, it must be in the required format**

![](RackMultipart20201201-4-o5vipc_html_9bdb3fbe08c77647.png)

- **If entered username already exits**

![](RackMultipart20201201-4-o5vipc_html_4bdc23b63a400eee.png)

- **If passwords do not match or the registered email already exists in the database**

![](RackMultipart20201201-4-o5vipc_html_3acc1e057d0cdda1.png)

_ **LOGIN PAGE** _ _ **– login.php** _

If one is already registered, then they can directly log in.

![](RackMultipart20201201-4-o5vipc_html_2a50421dd5ff458f.png)

This checks if the user has filled the form correctly, verifies that their credentials match a record from the database and logs them in if it does. After logging in, the user is redirected them to the **index.php** file with a success message.

_ **INDEX PAGE** _ _ **– index.php** _

![](RackMultipart20201201-4-o5vipc_html_da7503562d1f3203.png)

_ **DETAILS PAGE** _ _ **-g.php** _

![](RackMultipart20201201-4-o5vipc_html_f2ca32c1d32b52f1.png)

The user can view all the pets that can be adopted. They can also add pets to their **Wishlist** so that it can be viewed later.

If they wish they can also **ADD** a pet.

**DELETING** a pet can be done only by the admin.

**Logging**** out** will end the user session and would be redirected to the initial(first.php) page.

_ **ADD A PET** _ _ **– add.php** _

![](RackMultipart20201201-4-o5vipc_html_8a8232f8d03b4c8d.png)

_ **DELETE A PET** _ _ **– delete.php** _

![](RackMultipart20201201-4-o5vipc_html_ed90000ff3acb11.png)

![](RackMultipart20201201-4-o5vipc_html_45709013b8835857.png)

![](RackMultipart20201201-4-o5vipc_html_21e3fd0916d5c122.png)

_ **WISHLIST** _ _ **– wish.php** _

Every user can have their personalized Wishlist where they cam save all their likes which would help them narrow down on a pet of their choice.

![](RackMultipart20201201-4-o5vipc_html_653289694b5adf3c.png)

One can also remove a pet from the list. This option can be used by clicking &quot;Remove a pet&quot; which is present on the side navigation bar.

**PERSONALISED WISHLIST**

![](RackMultipart20201201-4-o5vipc_html_d739d369b0fe79d.png)
