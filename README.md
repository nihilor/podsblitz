# podsblitz

Generates RSS feeds from local audio files to serve the feed via and files via Github pages and other static file hosters.

## How it works

It's simple. Just place the podcast media file in the `media` directory. Add a file of the same filename as the podcast media file, but use the file ending `md`. Then store all the relevant meta information in the Markdown file. Use the YAML frontmatter to provide structured data and the content area of the Markdown file to add a longer description.

For example:

```
./media/2019-09-06_my-first-podcast.mp3
./media/2019-09-06_my-first-podcast.md
```

If you want to add an image as a thumbnail or cover art for services like Soundcloud, use the same filename as the podcast file, but with an ending `jpg` or `png`.

```
./media/2019-09-06_my-first-podcast.mp3
./media/2019-09-06_my-first-podcast.md
./media/2019-09-06_my-first-podcast.jpg
```

Finally run `npm publish`. Podsblitz will read the `media` directory and automatically builds a RSS feed. This feed and a copy of all the media files will be stored under `docs`.

