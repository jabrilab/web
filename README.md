# How to run a copy of this website locally

You can run a local version of this website to see how your changes will look like when they are pushed. For this, you need to install `jekyll`, which can be doen the following way on a Mac OSX:

```
sudo gem install jekyll
```

If the command `gem` is not found, or your Ruby version is outdated, try to install it the following way first:

```
brew install ruby
```

Once the installation is complete, you can get a copy of the web site from GitHub:

```
git clone https://github.com/jabrilab/web.git
cd web
```

To make sure you have the necesary gems, run:

```
bundle install
```

And run the following command in this directory:

```
bundle exec jekyll serve --incremental
```

You should see a similar output in your terminal:

```
Configuration file: .../web/_config.yml
Configuration file: .../web/_config.yml
            Source: .../web
       Destination: .../web/_site
 Incremental build: enabled
      Generating...
                    done in 6.585 seconds.
 Auto-regeneration: enabled for 'web'
Configuration file: /Users/evan/Software/web/_config.yml
    Server address: http://127.0.0.1:4000/
  Server running... press ctrl-c to stop.
```

This basically runs a local server for you to see the changes you've made locally. You can access to this server by visiting the URL `http://127.0.0.1:4000/` with your browser.

With the `--incremental` flag every change you will make in any of the files will be reflected to your local website automatically.

If you are not seeing some of the changes you expect to see, press `ctrl-c` to stop the server on your termianl, clean out the static web directory by running the command `rm -rf _site/`, and re-run the server using the command above.

When you make changes to the contents of this page and you are satisfied with these changes, you can commit them tothe main repository:

```
git add .
git commit -m "name upgrade"
git push origin master
```

Please note that it will take some time for changes to appear.

I suggest you to use MacDown to edit markdown files (if you're using a Mac computer), and GitHub Desktop to manage your commits to the repository.
