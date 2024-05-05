# Useage
> [!IMPORTANT]  
> If you want proper messaging allignment, i.e, your messages on the right side, use Vencord.  
> BetterDiscord won't work as this uses ThemeAttributes plugin in Vencord.

## Root to place in Quick CSS
```css
  --default-msg-color: rgba(210, 210, 210, 0.2);
  --self-color: rgba(204, 108, 231, .2);
  --attachment-color: rgba(210, 210, 210, 0.2);

  --default-time-color: rgba(210, 210, 210, .5);
  --self-time-color: rgba(204, 108, 231, .5);
```
You can also include this if you don't want rainbow attachments:
```css
/* attachment/embed color */
.container__62863 > :not(.reactions_da5b2a, .searchResultsWrap__2e184 *) {
  animation: none;
}
```
