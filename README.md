# git
git clone <url> 					// first pull is clone 
git push                                            	// if upstream is set git push can be used alone, by default will push to same branch or create if not exist
git push origin <master> 				// need to use origin master if upstream was not set 
git push --set-upstream origin master               	// for upstream
git push -u origin master/main                      	// shorthand
git pull origin {remotebranc}:{localbranch}	    	// pull from remote branch
git pull                                            	// will fetch and merge corresponding to current branch 
git pull origin master 
git pull --rebase					// to rebase from remote
git fetch						// updates remote references i.e pointers copy                           
git merge origin/master              			// used after fetch to fast forward and should be called from the branch receiving the merge
git remote add origin <url>  				// add origin as remote alias
git remote                                          	// will return origin which is the remote pointer 
git remote -v                                       	// list remote repositories
git remote show                                 	// view remotes
git remote show origin
git branch -a					   	// view remote branches
git remote rm remotename                         	// remove remote

git stash save "reminder"				// new stash
git stash save -u "reminder"				// new stash including added
git stash lis						// view stashes with their id and messages
git stash apply stash@{id}				// go back to stash without deleting it
git stash pop						// go back to stash and delete it
git stash drop stash@{id}				// delete stash by id
git stash clear						// remoove all stashes
git stash show 0					// view what is stashed
git stash show -p 0					// view full tree stashed


git init 						//  initialize as git repository                            
git add .                                          	// all files in directory 
git add -A                                         	// all files in directory  
git commit -m "message" -m "description"
git commit -am "message"  			   	// add and commit works for modified files but not newly created 
git status



# Branchs
git branch                                          	// view branches
git branch <branch name>                            	// create branch
git checkout -b <branchName/feacher/convention>     	// create branch and switch to it
git checkout master                                 	// switch back to master
git branch -d <branch name>                         	// to delete a branch
git diff <branch to compare against>                	// view deference in branchs
git diff 					    	// compare before staged
git diff --cached					// compare to staged
git diff --ataged   				    	// view changes from last commit and staging area


# Rebase
git rebase master				    	// should be called from the branch that is being rebased
git checkout master                                 	// then move to master
git merge <branch>                                  	// then fast forward master


# Undoing
git checkout-- .							// revert changes before add
git reset                                           	// reset staging
git reset HEAD~1                                    	// delet commit and point header one commit before
git reset HEAD filename.txt    			    	// take back from staging area
git log                     			    	// view commits
git log -p					    	// view patch diffs			
git log --author="Yishay"   			    	// view individual committer 
git log --graph				            	// view merg points
git reset <hash of specific commit>		    	// can get hash commit from git log command
git reset --hard <hash>                             	// will delete commit and delete from file as well
git checkout firstnumbersofcommit -- filename.txt  	//revert back a commit


git checkout -- .				    	// revert saved changes that are not yet added
git checkout -- filname.txt    			    	//undo changes on work space frome repository
git restore --staged <file name>                    	// revert staged after adding (it is a new command)
git restore <file name>                             	// discard changes from working directory ie changes not added
git commit --amend              		    	// could modify last commit if previous commit is staged and allows new commit message
git commit --amend		                    	// will change commit message only, if nothing is in staging area



# Config
git config --global user.name "Yishay 			cnofig username 
git config --global user.email "yishaycooper@gmail.com"	config email
git config --global user.name				view username
git config --global user.email				view email	
git config --global --list				view username and email	



# Create a new repository on the command line
echo "# test" >> README.md
git init
git add README.md
git commit -m "first commit"
git commit -m "first -m is a message" -m "second -m is the description" 
git branch -M main
git remote add origin https://github.com/yishaycooper/test.git

# Or push an existing repository from the command line
git remote add origin https://github.com/yishaycooper/test.git
git branch -M main		


# To generate ssh key
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"


git rm filename.txt 					//deletes from work space and repository but must commit as well
git rn newname.txt  					//these two lines are used to rename directories but must commit as well
git mv oldname.txt newname.txt  			//this also renames
git mv file.txt IntoFolder      			//move file into folder



git config --global http.sslverify “false”         fix ERROR SSL certificate problem: unable to get local issuer certificate git lab

windows uses the byte cod CRLF carriage return line feed unix uses LF and mac uses CR.

Get-ChildItem . -Attributes Directory,Directory+Hidden -ErrorAction SilentlyContinue -Include ".git" -Recurse (find .git files using powershell)


