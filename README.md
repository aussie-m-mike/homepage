# Homepage
Donald Trump personal website. Basically this is just a résumé.

You could view the website here: https://aussie-m-mike.github.io/homepage/


#### For local development:
1. Clone the repo 

```git clone https://github.com/aussie-m-mike/homepage.git```

2. Install server

```npm install --global serve```

3. Run 

```serve```

4.  For build a decent Service Worker

```npm install --global workbox-cli serv```

5. git/hooks/pre-commit looks as simple as this (Make sure it's executable, chmod +x .git/hooks/pre-commit if necessary):

``` bash
#!/bin/sh
if workbox generateSW workbox-config.js ; then
  git add sw.js
  exit 0
else
  echo "Cannot generate sw.js"
  echo "Aborting"
fi
```