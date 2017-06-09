# Basic UNIX commands

Display list of files
```bash
ls
ls -la
```

Delete files/folders
```bash
rm filename.txt

# Permanently delete folder and all subfolders and files inside
# Warning: This cannot be undone, always double check before running this command
rm -rf folder_name
```

Create file:
```bash
touch README.md
```

View contents of file:
```bash
cat README.md
```

Use sudo ("super user do") when there's permission errors:
```bash
sudo <command>

# Shortcut to repeat previous command with sudo
sudo !!
```

Change ownership of pem file:
```bash
chmod 400 pemfile.pem
```

Read about Unix file permissions:
- https://www.tutorialspoint.com/unix/unix-file-permission.htm
- http://www.guru99.com/file-permissions.html

Vim (terminal text editor)

```bash
vim filename.txt
```

(Learn VIM keystrokes/shortcuts here: http://www.openvim.com/)



# Git
```bash
git status
git log

# Display the changes since last commit
git diff
git diff filename.txt
git diff foldername

# Pull changes
git pull

# Add, commit, push
git add .
git commit -m "Commit msg"
git push

# Remove all changes (return to previous commit)
git reset --hard

git stash
git stash apply
```



# SSH

SSH directory (store config and .pem files here):
```bash
~/.ssh
```

SSH Command:
```bash
ssh -i ~/.ssh/pemfile.pem ubuntu@<public ip address of ec2>
```



# Ubuntu

Install packages:
```bash
sudo apt-get update
sudo apt-get install <package-name>
# (e.g. sudo apt-get install apache2)
```

Install LAMP stack on Ubuntu: https://www.digitalocean.com/community/tutorials/how-to-install-linux-apache-mysql-php-lamp-stack-on-ubuntu-16-04



# PM2 (process manager for node)

Docs: http://pm2.keymetrics.io/docs/usage/quick-start/

Install pm2:
```bash
npm install -g pm2
```

Run a node app forever:
```bash
pm2 start index.js
```

List all running node apps:
```bash
pm2 list
```

Stop the app:
```bash
pm2 stop <app_name>
```

Remove/Delete the app:
```bash
pm2 delete <app_name>
```
