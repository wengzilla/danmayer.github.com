---
layout: page
title: "Random Ideas"
---
{% include JB/setup %}

This is a page, where I can list ideas as I have them. Then post links to either the project when I build it, or more likely the link to a existing project when I find someone already implemented it. I might also convert some ideas into blog posts about why I decided it was a bad idea after I researching a project. The ideas here are just brainstorming or quick little thoughts, not full thought out just sentence or two I jot down to refresh my memory or for me to collect related thoughts.

Project Ideas
===

* pre git commit hook spellcheck, cmd-line likely using aspell or something build in osx 
* Sinatra app that just polls mysql slow and displays it with history etc
* github -> kindle reader format the code for kindle readability and have links / section browsing for the files.
* remote ping pong pair programming over a shared updated git repo or gist.
* combiner allows multiple micro apps / apis to be combined by connecting them feeding one into another JSON can be uploaded or output nice html wysiwyg interface, has a container app for app running.
* google map game... point on a map, red virus starts to spread... survive as long as possible, traveling and trying to be in the last city overtaken by the virus... Like the opposite of pandemic 2
* community chess play as a team. (you make random moves in games with a collective group of people, your score is the aggregate of how many games you win. You never end up making a move in a game against yourself, but you can be in N/2 total games at any time.)
* build something like this but perhaps for stocks or ruby community projects / posts / tweets? http://disqus.com/gravity/
* Test results collector api, just a API that collects test time, speed, # failures, which tests failed, etc and reports over time
* paid version of http://www.free-ocr.com/ using open source OCR tools
* gem to monitor and send live line number / code usage over to server (find most common hot spots, least used code, and dead code) (http://codecovtest.herokuapp.com/, blog about the failed attempt where ruby keeps segfaulting)
   * http://www.rubyinside.com/how-to-create-a-ruby-extension-in-c-in-under-5-minutes-100.html
   * http://blog.jcoglan.com/2012/07/29/your-first-ruby-native-extension-c/
   * https://www.ruby-lang.org/en/documentation/ruby-from-other-languages/to-ruby-from-c-and-cpp/
   * http://www.ruby-doc.org/stdlib-2.0.0/libdoc/coverage/rdoc/Coverage.html
   * https://github.com/sj26/ruby-1.9.3-p0/blob/master/ext/coverage/coverage.c
* web app that crawls site and finds common errors like mixed content warnings, missing images, broken links, etc, etc
* crawler to find dead CSS
* crawler to find dead JS
* counters app, just tiny up down counters users can create and increment with icons and images private / public, user only or public can increment / decrement

Posts for API reviews
===

* review https://www.codeship.io/
* review nitrous.io 
* review some of the online schools / code academy
* review travis CI
* review https://kraken.io/ image optimization
* review/try http://www.iron.io/ possibly to make ebook https://github.com/harrisj/iron_ebooks 
* Blog post on some work related to the "[ruby-6] Metaprogramming challenge" search email for details but
    * New Relic is looking for another "Ruby Instrumentation Engineer" chellange
    * https://gist.github.com/3631742
    
          Your challenge, should you choose to accept it, is to write a Ruby library that will modify an existing program to output the number of times a specific method is called. 

          You solution library should be required at the top of the host program, or via ruby's -r flag (i.e. ruby -r ./solution.rb host_program.rb)

          Your solution library should read the environment variable COUNT_CALLS_TO to determine the method it should count.  Valid method signatures are Array#map!, ActiveRecord::Base#find, Base64.encode64, etc.

          Your solution library should count calls to that method, and print the method signature and the number of times it was called when the program exits.

          Also, your solution should have a minimal impact on the program's running time.  Sorry set_trace_func"
 
Solved past Ideas
===

* [churn as a tiny app / service run on deferred-servers](http://churn.picoappz.com), I ended up completing this project.
* Better local development environment configuration: 
  * One problem with database.yml if the development configuration file is checked it, it really can't be used for local environment configuration, allow for local overrides. All systems will not be setup the same
  * How to allow better overrides for multiple systems different dev configurations possibly different server deployments?
  * Looks like best solution is [figaro rails configuration](https://github.com/laserlemon/figaro)
* Tiny micro services from people, this is pretty cool [fiverr](http://fiverr.com/)
* Code language detection https://help.github.com/articles/my-repository-is-marked-as-the-wrong-language, I could use this for churn language detection and possibly to break down % of a file that is html, js, CSS