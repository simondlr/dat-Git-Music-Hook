##dat Git Music Hook ##

Append your most recently listened to track from Last.fm to your commit messages in git. Add that tune's hook to your githook.

I listen to a lot of music. Throughout my code you'll find random lyrics, and band names I've listened to. As a nice reflection (or zeitgeist of sorts), I thought it would be cool to add my track I'm currently listening to, to my git commit messages.

### How does it work ###

It works through the "commit-msg" githook. When commititing to your repo, it will query your recently listened to track from Last.fm's API and append it at the end of the commit message.

### Installing/Using "dat Git Music Hook" ###

Githooks are locally stored in each git repo under the .git/hooks/ folder. Copy the "commit-msg" file straight to that folder. Make sure the permissions are set to execute as well (chmod 755). 

Once copied, you will need to add 2 variables (LASTFM_API_KEY, LAST_FM_USER): an API key (gained from Last.fm: [http://www.last.fm/api/accounts](http://www.last.fm/api/accounts)), and your Last.fm username.

### Example use case ###

`git commit -m "Initial Commit"`

and it will automagically append it to something like this in your commit message:

``` 
Date:   Thu Feb 21 10:38:58 2013 +0200

    Initial Commit
    - Listened to: Eskmo - Oh in This World of Dread, Carry On
```

To not use the githook, simply add the "-n" or "--no-verify" flag to your commits. This will skip the "commit-msg" hook.

`git commit -nm "Removed rails security bugs."`

### Authors/Contributors ###

Jacques Bruwer and Simon de la Rouviere. Cool, cool cool cool.

Understanding of githooks using Python was gleamed/taken from Sprint.ly's [commit-msg githook](https://github.com/nextbigsoundinc/Sprintly-GitHub).

### MIT License ###

Copyright (c) 2012 Simon de la Rouviere, Jacques Bruwer

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

