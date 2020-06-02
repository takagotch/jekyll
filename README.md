### jekyll
---

https://jekyllrb.com/
https://jekyllrb-ja.github.io/

https://github.com/jekyll/jekyll

https://jekylltips-ja.github.io/templates/
https://jekyllrb-ja.github.io/docs/structure/

https://help.github.com/ja/github/working-with-github-pages/creating-a-github-pages-site-with-jekyll



```
gem install jekyll
jekyll new app
cd app
jekyll serve
curl http://localhost:4000

gem install jekyll
gem install jekyll --pre
gem install jekyll -v '2.0.0.alpha.1'
git clone git@github.com/jekyll/jekyll.git
cd jekyll
script/bootstrap
bundle exec rake build
ls pkg/*.gem | head -n 1 |xargs gem install -l

jekyll build
jekyll build --destination <destination>
jekyll build --source <source> --destination <destination>
jekyll build --watch

jekyll server
curl http://localhost:4000/
jekyll serve --detach
jekyll serve --watch

vi _config.yml
jekyll build
jekyll build --source _source --destination _deploy


https://github.com/takagotch/jekyll/tree/master/jekyll_ex

```

https://github.com/github/pages-gem

```
```

