# Usage
> [!IMPORTANT]  
> If you want proper messaging allignment, i.e, your messages on the right side, use [Vencord](https://github.com/Vendicated/Vencord).  
> BetterDiscord won't work as this uses ThemeAttributes plugin in Vencord.

## Root to place in Quick CSS
```css
@import('https://raw.githubusercontent.com/its-x3non/DiscordSnippets/main/ProperMessages/ProperMessages.theme.css');

  :root {
    --default-msg-color: rgba(210, 210, 210, 0.2);
    --self-color: rgba(204, 108, 231, .2);
    --attachment-color: rgba(210, 210, 210, 0.2);
  
    --default-time-color: rgba(210, 210, 210, .5);
    --self-time-color: rgba(204, 108, 231, .5);
  }
```
### You can also include this if you don't want rainbow attachments:
```css
  /* attachment/embed color */
  .container__62863 > :not(.reactions_da5b2a, .searchResultsWrap__2e184 *) {
    animation: none;
  }
```

## You can also add the following if you want to include your friends too:
```css
  :root {
    --(NAME GOES HERE)-color: rgba(R, G, B, .2);
    --(NAME GOES HERE)-time-color: rgba(R, G, B, .5);
  }

  /* FRIEND BUBBLE COLOR */
  .messageListItem__050f9[data-author-id="FRIEND ID GOES HERE"] >
  .cozyMessage__9f4fd [class^="contents"] > [class^="markup"]:not(:empty, code){
    border: 2px solid var(--(NAME GOES HERE)-color);
    background-color: var(--(NAME GOES HERE)-color);
  } 

  /* FRIEND TIME STAMP */
  .messageListItem__050f9[data-author-id="FRIEND ID GOES HERE"]
  .contents_d3ae0d [class^="timestamp"]:not(:has(time)) {
    background: var(--(NAME GOES HERE)-time-color);
  }

  .messageListItem__050f9[data-author-id="FRIEND ID GOES HERE"]
  .contents_d3ae0d [class^="timestamp"]:has(time) {
    background: var(--(NAME GOES HERE)-time-color);
    border: 1px solid var(--(NAME GOES HERE)-time-color);
  }
```
___
# Here's what your QuickCSS file could look like
```css
@import('https://raw.githubusercontent.com/its-x3non/DiscordSnippets/main/ProperMessages/ProperMessages.theme.css');

  :root {
    --default-msg-color: rgba(210, 210, 210, 0.2);
    --self-color: rgba(204, 108, 231, .2);
    --attachment-color: rgba(210, 210, 210, 0.2);
    --(NAME GOES HERE)-color: rgba(R, G, B, .2);
    
    --(NAME GOES HERE)-time-color: rgba(R, G, B, .5);
    --default-time-color: rgba(210, 210, 210, .5);
    --self-time-color: rgba(204, 108, 231, .5);
  }

  /* FRIEND BUBBLE COLOR */
  .messageListItem__050f9[data-author-id="FRIEND ID GOES HERE"] >
  .cozyMessage__9f4fd [class^="contents"] > [class^="markup"]:not(:empty, code){
    border: 2px solid var(--(NAME GOES HERE)-color);
    background-color: var(--(NAME GOES HERE)-color);
  } 

  /* FRIEND TIME STAMP */
  .messageListItem__050f9[data-author-id="FRIEND ID GOES HERE"]
  .contents_d3ae0d [class^="timestamp"]:not(:has(time)) {
    background: var(--(NAME GOES HERE)-time-color);
  }

  .messageListItem__050f9[data-author-id="FRIEND ID GOES HERE"]
  .contents_d3ae0d [class^="timestamp"]:has(time) {
    background: var(--(NAME GOES HERE)-time-color);
    border: 1px solid var(--(NAME GOES HERE)-time-color);
  }
    
    /* attachment/embed color */
  .container__62863 > :not(.reactions_da5b2a, .searchResultsWrap__2e184 *) {
    animation: none;
  }
```
