# Category list plugin for Jekyll 
This  plugin was referred to [Octopress - Category List Plug-in](http://www.dotnetguy.co.uk/post/2012/06/25/jekyll-category-list-plugin/).

## How to install

### Get dependency package

    cd /path/to/jekyll

    vi Gemfile

    + gem 'stringex'

    bundle install --path vendor/bundle

or by gem command

    gem install amazon-ecs i18n
### Get category_list_tag.rb

    cd /path/to/plugins
    wget https://raw.github.com/longkey1/jekyll-category-list-plugin/master/category_list_tag.rb


or by git-submodule

    cd /path/to/jekyll
    git submodule add git://github.com/longkey1/jekyll-category-list-plugin.git _plugins/category-list


### Create category list template file

    example: category_list.html

    vi /path/to/jekyll/_includes/category_list.html

    + <section>
    +   <h1>Categories</h1>
    +   <ul id="categories">
    +     {% category_list %}
    +   </ul>
    + </section>


### Build

    cd /path/to/jekyll
    jekyll build
