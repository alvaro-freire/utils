## Generating a GPG key

```sh
gpg --full-generate-key
```

> `pg --default-new-key-algo rsa4096 --gen-key`

```sh
gpg --list-secret-keys --keyid-format=long
```

> From the list of GPG keys, copy the long form of the GPG key ID you'd like to use. In this example, the GPG key ID is `3AA5C34371567BD2`:

```sh
$ gpg --list-secret-keys --keyid-format=long
/Users/hubot/.gnupg/secring.gpg
------------------------------------
sec   4096R/3AA5C34371567BD2 2016-03-10 [expires: 2017-03-10]
uid                          Hubot 
ssb   4096R/42B317FD4BA89E7A 2016-03-10
```
```sh
gpg --armor --export 3AA5C34371567BD2
```

```sh
git config --global user.signingkey 3AA5C34371567BD2
```

> This command prints the GPG key ID, in ASCII armor format

- Copy your GPG key, beginning with `-----BEGIN PGP PUBLIC KEY BLOCK-----` and ending with `-----END PGP PUBLIC KEY BLOCK-----`.

```sh
git config --global commit.gpgSign true
```

- Add the GPG key to your GitHub account. 
> GitHub -> Settings -> SSH and GPG keys -> New GPG key
