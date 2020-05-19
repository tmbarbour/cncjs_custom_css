# cncjs_custom_css
Custom CSS to override CNCjs button styles

Clone (or download a .zip) of this repository
Find out where the CNCjs application is running. Mine is running from 
-  /usr/local/lib/node_modules/cncjs/dist/cncjs

Unix commands to find the location
You can track back where it's running with the following set of commands:
- ps aux | grep cnc
-- It should display something like:  

--- pi       30517  3.4  2.0 191252 82116 pts/7    Sl+  18:49   0:38 node /usr/local/bin/cncjs

-- cd to the parent directory of the running command

-- cd /usr/local/bin

-- Then list the details of that directory

-- ls -l

-- It should display something like:

``` 
lrwxrwxrwx 1 root root 35 Apr 20 17:16 cncjs -> ../lib/node_modules/cncjs/bin/cncjs
```

-- cd to that parent directory

-- cd ../lib/node_modules/cncjs/

-- List the contents

-- ls -l

```
drwxr-xr-x   2 root root  4096 Apr 20 17:14 bin
-rw-r--r--   1 root root    98 Oct 26  1985 CHANGELOG.md
drwxr-xr-x   3 root root  4096 Apr 20 17:14 dist
-rw-r--r--   1 root root  1082 Oct 26  1985 LICENSE
drwxr-xr-x 532 root root 20480 Apr 20 17:16 node_modules
-rw-r--r--   1 root root 13805 Apr 20 17:16 package.json
-rw-r--r--   1 root root 16433 Oct 26  1985 README.md
drwxr-xr-x   2 root root  4096 Apr 20 17:14 static
```

-- cd to the 'dist' directory

-- cd to cncjs

-- cd to app

- Inside the app directory there should be a app.css file. Append the contents of the custom_cncjs.css to that file
You can append using the linux 'cat' command, or in windows you can edit and update in notepad
- IT IS VERY IMPORTANT TO USE TWO GREATER THAN SIGNS TO APPEND AND NOT REPLACE

-- cat ~/my_download_dir/cncjs_custom_css/custom_cncjs.css >> app.css

- Restart your cncjs server

- Ctrl-Shift refresh your browser to clear the cache and load the new app

