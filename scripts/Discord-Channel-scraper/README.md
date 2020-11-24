# Discord Channel Scraper

This simple script logs in the user and scrapes up to `--limit` messages from a specified channel. There are a variety of features included to allow for different usecases.

## Requires
- [Rapptz's discord python API](https://github.com/Rapptz/discord.py)
  - Available through pip:
  ```bash
  pip3 install -U discord.py
  ```
  **See official documentation for further installation instructions**

## Usage

```
$ python3.5 scrape-logs.py --help
```
```
usage: scrape-logs.py [-h] [--username USERNAME] [--flag FLAG] [--quiet]
                      [--server SERVER] [--channel CHANNEL] [--limit LIMIT]
                      [--output OUTPUT] [--logging {10,20,30,40,50}]
                      [--format FORMAT] [--dl_attachments] [--dl_emoji]
                      [--skip_messages]

Scrapes messages from a Discord channel.

optional arguments:
  -h, --help            show this help message and exit
  --username USERNAME, -u USERNAME
                        Username to login under. If not specified, username
                        will be prompted for.
  --flag FLAG, -f FLAG  An alternative to specifying the server and channel,
                        specify a piece of regex which when matched against a
                        message sent by the target user, will trigger scraping
                        of the channel the message was posted in. Useful for
                        private messages and private chats. Default value is
                        "!yank", activates by default if no server is
                        specified.
  --quiet, -q           Suppress messages in Discord
  --server SERVER, --guild SERVER, -s SERVER
                        Discord server name to scrape from (user must be a
                        member of the server and have history privileges).
                        This field is case sensitive. If channel is not
                        specified the entire server will be scraped.
  --channel CHANNEL, -c CHANNEL
                        Discord channel name to scrape from (user must have
                        history privileges for the particular channel). This
                        field is case sensitive.
  --limit LIMIT, -l LIMIT
                        Number of messages to save. Default is 1000000
  --output OUTPUT, -o OUTPUT
                        Outputs all messages into a single file. If not
                        specified, messages are saved under the format:
                        <channel name>.txt.
  --logging {10,20,30,40,50}
                        Change the logging level. Defaults to 20, info.
  --format FORMAT, -F FORMAT
                        Message format (plain|json)
  --dl_attachments, -a  Download attachments
  --dl_emoji, -e        Download emoji
  --skip_messages, -S   Skip logging messages
```

## Future plans

- [ ]: Add 2FA support

