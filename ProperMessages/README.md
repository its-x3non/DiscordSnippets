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
    --(NAME GOES HERE)-color: rgba(R, G, B, .2);
    --(NAME GOES HERE)-time-color: rgba(R, G, B, .5);
    --(NAME GOES HERE)-text-color: rgb(R, G, B);
    --(NAME-GOES-HERE)-accent: rgb(R, G, B);
  }

.messageListItem__050f9[data-author-id="FRIEND ID"] {
/* chat bubble */
	.cozyMessage__9f4fd [class^="contents"] > [class^="markup"]:not(:empty, code),
	.cozyMessage__9f4fd .container__17159 {
	  border: 2px solid var(--goat-color);
	  background-color: var(--goat-color);
	  color: var(--goat-text-color);
		--text-brand: var(--goat-accent);
		--text-link: var(--goat-accent);
		--mention-foreground: var(--goat-accent);
	}
	
	/* time */
	.contents_d3ae0d [class^="timestamp"]:not(:has(time)) { background: var(--goat-time-color); }
	.contents_d3ae0d [class^="timestamp"]:has(time) {
	  background: var(--goat-time-color);
	  border: 1px solid var(--goat-time-color);
	  color: var(--goat-text-color);
	}
	
	/* username color */
	[class^="contents"] [class^="username"] { color: var(--goat-text-color); }
} 
```
___
# Here's what your QuickCSS file could look like
