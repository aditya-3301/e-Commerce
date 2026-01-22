# Setting Up e-Commerce - Online Delivery System
e-Commerce is a plain html css and python backend driven online delivery system designed to simulate the functionality of a modern e-commerce platform. This project concentrates on products, authentication of users, verifying thru e-mail, and database operations.

It is built using Python with FastAPI and uses a SQLite database for local development. The system includes a database population script that automatically seeds the application with a sample retailer account and hundreds of products with their  images that make testing features easy .


## Initial Requirements

To get started with this project, ensure you have the following installed on your machine:

- Python version 3.9 or higher
- Pip (Python package manager)

## Installing Required Packages

Navigate to the main project directory and install the required dependencies using:

    pip install -r requirements.txt

## Environment Configuration

To enable core features such as email verification, environment variables must be configured.

Create a `.env` file inside the `backend/app/` directory and add the following values:

    SECRET_KEY=your_unique_secret_key_here
    MAIL_USERNAME=your_gmail_address@example.com
    MAIL_PASSWORD=your_gmail_app_password
    MAIL_FROM=your_gmail_address@example.com
    MAIL_PORT=587
    MAIL_SERVER=smtp.gmail.com

For local testing, these values can alternatively be hardcoded directly in the `auth.py` file.

## Preparing the Database

The application requires initial data to function properly.

Navigate to the backend application directory and run the database population script:

    cd backend/app
    python populate_db.py

This script will:
- Create the `livemart.db` database file
- Create a sample retailer account with ID 1
- Insert over 200 products
- Download and store product images in `backend/data/product_images/`

## Launching the Application

Start the development server by running the following command from the `backend/app/` directory:

    uvicorn main:app --reload

Once running, the application will be accessible through your web browser.
