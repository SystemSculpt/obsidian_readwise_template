Useful Links:
- [The Readwise Obsidian Preferences link](https://readwise.io/export/obsidian/preferences)
- [Readwise Syncing (I sync my Twitter as well as my Reader profiles)](https://readwise.io/welcome/sync)
- [Readwise Exporting to Obsidian](https://readwise.io/export)

Group files in category folders:
- I don't use this feature because my note-taking system is based on the [Zettelkasten System.](https://zettelkasten.de/introduction/)
- That means every new article/tweet/piece of content from Readwise/Reader is placed in my Readwise directory.

File name:
```
{{date}} - {{title}}
```

Page title:
- I leave this blank because I find it redundant to have two titles present (the file name includes the title).

Page metadata:
- I leave this blank because any metadata that I want for my imported content will be inserted into the front matter (down below), which lets me search through / utilize dataview / scripting much more effectively instead of having important searchable details within the file's body.

Highlights header:
```
# Highlights
```

Highlight:
```
> [!tldr]- {{ highlight_text }} {% if highlight_location_url %} [🔗]({{highlight_location_url}}){% endif %}
{% if highlight_note %}>> [!info] 📝 **Mike's Note**:
{{ highlight_note }}
{% endif %}
```

YAML front matter:
```
{% if author %}author: "[[{{author}}]]"{% endif %}
{% if url -%}
source: {{url}}
{% endif -%}
date: {{date}}
discussed: false
```

Sync notification:
```
- [[{{date|date('Y-m-d')}}]] {{time}} — Synced {{num_highlights}} highlight{{num_highlights|pluralize}} from {{num_books}} document{{num_books|pluralize}}.
{% for book in books %}    - {{ book.num_highlights_added}} highlights from {{ book.title }}
{% endfor %}
```