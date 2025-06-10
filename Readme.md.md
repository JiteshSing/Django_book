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
   * **On macOS/Linux:**  
     source venv/bin/activate

   * **On Windows:**  
     venv\\Scripts\\activate

4. **Install project dependencies:**  
   pip install django djangorestframework

5. Navigate into the library\_api directory (if you created it manually):  
   If you're following the file-by-file creation, ensure your terminal is in the root directory where manage.py resides.  
6. Apply database migrations:  
   This creates the necessary tables in your sqlite3 database.  
   python manage.py makemigrations  
   python manage.py migrate

## **Running the Application**

1. **Start the Django development server:**  
   python manage.py runserver

   The server will typically run on http://127.0.0.1:8000/.

## **API Endpoints**

All API endpoints are prefixed with /api/.

### **Books API**

* **List all books / Create a new book:**  
  * **URL:** /api/books/  
  * **Methods:** GET, POST  
  * **GET Response (example):**  
    \[  
        {  
            "id": 1,  
            "title": "The Hitchhiker's Guide to the Galaxy",  
            "author": "Douglas Adams",  
            "publication\_year": 1979,  
            "isbn": "9780345391803"  
        },  
        {  
            "id": 2,  
            "title": "1984",  
            "author": "George Orwell",  
            "publication\_year": 1949,  
            "isbn": "9780451524935"  
        }  
    \]

  * **POST Request Body (example):**  
    {  
        "title": "New Book Title",  
        "author": "Author Name",  
        "publication\_year": 2023,  
        "isbn": "9781234567890"  
    }

* **Retrieve, Update, or Delete a specific book:**  
  * **URL:** /api/books/\<book\_id\>/ (e.g., /api/books/1/)  
  * **Methods:** GET, PUT, PATCH, DELETE  
  * **GET Response (example):**  
    {  
        "id": 1,  
        "title": "The Hitchhiker's Guide to the Galaxy",  
        "author": "Douglas Adams",  
        "publication\_year": 1979,  
        "isbn": "9780345391803"  
    }

  * **PUT Request Body (full update, example):**  
    {  
        "title": "Updated Book Title",  
        "author": "Updated Author Name",  
        "publication\_year": 2024,  
        "isbn": "9780987654321"  
    }

  * **PATCH Request Body (partial update, example):**  
    {  
        "title": "Partially Updated Title"  
    }

  * **DELETE:** Returns a 204 No Content on success.
