# Redash using docker compose
## Requirements to run this project

- docker (20.10.5+): To install docker visit https://docs.docker.com/get-docker/
- docker-compose (1.25.5+): To install docker-compose visit https://docs.docker.com/compose/install/
- Make:
    - MACOS USERS:
        - Make should be installed with XCode dev tools
        - If not, run `xcode-select --install` in Terminal to install.
    - WINDOWS USERS:
        - Install Chocolately package manager: https://chocolatey.org/
        - Open Command Prompt in administrator mode
        - Run `choco install make`
        - Restart all Git Bash/Terminal windows.


## Getting started

**To start project with make command:**
 - install docker
 - install docker-compose
 - install make command
 - Clone the project  
 - Change directory to the project directory
 - Create `.env` file in project root or in same directory as `.sample.env`
 - Copy values from `.sample.env` to `.env`
 - Run:
    ```bash
    make start-redash
    ```
 - The application would be available at http://localhost:5000/


**To stop project with make command:**
 - Run:
    ```bash
    make stop-redash
    ```
 - Delete data folder created (This step is optional).

**To start project with docker-compose:**
 - Change directory to the project directory 
 - Create `.env` file in project root or in same directory as `.sample.env`
 - Copy values from `.sample.env` to `.env`
 - Run:
    ```bash
    docker-compose run --rm server create_db
    ```
- Run:
    ```bash
    docker-compose up --build
    ```
 - The application would be available at http://localhost:5000/


**To stop project with docker-compose:**
- Run:
    ```bash
    docker-compose down -v 
    ```
- Run:
    ```bash
    docker-compose down
    ```
- Delete data folder created (This step is optional).
