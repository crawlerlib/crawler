# Crawler

Crawls a website and does something with the URLs. By default it will output each URL on a single line in a txt file.

This could fairly easily be extended to do many other things. You would just need to create a new Observer (`src/Observer`)

## install
`composer require imarc/crawler`

## usage
From your project's directory: `./vendor/bin/crawler csv URL DESTINATION`

From the repo: `./crawler.php csv URL DESTINATION`

## options
`crawler --help`
```
Usage:
  csv [options] [--] <url> <destination>

Arguments:
  url                    URL to crawl.
  destination            Write CSV to FILE

Options:
  -s, --show-progress    Show the crawl's progress
  -e, --crawl-external   Crawl external URLs
  -q, --quiet            Do not output any message
      --exclude=EXCLUDE  Exclude certain extensions [default: ["css","gif","ico","jpg","jpg","js","pdf","pdf","png","rss","txt"]] (multiple values allowed)
  -h, --help             Display this help message
  -V, --version          Display this application version
      --ansi             Force ANSI output
      --no-ansi          Disable ANSI output
  -n, --no-interaction   Do not ask any interactive question
  -v|vv|vvv, --verbose   Increase the verbosity of messages: 1 for normal output, 2 for more verbose output and 3 for debug
```

## tests

`codecept run`
