# SSH (Mac OS)

Information about SSH on Mac OS

---

## Add a key

```bash
ssh-add --apple-use-keychain ~/.ssh/name of key
```

### Config Hosts

```bash
Host *  
AddKeysToAgent yes  
UseKeychain yes  
IdentityFile ~/.ssh/name of key
```

## Delete a key

```bash
ssh-add -d <keyfile>p9uu
```

## Fix Permissions

```bash
sudo chmod 755 ~/.ssh  
udo chmod 600 /path/to/my/key.pem
```

## List active keys

```bash
ssh-add -l
```