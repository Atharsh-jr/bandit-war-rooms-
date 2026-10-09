──(atharsh㉿kali)-[~]
└─$ ssh bandit4@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _   
                        | |__   __ _ _ __   __| (_) |_ 
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_ 
                        |_.__/ \__,_|_| |_|\__,_|_|\__|
                                                       

                      This is an OverTheWire game server. 
            More information on http://www.overthewire.org/wargames

backend: gibson-1
bandit4@bandit.labs.overthewire.org's password: 

      ,----..            ,----,          .---.
     /   /   \         ,/   .`|         /. ./|
    /   .     :      ,`   .'  :     .--'.  ' ;
   .   /   ;.  \   ;    ;     /    /__./ \ : |
  .   ;   /  ` ; .'___,/    ,' .--'.  '   \' .
  ;   |  ; \ ; | |    :     | /___/ \ |    ' '
  |   :  | ; | ' ;    |.';  ; ;   \  \;      :
  .   |  ' ' ' : `----'  |  |  \   ;  `      |
  '   ;  \; /  |     '   :  ;   .   \    .\  ;
   \   \  ',  /      |   |  '    \   \   ' \ |
    ;   :    /       '   :  |     :   '  |--"
     \   \ .'        ;   |.'       \   \ ;
  www. `---` ver     '---' he       '---" ire.org


Welcome to OverTheWire!

If you find any problems, please report them to the #wargames channel on
discord or IRC.

--[ Playing the games ]--

  This machine might hold several wargames.
  If you are playing "somegame", then:

    * USERNAMES are somegame0, somegame1, ...
    * Most LEVELS are stored in /somegame/.
    * PASSWORDS for each level are stored in /etc/somegame_pass/.

  Write-access to homedirectories is disabled. It is advised to create a
  working directory with a hard-to-guess name in /tmp/.  You can use the
  command "mktemp -d" in order to generate a random and hard to guess
  directory in /tmp/.  Read-access to both /tmp/ is disabled and to /proc
  restricted so that users cannot snoop on eachother. Files and directories
  with easily guessable or short names will be periodically deleted! The /tmp
  directory is regularly wiped.
  Please play nice:

    * don't leave orphan processes running
    * don't leave exploit-files laying around
    * don't annoy other players
    * don't post passwords or spoilers
    * again, DONT POST SPOILERS!
      This includes writeups of your solution on your blog or website!

--[ Tips ]--

  This machine has a 64bit processor and many security-features enabled
  by default, although ASLR has been switched off.  The following
  compiler flags might be interesting:

    -m32                    compile for 32bit
    -fno-stack-protector    disable ProPolice
    -Wl,-z,norelro          disable relro

  In addition, the execstack tool can be used to flag the stack as
  executable on ELF binaries.

  Finally, network-access is limited for most levels by a local
  firewall.

--[ Tools ]--

 For your convenience we have installed a few useful tools which you can find
 in the following locations:

    * gef (https://github.com/hugsy/gef) in /opt/gef/
    * pwndbg (https://github.com/pwndbg/pwndbg) in /opt/pwndbg/
    * gdbinit (https://github.com/gdbinit/Gdbinit) in /opt/gdbinit/
    * pwntools (https://github.com/Gallopsled/pwntools)
    * radare2 (http://www.radare.org/)

--[ More information ]--

  For more information regarding individual wargames, visit
  http://www.overthewire.org/wargames/

  For support, questions or comments, contact us on discord or IRC.

  Enjoy your stay!

bandit4@bandit:~$ ls
inhere
bandit4@bandit:~$ cd inhere
bandit4@bandit:~/inhere$ ls
-file00  -file02  -file04  -file06  -file08
-file01  -file03  -file05  -file07  -file09
bandit4@bandit:~/inhere$ cat -file00
error: unexpected argument '-f' found

  tip: to pass '-f' as a value, use '-- -f'

Usage: cat [OPTION]... [FILE]...

For more information, try '--help'.
bandit4@bandit:~/inhere$ cat ./'-file00'
<Э�����4���b�y����ͻQ�Ov�N+Ďbandit4@bandit:~/inhere$ pwd
/home/bandit4/inhere
bandit4@bandit:~/inhere$ cat./"-file02"
-bash: cat./-file02: No such file or directory
bandit4@bandit:~/inhere$ cat./'-file02'
-bash: cat./-file02: No such file or directory
bandit4@bandit:~/inhere$ ls -la
total 48
-rw-r----- 1 bandit5 bandit4   33 Sep 26 21:53 -file00
-rw-r----- 1 bandit5 bandit4   33 Sep 26 21:53 -file01
-rw-r----- 1 bandit5 bandit4   33 Sep 26 21:53 -file02
-rw-r----- 1 bandit5 bandit4   33 Sep 26 21:53 -file03
-rw-r----- 1 bandit5 bandit4   33 Sep 26 21:53 -file04
-rw-r----- 1 bandit5 bandit4   33 Sep 26 21:53 -file05
-rw-r----- 1 bandit5 bandit4   33 Sep 26 21:53 -file06
-rw-r----- 1 bandit5 bandit4   33 Sep 26 21:53 -file07
-rw-r----- 1 bandit5 bandit4   33 Sep 26 21:53 -file08
-rw-r----- 1 bandit5 bandit4   33 Sep 26 21:53 -file09
drwxr-xr-x 2 root    root    4096 Sep 26 21:53 .
drwxr-xr-x 3 root    root    4096 Sep 26 21:53 ..
bandit4@bandit:~/inhere$ cat ./'-file01'
�����:�|�Y|fEHUv�#�����P��}bandit4@bandit:~/inhere$ 
bandit4@bandit:~/inhere$ cat ./'-file02'
O�9�pJ
      �(�g�%�j~6��ɹ���l���9�bandit4@bandit:~/inhere$ 
bandit4@bandit:~/inhere$ cat ./'-file03'
2R謡g���B�Ef�>c���ڂ~E9&��nbandit4@bandit:~/inhere$ 
bandit4@bandit:~/inhere$ cat ./'-file04'
�J���3�c��ـ�{~����hI�x.�d�k>bandit4@bandit:~/inhere$ 
bandit4@bandit:~/inhere$ cat ./'-file05'
�

dgy��Bp�7�
�������6�s�� Z70�bandit4@bandit:~/inhere$ 
bandit4@bandit:~/inhere$ cat ./'-file06'

���MW�� ��j▒N<�▒a�L�Lj=1���bandit4@bandit:~/inhere$ 
bandit4@bandit:~/inhere$ cat ./'-file07'
6C7h9GD8M6ai5nr7wo1RonrzFjj9yIrG
bandit4@bandit:~/inhere$ cat ./'-file08'
�T�|����6��Դ9�(��
                 ^�����*��▒bandit4@bandit:~/inhere$ 
the key for the next level is 6C7h9GD8M6ai5nr7wo1RonrzFjj9yIrG

