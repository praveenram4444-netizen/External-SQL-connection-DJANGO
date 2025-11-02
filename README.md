                                    EXTERNAL SQL Connection Django Project
Project Objective:
To connect MYSQL database to Django for performing CRED operations to tables.
We used POSTMAN tool to perform CRED operations.

Make the DB settings in settings.py to connect external sql

        'ENGINE': 'django.db.backends.mysql',
        'NAME': "django",
        "USER":"root",
        "PASSWORD":'*****',
        "HOST":"localhost",
        "PORT":"3306",

Table Creation[app_sql/models.py]
We created book table in connected database.
Book name and author name created unique constraint so that it should be unique

Forms[app_sql/forms.py]
To handle user inputs, we created forms for book table

[app_sql/api.py]
To define all CRED operation GET,PUT,POST,DELETE
GET- Used to recieve data from table
POST-Used to insert new data to table
DELETE- Used to delete data from table
PUT- used to update data in table

Whatever operation doing here, it reflecting in Database also.

[app_sql/urls.py]
URL:http://127.0.0.1:8000/api
All url defined here to navigate.
Based on this definition only respective view will excute

POSTMAN Tool:
Use http://127.0.0.1:8000/api URL in postman tool to perform cred operations

Conclusion:
External SQL database connected to DJANGO to perform and store all operations. We checked with the help of POSTMAN tool, all operation performed perfectly.



