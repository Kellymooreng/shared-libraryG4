# Shared Library Configuration 
1.  -Create 3 git repositories for the 3 different applications.
2.  Create a git repository for the Jenkins shared library.
3.  In your vscode, you make a directory and cd into that directory.
4.  Then you do your git clone repository url for the 3 different applications and the Jenkins shared library
## Starting with the Jenkins shared library, 
5.  Do your git clone repository url of the Jenkins shared library, you create a branch and switch into it using git checkout -b branchname.
6.  Create a vars directory in the Jenkins shared library directory
7.  In the vars directory you create a Groovy file and you make sure that it should be camel case, example etechApp.
8.  Create a call function inside the Groovy file, and then define the parameters of your pipeline.
## Working in the 3 different applications.
9.  In the different applications, you need to create a Jenkinsfile. 
10. In that Jenkinsfile, you need to use the Shared library in the Jenkins pipeline by adding “@Library(‘your-shared-library-name’)” _ 
    Note: The _ at the end of the library is very important, if not present it is not going to be able to detect that Jenkins shared library.
11. After writing the library name, then you write the name of the groovy file followed by the repo url of the app.
    Example; etechApp 'https://github.com/Big-Zaza/demo-app1.git'
## Now you move to the Jenkins UI.
12. Now you configure Global pipeline libraries: Manage jenkins--> Configure systems-->point jenkins to the global pipeline library 
13. You add the Jenkins shared library name
14. You add the repo url of the Jenkins shared library
15. You configure your credentials as a service account.
    Once this is done, go to Jenkins UI
    -Apply and save.
    -Then you create a job and run the pipeline.
