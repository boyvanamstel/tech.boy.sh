# tech.boy.sh

This is [where I write about tech stuff](https://tech.boy.sh). It uses [Jekyll](https://jekyllrb.com/) with the default theme.

I try to keep this site straightforward and easy to maintain.

## Development

Here's how to get the project up and running.

### Installing dependencies

The only requirements are listed in the `Gemfile`.

```bash
$ bundle install
```

### Running the project

```bash
$ bundle exec rake serve
```

## Deployment

Deploying the site builds it with the `JEKYLL_ENV` environment variable set to `production`. It then gets the remote path from the `REMOTE_PATH` environment variable and uses `rsync` to copy the files over.

```bash
$ bundle exec rake deploy
```

### Setting the `REMOTE_PATH`

You could add it the command each time you run it:

```bash
$ REMOTE_PATH=account@example.com:/some/path bundle exec jekyll deploy
```

A more convenient solution would be to create a `.env` file and store the path there:

```bash
$ echo 'REMOTE_PATH=account@example.com:/some/path' >> .env
```

After that, just run:

```bash
$ bundle exec jekyll deploy
```
