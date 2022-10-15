# Fetch, Pull, Push: What are the differences?
The content below provides insight to help you distinguish the fetch, pull, and push commands. It is important to note that *local repository* refers to the files on your local machine (only accessible to you), and *remote repository* refers to the files in the GitHub environment (a collaborative space accessible to approved team members). Branches are versions of the code or documentation, which usually contain many files. The primary branch is **master**, which is more appropriately referred to as **main**. With rare exception, when you create a branch to add new or updated code or documentation, you first retrieve this information from the main branch to ensure you have the most current files.

An example best distinguishes fetch, pull, and push. 

**EXAMPLE #1** assumes you have cloned the Pets repository such that the files on your local machine align with the same files in GitHub; in addition, this example assumes you are updating files using markdown (.md) in VS Code. This example lists the steps you must perform to update Puppy.md, using fetch, pull, and push. These examples enable you to glean a reasonable understanding of each command.

**EXAMPLE #1**

*From VS Code . . .*
1.	From the Pets repository in VS Code (local repository), perform a **Fetch** to retrieve and review branches or changes. This command allows you to review all updates to the remote branches in this repository. While you can review changes, this action does not impact the files in your local repository.
2.	From the Pets repository in VS Code (local repository), access the main branch (remote repository).
3.	To ensure the main branch has the most current documentation files, click **Pull**. This command retrieves files from the remote repository, moving them into your local repository and ensuring you have all updates available at this time.
4.	From this main branch in remote repository, create a new branch – naming this branch per your internal naming convention. At this point, the new branch has the most current documentation files specific to the Pets repository.
5.	Identify the Puppy.md file and make changes before saving your content. 
6.	Stage your changes, add a Commit statement, and click Commit. These actions finalize the saved changes to Puppy.md in your local repository. 
7.	To move these changes to the remote repository (GitHub), click **Push**. This command moves the file updated in your local repository to the remote GitHub environment.
8.	From GitHub, create a pull request (PR) specific to your branch. The PR allows team members to review changes to Puppy.md and, if all updates are approved, you can merge the PR into the main branch. The main branch now includes all Puppy updates.
9.	Delete your branch.
/br

**EXAMPLE #2** assumes you have cloned the Pets repository such that the files on your local machine align with the same files in GitHub; in addition, this example assumes you are updating files using markdown (.md) in VS Code. This example lists the steps from the Git Bash command line that you must perform to update Puppy.md, using fetch, pull, and push.

**EXAMPLE #2**

*From Git Bash . . .*
1.	cd repo-name
2.	git **fetch** (This command allows you to review all updates to the remote branches in this repository. While you can review changes, this action does not impact the files in your local repository.) 
3.	git checkout main
4.	git **pull** (This command retrieves files from the remote repository, moving them into your local repository and ensuring you have all updates available at this time.)
5.	git checkout -b branchname
6.	git merge master
7.	code . (Provides access to VS Code where you can make and save changes.)
8.	git status (Confirm modifications.)
9.	git add . (Stage changes.)
10.	git commit -m “Ticket 123: Puppy updates”
11.	git **push** (This command moves the file updated in your local repository to the remote GitHub environment.)
12.	Access GitHub and create PR specific to this branch.
13.	Request PR review and approval.
14.	Merge PR into the main branch.
15.	Delete your branch.
