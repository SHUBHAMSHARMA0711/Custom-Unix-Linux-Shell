# **Description of Shell** 

**Commands that Shell can Handle:-** 

**External Commands:-** 

1. **ls** 
   - ls -a 
   - ls -m 
2. **cat** 
    - cat -n 
    - cat -E 
3. **date** 
    - date -u 
    - date -I 
4. **rm** 
    - rm -v 
    - rm -i 
5. **mkdir** 
    - mkdir -p 
    - mkdir -v 

**Internal:-** 

1. **cd** 
    - cd ~ 
    - cd **..** 
2. **echo** 
    - echo \* 
    - echo - - help 
3. **pwd** 
    - pwd -L 
    - pwd -P 

**Errors I handled:-** 

1. *If  the  User  Enters  any  Command,  Other  than  the above-mentioned then he will get a “command not found” Error.* 
1. *In  the  “cat  and  rm”  command, if the user enters any file name that does not exist in that particular directory, he will get a “No such file or directory” Error.* 
1. *In the “cd” command, if the user enters any directory name that  will  not  exists  then,  he  will  get  “No  such  file  or directory” Error.*
1. *For any command, if user enters any other option that will not be handled by Shell then he will get an “invalid option” Error.* 
1. *In “cat” command if user enters cat without any argument then he will get “missing operands” Error.*
1. *In “mkdir” command if user try to make duplicate directory then he will get “cannot create directory” Error.* 
1. *Also,  I  have  handled  Errors  in  creating  a  Child  process using  Fork  System  Call  by  printing  “Fork  Error  (Child Process Not Created)”.* 

**Test Cases:-** 

1. **ls** & **ls &t** 
    - ls -a **&** ls -a &t 
    - ls -m  **&** ls -m &t 

2. **cat** 
    - cat -n cat.c **&** cat -n cat.c &t 
    - cat -E cat.c **&** cat -E cat.c &t 
3. **date** & **date &t** 
    - date -u **&** date -u &t 
    - date -I **&** date -I &t 
4. **rm hello.c** & **rm hello.c &t** 
    - rm -v hello.c **&** rm -v hello.c &t 
    - rm -i hello.c **&** rm -i hello.c &t
5. **mkdir newDir** & **mkdir newDir &t** 
    - mkdir -p newDir/newDir2 **&** mkdir -p newDir/newDir2 &t 
    - mkdir -v newDir **&** mkdir -v newDir &t 

1. **cd** 
    - cd ~ 
    - cd **..** 
2. **echo** 
    - echo \* 
    - echo - - help 
3. **pwd** 
    - pwd -L 
    - pwd -P 

**Assumptions:-** 

1. *I  assume  that  for  any  command  user  will  not  pass  any unnecessary arguments in between or after the command.*
1. *I assume the user will not pass Directory as an argument in “cat and rm” command.* 
1. *I assume the user will not enter “mkdir and rm” without any arguments.* 
