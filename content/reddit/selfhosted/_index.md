---
title: Selfhosted
---

## Etebase - An open source and end-to-end encrypted Firebase alternative

source [^1] [^2]

[^1]: https://www.reddit.com/r/degoogle/comments/jrln3h/etebase_an_open_source_and_endtoend_encrypted/?utm_source=share&utm_medium=web2x&context=3

[^2]: https://www.etebase.com/

## Complete beginner guides?

> - Disable SSH using passwords, use private-key authentication instead
>
> - Don't work from the root user, create another user and give that user sudo rights
>
> - Disable root ssh access (if you need to use the root user, which you shouldnt need to, ssh into a non-root user, and then sudo su)
>
> - Block all ports you don't need from the outside (in other words, whitelist only port 22, 80, 443, and maybe other ports for f.e. websockets, you can use UFW for this)
>
> - Setup fail2ban
>
> - Use strong passwords, even for stuff like local (non-public) MySQL servers
>
> - Use a reverse-proxy in front of your applications if possible, including rate-limiting and such (also improves performance due to the fact that you can do caching and Gzip stuff using Nginx/Apache)
>
> - Don't use FTP, use SFTP instead [^3]

[^3]: https://www.reddit.com/r/selfhosted/comments/bh8090/complete_beginner_guides/elr0ptb?utm_source=share&utm_medium=web2x&context=3

## What are your favourite self hosted apps? Which ones do you use?

discussion[^4]

[^4]: https://www.reddit.com/r/selfhosted/comments/axlt0a/what_are_your_favourite_self_hosted_apps_which/?utm_source=share&utm_medium=web2x&context=3