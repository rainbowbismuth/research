# You can set up a fetch-only remote in git
Each remote has two different URLs, one for fetching and one for pushing. You can set these individually, and put a dummy URL for one of them.

```
> git remote -v 
origin	https://github.com/rainbowbismuth/research.git (fetch)
origin	https://github.com/rainbowbismuth/research.git (push)

> git remote set-url --push origin DISABLE

> git remote -v
origin	https://github.com/rainbowbismuth/research.git (fetch)
origin	DISABLE (push)
```
