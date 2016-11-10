# jekyll installeren

```
sudo apt-get install ruby-full
sudo apt-get install g++
sudo apt-get install zlib1g-dev

sudo gem install bundle
sudo gem install jekyll
```

# jekyll gebruiken in een bestaande github-pages repo

Werkwijze:

- Maak een `index.md` in je repo met front-matter `layout: default`
- Zet een `_config.yml` in je repo (zie b.v. de file in deze repo)
- Zet een template in `_layout/default.html`

Om met Jekyll ook lokaal (d.w.z. niet op GitHub Pages) dezelfde repo te kunnen gebruiken:

- Zet een `Gemfile` in je repo. Hierin staan de gems die jekyll nodig heeft om een lokale (development) server te starten.

```
source 'https://rubygems.org'
gem 'github-pages', group: :jekyll_plugins
gem 'execjs'
gem 'therubyracer'
```

- Doe `bundle install` om alle gems te installeren
- Doe `bundle exec jekyll serve` om de jekyll server te starten
