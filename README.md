# freetar - an alternative frontend for ultimate-guitar.com

This is like [Invidious](https://invidious.io/) but only for [Ultimate Guitar](https://www.ultimate-guitar.com/).  

This is a fork of Freetar, which makes one modification: The ability to set the CSS 'column-count' property in the UI (see screenshot). This enables me to display long charts without scrolling on my 27" 1440p display.
(Note "Cols" option next to "Show chords," "Autoscroll," etc.)
![image](https://github.com/jpaskaruk/freetar/assets/5622722/aab53a99-566a-408f-9a47-79b85e7b89bc)



## Instances
- https://freetar.de
- https://freetar.habedieeh.re
- https://tabs.adast.dk

## Features
- no ads, popups, AI, blockchain. Just a simple design
- search for tabs and view them
- save your favorite chords as favs (everything is stored in session storage (not send to the server), no account needed)
- dark mode
- auto scroll
- useful for printing chords
- show chords


## How to use it
After successfull installation, there is an executable called `freetar` in the PATH. Execute it without parameters and it listens on 0.0.0.0:22000.  


**PyPi**  
Package: https://pypi.org/project/freetar/

```
pip install freetar
```

**Docker**  
Image: https://hub.docker.com/r/kmille2/freetar  
Port: 22000

```
sudo docker pull kmille2/freetar
sudo docker run -p 127.0.0.1:22000:22000 kmille2/freetar
```


### Dev environment
You need [poetry](https://python-poetry.org/). Then:
```
poetry install
vim freetar/*.py
poetry run python freetar/backend.py
Visit localhost:22000 in browser

# static files: freetar/static/*
# html templates: freetar/templates/*
poetry run freetar
```

## Future work

- ~~show chords~~
- improve UX on mobile devices
- on smartphones: prevent lock screen
- ~~share chords (qr code)?~~ (done by #12 with export/import functionality)
- save favs encrypted server side?
- Browser Extension like [Invidious Redirection](https://addons.mozilla.org/en-US/firefox/addon/invidious-redirection/)
