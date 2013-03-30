---
layout: 2012-01-08-octopress
title: "Make a blog use octopress"
thumb: "/assets/images/posts/2012-01-08-octopress.png"
date: 2012-01-08 13:02
comments: true
categories: 
---

这是一个变革的时代，web开发正在逐渐跨入一个新的境地。过去我们使用Ruby On Rails最让人兴奋的是ActiveRecord提供的简单但有点神奇的接口，但随着Rails3.1 Asset Pipeline<sup class="footnote"><a href="#fn1">1</a></sup>的发布，js,css正式成为了一等公民。我们越来越多开始遇到Rails提供API，前端HTML5 + CSS3 + Heavy  JS的App。

这是一个很让人兴奋的改变，同时发生的是Hacker/Geeker们开始研究新的花样来发布个人网站，记录博客。从wordpress开始
Blog程序一直在发展，但没有本质的改变。2007－2009的时候你打开Rails程序员的博客，十有九是Mephisto<sup class="footnote"><a href="#fn2">2</a></sup>，到现在Rails官方的博客仍然是Mephisto。Mephisto基本上使用Rails写的Wordpress，理念上比较相似，也有挺多Theme，但Rails与生俱来的部署难问题限制了他的发展。Mephisto之后最不错的一个博客软件是Enki<sup class="footnote"><a href="#fn3">3</a></sup>，Enki的目标很简单，就是一个给Developer的博客软件，所以不像Mephisto一样大包大揽，没有太多东西需要配置，“clean, simple, easy to understand code base”，是Enki的哲学。我觉得Enki确实是一个不错的给程序员使用的博客软件，但问题是这已经不是一个写博客的时代了，所以事实上我们没有遇到几个使用Enki的博客。

但Hacker们不是普通的互联网用户，Twitter虽然满足了60％的使用需求，有的时候人们仍然需要通过一篇较长的文字来分享自己对某个技术问题的理解，或者最近做的一些新的尝试，很多时候这些文章促进了技术的发展，我们需要这些文字，也希望那些出色的Hacker们能多多分享。所以大家开始尝试新的记录博客的方法。最成功的就是Jekyll<sup class="footnote"><a href="#fn4">4</a></sup>。

Jekyll是github的创始团队中的[Tom Preston](https://github.com/mojombo)建立的，“Jekyll is a blog-aware, static site generator in Ruby”，静态文件，template driven，可以直接部署到Github Pages<sup class="footnote"><a href="#fn11">11</a></sup>等各种优点让Jekyll成为了最近一俩年Hacker们记录博客的首选。今天我介绍的Octopress<sup class="footnote"><a href="#fn5">5</a></sup>就是完全基于Jekyll的一个blog框架，在Jelyll的基础上增加了默认的html模板，默认的js，css，和一套简单的配置，部署方案。因为Github Pages是使用Jekyll来驱动的，所以使用Octopress也可以直接部署到Github Pages。

从我自己的需求出发，有几个原因选择Octopress而不是其他的开源博客引擎来写blog：

* ruby写的，我可以二次开发
* 静态页面，不要数据库
* 简单部署，不需要自己的host
* 默认支持markdown<sup class="footnote"><a href="#fn6">6</a></sup>
* 默认支持git发布
* 默认支持SCSS<sup class="footnote"><a href="#fn7">7</a></sup>
* 有那么一点挺酷的感觉

Octopress的安装，部署都很简单，默认的主题也不错，很适合想记录一点文字的Developer。但如果需要一个CMS，建立一个简单但是功能完整的站点，有比较多的逻辑需要处理，需要完全制作新的样式，可能Octopress不是最适合的。有很多Ruby Base的CMS，都大同小异，使用最广泛的是Radiant<sup class="footnote"><a href="#fn8">8</a></sup>, Rails官方的站点也是用的他。不过我推荐的是Nestacms<sup class="footnote"><a href="#fn9">9</a></sup>，Nesta是Sinatra<sup class="footnote"><a href="#fn12">12</a></sup>写的，和Octopress很相似，静态页面，支持markdown，支持git发布，但因为是Sinatra Base，扩展起来很方便，加入SCSS,甚至Coffee Script<sup class="footnote"><a href="#fn10">10</a></sup>都很简单。

所以我的结论是，写Blog用Octopress，写一个小站点，用Nesta，唯一麻烦的是需要自己的host。

<div class="refer">
  <h4>参考</h4>

  <p id="fn1"><sub>1</sub> Rails3.1引入了<a href="http://guides.rubyonrails.org/asset_pipeline.html">asset pipeline</a>.</p>

  <p id="fn2"><sub>2</sub> <a href="https://github.com/halorgium/mephisto">mephisto</a> is a Rails implemented Blog System.</p>

  <p id="fn3"><sub>3</sub> <a href="https://github.com/xaviershay/enki">enki</a> is A Ruby on Rails blogging app for the fashionable developer .</p>

  <p id="fn4"><sub>4</sub> <a href="http://jekyllrb.com/">jekyll</a> is a blog-aware, static site generator in Ruby.</p>

  <p id="fn5"><sub>5</sub> <a href="http://octopress.org">octopress</a> is A blogging framework for hackers.</p>

  <p id="fn6"><sub>6</sub> <a href="http://daringfireball.net/projects/markdown/">Markdown</a> is a text-to-HTML conversion tool for web writers.</p>

  <p id="fn7"><sub>7</sub> <a href="http://sass-lang.com/">SCSS</a> makes CSS fun again.</p>

  <p id="fn8"><sub>8</sub> <a href="http://radiantcms.org/">Radiant</a> is a no-fluff, open source content management system designed for small teams.</p>

  <p id="fn9"><sub>9</sub> <a href="https://github.com/gma/nesta">Nesta</a> is A lightweight CMS, implemented in <a href="http://www.sinatrarb.com/">Sinatra</a>.</p>

  <p id="fn10"><sub>10</sub> <a href="http://coffeescript.org/">Coffee Script</a> is a little language that compiles into JavaScript.</p>

  <p id="fn11"><sub>11</sub> <a href="http://pages.github.com/">Github Pages</a> allows you to publish content to the web by simply pushing content to one of your GitHub hosted repositories.</p>  
  
  <p id="fn12"><sub>12</sub> <a href="http://www.sinatrarb.com/">Sinatra</a> is a ruby based lightweight web development framework.</p>

</div>










