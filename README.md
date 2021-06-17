# CICD_with_Jenkins
![jenkins](https://user-images.githubusercontent.com/32297246/122410832-2ba41500-cf7c-11eb-8f5d-1bfca6339171.png)

## Creating a job on Jenkins
- Click 'create new job'
- Name the job appropriately
- Select 'freestyle project'
- Enter an appropriate description
- Check the 'discard old builds box' and enter 3 as the max number of builds (keeps workspace clean)
- Under build select 'shell'
- Linux commands can be entered here to test
- Once the job is saved, 'build now' can be clicked to start the job
- A console is avaible to view test progress/stack trace
 
 
## Linking with Github
### Generating SSH key
- generate a new key on the command line using `ssh-keygen -t rsa -b 4096 "email@example.com"`
- Do not add a passphrase
- This will generate a public and private key.
- The public key goes into the repo Deploy keys


## Editing the job
- Tick the github project box and link the repo
- Tick git under source code management and add the SSH URL to the repo
- Create a new keya nd select SSH username with private key
- Enter the username and private key
- Tick the git hook trigger
- In this instance, tick the box to install node
- in the console box, write 
```
cd app
npm install
npm test
````
- This will run the tests in the app folder

