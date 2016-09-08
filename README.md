# mindcontrol_configs
Mindcontrol configuration for open neuroimaging datasets

## Purpose

This is a repository to hold all the different mindcontrol configurations


## How to add your configuration

You need 2 .json files:

* initializer.json (this is the file that will fill the database with entries initially.) This file should be saved in **this** repositry in 
```
mindcontrol_configs/<your_project_name>/intitializer.json
```


* generator.json
  * This file lives in a **mindcontrol branch** that you should **pull request** to akeshavan/mindcontrol 
  * make sure you point to your initializer.json file in akeshavan/mindcontrol/imports/python_generate/generator.json after the PR for mindcontrol_configs is accepted
    * go to http://rawgit.com/ to get the raw URL path of the intializer.json file
    
  * Next Steps:
    * Create a branch called <your_project_name>
    * uplaod the branch back to your fork, and send a pull request to akeshavan/mindcontrol
    * go back to your mindcontrol_configs folder, and add a submodule:
    
    ```
    git submodule add https://github.com/akeshavan/mindcontrol.git <your_project_name>/mindcontrol
    ```
  
  * `cd` to <your_project_name>/mindcontrol and switch the branch to your project branch `git checkout <your_branch_name>`
  * `cd` back the mindcontrol_configs and `git add <your_project_name>/mindcontrol` 
  * run `git push origin master` and send a pull request to akeshavan/mindcontrol_configs
