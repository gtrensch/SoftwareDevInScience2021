# Manage your Projects in GitHub

***In these exercises, we will use GitHub functionality to organize our software development work into projects and a Kanban-like workflow. We will extend our small Python example source code with new functionality, using the test-driven software development approach.***

## Exercise III: Create a Project in GitHub.

1. Update your _'main branch'_ to be in sync with the GitHub workshop repository.

     **Solution:**
     
     add the workshop repository and assign alias _'upstream'_ :
      
          git remote add upstream https://github.com/gtrensch/SoftwareDevInScience2021
          
          git remote -v
          
     switch to main branch and pull latest changes from workshop repository:
     
          git checkout main
          
          git pull upstream main

2. Create a new project on GitHub, e.g., for adding new math-functions and unit tests. Chose the basic-Kanban template. Explore the possibilities of setting up a project!

     **Solution:**
     
     ![](https://github.com/gtrGitHub/SoftwareDevInScience2021/blob/main/exercises/figures/projects_01.png)
     
     ----

     ![](https://github.com/gtrGitHub/SoftwareDevInScience2021/blob/main/exercises/figures/projects_02.png)
     
     
3. Create a ToDo list with at least two activity cards for the implementation of a unit test and a new function. The unit test should describe test cases corresponding to the function you are planning to implement.

     ![](https://github.com/gtrGitHub/SoftwareDevInScience2021/blob/main/exercises/figures/projects_03.png)
     

4. (optional) Enable _'Issues'_ under _'repository settings'_ to integrate lightweight task tracking into your repository.

     ![](https://github.com/gtrGitHub/SoftwareDevInScience2021/blob/main/exercises/figures/enable_issues.png)
     

## Exercise IV: Test-Driven Development. Work with a partner and form a two-developers team!

1. Developer A: Create a new feature-branch for your project that you have set up in exercise III. 

     **Solution:**
     
          git checkout -b <feature-branch-xyz>
          
2. Developer A: Implement the unit test cases that you have defined in exercise III.

3. Developer A: Add and commit your changes.

     **Solution:**
     
          git add *
          
          git commit -m"<commit_message>"

4. Developer B: Pull the feature-branch from Developer A.

     **Solution:**
     
     add the developer A repository:
      
          git remote add <developer_A_alias> https://github.com/<developer_A_github_name>/SoftwareDevInScience2021
          
          git fetch <developer_A_alias>
          
     switch to feature-branch created by developer A:
     
          git checkout <feature-branch-xyz>

5. Developer B: Create a working-branch.

     **Solution:**
     
          git checkout -b <working-branch-xyz>

6. Developer B: Implement the functionality that your test cases define. Use the unit tests to verify the correctness of your implementation.

7. Developer B: Add and commit your changes.

     **Solution:**
     
          git add *
          
          git commit -m"<commit_message>"
          
          git push origin <working-branch-xyz>

8. Developer B: Issue a pull request against the feature-branch.

     **Solution:**
     
                                             pull request
          <developer_A/feature-branch-xyz> <-------------- <developer_B/working-branch-xyz>
          
     ----
               
     ![](https://github.com/gtrGitHub/SoftwareDevInScience2021/blob/main/exercises/figures/feature_pull_request.png)
          

9. Developer A: Code-review the pull request and merge it.

     **Solution:** see exercise II 5.

10. Developer A: Issue a pull request against the workshop repository. 

     **Solution:**
     
                                            pull request
          <SoftwareDevInScience2021/main> <-------------- <developer_A/feature-branch-xyz>

## :+1: Hints ##

* In order to be able to pull from a repository it needs to be added to git: `git remote add <aliasname> <repository URL>`

  _'origin'_ is the default alias set by git when a repository is cloned.
  
  Use the alias _'upstream'_ for the workshop repository!


