## What I wanted
 1. How to store my login info. (Just one time.)
 2. How to change another account when I changed directory.  
 3. How to solve a SourceTree Authentication error.
 
## Search Keyword : 
```
git multi account Completed with errors, see aboveremote: Invalid username or password. fatal: Authentication failed for
```

## Solution :
 1. Remove your keychain
 ```
 $ cd ~/Library/Application/Application Support/SourceTree
 $ rm userName@STAuth-bitbucket.org
 ```
 2. Open KeyChain Access and Search for sourctree
 3. Delete the 'login' items
 4. Check your config
 ```
 $ git config --list
 ```
 or
 ```
 On Terminal
 $ git config user.name
 $ git config user.email
 ```
 5. Store your credential
 ```
 $ git config credential.helper store
 ``` 
 `But, This way you have to execute that commands when changed directory. just onece.`
    
###### Reference Site : 
 https://stackoverflow.com/questions/45622960/sourcetree-remote-invalid-username-or-password
 https://git-scm.com/book/ko/v1/%EC%8B%9C%EC%9E%91%ED%95%98%EA%B8%B0-Git-%EC%B5%9C%EC%B4%88-%EC%84%A4%EC%A0%95