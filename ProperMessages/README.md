# Usage
> [!IMPORTANT]  
> If you want proper messaging allignment, i.e, your messages on the right side, use [Vencord](https://github.com/Vendicated/Vencord).  
> My main focus is Vencord, but I will work on a BetterDiscord Version at a later date.

## Root to place in Quick CSS
These are also the default settings if you ever want to revert back
```css
@import url('https://raw.githubusercontent.com/its-x3non/DiscordSnippets/main/ProperMessages/ProperMessages.theme.css');

:root {
  --default-msg-color: hsla(0, 0%, 82%, 0.2);
  --self-color: hsla(286, 72%, 66%, 0.2) ;

  --default-time-color: hsla(0, 0%, 82%, 0.45);
  --self-time-color: hsla(286, 72%, 66%, 0.45);

  --default-text-color: hsla(0, 0%, 100%);
  --self-text-color: hsl(287, 100%, 80%);

  --default-accent: hsl(185, 100%, 50%);
  --self-accent: hsl(287, 100%, 90%);

  --accent-1: var(--self-accent); /* links */
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
	.contents_d3ae0d [class^="timestamp"]:has(time) { color: var(--(FRIEND NAME)-text-color); }
	
	/* username color */
	[class^="contents"] [class^="username"] { color: var(--(FRIEND NAME)-text-color) !important; }
} 
```
___
# Here's what your QuickCSS file could look like
