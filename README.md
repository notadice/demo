# Squirt

A speed reading bookmarklet.

## Features

- automatically extracts text from blogs and articles
- manual text selection
- gorgeous
- no external API dependencies


## How to set it up

1.Create a bookmark on your browser's bookmarks bar.

2.Set the title to Squirt or any other title you may prefer.

3.Paste the code below as is into the url field and click save.

```
javascript:(function(){
  if(window.sq){
     window.sq.closed && window.document.dispatchEvent(new Event('squirt.again'));
  } else {
    window.sq = {};
    window.sq.userId = '--squirtUser--';
    s = document.createElement('script');
    s.src = 'https://rawgit.com/notadice/demo/master/squirt.js';
    s.s = window.location.search;
    s.idx = s.s.indexOf('sq-dev');
    document.body.appendChild(s);
  }
})();

```
4.Visit an article and click the bookmark previously saved to activate.
