# Readme

## Setup

For more information, visit [How to Create an X509 Certificate](https://www.gnupg.org/documentation/manuals/gnupg/Howto-Create-a-Server-Cert.html).

## Configure

From your Git repository, execute the following set of commands.

```
git config --local commit.gpgsign 'true'
git config --local gpg.program 'gpgsm'
```

```
git config --local user.name 'John Doe'
git config --local user.email 'john@doe.com'
git config --local user.signingkey 'Thumbprint'
```

### Verify

```
git config --list --local
```

## Usage

```
git commit -S -m 'Your Commit Message'
```

### Verify

```
git cat-file commit HEAD
```

## References

- [Telling Git about your signing key](https://help.github.com/articles/telling-git-about-your-signing-key)
- [Signing commits](https://help.github.com/articles/signing-commits)
- [Signing tags](https://help.github.com/articles/signing-tags)

Fin.
