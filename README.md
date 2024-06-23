# Flask-SSO
# Google OAuth 2.0 Example App
This is a Flask app that demonstrates how to use Google OAuth 2.0 to authenticate users and retrieve their email addresses.

# Setup
1. Create a Google Cloud Console project and enable the Google OAuth 2.0 API.
2. Create a new OAuth 2.0 client ID and secret key.
3. Set the `GOOGLE_CLIENT_ID` and `GOOGLE_SECRET_KEY` environment variables to your client ID and secret key, respectively.
4. `pip install -r requirements.txt`
5. Run the app using `python app.py` & `flask run`.

# How it Works
1. The app redirects the user to the Google OAuth 2.0 authorization URL.
2. The user authenticates with Google and grants access to their email address.
3. Google redirects the user back to the app with an authorization code.
4. The app exchanges the authorization code for an access token.
5. The app uses the access token to retrieve the user's email address from the Google OAuth 2.0 API.
6. The app redirects the user to a success page with their email address.

# Endpoints
* `/`: Redirects to the Google OAuth 2.0 authorization URL.
* `/home`: Handles the redirect from Google OAuth 2.0 and exchanges the authorization code for an access token.
* `/user/<email>`: Displays a success page with the user's email address.
# Dependencies
* Flask
* oauthlib
* requests
* dotenv