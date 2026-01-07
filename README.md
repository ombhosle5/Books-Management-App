# 📚 Books Management App

A simple Django web application for managing a collection of books with full CRUD (Create, Read, Update, Delete) functionality.

## 🎯 Features

- **List View**: Display all books in the database
- **Detail View**: View individual book information
- **Create**: Add new books to the collection
- **Update**: Edit existing book details
- **Delete**: Remove books from the database
- **Responsive UI**: Clean and simple styling with CSS
## images
<img width="1920" height="1080" alt="Book_list " src="https://github.com/user-attachments/assets/46edeb8f-5641-4012-8322-39436389bfc4" />
<img width="1920" height="1080" alt="new_book" src="https://github.com/user-attachments/assets/584a2570-8de4-4b5f-84e3-914494cabf39" />
<img width="1920" height="1080" alt="edit_book" src="https://github.com/user-attachments/assets/690ba34b-2c49-4bba-a481-0b6ecfb4d720" />
<img width="1920" height="1080" alt="delete_book" src="https://github.com/user-attachments/assets/bd2f22b3-80f2-4584-a492-c214299f72ca" />

## 🛠️ Technology Stack

- **Backend**: Django 5.x
- **Database**: SQLite (default)
- **Frontend**: HTML, CSS
- **Python**: 3.12

## 📁 Project Structure

```
app/
│   admin.py          # Admin panel configuration
│   apps.py           # App configuration
│   forms.py          # Django forms for book creation/editing
│   models.py         # Book model definition
│   tests.py          # Unit tests
│   urls.py           # URL routing for the app
│   views.py          # View functions (business logic)
│   __init__.py
│
├───migrations/       # Database migrations
├───static/css/       # CSS stylesheets
├───templates/books/  # HTML templates
│       book_delete.html
│       book_detail.html
│       book_form.html
│       book_list.html
└───__pycache__/      # Python cache files
```

## 🚀 Getting Started

### Prerequisites

- Python 3.8 or higher
- pip (Python package manager)

### Installation

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd Django_1
   ```

2. **Create a virtual environment** (recommended)
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install django
   ```

4. **Run migrations**
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

5. **Create a superuser** (for admin access)
   ```bash
   python manage.py createsuperuser
   ```

6. **Run the development server**
   ```bash
   python manage.py runserver
   ```

7. **Access the application**
   - Main app: `http://127.0.0.1:8000/books/`
   - Admin panel: `http://127.0.0.1:8000/admin/`

## 📝 Database Model

### Book Model

| Field  | Type          | Description           |
|--------|---------------|-----------------------|
| id     | Integer (PK)  | Auto-generated ID     |
| title  | CharField     | Book title (max 200)  |
| author | CharField     | Author name (max 100) |
| price  | DecimalField  | Book price            |

## 🔗 URL Routes

| URL Pattern           | View Function  | Description              |
|-----------------------|----------------|--------------------------|
| `/books/`             | book_list      | Display all books        |
| `/books/create/`      | book_create    | Form to add new book     |
| `/books/<pk>/`        | book_detail    | View single book details |
| `/books/<pk>/update/` | book_update    | Edit existing book       |
| `/books/<pk>/delete/` | book_delete    | Delete confirmation page |

## 💡 Usage Examples

### Adding a New Book
1. Navigate to `/books/create/`
2. Fill in the book details (title, author, price)
3. Click "Save"
4. Redirects to the book list

### Editing a Book
1. From the book list or detail page, click "Edit"
2. Modify the fields
3. Click "Save"

### Deleting a Book
1. Click "Delete" on any book
2. Confirm deletion
3. Book is removed from database

## 🎨 Customization

### Modifying the Model
Edit `models.py` to add more fields:
```python
class Book(models.Model):
    title = models.CharField(max_length=200)
    author = models.CharField(max_length=100)
    price = models.DecimalField(max_digits=6, decimal_places=2)
    # Add new fields here
    isbn = models.CharField(max_length=13)
    published_date = models.DateField()
```

Then run:
```bash
python manage.py makemigrations
python manage.py migrate
```

### Styling
CSS files are located in `static/css/style.css`. Modify to change the appearance.

## 🧪 Testing

Run tests with:
```bash
python manage.py test app
```

## 📚 Learning Objectives

This project demonstrates:
- Django MVT (Model-View-Template) architecture
- CRUD operations with Django ORM
- Form handling and validation
- URL routing and naming
- Template inheritance
- Static file management
- Admin interface integration

## 🤝 Contributing

This is a learning project. Feel free to fork and experiment!

## 📄 License

This project is open source and available for educational purposes.

## 👤 Author

**Om Bhosle**
- Practice Project: Django CRUD Operations
- Date: January 2026

## 🙏 Acknowledgments

- Django Documentation
- Python Community
- Learning by building!

---

**Happy Coding!** 🚀
