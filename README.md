### linux-tricks

#### 1. Check list of users
```
awk -F':' '{ print $1}' /etc/passwd
```

### 2. Set permissions to file/folder
There are two ways to represent permissions
- With symbols (alphanumeric characters)
```
chmod u=rwx,g=rx,o=r myfile
```
- With octal numbers (the digits 0 through 7)

