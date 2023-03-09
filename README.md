
# Mod Manager Template for Pywebview and Jinja2 GUIs
This solution is designed for mapping out all Steam Games, Installs, and Running processes. Depending on the type of mod you want to load as a dev, or as a community, this will handle it. 
# 



This is a new projects as of 3/10/23, expect small bugs and changes daily. Original built off of https://github.com/samfisherirl/Boostrap-with-CSS-and-JS-for-Jinja2-Pywebview-GUIs 

#

Requirements: 
- Python 311
- html_minify

More details about the foundational project:

This solution takes Pywebview with Jinja2, and loops through all files in your ./assets/ or ./templates/ looking for any file with *.js and *.css extensions. Read, and inject the code into (eg.) index.html prior to Pywebview displaying in Webview. 


Very simply, before the index file loads, main.py loops through all files in /templates/. For all files with  *.css, they get read and inserted right before the  `</header>` tag, inbetween `<style>`and `</style>`. Same thing for js happens before end of `</body>` tag. 
bootstrap, jquery all works, just place those files in the /template/ folder (anywhere, including "/templates/assets/bootstrap", keep your file structure as is) and that code will be injected before showing pywebview. Index backups are made to preserve original and index will be restored to its original upon close. 
