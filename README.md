# WinRar Password: xov0113

# Setup project

### install dependencies:
```bash
composer install
```

### generate app key
```bash
php artisan key:generate
```

### get api keys
1. install fortnite / make epic games account.
2. install / open [Fiddler 4](https://www.telerik.com/download/fiddler)
3. go to Tools -> Options -> HTTPS, Select Capture HTTPS Connects
4. open Epic games launcher.
5. Look for request with `/account/api/oauth/token` endpoint. The authorization header minus the word `basic` is your **launcher token**.
6. launch fortnite.
7. Look for a **new** request with `/account/api/oauth/token` endpoint. The authorization header minus the word `basic` is your **game token**.
8. your epic games email and password are the other login credentials needed for the api.

### insert api keys
1. copy `.env.example` to `.env`
2. insert the api keys / credentials

### start server
```bash
php artisan serve
```

### get stats.
go to `/stats/{username}` route to get stats.
example: `http://localhost:8000/stats/zebthewizard`
example: `http://localhost:8000/stats/gushyz`