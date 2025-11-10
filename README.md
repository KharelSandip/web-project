
# Connect a GitHub Repo with AWS


**Author:** sandip kharel  
**Email:** kharelsundeep7@gmail.com

---

## Connect a GitHub Repo with AWS

![Image](http://learn.nextwork.org/inspired_pink_joyful_camel/uploads/aws-devops-github_dd9d254e)

---

## Introducing Today's Project!

In this project, I will demonstrate how to set up Git and Git. Hub to manage a web application. I'm doing this project to learn how to connect a local project using a GitHub repository, make commits, push code updates, and document my project using a README file.

### Key tools and concepts

Services I used were Git, GitHub, and an EC2 instance. Key concepts I learnt include setting up Git for version control, creating and connecting a GitHub repository, making commits, and pushing changes from a local repo to the cloud. I also learned how to use a GitHub token for secure authentication.

### Project reflection

This project took me approximately 2 to 3 hours to complete. The most challenging part was setting up the GitHub token for authentication. It was most rewarding to see my local code successfully pushed to GitHub and tracked through commits.

I did this project because I wanted to learn how Git and GitHub work together to manage code changes. It helped me understand version control, commits, and how to connect a local project to a remote repository.

This project is part two of a series of DevOps projects where I’m learning how to build and automate a CI/CD pipeline. I’ll be working on the next project soon to continue improving my skills in GitHub, AWS, and automation workflows.

---

## Git and GitHub

Git is a version control tool that helps track changes in code and manage different versions of a project. I installed Git using the command sudo dnf install git -y on my EC2 instance.

GitHub is an online platform that stores and manages different versions of a project using Git. I’m using GitHub in this project to keep my code backed up in the cloud, easily track changes, and share updates from my EC2 instance. It also helps me collaborate and view my project history from anywhere.

![Image](http://learn.nextwork.org/inspired_pink_joyful_camel/uploads/aws-devops-github_efaadbf7)

---

## My local repository

A Git repository is a folder that stores all the files, code, and version history of a project. It keeps track of every change made so we can easily update, revert, or collaborate with others. Hosting it on GitHub lets us access it from anywhere and share it with our team.

git init is a command that creates a new local Git repository in the current folder, allowing Git to start tracking changes in that project. I ran git init in my web app directory to turn it into a version-controlled project.

A branch in Git is a separate line of development that lets us work on new features or fixes without affecting the main project. After running git init, the terminal showed “Initialized empty Git repository on branch main,” which means the default branch was created.

![Image](http://learn.nextwork.org/inspired_pink_joyful_camel/uploads/aws-devops-github_7bf21bae)

---

## To push local changes to GitHub, I ran three commands

### git add

The first command I ran was git add ., which stages all the files in my project for the next commit. A staging area is like a preparation zone where Git collects the files I’ve changed before saving them permanently. This helps me review my changes and make sure everything is ready to be committed.

### git commit

The second command I ran was git commit -m "Updated index.jsp with new content". This command saves the staged changes as a new version in my project’s history. Using -m means I can add a short message describing what the commit is about, which helps track what changes were made.

### git push

The third command I ran was git push -u origin master, which uploads my committed changes from the local repository to GitHub. Using -u means I’m setting the upstream branch, so in the future I can just use git push without typing the full command again.

---

## Authentication

When I commit changes to GitHub, Git asks for my credentials because it needs to verify my identity before allowing me to push changes to the remote repository. This helps keep my GitHub account and code secure.

### Local Git identity

Git needs my name and email because it uses them to record who made each commit. This helps identify contributors in a project’s history and keeps track of who made specific changes.

Running git log showed me the history of all commits made in my project, including the commit IDs, author names, dates, and messages. It helped me see what changes were made and when.

![Image](http://learn.nextwork.org/inspired_pink_joyful_camel/uploads/aws-devops-github_9a27ee3b)

---

## GitHub tokens

GitHub authentication failed when I entered my password because GitHub no longer accepts passwords for HTTPS access. Instead, it now requires a personal access token, which is a more secure way to log in and interact with repositories.

A GitHub token is a unique string of characters that works like a secure password for accessing GitHub. I’m using one in this project because GitHub no longer allows password logins, and tokens provide a safer way to connect my local repository with my GitHub account.

I could set up a GitHub token by going to my GitHub account settings, selecting Developer settings → Personal access tokens, and generating a new token with the necessary permissions. Then I copied the token and used it instead of my password to connect Git with my GitHub repository.

![Image](http://learn.nextwork.org/inspired_pink_joyful_camel/uploads/aws-devops-github_fa11169d)

---

## Making changes again

I wanted to see Git working in action, so I updated the index.jsp file in my web-project by adding a new line of text. I couldn’t see the changes in my GitHub repo initially because saving in VS Code only updates the local repository. I had to commit and push the changes to make them appear on GitHub.

I finally saw the changes in my GitHub repo after staging the updated file with git add ., committing it using git commit -m "Add new line to index.jsp", and then pushing it to GitHub with git push.

![Image](http://learn.nextwork.org/inspired_pink_joyful_camel/uploads/aws-devops-github_6becb2bc)

---


