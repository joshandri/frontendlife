---
layout: post
title:  "How to install jekyll on windows"
date:   2013-09-01 17:21:07
category: articles
tags: [jekyll]
comments: true
---

#Installation
1. Install [RubyInstaller][ruby-inst]. (I used version 1.9.2-p290).  
2. Install [DevKit][ruby-inst] (I used version DevKit-tdm-32-4.5.2-20111229-1559-sfx.exe) during the execution of the file be sure to customise the install path in the ruby path.( e.g  C:\Ruby193\Devkit\).  
3. To install the "Development Kit" run "Start Command Prompt with Ruby" and execute:  
`c:\Ruby193\Devkit\ruby dk.rb init`  
`c:\Ruby193\Devkit\ruby dk.rb install`
4. At this time Rubygems is installed, install Jekyll with this command:
	`c:\Ruby193\gem install jekyll`  
5. Install an another gem : rdiscount  
`c:\Ruby193\gem install rdiscount`  
RDiscount is a fast implementation of markdown in C.
    
#Test
1. Run the "Start Command Prompt with Ruby". 
2. Go to your work directory e.g `c:\myrep` , here "myblog" is the new repository of the blog and enter:  
`c:\myrep\jekyll new myblog`  
`c:\myrep\cd myblog`
3. Before to run the server enter this two command to avoid incompatible character encodings error:  
`c:\myrep\myblog\set LC_ALL=en_US.UTF-8`  
`c:\myrep\myblog\set LANG=en_US.UTF-8`  
And open the _config.yml to change the variable pygments to false  Pygments is a Python based syntax highlighter.  
You do not need to install Pygments if you do not plan on posting code snippets on your website.  
You must install python tu use it.  
4. To run the server:  `c:\myrep\myblog\jekyll serve`  
Now browse to `http://localhost:4000` to see your site.  
Or Enter `jekyll serve --watch` to build your site and launch a web server that rebuilds your site every time you save in your editor.
    
Check out the [Jekyll docs][jekyll] for more info on how to get the most out of Jekyll. 
File all bugs/feature requests at [Jekyll's GitHub repo][jekyll-gh].  
Look at : [Jekyll blog list][jekyll-ls] to see many examples of blog with jekyll. 

[jekyll-gh]: https://github.com/mojombo/jekyll
[jekyll]:    http://jekyllrb.com
[ruby-inst]: http://rubyinstaller.org/downloads
[jekyll-ls]: https://github.com/mojombo/Jekyll/wiki/Sites