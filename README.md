# Variables and Databases
---
### Variables and environment variables
- Defining a variable in linux is done like so:
``name="Agbo Lamina"``
- Calling a variable is done like so:
``echo $name``
- Agbo Lamina should be returned 
- Environment variables are different becasue they exist within the ``env``, they are created by:
``export name="Agbo Lamina"``
- Then enter ``env`` to see the variable among the list of environment variables
- Next, to make the environment variable persistent, you would input:
 ``export name="Agbo Lamina"`` into .bashrc
- Then enter ``env`` to see the list of environment variables available in the system

---
### Task: Create env_var.sh file
- `` touch env_var.sh ``
- Next, `` chmod +x env_var `` as when the file is initially created it has no rights, so this gives it rights
- `` nano env_var.sh ``
- Within the nano text editor, I entered my name, then echoed it.
- Next `` dir=$(ls)`` followed by `` echo $dir
- Next ``./env_var.sh`` command outputs the name variable and the other files in the directory 
---
We made the DB_HOST into an environment variable becasue when the app runs, it looks for the IP address
`` export DB_HOST="mongodb://192.168.10.111:27017/posts" `` - this becomes stored in the environment like the other ``env`` variables
- We had a task to make the DB_HOST persistent
- this was completed by navigating to .bashrc (it us ususally hidden so `` ls -a`` reveals it)
- if we make changes to any of the .profile, .bash_login, .bash_profile - the changes are usually persistent  
---

Notes on reverse proxy
- etc/nginx cd sites-available
- nano default
- We then enter the default file. This file had the default IP address of the VM and the address it is listening on
