# internsctl_project1
Scenario There is a customer who came to you with a problem to have a custom linux
command for his operations. Your task is to understand the problem and create a linux
command via bash script as per the instructions.
Command name - internsctl
Command version - v0.1.0

**Section A and B** 
1. I want a manual page of command so that I can see the full documentation of the command.
For example if you execute the command
man ls
as output we get the doc and usage guidelines. Similarly if I execute man internsctl I want
to see the manual of my command.
2. Each linux command has an option --help which helps the end user to understand the use
cases via examples. Similarly if I execute internsctl --help it should provide me the
necessary help

3. I want to see version of my command by executing
internsctl --version

<img width="374" alt="image" src="https://github.com/Akash19sept/internsctl_project1/assets/127194626/05dfaa0e-e488-4f13-8e16-ffbdbdef7877">

4. for cpu information:
   
./newproject.sh cpu getinfo

<img width="375" alt="image" src="https://github.com/Akash19sept/internsctl_project1/assets/127194626/b247e1ba-b00b-41fe-a56a-1da80a60c4dc">

5. memory information:
./newproject.sh memory getinfo

<img width="372" alt="image" src="https://github.com/Akash19sept/internsctl_project1/assets/127194626/ebccc37c-6992-4f6a-9253-6007dcc6641d">

   
6. Create new user:
./newproject.sh user create akash

<img width="366" alt="image" src="https://github.com/Akash19sept/internsctl_project1/assets/127194626/40c20daf-7c88-44c0-918c-4b798ecdc19e">

7.Show user list:
./newproject user list

<img width="369" alt="image" src="https://github.com/Akash19sept/internsctl_project1/assets/127194626/2540439c-1cda-49c6-8dd1-388b4c0675a5">

**Part 3:**

#!/bin/bash

if [[ "$#" -eq 1 ]]; then Is -1 $1

elif [[ "$#" -eq 2 ]]; then

if [ "$1" = "-s"] || [ "$1" == "--size" ] then wc -c $2

elif [ "$1"-"-p"] || [ "$1" = "--permissions" ] then ls -ld $2 awk '{ print $1; }'

elif [ "$1" = "o"] || [ "$1" == "--owner" ] then

stat -c '%U' $2

elif [ "$1" = "m"] || [ "$1" == "--last-modified" ]

then

stat -c '%y' $2

fi

fi











