# [CoreUI](https://appseed.us/generator/coreui/) Flask

Open-source **Flask Dashboard** generated by `AppSeed` op top of an iconic design. For newcomers, **[CoreUI](https://appseed.us/generator/coreui/)** is one of the best open-source admin dashboard & control panel theme. Built on top of Bootstrap, `CoreUI` provides a range of responsive, reusable, and commonly used components. 

- 👉 [CoreUI Flask](https://appseed.us/product/coreui/flask/) - product page
- 👉 [CoreUI Flask](https://flask-coreui.appseed-srv1.com/) - LIVE Deployment
- 👉 [Complete documentation](https://docs.appseed.us/products/flask-dashboards/coreui) - `Learn how to use and update the product`
  - ✅ [Set up the environment](https://docs.appseed.us/products/flask-dashboards/coreui#environment)
  - ✅ [Manage App users](https://docs.appseed.us/products/flask-dashboards/coreui#manage-app-users)
  - ✅ [Application Bootstrap Flow](https://docs.appseed.us/products/flask-dashboards/coreui#application-bootstrap-flow)
  - ✅ [UI Assets and Templates](https://docs.appseed.us/products/flask-dashboards/coreui#ui-assets-and-templates)
  - ✅ [Set up the MySql Database](https://docs.appseed.us/products/flask-dashboards/coreui#set-up-the-mysql-database)
  - ✅ [Static Assets for production](https://docs.appseed.us/products/flask-dashboards/coreui#static-assets-for-production) 

<br />

> Built with [CoreUI Generator](https://appseed.us/generator/coreui/)

- Timestamp: `2022-06-01 09:08`
- Build ID: `6e2f2c1a-9b20-4bf8-8b7a-2d8717100cb0`
- **Free [Support](https://appseed.us/support/)** (registered users) via `Email` and `Discord`

<br />

> Features

- `Up-to-date dependencies`
- Database: `mysql`
- `DB Tools`: SQLAlchemy ORM, Flask-Migrate (schema migrations)
- Session-Based authentication (via **flask_login**), Forms validation

<br />

![CoreUI Dashboard - Starter generated by AppSeed.](https://user-images.githubusercontent.com/51070104/171336361-b125ca1d-8936-4f4a-b662-9e45ee25f404.png)

<br /> 

## ✨ Start the app in Docker

> **Step 1** - Download the code from the GH repository (using `GIT`) 

```bash
$ # Get the code
$ git clone https://github.com/app-generator/flask-coreui.git
$ cd flask-coreui
```

<br />

> **Step 2** - Edit `.env` and set `DEBUG=True`. This will activate the `SQLite` persistance. 

```txt
DEBUG=True
```

<br />

> **Step 3** - Start the APP in `Docker`

```bash
$ docker-compose up --build 
```

Visit `http://localhost:5085` in your browser. The app should be up & running.

<br />



## ✨ Set up the MySql Database

**Note:** Make sure your Mysql server is properly installed and accessible. 

> **Step 1** - Create the MySql Database to be used by the app

- `Create a new MySql` database
- `Create a new user` and assign full privilegies (read/write)

<br />

> **Step 2** - Edit the `.env` to match your MySql DB credentials. Make sure `DB_ENGINE` is set to `mysql`.

- `DB_ENGINE`  : `mysql` 
- `DB_NAME`    : default value = `appseed_db`
- `DB_HOST`    : default value = `localhost`
- `DB_PORT`    : default value = `3306`
- `DB_USERNAME`: default value = `appseed_db_usr`
- `DB_PASS`    : default value = `pass`

<br />

Here is a sample:  

```txt
# .env sample

DEBUG=False                   # False enables the MySql Persistence

DB_ENGINE=mysql               # Database Driver
DB_NAME=appseed_flask         # Database Name
DB_USERNAME=appseed_flask_usr # Database User
DB_PASS=STRONG_PASS_HERE      # Password 
DB_HOST=localhost             # Database HOST, default is localhost 
DB_PORT=3306                  # MySql port, default = 3306 
```

<br />


## ✨ How to use it

> Download the code 

```bash
$ # Get the code
$ git clone https://github.com/app-generator/flask-coreui.git
$ cd flask-coreui
```

<br />

### 👉 Set Up for `Unix`, `MacOS` 

> Install modules via `VENV`  

```bash
$ virtualenv env
$ source env/bin/activate
$ pip3 install -r requirements.txt
```

<br />

> Set Up Flask Environment

```bash
$ export FLASK_APP=run.py
$ export FLASK_ENV=development
```

<br />

> Start the app

```bash
$ flask run
```

At this point, the app runs at `http://127.0.0.1:5000/`. 

<br />

### 👉 Set Up for `Windows` 

> Install modules via `VENV` (windows) 

```
$ virtualenv env
$ .\env\Scripts\activate
$ pip3 install -r requirements.txt
```

<br />

> Set Up Flask Environment

```bash
$ # CMD 
$ set FLASK_APP=run.py
$ set FLASK_ENV=development
$
$ # Powershell
$ $env:FLASK_APP = ".\run.py"
$ $env:FLASK_ENV = "development"
```

<br />

> Start the app

```bash
$ flask run
```

At this point, the app runs at `http://127.0.0.1:5000/`. 

<br />

### 👉 Create Users

By default, the app redirects guest users to authenticate. In order to access the private pages, follow this set up: 

- Start the app via `flask run`
- Access the `registration` page and create a new user:
  - `http://127.0.0.1:5000/register`
- Access the `sign in` page and authenticate
  - `http://127.0.0.1:5000/login`

<br />

## ✨ Code-base structure

The project is coded using blueprints, app factory pattern, dual configuration profile (development and production) and an intuitive structure presented bellow:

```bash
< PROJECT ROOT >
   |
   |-- apps/
   |    |
   |    |-- home/                           # A simple app that serve HTML files
   |    |    |-- routes.py                  # Define app routes
   |    |
   |    |-- authentication/                 # Handles auth routes (login and register)
   |    |    |-- routes.py                  # Define authentication routes  
   |    |    |-- models.py                  # Defines models  
   |    |    |-- forms.py                   # Define auth forms (login and register) 
   |    |
   |    |-- static/
   |    |    |-- <css, JS, images>          # CSS files, Javascripts files
   |    |
   |    |-- templates/                      # Templates used to render pages
   |    |    |-- includes/                  # HTML chunks and components
   |    |    |    |-- navigation.html       # Top menu component
   |    |    |    |-- sidebar.html          # Sidebar component
   |    |    |    |-- footer.html           # App Footer
   |    |    |    |-- scripts.html          # Scripts common to all pages
   |    |    |
   |    |    |-- layouts/                   # Master pages
   |    |    |    |-- base-fullscreen.html  # Used by Authentication pages
   |    |    |    |-- base.html             # Used by common pages
   |    |    |
   |    |    |-- accounts/                  # Authentication pages
   |    |    |    |-- login.html            # Login page
   |    |    |    |-- register.html         # Register page
   |    |    |
   |    |    |-- home/                      # UI Kit Pages
   |    |         |-- index.html            # Index page
   |    |         |-- 404-page.html         # 404 page
   |    |         |-- *.html                # All other pages
   |    |    
   |  config.py                             # Set up the app
   |    __init__.py                         # Initialize the app
   |
   |-- requirements.txt                     # App Dependencies
   |
   |-- .env                                 # Inject Configuration via Environment
   |-- run.py                               # Start the app - WSGI gateway
   |
   |-- ************************************************************************
```

<br />

## ✨ PRO Version

> For more components, pages and priority on support, feel free to take a look at this amazing starter:

Soft UI Dashboard is a premium Bootstrap 5 Design now available for download in Flask. Made of hundred of elements, designed blocks, and fully coded pages, Soft UI Dashboard PRO is ready to help you create stunning websites and web apps.

- 👉 [Soft UI Dashboard PRO Flask](https://appseed.us/product/soft-ui-dashboard-pro/flask/) - Product Page
- 👉 [Soft UI Dashboard PRO Flask](https://flask-soft-ui-dashboard-pro.appseed-srv1.com/) - LIVE Demo 

<br >

![Soft UI Dashboard PRO - Starter generated by AppSeed.](https://user-images.githubusercontent.com/51070104/170829870-8acde5af-849a-4878-b833-3be7e67cff2d.png)

<br />

---
[CoreUI](https://appseed.us/generator/coreui/) Flask - Open-source starter generated by **[AppSeed Generator](https://appseed.us/generator/)**.
