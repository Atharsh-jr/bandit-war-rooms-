**bandit level 0**
step 1:: we need to use an linux terminal and type ssh bandit0@bandit.labs.overthewire.org
step 2:: youll be requested to enter an password : bandit0
step3:: the connection with the platform is confirmed and it will take you to the bandit over the wire.
step 4 :youll need to use the commands like ls to find the files present in the particular directory. 
step 5: the readme file will be found in that specific directory
step6: you can use these commands like ls,cd,cat,file,du,find
step7:cd is for changing the directory
step8: cat is to read the file and du is to find the size of the file
step9: using this commands we will find an password that is 6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR
****************************************************
**bandit level 1**
step1::use the linux terminal and type ssh bandit1@bandit.labs.overthewire.org
step2: password would be the one you cracked in bandit0 lab that is 6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR
step3::use an ls command to know the files in the directory
step4::so in this bandit1 lab we found an file created with '-' thats an dashed file name this is an special case scenario.
step5::let us understand what is the dashed file 
step6::If its an dashed file the terminal consider '-' it has an flag .generated output with that with an cat command would be null.
step7::In this scenario we use the file path and with respect to filename example: cat /home/bandit1/- or we can use an '.' to represent the current working directory and example : cat ./-
step8:: using the above mentioned steps we will acheive an password to the level 2 lab that is PK8fYLZg2hnHSz83plBL1iEPKdD3QToB
