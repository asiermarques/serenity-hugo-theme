# Serenity Hugo Theme

A minimalistic theme for your personal blog based on Hugo static site generator.  
This is a port my the deprecated [Gatsby Serenity theme](https://github.com/asiermarques/gatsby-theme-serenity).

## Live demo

I'm using this theme for my personal blog, you can see it live at [blog.asiermarques.com](https://blog.asiermarques.com)

## Installation

There are two ways to install this theme:

### Option 1: Hugo Modules (Recommended)

1. Initialize Hugo Module system in your site if you haven't already:

```bash
hugo mod init github.com/username/your-site-name
```

2. Add the theme to your hugo.toml:

```toml
theme = "github.com/asiermarques/serenity-hugo-theme"

[module]
  [[module.imports]]
    path = "github.com/asiermarques/serenity-hugo-theme"
```

3. Get the theme:

```bash
hugo mod get github.com/asiermarques/serenity-hugo-theme
```

### Option 2: Git Submodule

1. Add the theme as a submodule:

```bash
git submodule add https://github.com/asiermarques/serenity-hugo-theme.git themes/serenity-hugo-theme
```

2. Add the theme to your hugo.toml:

```toml
theme = "serenity-hugo-theme"
```

## Basic Configuration

Add these parameters to your hugo.toml:

```toml
[params]
  description = "Your site description"
  author = "Your Name"

  [params.social]
  github = "https://github.com/yourusername"
  linkedin = "https://linkedin.com/in/yourusername"
  instagram = "https://instagram.com/yourusername"
  mail = "mailto:your@email.com"
  bluesky = "https://bsky.app/profile/yourdomain.com"

[menu]
  [[menu.main]]
    identifier = "home"
    name = "Articles"
    url = "/"
    weight = 1
  [[menu.main]]
    identifier = "about"
    name = "About"
    url = "/about/"
    weight = 2
  [[menu.main]]
    identifier = "rss"
    name = "RSS"
    url = "/index.xml"
    weight = 3
```

## Preview

```bash
hugo server \
--gc \
--source exampleSite \
--config exampleSite/config.toml \
--themesDir ../.. \
--theme serenity-hugo-theme
```
