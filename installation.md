# Installation

There are two ways of usage the app.
1. **Docker containers**
2. Cloud version

In this section we will consider only the Docker containers installation


## Steps

### Backend part

1. create .env file

```
MONGO_URL=mongodb+srv://username:*@cluster123.r05de.mongodb.net/sftm?retryWrites=true&w=majority
SNOWFLAKE_PASSWORD="password"
SNOWFLAKE_ACCOUNT="youraccount.west-europe.azure"
PORT=8080
JWT_SECRET_KEY="set any random string here to protect your jwt authentification"
# set any random string to encrypt your password
PASSWORD_KEY="p3tiwOCewuDrE0gnZrNJqNb46DOEbF"
```

2. run the container
```
docker run -ti --env-file .env -p 8080:8080  hollister/sftm-backend
```

3. Check that the backend is installed correctly. Go to http://YOURHOSTNAME:8080/api in your browser. You should see the similar page
![](https://firebasestorage.googleapis.com/v0/b/snowflake-test-manager.appspot.com/o/backend%2Fbackend.jpg?alt=media&token=fe784267-bf65-4e99-b5a7-2903133fec72)
