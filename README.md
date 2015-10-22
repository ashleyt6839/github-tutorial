# GitHub Tutorial

_by Ashley Toro_

---
## Git vs. GitHub
###Git  
Git is _version control_ and as said in the name, it allows you to be able to save diiferent versions of code on easy access. Git allows you to take _snapshots_ of code and keeps track of the changes youve done to your files with each snapshot.  
###Github  
Github is set up in the cloud. That means that code that you create is stored in the cloud and your able to colaborate withothers not only on yoru code but with others aswell.  
###Difference?  
The difference between both is that in order to use Github you **NEED** Git. Git is intended to use be used for solo work and Github is great for colaboratin work. When saving code Github stores it in the cloud as where Git stores your snapshots of code in your local machine that your using.


---
## Initial Setup  
A [**Github Account**](https://github.com) and a [**Cloud 9 Account**](https://c9.com) is needed.

Once you have created your Github account now we have to set up the SSH key, which connects your local machine(c9 or nitrous) to your remote(Github).  

 1. Click profile icon on the upper right hand corner  
 2. Go to settings  
 3. Click the SSH key tab  
 4. Click add SSH key and title the remote whatever your local machine is called   
 5. On the SSH Key for cloud 9 you click on the settings icon on your home page  
 6. Click on the SSH key tab and copy and paste the Default SSH key on your Github key box  
 7. Now click Add Key  
 
**Keep in mind** unless you signed up for Cloud 9 with your github account you should:  
1. git init (Initializes git in your local machine)  
2. git config --global user.name "First Last"  
git config --global user.name "username@email.com" (the e-mail address you used to sign up for github)

---
## Repository Setup
Let's create our first _repo_!  
With our knowldge of the command line lets:  
make a new directory and call it _github-learning_ and lets get into that _directory_   

* `mkdir github-learning`  
* `cd github-learning`  

Now lets create our repo!  
make a new directory and call it _first-repo_ and lets get into that directory  

* `mkdir first-repo`
*  `cd first-repo`

but now lets check that were in the correct spot so lets `pwd` and check that you are in:  
`~/workspace/github-learning/first-repo`  
In order to make our first add, commit, and push we have to create a file.  
Lets create a README.md file in our first-repo:  
`touch README.md`  
Open the file and type into the file "This is my first repo"  

Now lets do our first add, commit, and push!  
to add a file type in   
`git add README.md`  
`git status` to check if the file was added to the stage correctly  
`git commit -m "create my first repo"`  

However, we don't have a remote to push up to:  
1. Got to github and at the top right click the + at the top of the corner and click new repository  
2. Your repository name HAS to be the same name as "first-repo"  
3. Once you create your repository click on the SSH key and copy and paste one at a time  
`git remote add origin git@github.com:(github username)/first-repo.git`  
press enter then copy and paste  
`git push -u origin master`  

Now next time we push we don't have to type -u origin master because it has already been set up once. 


---
## Workflow & Commands

In _cloud 9_ you will need to do `git status` once in a while in order to check that what you add really adds to the stage ready to be _commited_.  
Here are some basic comannds in git:  

 * `git add`: adds the current directory onto the stage   
 Use: `git add README.md`(README.md or whatever your file name is) 
 * `git commit -m "short message"`: short present tense comments that tell you what you did to that block of code. Commiting shouldnt happen everytime you write two lines of code however you should do it to save your code and refer back to it. It also takes a snapshot of the code.  
 Use: `git commit -m "Write file name"`
 * `git log`: allows you to see your past commits  
 (Press Q to quit)
 * `git init`: initializes git in our local machine
 * `git diff`: allows you to see the difference between your old code and the new one
 * `git push`: pushes your code to your remote
 * `git add file.ext`: adds files to the stage
