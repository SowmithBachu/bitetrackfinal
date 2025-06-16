BiteTrack
BiteTrack is a comprehensive meal planning and nutrition tracking application built with Flask. It features an interactive dashboard for meal planning, nutrition analytics, and health monitoring.

Features
Interactive dashboard with meal planning
Nutrition analytics and charts
Weight progress tracking
Food allergy alerts
Meal generation based on preferences
User authentication system
Installation
Clone the repository:
git clone https://github.com/yourusername/bitetrack.git
cd bitetrack
Create a virtual environment and activate it:
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
Install dependencies:
pip install -r requirements.txt
Set up the database:
flask db init
flask db migrate
flask db upgrade
Running the Application
Set the Flask environment variables:
set FLASK_APP=bitetrack.app
set FLASK_ENV=development
Run the application:
flask run
The application will be available at http://localhost:5000

Project Structure
bitetrack/
├── app.py              # Main application file
├── static/            # Static files (CSS, JS)
│   ├── css/
│   └── js/
└── templates/         # HTML templates
    ├── base.html
    ├── dashboard.html
    └── analytics.html
Contributing
Fork the repository
Create your feature branch (git checkout -b feature/AmazingFeature)
Commit your changes (git commit -m 'Add some AmazingFeature')
Push to the branch (git push origin feature/AmazingFeature)
Open a Pull Request
License
This project is licensed under the MIT License - see the LICENSE file for details.

Deployment Options
1. Deploy to Render (Recommended)
Create a Render account
Click "New +" and select "Web Service"
Connect your GitHub repository
Fill in the details:
Name: bitetrack
Environment: Python
Build Command: pip install -r requirements.txt
Start Command: gunicorn -c gunicorn_config.py 'bitetrack.app:app'
Click "Create Web Service"
2. Deploy to Railway
Create a Railway account
Click "New Project" and select "Deploy from GitHub repo"
Select your repository
Railway will automatically detect your Python app
Add the following environment variables:
FLASK_ENV=production
SECRET_KEY=your-secret-key
3. Deploy to PythonAnywhere
Create a PythonAnywhere account
Go to the Web tab and click "Add a new web app"
Choose Manual Configuration and Python 3.9
Set up your virtual environment:
mkvirtualenv --python=/usr/bin/python3.9 myenv
pip install -r requirements.txt
Configure your WSGI file according to PythonAnywhere's instructions
Environment Variables
Make sure to set these environment variables in your deployment platform:

FLASK_ENV: Set to 'production'
SECRET_KEY: Your secret key for Flask
DATABASE_URL: Your database URL (if using external database)
Database Setup
The application uses SQLite by default, but for production, it's recommended to use PostgreSQL:

Create a PostgreSQL database in your deployment platform
Set the DATABASE_URL environment variable
The application will automatically use the PostgreSQL database in production
Running Locally
# Install dependencies
pip install -r requirements.txt

# Run the application
python -m flask run
Features
User authentication
Meal tracking
Nutrition analytics
Progress monitoring
Meal planning
Interactive dashboard
