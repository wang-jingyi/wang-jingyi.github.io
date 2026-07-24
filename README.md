# wang-jingyi.github.io

A Jekyll site. GitHub Pages builds Jekyll for you, so there is no CI to set up
and nothing to install: **edit a file, commit, push, and the site rebuilds in
about a minute.** You can do all of it in the GitHub web editor from a phone
if you want.

## Where things live

```
_config.yml              your name, role, photo, contact links, nav
_data/publications.yml   every paper
_data/books.yml          books and edited volumes
_data/themes.yml         the research themes
index.md                 home page
service.md               service and talks
vac.md                   openings
pubs.html                generated from the data files — you never edit this
_layouts/, _includes/    the templates
assets/style.css         all styling
assets/photo.jpg         your photo
```

Prose lives in markdown. Anything that repeats with the same shape — papers,
themes — lives in a data file instead, because a list of fields is easier to
append to than a wall of HTML, and it lets one paper appear correctly in the
list, the filter and the counts without you touching three places.

## Adding a paper

Open `_data/publications.yml` and add an entry. Order does not matter; the
site groups and sorts by year itself.

```yaml
- year: 2026
  venue: ICSE
  tier: CCF A
  theme: se4ai
  title: The title of the paper
  authors: Some Coauthor, **Jingyi Wang***, and Another Coauthor
  note: 48th International Conference on Software Engineering, Apr 2026
  links:
    - name: paper
      url: https://example.com/paper
    - name: code
      url: https://github.com/example/repo
```

Only `year`, `venue`, `theme`, `title` and `authors` are required. Wrap your
own name in `**` to bold it. `theme` must be one of the ids in
`_data/themes.yml` — currently `fm`, `se4ai` or `ai4se`.

A new year needs nothing special. Add a 2027 paper and a 2027 heading appears.

## Changing the research themes

Edit `_data/themes.yml`. Renaming a theme updates the home page, the openings
page and the filter buttons together. To add a fourth theme, give it an `id`,
`tag`, `filter`, `name` and `blurb`, then start putting that id in papers'
`theme:` fields.

To split SE4AI back out into a separate safety theme later, add the theme here
and change `theme: se4ai` to the new id on the papers that belong to it.

## Editing the prose pages

`index.md`, `service.md` and `vac.md` are ordinary markdown. Two conventions
beyond plain markdown are worth knowing, both standard kramdown:

A two-column year row is a definition list — the term becomes the left
column:

```markdown
2026
: ICFEM (PC co-chair), ACM CCS, ASE
```

A class can be attached to the block above it with `{: .class}`. The site uses
`{: .lede}` for an opening paragraph, `{: .note}` for small grey text, and
`{: .plain}` for a list with hairline rules instead of bullets.

## Your photo

Replace `assets/photo.jpg`, keeping the filename. Square, 400×400 px or
larger. It is cropped to a circle in CSS. To use a different filename, point
`photo:` in `_config.yml` at it.

## Contact and social links

`profile_links` in `_config.yml`. Google Scholar, DBLP and GitHub entries are
there, commented out — uncomment and fill in your ids.

## Colours and type

The `:root` block at the top of `assets/style.css`. `--accent` is the deep
teal on links and theme tags; change that one value to re-tint the site. Dark
mode is defined just below and follows the reader's system setting.

## Previewing locally (optional)

Not required — pushing is a fine way to preview. But if you want a local loop:

```
bundle install
bundle exec jekyll serve
```

then open http://localhost:4000. The `Gemfile` pins the same versions GitHub
Pages runs.

## One thing to watch

Do not add a `.nojekyll` file to this repository. It tells GitHub Pages to
skip the Jekyll build, which would serve these markdown files as raw text.
