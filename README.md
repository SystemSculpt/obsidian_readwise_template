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
- I like to keep things simple and to-the-point. I want to understand the different sections that I am importing in, and (for now) it seems like Highlights are the only thing that can be synced through Obsidian from Readwise, but I'm hoping that will change sometime soon if, for example, I want to import the entire article/tweet AS WELL as the highlights. That would be a killer feature to add.


Highlight:
```
> [!tldr]- {{ highlight_text }} {% if highlight_location_url %} [🔗]({{highlight_location_url}}){% endif %}
{% if highlight_note %}>> [!info] 📝 **Mike's Note**:
{{ highlight_note }}
{% endif %}
```
- This is how I'm setting up my specific highlights - I use callouts to make them look nice instead of just boring text, and it's easy to create these extendable/clickable windows all natively within Obsidian so that I can easily see the main idea of the tweet and expand it if I want to read up more.
- [More details about callouts and how they work here.](https://help.obsidian.md/Editing+and+formatting/Callouts)

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

## Support

- Your support helps me, Mike, dedicate more time to creating and refining.

<p>
  <a href="https://www.patreon.com/SystemSculpt">
    <img
      align="left"
      src="https://indigenousx.com.au/wp-content/uploads/2017/03/patreon-medium-button.png"
      height="50"
      width="210"
      alt="Support on Patreon"
  /></a>
  <a href="https://www.buymeacoffee.com/SystemSculpt">
    <img
      align="left"
      src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png"
      height="50"
      width="210"
      alt="Buy Me A Coffee"
  /></a>
</p>
<br /><br />
