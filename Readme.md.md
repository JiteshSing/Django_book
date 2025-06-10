# **Django Books CRUD API**

This is a simple Django REST Framework application that provides a CRUD (Create, Read, Update, Delete) API for managing books.

## **Requirements**

* Python 3.8+  
* pip

## **Setup and Installation**

1. Clone the repository (or create the files manually as described below):  
   If you're creating the files manually, skip this step.  
2. Create a virtual environment (highly recommended):  
   This isolates your project's dependencies from your system's Python packages.  
   python \-m venv venv

3. **Activate the virtual environment:**  

   * **On Windows:**  
     venv\\Scripts\\activate

4. **Install project dependencies:**  
   pip install django djangorestframework

5. Navigate into the library\_api directory (if you created it manually):  
   If you're following the file-by-file creation, ensure terminal is in the root directory where manage.py resides.  
6. Apply database migrations:  
   This creates the necessary tables in sqlite3 database.  
   python manage.py makemigrations  
   python manage.py migrate

## **Running the Application**

 **Start the Django development server:**  
   python manage.py runserver

   The server will typically run on http://127.0.0.1:8000/.

## **API Endpoints**

All API endpoints are prefixed with /api/.

