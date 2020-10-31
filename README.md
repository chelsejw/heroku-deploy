
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

## 7. Add you environment variables

1. Go to https://dashboard.heroku.com/apps
2. Click on your app
3. Go to Settings
4. Scroll down a bit, there should be a Reveal Config Vars button
5. Set the key value pairs as per your .env

## 8. Ensure your package.json is in the root of your project

Your file structure should be such that if you do an `ls` from the root you should see package.json right away. (So your package j.json should be located in `~/project-directory/package.json`, not something like `~/project-directory/main/package.json`)

If it's not in the root you will get an error from Heroku saying that the build failed when you do `git push heroku master`
