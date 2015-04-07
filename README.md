First step to installing nmap is opening your terminal (just go to spotlight and type terminal).
Once the terminal is open, type brew install nmap.

![screenshot 1](https://cloud.githubusercontent.com/assets/11819609/7016064/de0f0c56-dcab-11e4-9fc3-8b988649952c.png)

You will see that it installs the nmap package. But the terminal throws a problem saying 
"the brew link step did not complete"
"the formula built, but is not symlinked into /usr/local"
"could not symlink share/man/de/man1/nmap.1"
"/usr/local/share/man/de/man1 is not writable"

![screenshot 2](https://cloud.githubusercontent.com/assets/11819609/7016078/10989930-dcac-11e4-95de-6116d03efaa4.png)


Now, even if you try installing nmap again ( brew install nmap). It won't work. 
If you try brew link nmap, it still doesn't link nmap.

![screenshot 3](https://cloud.githubusercontent.com/assets/11819609/7016095/3e754a10-dcac-11e4-8f6b-3bf24405b966.png)


So, the main problem here is that, it says "/usr/local/share/man/de/man1 is not writable".
Meaning that you don't have the permission as a user to write.

So all you need to do is change permissions for the user. You just need to give the user the permission to write. It can be done as follows.

**BUT WAIT, BEFORE YOU DO THE NEXT STEP**

 my username is Ashwin. For it to work on your terminal you have to write 
"sudo chown your-username /usr/local/share/man/de" (ofcourse without the double quotes :P)

instead of Ashwin, just write your username. If you don't know your username, just type "whoami" in the terminal and it will give you the current user.

![screenshot 4](https://cloud.githubusercontent.com/assets/11819609/7016128/b9d903c2-dcac-11e4-9c45-6aab1eae299a.png)


You also need to do the next step.
**AND REMEMBER**, once again you have to change "Ashwin" to your username.

![screenshot 5](https://cloud.githubusercontent.com/assets/11819609/7016134/c1ddb482-dcac-11e4-9133-6281779b6269.png)


Now, we have changed the permission. ( HOORAY ! ).
All you have to do now is "brew link nmap".
And it will show you this screen.

![screenshot 6](https://cloud.githubusercontent.com/assets/11819609/7016146/fb7db0ac-dcac-11e4-9b2e-e0a9316beb0b.png)



AND... **BAZINGA** ... You my friend are done.

GO ENJOY !
