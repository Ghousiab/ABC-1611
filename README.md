1.create a Azure cintainer registry 
   created conatiner registry named abcabc
   login using command :docker login abcabc.azurecr.io
   push the image to check : docker push abcabc.azurecr.io/9e4e0201ea99
   ---------------------------------------------------------------------------
2. create a shell script  
    2.a takes 1 input (0/1)  
    2.b hava a conditional check  
        if 1 -> create a folder and a file inside that at a specific location  
        if 0 -> delete the folder/s present at that location
      
    created directory and moved to the directory
    mkdir abc/b1
    created file using : vi ff1.sh
    executed using : ssh ff1.sh 
    --------------------------------------------------------------------
 3.  Write a multi stage docker file  
    3.a base stage  
        -> use ubuntu image and create abc user  
        -> install cron  
        -> create specific folder chage owner permission to abc
    3.b intermediate stage  
        -> copy the shell script inside the container  
        -> chane the permission to execution  
        -> setup a cronjob for the script  
    3.c clean up stage  
        -> run the script as cron with 0 as input as abc user  
    3.d create stage  
        -> run the script as cron with 1 as input as abc user

       created folder using mkdir dd
     in dd folder created Dockerfile
     myscript.sh
     build it using docker build --target -t create-my-image .
     to list the images : docker images
------------------------------------------------------
  4. publish this image to container registry
      push the image to check : docker push abcabc.azurecr.io/9e4e0201ea99
 --------------------------------------------
     
  5. create a github repository with name ABC-1611 and push the file
     created directory using mkdir abcgit
     moved to the directory using cd abcgit
     initialized git git init
     added remote rpository using git remote add origin https://https://github.com/Ghousiab/ABC-1611.git
     created file using vi ff1.txt
     added git add .
     commited uding git commit
     git push -u origin main 
