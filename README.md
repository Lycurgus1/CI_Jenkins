# Continuous integration with Jenkins

## Jenkins
**Creating a project**
- Enter descripton of project
- Discord old builds ticked normally
- Enter github repositry under github project tickbox
- Restrict where project can be run
	- Tick then fill in box with sparta-ubuntu-node
- Source code
	- Use git per industry standard. 
	- Copy link to repositry as ssh per git clone syntax
	- Means jenkins will need verified keys

**Adding SSH key to jenkins**
- follow steps to generate github SSH Key
- https://docs.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent
- Once done go to repostries > add credentials > Jenkins.
- Kind is SSH username
- ID and description is dependent on contect e.g eng67max - public ID
- SSH private key is got by ```cat key_name```
- Private key is generated ssh key
- Add key then select it. 
- SSH public key is got by ```cat key_name.public```
- This is then pasted into Github SSH keys list. 
- Reselect your credentials and it should work


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

