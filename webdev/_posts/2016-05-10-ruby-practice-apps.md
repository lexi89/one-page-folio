---
title: The "2 Rails Apps / Week" Journal

---
This page documents my progress towards Ruby on Rails mastery.

The purpose of this is to expose myself to as much Rails code as possible, practice research & planning, and documenting. As a by-product, I will create a portfolio of live mini-apps, be able to see how far I've come, and expose the bullshit monkey-mind insecurities that come up in the process.

The format of the exercise is this:

*Day 1*: Decide on a feature to explore. Document the plan and research.

*Day 2*: Build and deploy the demo app to Heroku.

*Day 3*: Document reflections and add demo-app to potfolio listing.

***

### Resources for checking out features:

[Gorails](https://gorails.com/)

[Railscasts Reloaded](https://www.youtube.com/user/RailscastsReloaded)

### Templates

HTML5 boilerplate?
Bootstrap template?

***

# #1 — Twitter API practice

### Le Plan

Connect to API with the [Twitter Gem](https://github.com/sferik/twitter)

Find interesting tweets and write down the code snippets next to the results.

Ideas:

- The last 3 tweets about Trump.
- Funniest joke of the day (most retweeted / favourited?)
- Quote of the day (most retweeted / favourited?)
- Top 3 news stories in the UK
- Most retweeted thing in the whole of Twitter?

Style with Bootstrap & jQuery

Extras: Try using [livereload](https://github.com/guard/guard-livereload) to improve workflow

### Learnings & docs

***

# #2 — News media headline analyzer

_Plan_
Scrape x number of new sites for headlines with Mechanize / Nokogiri

Save to database a sentiment and a sentiment score from the sentimental gem for each headline.

Display how positive / negative each media outlet is.

Optional: heatmap of negative / positive by score.

_Learnings & docs_
