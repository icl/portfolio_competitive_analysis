To prepare yourself to upload your first assignment you will need to do the following:

Please email any questions to: **ethan@ucsd.edu**

**Completing these steps does not complete your first assignment. Please see the course web site for the assignment specification.**

###Prepare Yourself
1. Sign up for a [free Github account](https://github.com/signup/free). Git is a version control system that you will use to submit your assignments.  

2. Set up Git on your computer http://help.github.com/set-up-git-redirect
	
	There are a couple steps while you are setting up ssh that require careful reading. In general you should copy the commands exactly as written, but occasionally you will need to substitute you name or email. In general for mac users we recommend using `pbcopy` in the step for copying your private key.

3. Go to Github at https://github.com/icl/portfolio_competitive_analysis You will find there a bunch of directories you can add to, such as images, stylesheets.

4. Before you can actually take ownership of this directory exclusively you need to have Github know where your files come from.  This is called forking because Github creates a new path with your identity, separating your files from others.  If you are part of a team it will keep track of your team's files and who made what changes.  To cause Github to keep a copy of your files that you can periodically write to (thereby updating the latest files but also keeping a record of previous files) you have to hit the FORK button on the Github page for this assignment (ie https://github.com/icl/portfolio_competitive_analysis).  The FORK button is at the top along with WATCH ...  Click it and you will now create a directory with your name and a subdirectory for this assignment. This will redirect you to your own copy of the assignment, youou can see that in the url it now shows your name instead of 'icl'.  

5.  Obviously you will want to work on your assignment on your computer and periodically push your own files up to your Github account and then once they are there you will periodically push again to update the files on Github.  

6.  There is one more step to understand.  Your own computer needs to have the files we are already put up in the portfolio_competitive_analysis directory.  To do that we need to "clone" Github's repository.  This will duplicate its current directory structure on your machine.  Once you have cloned this repository if anyone else were to change files there (because you were collaborating with them) then you will need to 'Pull' from Github and it will add whatever is new to your own repository [you don't need to worry about pulling until you work in teams].  


###Get the Files on Your Computer
7. Open up a **new** Terminal, or the Git-Bash shell if you are using windows.

8. Enter the following, replacing "[your username here]" with your Github account name:

    Please note we will use $ as a marker to show what you should enter in the command line. You should not enter the $. Any lines without the $ should be read as expected output

	**Remember to replace "yournamehere" with your Github username**

    ```bash
    $ git clone git@github.com:yourusernamehere/portfolio_competitive_analysis.git
    ```
    This will create a folder on your computer called "portfolio_competitive_analysis" with the project files in it.

9. Go to that directory in terminal

    ```bash
    $ cd portfolio_competitive_analysis
    ```

10. In terminal, type `git status`
    if everything up to this point has worked you should see:

    ```bash
    $ git status
    # On branch master
    nothing to commit (working directory clean)
    ```

###Work With Files

11. Take a look at the contents of the folder which should be in your home directory. The files should be the same as you saw on Github.

