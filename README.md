
## 1. Ensure heroku is installed
```
heroku --version
```

## 2. Check that you're logged in to heroku 

```
heroku login
```

## 3. Navigate to your project directory, and create a Heroku app

The appName argument is optional. If you just run `heroku create` it will give you a random app name (e.g. ocean-breeze93.herokuapp.com). This app name is also what will be your URL (e.g. appName.herokuapp.com)

```
heroku create <appName>
```

## 4. Remember to set your port to
```
const port = process.env.PORT || <yourOriginalPortNum>

app.listen(port, ()=> {
  ....
})
```

## 5. Add your start scripts in package.json
```
  "scripts": {

    "start": "node server.js",
```

## 6. Commit all your changes via git 
```
git add, git commit
```

## 5. Push your changes to both Github (origin) and Heroku (heroku)

```
git push origin master
git push heroku main
```

## 6. Check your app on heroku! (It won't work without the environment variables)
```
<appname>.herokuapp.com
```
