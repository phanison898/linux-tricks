### linux-tricks

#### 1. Check list of users

```
awk -F':' '{ print $1}' /etc/passwd
```

---

### 2. Set permissions to file/folder

There is a file named script.ph (assume). There are two ways to represent permissions

- With symbols (alphanumeric characters), where

  - u = user
  - g = group
  - o = other
  - r = read
  - w = write
  - x = execute

  ```
  chmod u=rwx,g=rx,o=r script.sh
  ```

- With octal numbers (the digits 0 through 7)

  - 4 stands for "read",
  - 2 stands for "write",
  - 1 stands for "execute"
  - 0 stands for "no permission."
  - summation of these digits assigns the required permission

    ```bash
    chmod 754 script.sh
    ```