12. Open **index.html** in an editor, we recommend [Komodo Edit](http://www.activestate.com/komodo-edit/downloads)

	```html
	<!DOCTYPE html>
	<html lang="en">
	  <head>
	    <meta charset="utf-8">
	    <title>A Generic Page</title>
	    <meta name="description" content="something good should go here">
	    <meta name="author" content="your name should go here">

	    <!-- Le HTML5 shim, for IE6-8 support of HTML elements -->
	    <!--[if lt IE 9]>
	      <script src="http://html5shim.googlecode.com/svn/trunk/html5.js"></script>
	    <![endif]-->

	    <!-- Base Stylsheets -->
	    <link rel="stylesheet" href="stylesheets/lib/bootstrap.css" >
	    <link rel="stylesheet" href="stylesheets/lib/fancybox.css" >

		<!-- Your Stylesheets -->
		<link rel="stylesheet" href="stylesheets/style.css" >

		<!-- Base Javascripts -->
	    <script src="javascripts/lib/base.min.js"></script>

		<!-- Your Javascripts -->
	    <script src="javascripts/main.js"></script>
	  </head>

	  <body>
	    <div class="container">
			PUT STUFF HERE
	    </div>
	  </body>
	</html>
	```

13. Replace the line "PUT STUFF HERE" with something of your own and save the file.

14. Back in Terminal, type `git status` again. You should see that Git notices that the file has changed.

	```bash
	$ git status
	# On branch master
	# Changes not staged for commit:
	#   (use "git add <file>..." to update what will be committed)
	#   (use "git checkout -- <file>..." to discard changes in working directory)
	#
	#	modified:   index.html
	#
	no changes added to commit (use "git add" and/or "git commit -a")
	```
15. One of Git's most useful features is that you can "commit" versions of your files whenever you want. Each commit saves the a copy of whatever changes you made since the last one. If you accidentally delete a file or lose some work you can check the file from Git's history. Just like it's a good idea to "Save early; save often" its a good idea to commit early and commit often.

16. Take Git's advice and type `git commit -am 'I edited the index'`

	*Note: the -m 'some message in quotes' is meant to add a message to the history so you know what you did later. If you omit it, git will pop up an editor called vi to prompt you for a message, press **esc** then **q** to quit if you need to.*

	```bash
	$ git commit -am 'I edited the index!'
	[master bdd6efa] I edited the index!
	 1 files changed, 1 insertions(+), 1 deletions(-)
	```

###Add Files

17. Make a new file in the directory; you can put whatever you want in it (baring in mind the whole world might see it :).

18. Git status should now show your new file:

	```bash
	$ git status
	# On branch master
	# Your branch is ahead of 'origin/master' by 1 commit.
	#
	# Untracked files:
	#   (use "git add <file>..." to include in what will be committed)
	#
	#	somenewfilename
	nothing added to commit but untracked files present (use "git add" to track)
```
19. Git was originally described as "A Stupid Content Tracker", which in a way it is. It won't register changes to files unless you tell it to track them.

	```bash
	$ git add somenewfilename
	```

20. Now git status should show you that git is ready to commit your new file

	```
	$ git status
	# On branch master
	# Your branch is ahead of 'origin/master' by 1 commit.
	#
	# Changes to be committed:
	#   (use "git reset HEAD <file>..." to unstage)
	#
	#	new file:   somenewfilename
	#
	```

19. Do that now with git commit -m 'Add somenewfile'

	```
	$ git commit -m 'Add somenewfile'
	[master 4ff38f9] Add somenewfile
	 0 files changed, 0 insertions(+), 0 deletions(-)
	 create mode 100644 somenewfilename
	```

20. As you work through these steps you make have noticed this line in the git status messages

	`# Your branch is ahead of 'origin/master' by 2 commits.`

	This means that the commits you've made have pushed the history on your computer ahead of whats on your Github repository online.

21. Confirm this by Going to your project's web page on Github

	Your new file won't show up, and index.html should be just as you downloaded it.

22. You can pull down changes from Github by using `git pull`. Right now there shouldn't be any, but its a good habit to get in to if you are working with other people, or on multiple computers.

	```bash
	$ git pull
	Already up-to-date.
	```

23.	You use the command `git push` to bring Github up to date with the changes you've made.

	```bash
	$ git push
	Counting objects: 8, done.
	Delta compression using up to 2 threads.
	Compressing objects: 100% (5/5), done.
	Writing objects: 100% (6/6), 557 bytes, done.
	Total 6 (delta 3), reused 0 (delta 0)
	To git@github.com:icl/portfolio_competitive_analysis.git
	   78c917c..4ff38f9  master -> master
	```

24. If you go to the Github web page for your project you should now see your changes. You can push changes as many times as you want. When grading assignments we will pull the last commit you pushed before the due date for an assignment.

**Completing these steps does not complete your first assignment. Please see the course web site for the assignment specification.**


###More Cool Stuff:

* [Learn More about Git](http://rogerdudler.github.com/git-guide/)
* [Learn about HTML CSS and Javascript](http://code.google.com/edu/submissions/html-css-javascript/)
* [Get Up to Speed with the Twitter Bootstrap](http://twitter.github.com/bootstrap/)
* [Dive in](http://gitimmersion.com/)
* [Check out Github's Mac App](http://mac.github.com/)
* [or TortoiseGit for Windows](http://code.google.com/p/tortoisegit/)
