# wintersmith-static-comments

## Usage

1. Add this repository as a `submodule` within your `templates` directory
2. Add an email in `config.json` with the key `comment_email`

        "locals": {
          ...
          "comment_email": "comment@example.com"
        }

3. Include `wintersmith-static-comments/comments.jade` in your main template
4. Create a directory tree within your `contents` directory in the form:

        comments
        |-- [post-url]
        |   `-- 01.txt
        `-- [post2-url]
            |-- 01.txt
            `-- 02.txt

... where `01.txt`, `02.txt`, etc. are plain-text files in chronological order
with some leading metadata, e.g.:

    name: Tom Vincent
    date: 2011-04-07T19:18:06
    url: http://tlvince.com

    An insightful comment.

The only mandatory metadata keys are `name` and `date`; arbitrary keys can
later be accessed in the template.

## Author

Copyright 2012 Tom Vincent <http://tlvince.com/contact>

## License

Released under the [MIT License][license].

  [license]: http://tlvince.mit-license.org/
