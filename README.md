[![Stories in Ready](https://badge.waffle.io/arresteddevops/ado-hugo.png?label=Ready&title=Ready)](http://waffle.io/arresteddevops/ado-hugo) [![Stories in Progress](https://badge.waffle.io/arresteddevops/ado-hugo.png?label=In%20Progress&title=In%20Progress)](http://waffle.io/arresteddevops/ado-hugo) [![wercker status](https://app.wercker.com/status/dfa492ce79ae5083723b53a07e98c8f4/s "wercker status")](https://app.wercker.com/project/bykey/dfa492ce79ae5083723b53a07e98c8f4)

This is the thing that drives the new ADO website. You can see our progress on tasks at http://waffle.io/arresteddevops/ado-hugo

[![Throughput Graph](https://graphs.waffle.io/arresteddevops/ado-hugo/throughput.svg)](https://waffle.io/arresteddevops/ado-hugo/metrics)

## Contributing

Here are the steps to follow to get going as an ADO content contributor (or heck, even a code contributor)

1. Install [Hugo](http://gohugo.io) - *NOTE: Please make sure it is at least version 0.15*
2. Clone this repo
3. If you want to fire up a local copy to see your changes as you go, enter this command `hugo server -w --baseUrl="http://localhost:1313"`
4. You probably want to do the previous thing in another pane/window, as it needs to keep running. The -w watches for any changes and rebuilds on the fly. You have to reset the baseUrl or it will try to go to new.arresteddevops.com
5. If you want to make a new episode, type in `hugo new episode/my-episode-name.md`
6. When you push to master on github, wercker will automatically build the site and publish it to http://new.arresteddevops.com

## Episodes

Every episode needs a few images. You need the following

1. **Episode thumbnail** - This must be square, PNG, and 500px by 500px. Enlarge it slightly if you have to. As of right now, these must be named EXACTLY the same as the episode file name (i.e., `devops-at-etsy.png`). They will live in the `content/episode/img` folder.
2. **Episode banner** - These need to be PNG, 800px by 420 px. The need to be named using the episode name as a template (i.e., `devops-at-etsy-banner.png`) and stored in `content/episode/img` folder.
3. **Facebook sharing image** - These need to be PNG, 1600px by 630 px, and named after the episode (i.e., `devops-at-etsy.png`). They are stored in `static/img/social/fb` folder

When you create a new episode, Hugo will populate the frontmatter of the .md file with a bunch of stuff for you. These are the required items to be sure to populate:
* **Description** - A string in double quotes. Please make sure that any double quotes are escaped, as such: `\"DevOps\"`
* **podcast** - this is the URL to the podcast MP3. You may not have this at the time you are creating an epiosde page, so that's okay.
* **guests** - a comma separated list of the guests, in the format first initial, last name (i.e., `"jhand", "srosenbaum"`). The names should line up to .yml files in `data/guests`
* **sponsors** - comma separated list of the sponsors for the episode. Same rules apply as guests, but the data files are in `data/sponsors`
* **friendly** - this is the shortname of the episode. It should be the name of the file minus the .md extension. I tried to automate this without success so far. Sorry :(
* **episode** - a string for the episode number, i.e., `"42"`
* **title** - the title of the episode. It's a string inside double quotes.
* **images** - Array of images for social sharing. You should be able to just take the default and replace the slug with the "friendly" for that episode.
* **author** - A string that contains either "Matt", "Bridget", or "Trevor"
* **aliases** - Array of strings for redirects. The only one you should ever need is for the episode number, i.e., `aliases = ["/27"]`
* **youtube** - the URL of the YouTube video, if there is one. If not, delete this line from the frontmatter of the episode.

## Contributing Code

Until you get your legs under you with the code (you'll need things like a LESS compiler, etc), I highly recommend just sticking with the content items. However, if you want to fix/enhance any of the Hugo code or CSS/Bootstrap stuff, please fork the repo and sumbit a PR for [@mattstratton](https://github.com/mattstratton) to evaluate.


### Credits

Thanks to <a href = "https://github.com/nozzle">nozzle</a> for the <a href = "https://github.com/nozzle/hugo-snippets">hugo-snippets</a> repo, which we use for adding wonderful SEO and social sharing markup!
