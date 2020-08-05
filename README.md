# Continuous integration with Jenkins

## Jenkins
**Creating a project**
- 1 .Enter descripton of project
- 2 .Discord old builds ticked normally
- 3 .Enter github repositry under github project tickbox
- 4. Restrict where project can be run
	- Tick then fill in box with sparta-ubuntu-node
- 5 .Source code
	- Use git per industry standard. 
	- Copy link to repositry as ssh per git clone syntax
	- Means jenkins will need verified keys

**Adding SSH key to jenkins**
- follow steps to generate github SSH Key(in .ssh folder)
- https://docs.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent
- Once done go to repostries > add credentials > Jenkins.
- Kind is SSH username
- ID and description is dependent on contect e.g eng67max - public ID
- SSH private key is got by ```cat key_name``` (in .ssh folder)
- Private key is generated ssh key
- Add key then select it. 
- SSH public key is got by ```cat key_name.public``` (in .ssh folder)
- This is then pasted into Github SSH keys list. 
- Reselect your credentials and it should work

**Build Triggers**
- Github hook trigger for GITScm polling
- Go onto the specific repo on github
- Settings > webhook > add webhook
- Insert ```http://jenkins.spartaglobal.academy:8080/jenkins/github-webhook/```
- Just the push event as lots of people on small server (will likely change)


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

