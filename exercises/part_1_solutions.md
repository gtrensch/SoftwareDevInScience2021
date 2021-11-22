# GitHub Agile Workflow

***In these exercises, we practice the basic GitHub workflow for contributing to a project.***

## Exercise I: Contribute to a Project

1. Fork the workshop repository to your own GitHub account.

      **Solution:** 
      
      ![](https://github.com/gtrGitHub/SoftwareDevInScience2021/blob/main/exercises/figures/fork.png)
      
2. Create a clone of the forked (your) workshop GitHub repository on your local machine.

      **Solution:**
      
          git clone https://github.com/<your_GitHub_user_name>/SoftwareDevInScience2021

3. Create a local branch to work on.

      **Solution:**
      
          git checkout -b <branch-xyz>
      
      or 
      
          git branch <branch-xyz> + git checkout <branch-xyz>
      
      to show all branches: 
      
          git branch -a 

4. Apply any changes you like and add them to your local branch.

      **Solution:**
      
      show repository status:
      
          git status

     add changes:
          
          git add *
          
5. Commit your changes and push them back to your GitHub repository.

      **Solution:**
      
      show repository status:
      
          git status
     
      commit changes:
          
          git commit -m"<commit_message>"

      push changes:
          
          git push origin <branch-xyz>

6. Issue a pull request against the workshop repository.

      **Solution:** 
      
      ![](https://github.com/gtrGitHub/SoftwareDevInScience2021/blob/main/exercises/figures/pull_request.png)
      

## Exercise II: Work in groups. Choose a developer to collaborate with!

1. Create a new local branch to work on.

      **Solution:** see exercise I 3.

2. Apply any changes you like and add them to your local branch.

      **Solution:** see exercise I 4.

3. Commit your changes and push them back to your GitHub repository.

      **Solution:** see exercise I 5.

4. Issue a pull request against your collaborator’s branch.

      **Solution:**
      
      ![](https://github.com/gtrGitHub/SoftwareDevInScience2021/blob/main/exercises/figures/pull_request.png)
      
      ----
            
      ![](https://github.com/gtrGitHub/SoftwareDevInScience2021/blob/main/exercises/figures/create_pull_request.png)

5. Let your collaborator review your pull request using GitHub's review workflow.

      **Solution:** 
      
      ![](https://github.com/gtrGitHub/SoftwareDevInScience2021/blob/main/exercises/figures/review_pull_request.png)

6. Let your collaborator merge your pull request.

      **Solution:** 

      ![](https://github.com/gtrGitHub/SoftwareDevInScience2021/blob/main/exercises/figures/merge_pull_request.png)

7. Let your collaborator issue a pull request against the project 'main'!

      **Solution:** see exercise I

8. (optional) Use the graphical repository browser gitk to display the changes in the repository.

      **Solution:** 
      
          gitk

      ![](https://github.com/gtrGitHub/SoftwareDevInScience2021/blob/main/exercises/figures/gitk.png)


## :+1: Hints ##

* Cloning the forked repository: `git clone https://github.com/<your_GitHub_user_name>/SoftwareDevInScience2021`

* GitHub/git cheat sheet: *https://education.github.com/git-cheat-sheet-education.pdf*

* Gitk documentation: *https://git-scm.com/docs/gitk*

* How to fix error message *"authentication fails"* returned from `git push origin main`
 
  In August 2021 GitHub removed the support for password authentication. Instead, a personal access token or an SSH key-based secure authentication must be used.
  - For creating a user token go to: *https://github.com/settings/tokens*
  - SSH key
    
    - To create an SSH key run:
      
      `ssh-keygen -t rsa -b 4096`
    
    - Add the public key to your GitHub account: 
     
      *https://github.com/settings/keys*
    
    - To test SSH access, issue the following command:
      
      `ssh -T git@github.com` 
      
    - Enable the SSH URL: 
     
      `git remote set-url origin git@github.com:<your_GitHub_user_name>/SoftwareDevInScience2021`


