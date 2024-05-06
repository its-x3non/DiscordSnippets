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
  
    --default-time-color: rgba(210, 210, 210, .5);
    --self-time-color: rgba(204, 108, 231, .5);

    --default-text-color: rgb(255, 255, 255);
    --self-text-color: rgb(240, 187, 255);

    --default-accent: rgb(170, 239, 252);
    --self-accent: rgb(4, 4, 167);
  }
```
## You can also add the following if you want to include your friends too:
```css
  :root {
    --(NAME GOES HERE)-color: rgba(R, G, B, .2);
    --(NAME GOES HERE)-time-color: rgba(R, G, B, .5);
    --(NAME GOES HERE)-text-color: rgb(R, G, B);
    --(NAME-GOES-HERE)-accent: rgb(R, G, B);
  }

  /* FRIEND BUBBLE COLOR */
  .messageListItem__050f9[data-author-id="FRIEND ID GOES HERE"] >
  .cozyMessage__9f4fd [class^="contents"] > [class^="markup"]:not(:empty, code),
  .messageListItem__050f9[data-author-id="FRIEND ID GOES HERE"] > .cozyMessage__9f4fd .container__17159{
    border: 2px solid var(--(NAME GOES HERE)-color);
    background-color: var(--(NAME GOES HERE)-color);
    color: var(--(NAME GOES HERE)-text-color);
      --text-brand: var(--(NAME-GOES-HERE)-accent);
    	--text-link: var(--(NAME-GOES-HERE)-accent);
    	--mention-foreground: var(--(NAME-GOES-HERE)-accent);
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
    --(NAME GOES HERE)-color: rgba(R, G, B, .2);
    
    --(NAME GOES HERE)-time-color: rgba(R, G, B, .5);
    --default-time-color: rgba(210, 210, 210, .5);
    --self-time-color: rgba(204, 108, 231, .5);

    --default-text-color: rgb(255, 255, 255);
    --self-text-color: rgb(240, 187, 255);
    --(NAME GOES HERE)-text-color: rgb(R, G, B);

    --default-accent: rgb(170, 239, 252);
    --self-accent: rgb(4, 4, 167);
    --(NAME-GOES-HERE)-accent: rgb(R, G, B);
  }

  /* FRIEND BUBBLE COLOR */
  .messageListItem__050f9[data-author-id="FRIEND ID GOES HERE"] >
  .cozyMessage__9f4fd [class^="contents"] > [class^="markup"]:not(:empty, code),
  .messageListItem__050f9[data-author-id="FRIEND ID GOES HERE"] > .cozyMessage__9f4fd .container__1715{
    border: 2px solid var(--(NAME GOES HERE)-color);
    background-color: var(--(NAME GOES HERE)-color);
    color: var(--(NAME GOES HERE)-text-color);
      --text-brand: var(--(NAME-GOES-HERE)-accent);
    	--text-link: var(--(NAME-GOES-HERE)-accent);
    	--mention-foreground: var(--(NAME-GOES-HERE)-accent);
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
