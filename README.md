# Shared Library Configuration 
1.  Create a new repo at github
2.  Clone this repo and cd into it on your vs code terminal.
3.  Open a.groovy file and write in your library definitions, tools, stages and steps/actions
4.  Once this is done, go to Jenkins UI
5.  Manage jenkins--> Configure systems-->point jenkins to the global pipeline library 
6.  At Global pipeline libraries--add name of library you created
7.  Select option main (default verion)
8.  Retrieval method-->Select modern SCM--Git SCM
9.  Project repo (add url of repo), then credentials.
