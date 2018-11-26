# Git Commit Signing Using X509 Certificates

## Setup

For more information, visit [How to Create an X509 Certificate](https://www.gnupg.org/documentation/manuals/gnupg/Howto-Create-a-Server-Cert.html).

## Configure

From your Git repository, execute the following set of commands.

### Signing Parameters

```
git config --local commit.gpgsign 'true'
git config --local gpg.program 'gpgsm'
```

### Identity Parameters

```
git config --local user.name 'John Doe'
git config --local user.email 'john@doe.com'
git config --local user.signingkey 'Thumbprint'
```

## Usage

```
git commit -S -m 'Your Commit Message'
```

## Verify

```
git cat-file commit HEAD

tree 4eedc1902c2f7e309435241915f8f16c47e49726
author Darin Egan <5701436+darinegan@users.noreply.github.com> 1542811784 +0000
committer Darin Egan <5701436+darinegan@users.noreply.github.com> 1542967722 +0000
gpgsig -----BEGIN SIGNED MESSAGE-----
 MIAGCSqGSIb3DQEHAqCAMIACAQExDzANBglghkgBZQMEAgEFADCABgkqhkiG9w0B
 ...
 tLPqrL2mmYp0NRnnV/q/Zus3fEfasqG8o4rAt1rhHfU5wL/KC4XuoJR+AAAAAAAA
 -----END SIGNED MESSAGE-----

Genesis
```

## References

- [Telling Git about your signing key](https://help.github.com/articles/telling-git-about-your-signing-key)
- [Signing commits](https://help.github.com/articles/signing-commits)
- [Signing tags](https://help.github.com/articles/signing-tags)

Fin.
