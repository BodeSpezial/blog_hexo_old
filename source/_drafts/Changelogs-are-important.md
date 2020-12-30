---
title: "Your friend and helper: The changelog"
tags: [tools,go,changelog,project management]
---

Working in a team is different from working alone. I think we can all agree on that. But recently I learned some piece of workflow that I'll try to use from now in any project, that is at least maintained and intended to be shared with others: A good changelog.
After having some issues with merging and a bit of workflow adjustments I'm pretty pleased with the result and so today I want to point out my thougts on why changelogs are useful along with a tool that I wrote as an excercise and to ease the work with changelogs on versionated projects.

TLDR: While working in a team with regular reviews and releases a colleague and I tried to implement a good changelog workflow to have something to look into when discussing changes that had been made. Finding that very useful I wrote a liitle tool for some common problems.

# Changelogs

Overall is a changelog just the collection of all the changes made in the past, often in sections like "Added", "Changed", "Fixed", "Removed". The concrete style in which a changelog is written is decided by each person or team because there isn't something like a specification or something. Nonetheless are there some guidelines like Keep-A-Changelog which projects can follow to have a more standardized changelog. Findig it quite useful I use this styling too.

## Keep-A-Changelog
I won't go too deep into the spec of Keep-A-Changelog because they have a very well written documentation but I will go over the (imo) most important points of a nice changelog.

### Dated sections

However you structure your release or even publishing cycle you'll always have some changes, that happened in a specific timespan. To reflect this the main sections of your changelog will be your released so that you always see what happened between two releases.

### Categorized Subsections

Under each time-section "Keep-A-Changelog" recommends to use the subsections "Added", "Removed", "Changed" and "Removed". I think they're fairly self-explanatory, it only happens from time to time that it's a bit hard to distinguish between e.g. "Changed" and "Fixed" but don't let that take too long time because a changelog is nothing written in stone.

### Grouped Links

Something that is not directly recommended and only visible if you edit your changelog but that I find particularly useful is the grouping of links.
To understand, what the beauty behind this is you have to know a feature from Github (at least I first saw it there). There you can just write #123 to link the issue or pull-request with the number 123. This isn't directly supported in normal markdown but can be easily implemented for at least one file. Because if you have `[Name-of-the-link]: https://path.to.a/website` anywhere in your document you can always link to `https://path.to.a/website` by writing `Name-of-the-link`.
So if you now want to link the associated pull-request or even e.g. Jira-Ticket to your change you can just write `#123, JIRA-123` at the end of the link and then put all the links in one section either at the bottom of the dated section or your document.
Like this:
```markdown
...
Fixed:
  - Fixed bug from issue #123

<!-- Links -->
[#123]: https://github.com/name/project/issue/123
...
```

## Why and for who?

After talking that much about the what and how I'll now briefly talk about why I find them so useful and in what projects or teams I'd generally recommend them (although being sure, that a lot of you already use some form of changelog).
That said it's hard to _not recommend_ them because I think almost everyone can profit from them in one way or the other. The only time I think it's not necessary from day one is in private and side-projects that aren't intended for some kind of collaboration. E.g. for this blog I'll almost certainly not keep a changelog because I want to keep the code changes as minor as possible and new articles are literally live documented and can even be subscribed by over things like rss or atom.

# Chango (the mentioned tool)

As mentioned above I wrote a little go program to help with the changelog-workflow initially inspired by this article.


# Sources, Recomendations and further information

- Keep-A-Changelog
- Markdown links
- Chango
- That one article about changelogs
