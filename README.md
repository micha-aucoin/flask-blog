# Flask Blog Build
### Installing Dependencies
1. create a virtual environment:
    - `python -m venv venv`
2. activate virtual environment:
    windows
    - `venv\scripts\activate.bat`
    linux/mac
    - `source venv/bin/activate`
3. install all dependencies using requirements.txt file:
    - `pip install -r requirements.txt`

### Environment Variables
- create the following env variables:
    - `SECRET_KEY` = protects from unauthorized access 
        - create the secret key value by running the following in the python interpreter:
        - `import secrets`
        - `secrets.token_hex(16)` 
    - `SQLALCHEMY_DATABASE_URI` = the path to your database
        - set the value to `sqlite:///site.db`
    - password reset functionality is configured to use a gmail server
    - `EMAIL_USER` = gmail user name
    
    #### Create & use App Passwords for Gmail Account
    1. Go to your Google Account.
    2. Select Security.
    3. Under "Signing in to Google," select App Passwords. You may need to sign in. If you  don’t have this option, it might be because:
        a. 2-Step Verification is not set up for your account.
        b. 2-Step Verification is only set up for security keys.
        c. Your account is through work, school, or other organization.
        d. You turned on Advanced Protection.
    4. At the bottom, choose Select app and choose `other (custom name)` and then type `SMTP` and then Generate.
    5. Follow the instructions to enter the App Password. The App Password is the 16-character code in the yellow bar on your device.
    6. Tap Done.

    - `EMAIL_PASS` = gmail App Password

### Run the App
- open the project in the terminal and run the following:
    - `python run.py`
    - then [click_here](http://127.0.0.1:5000)
    - the app should be up and running

    

