### Generating a new SSH key

```sh
ssh-keygen -t ed25519 -C "your_email@example.com" 
```

### Adding your SSH key to the ssh-agent

```sh
eval "$(ssh-agent -s)"
```

```sh
ssh-add ~/.ssh/id_ed25519
```

### Adding a new SSH key to your GitHub account

```sh
cat ~/.ssh/id_ed25519.pub
```

    - Now, go to Github -> Settings, and click *SSH and GPG keys* on *Access* section.

    - Click *New SSH key* or *Add SSH key*.

    - In the *Title* field, add a descriptive label for the new key. For example, if you're using a personal Mac, you might call this key "Personal MacBook Air".

    - Paste your key into the *Key* field.

    - Click *Add SSH key*.

    - If prompted, confirm your GitHub password. That's it! You now have a SSH key in GitHub.
