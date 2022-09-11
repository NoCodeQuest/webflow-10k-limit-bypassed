# Webflow 10k character limit for custom code bypassed!

### ➡ More pro Webflow tips like this found at [NoCodeQuest.com](https://nocodequest.com/).

**Overview:**

This is the quick and easy way I bypass Webflow's 10,000 character limit for custom code.

For any type of production (live site) usage you'd want to host this on a CDN like [jsDeliver](https://www.jsdelivr.com/), or something similar.

**Step 1:**

Create a new repo in Github to host your Javascript.

**Step 2:**

Upload the Javascript.

Here's a [simple example of mine within this repo](https://github.com/NoCodeQuest/webflow-10k-limit-bypassed/blob/main/hello.js).

**Step 3:**

Tap the "Raw" button to get just the file and code itself:

```
https://raw.githubusercontent.com/NoCodeQuest/webflow-10k-limit-bypassed/main/hello-20k.js
```

**Step 4:**

Host it freely on [JS Deliver](https://www.jsdelivr.com/?docs=gh) by following this pattern:

```
https://cdn.jsdelivr.net/gh/user/repo@version/file
```

In my case, I don't have an `@version` so my url looks like this:

```
https://cdn.jsdelivr.net/gh/NoCodeQuest/webflow-10k-limit-bypassed/hello-20k.js
```

Note, I didn't have to upload anything, behind the sceens it grabs my code off of Github and hosts it on their CDN, nice!

**Step 5:**

Add that url to the `src` attribute on a Javascript tag:

```
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/NoCodeQuest/webflow-10k-limit-bypassed/hello-20k.js"></script>
```

**Step 6:**

At this to the "custom code" section of your Webflow page, under the "before </body> tag" section.

**Step 7:**

Publish and visit the live site.

