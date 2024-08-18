# Discord-Experiments-Guide
A short guide to set up Discord experiments on your local client.

 It allows you to use the "Favorites" tab which is pinned channels and DMs that you can pick and choose from channels.

To enable your discord to do this:
1. Press the Windows key, and type in "%APPDATA%" and open that folder.
2. Find and open the Discord folder in that tab.
3. Find "settings.json" and open that with notepad or any generic text editor.
4. Replace the text in "settings.json" with the following.
```json
{
  "BACKGROUND_COLOR": "#202225",
  "IS_MAXIMIZED": false,
  "IS_MINIMIZED": false,
  "WINDOW_BOUNDS": {
    "x": 288,
    "y": 51,
    "width": 1591,
    "height": 919
  },
  "OPEN_ON_STARTUP": false,
  "DANGEROUS_ENABLE_DEVTOOLS_ONLY_ENABLE_IF_YOU_KNOW_WHAT_YOURE_DOING": true
}
```

4 cont. Feel free to change OPEN_ON_STARTUP to true if you want your Discord to open when you turn on your computer.
5. Restart Discord.
6. On Discord now, Press this combination of keys Crtl+Shift+I

This will open up the hidden console of Discord. You want to go to the top and press the "Console" tab.

7. Within the Console command line textbox on the bottom, input the following code:

```js
let _, a = Object.values,
    b = "getCurrentUser",
    c = "actionHandler",
    d = "_actionHandlers",
    l = "_dispatcher",
    i = "ExperimentStore";
webpackChunkdiscord_app.push([
    [Date.now()], {},
    e => {
        _ = e
    }
]), m = a((u = a(_.c).find(e => e?.exports?.default?.[b] && e?.exports?.default?.[l]?.[d]).exports.default)[l][d]._dependencyGraph.nodes), u[b]().flags |= 1, m.find(e => "Developer" + i == e.name)[c].CONNECTION_OPEN();
try {
    m.find(e => i == e.name)[c].OVERLAY_INITIALIZE({
        user: {
            flags: 1
        }
    })
} catch {}
m.find(e => i == e.name).storeDidChange()
```

8. Press enter, and close the console.
9. Go to your settings, you will see there is an "Experiments" tab at the bottom. Here you can input whatever Experiment you want. If you want the Favorites tab, type "Favorites" and choose Treatment 1.

If you have any questions or need any help let me know. I wanted to write this guide so I have it for future reference.
