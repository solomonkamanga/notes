# Create Jekyll Site

## Requirements

- Install Ruby Development environemnt: 


## Install Bundler

```
$ gem install bundler
# Installs the Bundler gem
```

## Create a local repository for your Jekyll site

1. Open Git Bash.

2. On your local computer, initialize a new Git repository for your Jekyll site:

    ```
    $ git init JEKYLL-SITE-REPOSITORY-NAME
    > Initialized empty Git repository in /Users/octocat/my-site/.git/
    # Creates a new file directory on your local computer, initialized as a Git repository
    ```

3. Change directories to the new repository you created:
   
   ```
    $ cd JEKYLL-SITE-REPOSITORY-NAME
    # Changes the working directory
   ```

## Install Jekyll using Bundler

1. If you don't have a Gemfile, and add these lines to a new file:

    ```
    source 'https://rubygems.org'
    gem 'github-pages', group: :jekyll_plugins
    ```

2. Name the file `Gemfile` and save it to the root directory of your local Jekyll site repository. Skip to step 5 to install Jekyll.

3. Install Jekyll and other dependencies from the GitHub Pages gem:

    ```
    $ bundle install
    > Fetching gem metadata from https://rubygems.org/............
    > Fetching version metadata from https://rubygems.org/...
    > Fetching dependency metadata from https://rubygems.org/..
    > Resolving dependencies...
    ```

## Generate Jekyll site files (in exsiting folder)

1. Navigate into your new site directory:

    ```
    $ cd NEW-JEKYLL-SITE-REPOSITORY-NAME
    ```

2. Create a Jekyll template site in a existing directory:
   
    ```
    $ bundle exec jekyll _3.3.0_ new . --force
    ```

3. Edit your Gemfile and remove the following line:

    ```
    $ "jekyll", VESRION_NUMBER
    # VERSION_NUMBER is the actual of Jekyll you are using. Should be a number is double quotes.
    ``` 

4. Run `bundle install` to initiate changes made to `Gemfile`.

## Build your local Jekyll site

1. If you are not already there, navigate into the **root directory** of your local Jekyll site repository.

    ```
    $ cd JEKYLL-SITE-REPOSITORY-NAME
    # Changes the working directory
    ```

2. Run your Jekyll site locally:

    ```
    $ bundle exec jekyll serve
    > Configuration file: /Users/octocat/my-site/_config.yml
    >            Source: /Users/octocat/my-site
    >       Destination: /Users/octocat/my-site/_site
    > Incremental build: disabled. Enable with --incremental
    >      Generating...
    >                    done in 0.309 seconds.
    > Auto-regeneration: enabled for '/Users/octocat/my-site'
    > Configuration file: /Users/octocat/my-site/_config.yml
    >    Server address: http://127.0.0.1:4000/
    >  Server running... press ctrl-c to stop.
    ```

## Keeping your site up to date with the GitHub Pages gem

1. simply `bundle update` and all your gems will update to the latest versions.