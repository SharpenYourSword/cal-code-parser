# Access California statutes from your text editor.
Generate Sublime Text 3 snippets that insert formatted citations and full text of current statutes via California's official FTP repository.

![Screen capture of snippets in action.](http://www.gregkochansky.com/images/screen.gif "Screen capture of snippets in action.")

The script generates `*.sublime-snippet` files for each numbered provision based on the full text of any California Code as reflected in the state's [FTP repository](ftp://www.leginfo.ca.gov/pub/code/).
To use:
- Download any Code directory via FTP. (The files are tiny, but there can be thousands of them, many of which contain multiple code provisions. Perhaps a good idea to stick with the Codes you actually need.)
- `cal-code-parser.rb` goes in the same directory as the code directory, as in: `/dir/cal-code-parser.rb` and `/dir/code/`.
- `ruby cal-code-parser.rb cacp Cal.Civ.` where `cacp` is the directory that contains the Code and `Cal.Civ.` is whatever citation style you want to use. For instance, omit `Cal.` if following the California Style Manual. 
- In Sublime Text 3, the scope for each snippet is `text.lwd`. Save your file with that extension or change the template scope to the file extension of your choosing (`text.txt`, maybe).
- To trigger the snippet for Cal. Code of Civil Procedure section 2023.020, type `cacp2023.020[TAB]`, which will expand to a full citation, skip a line below the cursor, and insert the full text of the provision.

The benefit is rapid access to Code provisions, as you write, without switching focus to another application.
