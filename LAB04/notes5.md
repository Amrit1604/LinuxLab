# LAB-EXPERIMENT 5

**Permission Management:

1. Create the /home/consultants directory.

2. Add write permission to the consultants group. Use the symbolic method for setting the appropriate permissions.

3. Forbid others from accessing files in the /home/consultants directory. Use the octal method for setting the appropriate permissions.**

```
mkdir home
mkdir home/consultants

chmod g+w home/consultants
ls -l

chmod 770 home/consultants
ls -l
```

![home](https://github.com/user-attachments/assets/dd2c6585-62f2-469f-b379-ca4401ce7de8)

Change the default umask for the operator1 user. The new umask prohibits all access for users that are not in their group. Confirm that the umask is changed.

![umask](https://github.com/user-attachments/assets/afc5c23d-c1c9-46fc-9ab2-d3c3e00f52d1)

