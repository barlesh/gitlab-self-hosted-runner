# gitlab-self-hosted-runner
quickly setup a GitLab Self-hosted service on your local machine

## Instructions

1. Set the ```GITLAB_HOME``` variable in the .env file & load the .env variables into your session, or use any other method so this variable will be available for the **init-env.sh** script.
I'm using [teller](https://github.com/SpectralOps/teller) for these kind of actions
```
eval "$(teller sh)"
```
2. Run the init-env.sh script in order to create the necessary folders structure and give permissions. make sure GITLAB_HOME is set
```
./init-env.sh
```
3. Edit the .env file with your prefferd configurations.
4. Run init-gitlab-sh.sh in order to run the service.
```
./init-gitlab-sh.sh
```
5. After the service is up, make sure that the UI is available by routing to http://localhost:{SERVER_PORT} in your browser.
6. A root user is created automatically - root
7. The generated password for this user can be retrive with the get-root-password.sh script (make sure that GITLAB_HOME is set in the session, like in step 1)
```
./get-root-password.sh
```
8. Start using the service.  

Enjoy!