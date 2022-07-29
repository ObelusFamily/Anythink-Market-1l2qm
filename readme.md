# Welcome to the Anythink Market repo

To start the app use Docker. It will start both frontend and backend, including all the relevant dependencies, and the db.

Please find more info about each part in the relevant Readme file ([frontend](frontend/readme.md) and [backend](backend/README.md)).

## Development

When implementing a new feature or fixing a bug, please create a new pull request against `main` from a feature/bug branch and add `@vanessa-cooper` as reviewer.

## First setup
Install docker - https://docs.docker.com/get-docker/
### notes for linux users
The ubuntu repositories do not have a sufficiently recent version of docker-compose, and installing the debian available on the install page did not install docker-compose. I personally fixed with 
```shell
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```
Your mileage may vary.

### Verification
Run the following commands to ensure that docker is set up correctly now
```shell
docker -v
docker-compose -v
```

From within the repository, run `docker-compose up`. (This takes a bit, wait until logs calm down).

#### Verify the Backend
The following command will verify if the backend is up and running.
```shell
curl http://localhost:3000/api/ping
# {"msg":"Pong! Seems like Everythink is working, great job!"}

```
*Note: This appears to trigger a notification to anything backend, and Ness knows.*



#### Verify the Frontend
Open http://localhost:3000/register in the browser of your choice, and create a new user. 
