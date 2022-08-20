
# SHELL SCRIPTING
>- system executable(command - bin/shell script) are stored "/usr/bin"
>- user defined executable(command - bin ) are stored in "/usr/local/bin/"

---

## Use
>- When we need to write a big command in terminal which also have a variable which we need to add as an argument at the end

---

## ToDo -
>`>> sudo nano /usr/local/bin/script_name`
>- creating a bashscript in user defined bash scripting directory
>- you should be root user to edit it

---
#### The script(for for adding comminting and pushing together)
```
#!/bin/sh

git add . && \  
echo "" && \
echo "-- FILES ADDED --" && \ 
echo "" && \ 
git commit -m "$1" && \ 
echo "" && \
echo "-- PUSHING --" ; 
echo "" &&;
git push || echo "-- FAILED MONU --"
```

---

>`#!/bin/sh`
>- "#!" means SHEBANG - it tells which shell is being used
>- /sh is available in all linux device hence more useful

---

>`&&` 
>- joins differet command
>- RHS only execute when LHS is successfull

---

>`\`
>- used whenever you are jumping to next line instead of going on in same line even though it should be in one line

---

>`echo`
>- helpful to know a process is over

---

>`git commit -m "$1"`
>- here $1 means first argument
>- the value given after the script name as an argument will replace $1

---

>`||`
>- if LHS failed RHS will execute
>- helpful to know if the process failed or not

---

>`>> chmod +x scriptname`
>- after creating the file make it an executable
>- shoudl be in that directory else use path to give executable 
