# Ex02 Django ORM Web Application
## Date: 

## AIM
To develop a Django application to store and retrieve data from a Book database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

![image](https://github.com/rsubash17/ORM/assets/147139828/36428c39-5751-479b-a78a-a1410b4b3bc5)


## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 books

## PROGRAM
```
from django.db import models
from django.contrib import admin
class Book_DB(models.Model):
	author=models.CharField(max_length=20);
	book_name=models.CharField(max_length=50);
	book_no=models.CharField(primary_key="book_no",max_length=10);
	customer_id=models.CharField(max_length=20);
	edition_year=models.IntegerField();
	shelfno=models.CharField(max_length=20);
	

class Book_DBAdmin(admin.ModelAdmin):
	list_display=("author","book_name","book_no","customer_id","edition_year","shelfno");
```
## admin.py
```
from django.contrib import admin
from .models import Book_DB,Book_DBAdmin
admin.site.register(Book_DB,Book_DBAdmin)
```


## OUTPUT

![image](https://github.com/rsubash17/ORM/assets/147139828/39733f3f-8af4-4aea-8b88-0a7d80b18604)



## RESULT
Thus the program for creating a database using ORM hass been executed successfully
