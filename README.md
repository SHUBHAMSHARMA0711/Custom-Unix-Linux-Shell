# Shell Description
This comprehensive overview provides details on external and internal commands implemented in the shell, along with error-handling mechanisms. Additionally, test cases and assumptions are outlined to guide users in utilizing the shell effectively.

## External Commands

### 1. ls
    - ls -a
    - ls -m

### 2. cat
    - cat -n`
    - cat -E

### 3. date
    - date -u
    - date -I

### 4. rm
    - rm -v
    - rm -i

### 5. mkdir
    - mkdir -p
    - mkdir -v

## Internal Commands

### 1. cd
    - cd ~
    - cd ..

### 2. echo
    - echo *
    - echo -- help

### 3. pwd
    - pwd -L
    - pwd -P

## Error Handling

1. If the user enters any command other than the specified ones, they will receive a **command not found** error.
2. In the **cat** and **rm** commands, if the user enters a non-existing file name, they will get a **No such file or directory** error.
3. In the **cd** command, if the user enters a non-existing directory name, they will get a **No such file or directory** error.
4. For any command, if the user enters an option not handled by the Shell, they will receive an **invalid option** error.
5. In the **cat** command, if the user enters **cat** without any argument, they will get a **missing operands** error.
6. In the **mkdir** command, if the user tries to create a duplicate directory, they will receive a **cannot create directory** error.
7. Error handling for creating a child process using the Fork System Call, with a message **Fork Error (Child Process Not Created).**


## Implementation Details

The shell can be implemented using both forks and threads. If someone wishes to use threads, they can add `&t` at the end of the command. For example:
- `ls -a &t`
- `cat -n cat.c &t`
- `date -I &t`

  
## Test Cases

### 1. ls
   - `ls -a` & `ls -a &t`
   - `ls -m` & `ls -m &t`

### 2. cat
   - `cat -n cat.c` & `cat -n cat.c &t`
   - `cat -E cat.c` & `cat -E cat.c &t`

### 3. date
   - `date -u` & `date -u &t`
   - `date -I` & `date -I &t`

### 4. rm hello.c
   - `rm -v hello.c` & `rm -v hello.c &t`
   - `rm -i hello.c` & `rm -i hello.c &t`

### 5. mkdir newDir
   - `mkdir -p newDir/newDir2` & `mkdir -p newDir/newDir2 &t`
   - `mkdir -v newDir` & `mkdir -v newDir &t`

## Assumptions

1. No unnecessary arguments will be passed in between or after the command.
2. **cat** and **rm** commands will not be passed a directory as an argument.
3. **mkdir** and **rm** commands will not be entered without any arguments.
