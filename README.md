
## Overview

This is codeflower, an app for visualizing git repositories. If you give it a repo, it generates a force directed graph that allows you to see the overall file structure of the repo, as well as the languages used and the number of lines of code in each language. More info on the app can be found by clicking the WTF button on the lower left side of the page.

You can access the app in two ways:

1. by installing the app as an extension for [Chrome](https://chrome.google.com/webstore/detail/codeflower/mnlengnbfpfgcfdgfpkjekoaeophmmeh) or [Firefox](https://addons.mozilla.org/en-US/firefox/addon/codeflower/?src=search). Once it's installed, navigate to the github page of the repo you want to visualize and click the "Codeflower" tab.

2. by heading to [web.codeflower.la](https://web.codeflower.la), and entering the git clone url of the repo you want to visualize in the "add repo" input.

## Component Repos

These are the repo that make up the project --

#### cloc-server

This is the api. It takes in parameters that describe a repository (owner, name, optional branch) and returns a JSON object that describes the repository, based largely on data from the [cloc](https://github.com/AlDanial/cloc/blob/master/cloc) program.

#### client-web

This is the web app. It converts the JSON from the api into a visualization in your browser.

#### chrome

This is the bit of code that adds the "Codeflower" tab to github, and display the web application in an iframe when you click that tab.

#### admin

Miscellaneous administrative functions, like monitoring the cloc-servers and rotating SSL certs.

#### pm2-

These three repos are extensions to [pm2](https://github.com/Unitech/pm2), a process-manager for Node. The cloc-servers are run via pm2.
