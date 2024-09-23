# Setup project

## Setup Environment
1. Make a copy of `.env.example` and create `.env` file
2. Run `docker-compose build --no-cache`

#### Setup:Backend
4. Go to repository: [Book Store](https://github.com/entymon/book-store-php)
5. Clone project into `codebase` directory

#### Setup:Frontend
6. Go to repository: [Book Store UI](https://github.com/entymon/book-store-ui)
7. Clone project into `bookstore` directory

8. Follow instructions on README.md attached to the cloned projects
9. Run `docker-compose up` in the root of project


# Setup new project (IGNORE )

### Setup new SF project (Only)
1. Open `docker/server/Dockerfile` file and replace `{GITHUB_EMAIL_ADDRESS}` and `{GITHUB_USERNAME}` with appropriate data. Uncomment the lines.
2. Run command: `docker-compose exec server bash` to get in to the server
4. Run `symfony check:requirements` to check if all requirements for SF8 are met
5. Run `symfony local:new --dir .` 

### Re-create docker images
1. Run `docker-compose down`
2. Run `docker-compose build --no-cache` - recreating docker images
3. Run `docker-compose up` 