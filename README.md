# Continuous integration with Jenkins

## Jenkins
**Creating a project**
1. Enter descripton of project
2. Discord old builds ticked normally
3. Enter github repositry under github project tickbox
4. Restrict where project can be run
	- Tick then fill in box with sparta-ubuntu-node
5 .Source code
	- Use git per industry standard. 
	- Copy link to repositry as ssh per git clone syntax
	- Means jenkins will need verified keys

**Adding SSH key to jenkins**
1. follow steps to generate github SSH Key(in .ssh folder)
2. https://docs.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent
3. Once done go to repostries > add credentials > Jenkins.
4. Kind is SSH username
5. ID and description is dependent on contect e.g eng67max - public ID
6. SSH private key is got by ```cat key_name``` (in .ssh folder)
7. Private key is generated ssh key
8. Add key then select it. 
9. SSH public key is got by ```cat key_name.public``` (in .ssh folder)
10. This is then pasted into Github SSH keys list. 
11. Reselect your credentials and it should work

**Build Triggers**
1. Github hook trigger for GITScm polling
2. Go onto the specific repo on github
3. Settings > webhook > add webhook
4. Insert ```http://jenkins.spartaglobal.academy:8080/jenkins/github-webhook/```
5. Just the push event as lots of people on small server (will likely change)

**Build environment**
1. May need to provide secret files(dont for this example)
2. Provide Node and npm bin folder to path

**Build**
1. Add execute shell step
2. Add below command. Will automatically listen to github and test code
```
cd app/
npm install
npm test
``` 
## Theory

**Web hook**
- Inverted API call
- API call = When you ask employer if you got the job
- Inverted is where you are ready to recieve a call
- Github repositry needs link to Jenkins with this concept so it knows what to send and where to
        - Need to configure this

**Using web hook**
- Jenkins will listen for git changes
- These will then be directed to a test environment


## Web app

## Tests
**Language**
- Ran in Ruby

