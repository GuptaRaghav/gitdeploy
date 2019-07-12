# Deploygithub

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 7.3.0.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## To add current repo as remote git Repo

`git remote add origin https://github.com/GuptaRaghav/gitdeploy.git` where `GuptaRaghav` is github profile account and `gitdeploy` is github repository name

## Push changes to Remote (Github) Repository

`git push origin master`

## Deploying Prouction version to github pages

`ng build --prod --base-href="https://GuptaRaghav.github.io/gitdeploy/"`

## Publishing Challenges on Github Pages

Run `ngh` to publish on github wont be that easy what I have thought :sweat_smile:  Got following errors while publishing it on github page:
1. index.html could not be copied to 404.html. Continuing without an error.
(Hint: are you sure that you have setup the --dir parameter correctly?)
{ [Error: ENOENT: no such file or directory, lstat 'G:\Learning\Angular\deploygithub\dist\index.html']
  errno: -4058,
  code: 'ENOENT',
  syscall: 'lstat',
  path: 'G:\\Learning\\Angular\\deploygithub\\dist\\index.html' }
*** An error occurred!

Error: Unspecified error (run without silent option for detail)
    at C:\Users\UserName\AppData\Roaming\npm\node_modules\angular-cli-ghpages\node_modules\gh-pages\lib\index.js:232:19
    at _rejected (C:\Users\UserName\AppData\Roaming\npm\node_modules\angular-cli-ghpages\node_modules\q\q.js:844:24)
    at C:\Users\UserName\AppData\Roaming\npm\node_modules\angular-cli-ghpages\node_modules\q\q.js:870:30
    at Promise.when (C:\Users\UserName\AppData\Roaming\npm\node_modules\angular-cli-ghpages\node_modules\q\q.js:1122:31)
    at Promise.promise.promiseDispatch (C:\Users\UserName\AppData\Roaming\npm\node_modules\angular-cli-ghpages\node_modules\q\q.js:788:41)
    at C:\Users\UserName\AppData\Roaming\npm\node_modules\angular-cli-ghpages\node_modules\q\q.js:604:44
    at runSingle (C:\Users\UserName\AppData\Roaming\npm\node_modules\angular-cli-ghpages\node_modules\q\q.js:137:13)
    at flush (C:\Users\Raghav Gupta\AppData\Roaming\npm\node_modules\angular-cli-ghpages\node_modules\q\q.js:125:13)
    at process._tickCallback (internal/process/next_tick.js:61:11)
    
2. I tried with `ngh --no-silent` as suggested by community and got the following error:

index.html could not be copied to 404.html. Continuing without an error.
(Hint: are you sure that you have setup the --dir parameter correctly?)
{ [Error: ENOENT: no such file or directory, lstat 'G:\Learning\Angular\deploygithub\dist\index.html']
  errno: -4058,
  code: 'ENOENT',
  syscall: 'lstat',
  path: 'G:\\Learning\\Angular\\deploygithub\\dist\\index.html' }
Cloning https://github.com/GuptaRaghav/gitdeploy.git into C:\Users\Raghav Gupta\AppData\Roaming\npm\node_modules\angular-cli-ghpages\node_modules\gh-pages\.cache

Cleaning

Fetching origin

Checking out origin/gh-pages

Removing files

Copying files

Adding all

Committing

Pushing

*** An error occurred!

{ ProcessError: fatal: HttpRequestException encountered.
   An error occurred while sending the request.
bash: /dev/tty: No such device or address
error: failed to execute prompt script (exit code 1)
fatal: could not read Username for 'https://github.com': No error

    at ChildProcess.<anonymous> (C:\Users\UserName\AppData\Roaming\npm\node_modules\angular-cli-ghpages\node_modules\gh-pages\lib\git.js:47:23)
    at ChildProcess.emit (events.js:182:13)
    at maybeClose (internal/child_process.js:962:16)
    at Process.ChildProcess._handle.onexit (internal/child_process.js:251:5)
  code: 128,
  message:
   'fatal: HttpRequestException encountered.\n   An error occurred while sending the request.\r\nbash: /dev/tty: No such device or address\nerror: failed to execute prompt script (exit code 1)\nfatal: could not read Username for \'https://github.com\': No error\n',
  name: 'ProcessError' }

3. My bad luck unable to get sleep in night WTF i have done wrong :confounded: but shit lies in git itself :unamused: updated git to latest version using `git update` as i was on git version 2.15 

4. Again tried using ngh but still no luck on serving part though it got published but gave following error:
index.html could not be copied to 404.html. Continuing without an error.
(Hint: are you sure that you have setup the --dir parameter correctly?)
{ [Error: ENOENT: no such file or directory, lstat 'G:\Learning\Angular\deploygithub\dist\index.html']
  errno: -4058,
  code: 'ENOENT',
  syscall: 'lstat',
  path: 'G:\\Learning\\Angular\\deploygithub\\dist\\index.html' }
*** Successfully published!

5. Finally run `ngh --dir dist/deploygithub` where `dist` is distributable folder under current project and `deployggithub` is the Directory Name under dist Directory

Voila It works ! :smile:
## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).

# Emoji
used folowing cheatsheets
1. [Emoji](https://www.webfx.com/tools/emoji-cheat-sheet/)
