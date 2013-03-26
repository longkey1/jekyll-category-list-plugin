# Category list plugin for Octopress
This  plugin was referred to [Octopress - Category List Plug-in](http://www.dotnetguy.co.uk/post/2012/06/25/octopress-category-list-plugin/).

## How to install

### Get category_list_tag.rb

    cd plugins
    wget https://raw.github.com/longkey1/octopress-category-list-plugin/master/category_list_tag.rb


or by git-submodule

    cd /path/to/octopress
    git submodule add git://github.com/longkey1/octopress-category-list-plugin.git plugins/category-list


### Create category list template file

    example: category_list.html

    vi /path/to/octopress/source/_includes/asides/category_list.html

    + <section>
    +   <h1>Categories</h1>
    +   <ul id="categories">
    +     {% category_list %}
    +   </ul>
    + </section>


### Add new sides template in _config.yml

    vi /path/to/octopress/_config.yml

    - default_asides: [asides/recent_posts.html, asides/github.html, asides/twitter.html, asides/delicious.html, asides/pinboard.html, asides/googleplus.html]
    + default_asides: [custom/asides/category_list.html, asides/recent_posts.html, asides/github.html, asides/twitter.html, asides/delicious.html, asides/pinboard.html, asides/googleplus.html]


### Generate

    cd /path/to/octopress
    rake generate
