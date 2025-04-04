# Backend Setup

## Setting Django secret key
- Within the MD_Attractor/settings.py, replace the DJANGO_SECRET_KEY part with the secret key generated by you.
    ```
    SECRET_KEY = 'your_secret_key_here'
    ```

## Setting Spotify Credentials
- within the song_api/spotifyAPI.py, replace the client_id and client_secret_key part with the credentials generated by you.
    ```
    self.client_id = 'SPOTIFY_CLIENT_ID'
    self.client_secret = 'SPOTIFY_SECRET_KEY'
    ```

## Starting Backend Server
1. Setup admin user `python manage.py createsuperuser`.
2. Start the Django server by running `python manage.py runserver`.
3. The server will be running on `http://localhost:8000'.

## Usage
1. Access the application in your web browser at `http://localhost:8000`.
2. For better visualization and testing of API endpoints, you can use Postman. Download and install Postman from [https://www.postman.com/](https://www.postman.com/).


## API Endpoints
```bash
http://localhost:8000/admin         #View Django admin panel
http://localhost:8000/              #Song Search Feature
http://localhost:8000/history       #View Search History
```

Certainly! Below is an updated section for your `README.md` that addresses the installation issue and provides a resolution.

---

