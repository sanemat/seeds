# Smarty OR Plain PHP OR any template-engine ?
## by oneself OR separation

!SLIDE
# template engine?
"Smarty already exists."  
"Plain PHP is good template engine."  

!SLIDE
YES

!SLIDE
# agenda
* various template-engine
* requirement depend on purpose
    * by oneself?
    * separation?
* Smarty

!SLIDE
# self introduction
* murahashi kenichi (a.k.a sanemat)
* web programmer
* use
    * ruby
        * Ruby Association Certified Ruby Programmer Silver
    * php
* love
    * ruby on rails
    * cakephp
    * yet another micro framework
        * sinatra (ruby)
        * limonade (php)

!SLIDE
# various template-engine (my interest)
* [Smarty](http://www.smarty.net/)
* [Plain PHP](http://www.php.net/)
* [Tenjin](http://www.kuwata-lab.com/tenjin/)
* [Caty](http://bitbucket.org/m_hiyama/caty-python-proto1/)
* [Haml](http://haml-lang.com/)
* [Django](http://www.djangoproject.com/)
* [PHPTAL](http://phptal.org/)
* [Twig](http://www.twig-project.org/)
* [Template::Toolkit](http://search.cpan.org/dist/Template-Toolkit/)
* [rhaco](http://rhaco.org/)
* [Text::MicroTemplate](http://search.cpan.org/dist/Text-MicroTemplate/)
* [Text::MicroTemplate::Extended](http://search.cpan.org/dist/Text-MicroTemplate-Extended/)
* [wicket](http://wicket.apache.org/)

!SLIDE
# why do you use tempate-engine?
separate business-logic from view  
useful functions  
speed(user experience) on compiled (no mention)  
speed(coding) by less typing  
concentrate on importance  
all! all! all!

!SLIDE
all-in-one template-engine becomes *too* big.  
too big template-engine *close* to PHP, but *not* PHP.  
it's crazy.  

!SLIDE
#Programmer by oneself
DRY

!SLIDE code
haml example via [日本hamlの会](http://haml.ursm.jp/)  
    !!! XML
    !!! 1.1
    %html{:xmlns => 'http://www.w3.org/1999/xhtml'}
      %head
        %title Hello, Haml!
      %body
        #header
          %h1 Hello, Haml!
        #content
          %p
            I use Haml
            %span.version= Haml::VERSION

!SLIDE code
haml example via [日本hamlの会](http://haml.ursm.jp/)  
    <?xml version='1.0' encoding='utf-8' ?>
    <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.1//EN" "http://www.w3.org/TR/xhtml11/DTD/xhtml11.dtd">
    <html xmlns='http://www.w3.org/1999/xhtml'>
      <head>
        <title>Hello, Haml!</title>
      </head>
      <body>
        <div id='header'>
          <h1>Hello, Haml!</h1>
        </div>
        <div id='content'>
          <p>
            I use Haml
            <span class='version'>2.2.14 (Powerful Penny)</span>
          </p>
        </div>
      </body>
    </html>

!SLIDE
No complex HTML & CSS

!SLIDE
Template inheritance

!SLIDE code
django example via [Django テンプレート言語 ― Django v1.0 documentation](http://djangoproject.jp/doc/ja/1.0/topics/templates.html)  
(base.html)  
    <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
        "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
    <html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
    <head>
        <link rel="stylesheet" href="style.css" />
        <title>{% block title %}My amazing site{% endblock %}</title>
    </head>
    
    <body>
        <div id="sidebar">
            {% block sidebar %}
            <ul>
                <li><a href="/">Home</a></li>
                <li><a href="/blog/">Blog</a></li>
            </ul>
            {% endblock %}
        </div>
    
        <div id="content">
            {% block content %}{% endblock %}
        </div>
    </body>
    </html>

!SLIDE code
django example via [Django テンプレート言語 ― Django v1.0 documentation](http://djangoproject.jp/doc/ja/1.0/topics/templates.html)  
(base_SECTIONNAME.html)  
    {% extends "base.html" %}
    
    {% block title %}My amazing blog{% endblock %}
    
    {% block content %}
    {% for entry in blog_entries %}
        <h2>{{ entry.title }}</h2>
        <p>{{ entry.body }}</p>
    {% endfor %}
    {% endblock %}

!SLIDE code
django example via [Django テンプレート言語 ― Django v1.0 documentation](http://djangoproject.jp/doc/ja/1.0/topics/templates.html)  
    <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
        "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
    <html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
    <head>
        <link rel="stylesheet" href="style.css" />
        <title>My amazing blog</title>
    </head>
    
    <body>
        <div id="sidebar">
            <ul>
                <li><a href="/">Home</a></li>
                <li><a href="/blog/">Blog</a></li>
            </ul>
        </div>
    
        <div id="content">
            <h2>Entry one</h2>
            <p>This is my first entry.</p>
    
            <h2>Entry two</h2>
            <p>This is my second entry.</p>
        </div>
    </body>
    </html>


!SLIDE
Testable

Ajax & HTML5
toward ExtJS
PHP template engine?

!SLIDE
Separation

Sandbox
default html-escaped
responsibility
dreamweaver-friendly

template engine?

!SLIDE
#Smarty
PHPer also use framework.  
big framework has own template engine.  
cakephp have plain php and helper class.  
if framework have plugin system, it only for one framework.  
Smarty however, work with many framework know-how bad way.  
ANd how to use with smarty knowledge is shared.  
Like QuickForm.  

!SLIDE
# tutorial resource in japanese
* [Catyスクリプト：まだ出来てないけどチュートリアル - 檜山正幸のキマイラ飼育記](http://d.hatena.ne.jp/m-hiyama/20090907/1252284661)
* [日本Hamlの会](http://haml.ursm.jp/)
* [面白ラボBM11(ブッコミイレブン) 2009: Text::MicroTemplate::Extended](http://bm11.kayac.com/2009/project/text-microtemplate-extended/)
* [Django テンプレート言語 ― Django v1.0 documentation](http://djangoproject.jp/doc/ja/1.0/topics/templates.html)

!SLIDE
# template engine?
"Smarty already exists."  
"Plain PHP is good template engine."

!SLIDE
YES

!SLIDE
# but think thing that is focused on!
contact me  
sanemat  
[web site](http://sane.jp/)  
[weblog](http://sane.justblog.jp/)  
[twitter:sanemat](http://twitter.com/sanemat)  
[github:sanemat](http://github.com/sanemat)  
