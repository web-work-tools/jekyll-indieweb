---
type: post
title: "Indigo Authors - Indiweb Features"
categories: ["meta"]
tags: ["options", "indieweb","hugo","front matter"]
slug: /indigo-authors-indieweb/
aliases:
  - /indigo-authors-indieweb/
  - /posts/indigo-authors-indieweb/

---


> "The following classes are used to mark up the author bio for Indieweb parsing: h-card, u-photo, p-name, u-url, rel=me, p-locality, p-country-name, u-email, p-note. I'll be exploring these classes more thoroughly, soon."

## Note from the Editor

This post is from [AngeloStavrow/indigo](https://github.com/AngeloStavrow/indigo), the Hugo Indieweb theme, I'm using at [web-work.tools](https://web-work.tools).

## Indigo Authors
The bottom of every page in the theme can optionally show a short biography of the site author, including a profile picture, email link, and location.

## Setting up the author bio

A set of configuration options are used for displaying the biography.

```
[params]
  Author = "Author Name"
  Avatar = "images/site-logo.svg"
  Biography = "A short description, a few sentences describing the author. Set
               the 'ShowBio' parameter to false to hide this."
  ShowBio = true        

[params.indieWeb]  
    EmailAddress = "email.address@example.com"
    Country = "CountryName"
    City = "CityName"
```

Specifics on each setting item are as follows:

- `Author`: Your name; this is the site author name.
- `Avatar`: The path to your profile picture. By default, it will show the theme's logo (`/static/images/site-logo.svg`).
- `Biography`: Hopefully the placeholder text here is self-explanatory; add a couple of short sentences about yourself here.
- `ShowBio`: If you prefer not to show the author bio, set this to `false`. By default, it's set to `true`.
- `EmailAddress`: The email address at which you can be contacted.
- `Country`: The name of the country in which you live.
- `City`: The name of the city in which you live.

## IndieWeb features

The following classes are used to mark up the author bio for [IndieWeb][indieweb] parsing:

| Element         | Class                       |
| :-------------- | :-------------------------- |
| The author card | `h-card`                    |
| Profile picture | `u-photo`                   |
| Author URL*     | `p-name`, `u-url`, `rel=me` |
| City            | `p-locality`                |
| Country         | `p-country-name`            |
| Email address   | `u-email`                   |
| Biography       | `p-note`                    |

*Author URL is set to the site's base URL.

[indieweb]: https://indieweb.org/

