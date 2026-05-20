# Wisdom Expense Manager

A Flask-based web application for managing school expenses, categories, vendors, and generating reports.

## Features

- **Dashboard**: Overview of expenses and quick statistics.
- **Expenses**: View, add, edit, and delete expenses.
- **Categories**: Manage expense categories.
- **Vendors**: Manage vendor information.
- **Reports**: Generate expense reports.
- **Settings**: Application settings and user management.

## Prerequisites

- Python 3.8+
- pip (Python package installer)

## Installation

1. Clone the repository:
   ```bash
   git clone <your-repository-url>
   cd stitch_wisdom_expense_manager_dashboard
   ```

2. Create a virtual environment (optional but recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   ```

3. Install the dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Running the Application

1. Start the Flask development server:
   ```bash
   python app.py
   ```

2. Open your web browser and navigate to:
   ```
   http://127.0.0.1:5000/
   ```

## Project Structure

- `app.py`: The main Flask application file with routing logic.
- `templates/`: HTML templates for the application pages.
- `static/`: Static assets such as CSS, JavaScript, and images.
- `requirements.txt`: Python dependencies.
- `.gitignore`: Files and directories to be ignored by Git.

## License

[MIT License](LICENSE)
