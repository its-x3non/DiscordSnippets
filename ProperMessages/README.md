# Usage
> [!IMPORTANT]  
> If you want proper messaging allignment, i.e, your messages on the right side, use [Vencord](https://github.com/Vendicated/Vencord).  
> My main focus is Vencord, but I will work on a BetterDiscord Version at a later date.

## Root to place in Quick CSS
```css
@import url('https://raw.githubusercontent.com/its-x3non/DiscordSnippets/main/ProperMessages/ProperMessages.theme.css');

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
    --(FRIEND NAME)-color: rgba(R, G, B, .2);
    --(FRIEND NAME)-time-color: rgba(R, G, B, .5);
    --(FRIEND NAME)-text-color: rgb(R, G, B);
    --(FRIEND NAME)-accent: rgb(R, G, B);
  }

.messageListItem__050f9[data-author-id="FRIEND ID"] {
/* chat bubble */
	.cozyMessage__9f4fd [class^="contents"] > [class^="markup"]:not(:empty, code),
	.cozyMessage__9f4fd .container__17159 {
	  border: 2px solid var(--(FRIEND NAME)-color);
	  background-color: var(--(FRIEND NAME)-color);
	  color: var(--(FRIEND NAME)-text-color);
		--text-brand: var(--(FRIEND NAME)-accent);
		--text-link: var(--(FRIEND NAME)-accent);
		--mention-foreground: var(--(FRIEND NAME)-accent);
	}
	
	/* time */
	.contents_d3ae0d [class^="timestamp"]:not(:has(time)) { background: var(--goat-time-color); }
	.contents_d3ae0d [class^="timestamp"]:has(time) {
	  background: var(--(FRIEND NAME)-time-color);
	  border: 1px solid var(--(FRIEND NAME)-time-color);
	  color: var(--(FRIEND NAME)-text-color);
	}
	
	/* username color */
	[class^="contents"] [class^="username"] { color: var(--(FRIEND NAME)-text-color); }
} 
```
___
# Here's what your QuickCSS file could look like
