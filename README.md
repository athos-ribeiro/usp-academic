## What is this?

This is the repository for my academic website.

You can find it at www.ime.usp.br/~athoscr

Parts of this page are duplicated in my personal blog at athoscr.me

## How did you do it?

I am using [Hugo](http://gohugo.io/) based on [this](https://github.com/consequently/consequently-hugo) template.

## Deploying

I also have the following line in ./git/hooks/pre-push

```
rsync -avz --delete --exclude=papers --exclude=files public/ $SITE_SERVER:$SITE_PATH
```

so each time a modification is made the files are updated in the production server. Note that having this in a pre-push hook may not be a good idea in other contexts.

