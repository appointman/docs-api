Getting Started
------------------------------

Slate (this repo is forked from it) and widdershins is used to convert swagger api documentation into html website.

https://github.com/Mermade/widdershins

```shell
sudo npm install -g widdershins
```

### Generate from swagger endpoint

```shell
widdershins http://localhost:7080/v2/api-docs -o ./source/includes/_api.md --summary
```

### Run locally

Initialize and start Slate. You can either do this locally, or with Vagrant:

```shell
# either run this to run locally
bundle install
bundle exec middleman server

# OR run this to run with vagrant
vagrant up
```

You can now see the docs at http://localhost:4567. Whoa! That was fast!

Now that Slate is all set up on your machine, you'll probably want to learn more about [editing Slate markdown](https://github.com/lord/slate/wiki/Markdown-Syntax), or [how to publish your docs](https://github.com/lord/slate/wiki/Deploying-Slate).

### Deploy to github pages

```shell
. deploy.sh
```