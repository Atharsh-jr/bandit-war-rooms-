***** level5-level6************
┌──(atharsh㉿kali)-[~]
└─$ ssh bandit5@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _   
                        | |__   __ _ _ __   __| (_) |_ 
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_ 
                        |_.__/ \__,_|_| |_|\__,_|_|\__|
                                                       

                      This is an OverTheWire game server. 
            More information on http://www.overthewire.org/wargames

backend: gibson-1
bandit5@bandit.labs.overthewire.org's password: 
Permission denied, please try again.
bandit5@bandit.labs.overthewire.org's password: 

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

bandit5@bandit:~$ ls
inhere
bandit5@bandit:~$ cd inhere
bandit5@bandit:~/inhere$ cd
bandit5@bandit:~$ find inhere - type f - size 1033c ! -executable
inhere/maybehere19/.file2
inhere/maybehere19/spaces file2
inhere/maybehere19/-file2
inhere/maybehere11/.file2
inhere/maybehere11/spaces file2
inhere/maybehere11/-file2
inhere/maybehere04/.file2
inhere/maybehere04/spaces file2
inhere/maybehere04/-file2
inhere/maybehere18/.file2
inhere/maybehere18/spaces file2
inhere/maybehere18/-file2
inhere/maybehere14/.file2
inhere/maybehere14/spaces file2
inhere/maybehere14/-file2
inhere/maybehere05/.file2
inhere/maybehere05/spaces file2
inhere/maybehere05/-file2
inhere/maybehere13/.file2
inhere/maybehere13/spaces file2
inhere/maybehere13/-file2
inhere/maybehere09/.file2
inhere/maybehere09/spaces file2
inhere/maybehere09/-file2
inhere/maybehere02/.file2
inhere/maybehere02/spaces file2
inhere/maybehere02/-file2
inhere/maybehere12/.file2
inhere/maybehere12/spaces file2
inhere/maybehere12/-file2
inhere/maybehere10/.file2
inhere/maybehere10/spaces file2
inhere/maybehere10/-file2
inhere/maybehere15/.file2
inhere/maybehere15/spaces file2
inhere/maybehere15/-file2
inhere/maybehere01/.file2
inhere/maybehere01/spaces file2
inhere/maybehere01/-file2
inhere/maybehere07/.file2
inhere/maybehere07/spaces file2
inhere/maybehere07/-file2
inhere/maybehere00/.file2
inhere/maybehere00/spaces file2
inhere/maybehere00/-file2
inhere/maybehere16/.file2
inhere/maybehere16/spaces file2
inhere/maybehere16/-file2
inhere/maybehere06/.file2
inhere/maybehere06/spaces file2
inhere/maybehere06/-file2
inhere/maybehere03/.file2
inhere/maybehere03/spaces file2
inhere/maybehere03/-file2
inhere/maybehere08/.file2
inhere/maybehere08/spaces file2
inhere/maybehere08/-file2
inhere/maybehere17/.file2
inhere/maybehere17/spaces file2
inhere/maybehere17/-file2
find: ‘-’: No such file or directory
find: ‘type’: No such file or directory
find: ‘f’: No such file or directory
find: ‘-’: No such file or directory
find: ‘size’: No such file or directory
find: ‘1033c’: No such file or directory
bandit5@bandit:~$ find inhere -type f -size 1033c ! -executable
inhere/maybehere07/.file2
bandit5@bandit:~$ find inhere -type f - size 1033c ! -executable
find: paths must precede expression: `-'
bandit5@bandit:~$ find inhere - type f -size 1033c ! -executable
inhere/maybehere07/.file2
find: ‘-’: No such file or directory
find: ‘type’: No such file or directory
find: ‘f’: No such file or directory
Note:there should be no space between the '-'and the condition you are setting.
if incase there's an space you find the above errors
bandit5@bandit:~$ find inhere -type f -size 1033c ! -executable
inhere/maybehere07/.file2
inhere/maybehere07/.file2
bandit5@bandit:~$ cd inhere/maybehere07
bandit5@bandit:~/inhere/maybehere07$ cat ./'.file2'
pXa26xhMWaC2SvDotA4r9EgZkulOeSBW
                                                                                                                                                                                                                                                                
