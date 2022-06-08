# ComicMonoFonts
These are just different formats for importing fonts, for me I used it for a vscode portable version.

If you want to use ComicMono in vscode while its portable then:
1. Go to `File > Open Folder`
2. Navigate to your VS Code installation, and then go to:
   `resources > app > out > vs > code > electron-browser > workbench` Open that folder.
3. Edit `workbench.js` using VS Code and add the snippet to the **end** of it.
4. Save
5. Reload Visual Studio Code


**__Snippet:__**
```javascript
var styleNode = document.createElement('style'); 
styleNode.type = "text/css"; 
var styleText = document.createTextNode(`
    @font-face{
        font-family: 'Fira Code';
        src: url('https://raw.githubusercontent.com/lukxee2/ComicMonoFonts/main/ComicMono.eot') format('embedded-opentype'),
             url('https://raw.githubusercontent.com/lukxee2/ComicMonoFonts/main/ComicMono.woff2') format('woff2'),
             url('https://raw.githubusercontent.com/lukxee2/ComicMonoFonts/main/ComicMono.woff') format('woff'),
             url('https://raw.githubusercontent.com/lukxee2/ComicMonoFonts/main/ComicMono.ttf') format('truetype');
        font-weight: normal;
        font-style: normal;
    }`); 
styleNode.appendChild(styleText); 
document.getElementsByTagName('head')[0].appendChild(styleNode);
```
