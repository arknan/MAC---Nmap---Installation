First step to installing nmap is opening your terminal (just go to spotlight and type terminal).
Once the terminal is open, type brew install nmap.
![screenshot 1](https://cloud.githubusercontent.com/assets/11819609/7013265/c95cfad2-dc85-11e4-8779-45ecb1f4e855.png)

You will see that it installs the nmap package. But the terminal throws a problem saying 
"the brew link step did not complete"
"the formula built, but is not symlinked into /usr/local"
"could not symlink share/man/de/man1/nmap.1"
"/usr/local/share/man/de/man1 is not writable"

![screenshot 2](https://cloud.githubusercontent.com/assets/11819609/7013272/d5fb6972-dc85-11e4-8926-e590d79f1be4.png)

Now, even if you try installing nmap again ( brew install nmap). It won't work. 
If you try brew link nmap, it still doesn't link nmap.

![screenshot 3](https://cloud.githubusercontent.com/assets/11819609/7013478/860cefec-dc87-11e4-94ad-13f8882678c5.png)

So, the main problem here is that, it says "/usr/local/share/man/de/man1 is not writable".
Meaning that you don't have the permission as a user to write.

So all you need to do is change permissions for the user. You just need to give the user the permission to write. It can be done as follows.

**BUT WAIT, BEFORE YOU DO THE NEXT STEP**

 my username is Ashwin. For it to work on your terminal you have to write 
"sudo chown your-username /usr/local/share/man/de" (ofcourse without the double quotes :P)

instead of Ashwin, just write your username. If you don't know your username, just type "whoami" in the terminal and it will give you the current user.

![screentshot 4](https://cloud.githubusercontent.com/assets/11819609/7013510/d7b5460a-dc87-11e4-9f7c-f5e3a75233b0.png)

You also need to do the next step.
**AND REMEMBER**, once again you have to change "Ashwin" to your username.

![screenshot 5](https://cloud.githubusercontent.com/assets/11819609/7013569/769e997e-dc88-11e4-912f-79e7d561c942.png)

Now, we have changed the permission. ( HOORAY ! ).
All you have to do now is "brew link nmap".

![screenshot 6](https://cloud.githubusercontent.com/assets/11819609/7013630/30a378b2-dc89-11e4-8227-4466ede52e31.png)

And it will show you this screen.

![screenshot 7](https://cloud.githubusercontent.com/assets/11819609/7013653/4851e656-dc89-11e4-975a-463b1f98da3d.png)


AND... **BAZINGA** ... You my friend are done.

GO ENJOY !
