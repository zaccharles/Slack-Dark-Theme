## How to add the dark theme to slack

1) go to your version of `C:\Users\username\AppData\Local\slack\app-3.1.0\resources\app.asar.unpacked\src\static`
2) locate and open the file `ssb-interop.js` in notepad
3) add this code to the end of that file and save:
```
document.addEventListener('DOMContentLoaded', function () {
    $.ajax({
        url: 'https://raw.githubusercontent.com/earlduque/Slack-Dark-Theme/master/dark.css',
        success: function (css) {
            $("<style></style>").appendTo('head').html(css);
        }
    });
});
```
4) close and reopen slack

### Further, I like this as the sidebar coloring:

1) on the channel list at the top, click on your name and go to preferences
2) click on sidebar
3) scroll down and click on advanced/custom theme
4) paste this into the custom theme input box:
`#363636,#444A47,#D39B46,#FFFFFF,#434745,#ffffff,#99D04A,#DB6668`
