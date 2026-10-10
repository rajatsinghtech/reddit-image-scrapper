> Written manually, without AI assistance.

# Reddit Image Scrapper

## What this does

A Python class that scrapes images from any subreddit of reddit.com into a
local folder.

## Business process

Point it at a subreddit page; it scrolls the infinite-scroll listing the
requested number of times and downloads every image it finds â€” bulk dataset
collection without manual saving.

## Technical flow

One class ([`reddit_image_scrapper.py`](reddit_image_scrapper.py)) drives a
browser-style scroll loop, collects image URLs from the loaded page, and
writes the files to disk. Three parameters control it:

1. `Folder_path` â€” where to save the downloaded images
2. `Num_scrolls` â€” how many full-page scrolls to perform (more scrolls =
   more images loaded)
3. `Page_link` â€” the subreddit page URL
