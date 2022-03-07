---
title: Yubico with gpg, ssh keys, 2FA, and others
date: 2019-06-18T23:02:33+01:00
draft: false
tags:
    - yubico
    - ssh
    - gpg
    - 2fa
    - authentication

---


How many time did you lose your phone that contains all your 2FA ? or your hard disk along with your private keys, ssh or/and gpg?           
I did, aloooooot and it was excruciating every time, locked from your accounts, it is more likely to lose your phone/disk or have it damaged than your keychain.

YubiKey is a physical hardware device, that can save different type of authentication, GPG keys, ssh keys, 2FA, and even static password.            
It even supports U2F with [Firefox](https://support.yubico.com/support/solutions/articles/15000017511-enabling-u2f-support-in-mozilla-firefox) and chrome, which you can also use with [Google](https://support.yubico.com/support/solutions/articles/15000006418-using-your-yubikey-with-google) now, [and there is more](https://www.yubico.com/why-yubico/how-yubikey-works/).

YubiKey is not the only one there providing those features, there are [other providers](https://www.dongleauth.info/dongles/) too, but I have been using YubiKey for so long.


from all those features, I'm using it daily for:

- Static password storage: YubiKey can set more than 30 characters static password, you can add it to your password to make it more unbreakable, never use the static password only.       
    if you are using any Linux distro, install `yubikey-personalization-gui` package and use it to set the static password to slot 2.               
    After you set the static password, touch the kye for 4 seconds, and it will print the static password.               
    Check the [YubiKey Static password online documentation](https://support.yubico.com/support/solutions/articles/15000006480-understanding-core-static-password-features) for more details.

- Storing 2FA: Surely you are using 2FA with google account, Facebook or even GitHub, you can save those on the YubiKey and use the storage-less android app, that read 2FA tokens directly from the YubiKey and store them there instantly, fascinating, right?
Check the [YubiKey 2FA online documentations](https://support.yubico.com/support/solutions/articles/15000006419-using-your-yubikey-with-authenticator-codes) for details.

- Storing SSH and GPG key: you can [setup your YubiKey to store GPG keys](https://github.com/drduh/YubiKey-Guide), and later [configure your system to use gpg agent as ssh agent](https://eklitzke.org/using-gpg-agent-effectively), Yes GPG can do this, OMG !!


[You can use it for much much much more](https://wiki.archlinux.org/index.php/YubiKey).

One last thing, better to use at least two YubiKey for storing any of that stuff :)  
