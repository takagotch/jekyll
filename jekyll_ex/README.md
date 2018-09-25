#### default
```
source: .
destination: ./_site
plugins: ./_plugins
layouts: ./layouts
include: ['.htaceess']
exclude: []
keep_files: ['.git','.svn']
gems: []
timezone: nil
encoding: nil

future: true
show_drafts: nil
limit_posts: 0
pygents: true

relative_permalinks: true

permalink: date
paginate_path: 'page:num'

markdown: marku
markdown_ext: markdown,mkd,mkdn,md
textile_ext: texttile

except_separator: "\n\n"

safe: false
watch: false
server: 0.0.0.
port: 4000
baseurl: /
url: http://localhost:4000
lsi: false

maruku:
  use_text: false
  use_divs: false
  png_engine: blahtex
  png_dir: images/latex
  png_url: /imgages/latex
  fenced_code_blocks: true
  
rdiscount:
  extensions: []
  
redcarpet: 
  extensions: []
  
kramdown:
  auto_ids: true
  footnote_nr: 1
  entity_output: as_char
  toc_levels: 1..6
  smart_quotes: lsquo,rsquo,ldquo,rdquo
  use_coderay: false
  
  coderay:
    coderay_wrap: div
    coderay_line_numbers: inline
    coderay_line_numbers_start: 1
    coderay_tab_width: 4
    coderay_bold_every: 10
    coderay_css: style
    
  redclosth:
    hard_breaks: true
```
##### Front-matter
```
layout: post
title: Blogging Like a Hacker
```

```
<!DOCTYPE HTML>
<html>
  <head>
    <title>{{ page.title }}</title>
  </head>
  <body>
  ...
```
post
```
YEAR-MONTH-DAY-title.MARKUP
```

```
![SCREENSHOT]({{ site.url }}/assets/screenshot.jpg)
[PDFDOWNLOAD]({{ site.url }}/assets/mydoc.pdf)
```

```
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      {{ post.excerpt }} #{{ post.excerpt | remove: '<p>' | remove: '</p>' }}
    </li>
  {% endfor %}
</ul>
```

```
{% highlight ruby %}
def show
  @widget = Widget(params[:id])
  respond_to do |format|
    format.html # show.html.erb
    format.json { render json: @Wwiget }
  end
end
{% endhighlight %}

#=>
def show
  @widget = Widget(params[:id])
  respond_to do |fromat|
    format.html #show.html.erb
    format.json { render json: @widget }
  end
end

```

```
|-- drafts/
|  |--a-draft-post.md
```

```
.
|-- _config.yml
|-- _includes/
|-- _layouts/
|-- _posts/
|-- _site/
|--about.html # => http://localhost/about.html
|--index.html # => http://localhost/
|-- contact.html # => http://localhost/contact.html


.
|-- _config.yml
|-- _includes/
|-- _layouts/
|-- _posts/
|-- _site/
|-- about/
|  |-- index.html # => http://localhost/about/
|-- contact/
|  |-- index.html # => http://localhost/contact/
|-- index.html # => http://localhost/


```

