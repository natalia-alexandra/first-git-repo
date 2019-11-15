# SSH key with GitHub   :key:

## Add SSH key to GitHub account, :running: step by step  

1. Checking for existing SSH keys
```
ls -al ~/.ssh
```

2. Generating a new SSH key

```
ssh-keygen
```

3. Double check if the key was generated

```
ls -al ~/.ssh
```

4. Go to the .ssh folder and copy the public key

```
cd ~/.ssh 	(or cd .ssh/)
```

```
cat id_rsa.pub
```

5. Go to GitHub account and put the copied public key there

Settings → SSH → New SSH    
→ Title: e.g. My SSH Key  
→ Key: paste the copied key here    
→ Add SSH key


6. go back to console and add private key
Adding your private SSH key to the ssh-agent

```
eval ssh-agent
```
(it shows you something like that: … echo Agent 2950;)

```
ssh-add .ssh/id_rsa
```

give password (that you created at the beginning when generating ssh key)


7. That’s it :-) You have done it.

8. You can test if everything work well.

>e.g.   
clone a repository from GitHub to your local 
