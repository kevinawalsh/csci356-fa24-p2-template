CSCI 356 Fall 2024 Project 2 Starter Code
-----------------------------------------

This repository contains starter code for project 2, in which you will write a
pure-python dynamic web server. The main files are:

* `webserver.py` - Code for a mostly static, file-based, concurrent web server.

* `web_files` - A set of test html, css, image, and other files for the server.

Tasks:

- [ ] implemented from scratch without HTTP-related python libraries or modules
- [x] opens "welcoming" socket and waits for connections from browsers
- [x] concurrency via multithreading support: starts a separate thread for each connection
- [ ] installed and tested on localhost, logos, or another machine
- [x] responds to "GET /hello" requests
  - [ ] /hello page has html content and "text/html" mime-type
  - [ ] links in /hello page are all clickable and work as intended
  - [ ] /hello page content is dynamic, changing on each request
  - [ ] /hello page content is interactive, using client (user) input in some way
     - [ ] properly handles url escapes in client input
     - [ ] reach goal: use cookies to retain previous user inputs
- [x] tracks basic statistics, like number of connections, errors, etc.
- [x] responds to "GET /status" requests with nicely-formatted statistics
- [x] responds to requests for contents of a file
- [ ] support mime-types for file responses
    - [ ] If path ends in ".html" or ".htm", mime-type will be "text/html"
    - [ ] If path ends in ".jpg" or ".jpeg", mime-type will be "image/jpeg"
    - [ ] If path ends in ".png", then mime-type will be "image/png"
    - [ ] Supports ".txt", ".css", and ".js" path endings, with appropriate mime-types
- [ ] obtain more complete and complex web site contents for testing
- [ ] default page support for directories and subdirectories:
    - [ ] respond to "GET /" requests with top-level index.html
    - [ ] respond to "GET" requests ending with "/" with appropriate
      subdirectory index.html, if present
    - [ ] reach goal: respond with index.html, if present, for any path to a
      directory, even if trailing "/" is not present 
    - [ ] reach goal: if index.html is not present, instead respond with a
      "directory listing" of clickable links to each item in that directory
    - [ ] use appropriate mime-type for index.html and directory listings
- [ ] reach goal: respond to "GET /whoami" with page showing info about the client
    - [ ] show client's IP address and port number
    - [ ] show client's browser "user-agent" string, taken from request headers
    - [ ] show any cookies present in request headers
    - [ ] show the user's privacy preferences, from DNT and/or Sec-GPC headers
- [ ] reach goal: ban a browser, based on user-agent
- [ ] reach goal: support HTTP cookies
    - [ ] set a cookie with some contents, e.g. from input, or a visit counter
    - [ ] use cookie in some responses, e.g. for /hello, /status, or /whoami
- [ ] reach goal: support HTTP keep-alive feature, if requested by client
    - [ ] track and report statistics, including number of currently open
      connections, and average number of requests handled per connection
    - [ ] server initiates connection close eventually, e.g. after some number
      of requests, or after some amount of time has elapsed, or if connection
      remains idle for some amount of time.
- [ ] project still does not use HTTP related python libraries or modules
- [ ] includes basic error checking and does not crash under normal usage
- [ ] prints trace of activity and status messages to console, for debugging
- [ ] Rewrite README.md to describe final state of project, collaboration, etc.
