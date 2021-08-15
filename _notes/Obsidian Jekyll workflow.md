---
title: Obsidian Jekyll workflow
---
> ## tl;dr
> Make Obsidian Vault and Jekyll directory the same. Make the notes' filename and front matter title identical. Use Atom to push changes to Github which feeds Netlify and serves the site.💥

[[Obsidian is for building my body of work]] and tending to this digital garden. While my workflow is simple to me, it does require some setup. That's what we'll cover in this note.

🌱 This note is intended to help out my fellow digital gardeners who want to setup their own garden and simple workflow on MacOS. This is admittedly the first "technical walkthrough" I've ever written so **please please please** comment below or [message me on Twitter](https://twitter.com/miketnnnbm){:target="_blank"} with any troubles, challenges, or confusions you ran across. Enjoy!

<hr>
In essence, my workflow is

```
Obsidian → Atom → Github → Netlify → https://refinedmind.co
```

## Diving into my setup
This site is running on:
- [Jekyll](https://jekyllrb.com){:target="_blank"}
- [Netlify](https://www.netlify.com){:target="_blank"}
- [Github](https://www.github.com){:target="_blank"}

The words are written in [Obsidian](https://obsidian.md){:target="_blank"}.

The backend is managed in [Atom text editor](https://atom.io/){:target="_blank"}.

Before getting to Obsidian however, everything starts somewhere in [[my digital ecosystem]]. [[Ideas improve by writing about them not by thinking about them]], which is the whole purpose of this site: improving ideas.

While I have been building things on the internet my whole life, I'm not a `code from stratch`-type person, so I've built upon the foundation created by Maxime Vaillancourt, who graciously shared his Jekyll-based digital gardening template in a crystal clear walkthrough.

## Here's how I've connected Max's digital garden template with an Obsidian vault running on my Mac

### 1. Install your tools and backend systems
1. [Download the Atom text editor](https://atom.io/){:target="_blank"}
2. [Walk through Max's digital garden setup](https://maximevaillancourt.com/blog/setting-up-your-own-digital-garden-with-jekyll){:target="_blank"} *(this takes time so get comfy and come back here when things are working)*
3. [Install the latest version of Obsidian](https://obsidian.md/){:target="_blank"}
4. Create a new Vault in Obsidian and set the location to be the `_notes` directory within your main Jekyll directory
5. Create a new directory within `_notes` and name it `_staging`

> ✅  At this point you should have a working Jekyll install (Thanks Max!) and an Obsidian vault setup within the same directory as your Jekyll install.
<hr>
### 2. Create and link two notes
Jekyll works by taking any markdown file within `_notes` and turning it into a static page. Since you've put `_staging` within the `_notes` directory, your Gibhub repo will sync the folder but it will not interfere with the functionality of Jekyll. You can use this folder for notes you're working on but are not ready to go live on your public garden.

#### Make your first note
1. Open your Obsidian window, right click on the `_notes` folder within the left sidebar, and make a new note.
2. Give it the title `my new digital garden` and include the spaces. Jekyll will process them just fine.
3. Copy and paste the Jekyll "front matter" to the top of the note. You'll have to add this to every note you want to appear on your site.
```
---
title: 
---
```
4. Add the words *my new digital garden* to `title: ` so it reads
```
---
title: my new digital garden
---
```

Now the title of the markdown file (`my new digital garden.md`) matches the title of the note Jekyll will parse (`title: my new digital garden`). This is how all your links and backlinks will connect to one another when you push everything to Github.

> ❗️ If you find links not working when you know the notes exist, make sure the title of the markdown file matches the title within the front matter exactly.

#### Let's add some content
Below the front matter copy and paste the following into the body of the note:

```
Welcome to my garden!

This is where I explore my ideas and share them publicly so others can read and provide feedback to help me improve my thinking.
```

#### Link to a new note
Select the text `improve my thinking` and type double brackets `[[` which will automatically wrap that selection in brackets. That's one way to link to new notes.

While holding COMMAND, click on that newly created link to open a new window containing a blank note that's automatically been titled `improve my thinking`.

Once again copy and paste the front matter to the top of the note:

```
---
title: 
---
```

> 🚨 Now, this is important: make sure the title of the note **matches exactly** to the title in the front matter. If it doesn't, things will not link properly within Jekyll.

Your front matter on this new note should look like this:

```
---
title: improve my thinking
---
```

#### Write your new note
Have some fun writing a few sentences in that note and let's move on.
<hr>
### 3. Setup Atom editor
1. Open Atom text editor
2. Click File > Add Project Folder
3. Select the main directory of your Jekyll installation. If you followed Max's walkthrough, this will be the `my-digital-garden` directory. You should now see all your Jekyll files and `_notes` within the Atom editor.
4. In the right window pane click the button `Create repository` and follow the prompts to setup a git repository within the main project folder

You should now see a list of the files with *Unstaged Changes*. Click `Stage All` and watch them move down to the *Staged Changes* section.
<hr>
### 4. Push changes to Github
1. Enter a short note in the text box for `Commit message`
```
Just setting up my dgtl grdn
```
2. Click `Commit to master`
3. At the very bottom in the status bar of the editor, click `⇧Push 1` to push the changes to Github

> 💾  Your files are off to the interwebs!

From here it will take a few minutes for Github to recognize the changes and Netlify to deploy them to your site.

<blockquote class="quoteback" darkmode="" data-title="Setting%20up%20your%20own%20digital%20garden%20with%20Jekyll" data-author="" cite="https://maximevaillancourt.com/blog/setting-up-your-own-digital-garden-with-jekyll">
<p>Once that’s done, your digital garden should be available on the Internet via a generic Netlify URL, which you can change to a custom domain later if you’d like.</p>
<footer> <cite><a href="https://maximevaillancourt.com/blog/setting-up-your-own-digital-garden-with-jekyll">https://maximevaillancourt.com/blog/setting-up-your-own-digital-garden-with-jekyll</a></cite></footer>
</blockquote>
<script note="" src="https://cdn.jsdelivr.net/gh/Blogger-Peer-Review/quotebacks@1/quoteback.js"></script>
<hr>
## All done! Enjoy your garden!
### To wrap up, your workflow for tending your garden is as follows:
> 1. Write, edit, and link notes in Obsidian
> 2. Commit and push changes to Github via Atom
> 3. That's it! Just wait for Github + Netlify to do their thing and your garden will be updated within minutes!

<hr>
Thank you for following along with this walkthrough! I hope it was helpful and valuable to you, and not at all confusing.

Have fun gardening!

🌱

*If my work helps you in any way, [please consider buying me a coffee ☕  !](https://www.buymeacoffee.com/miketannenbaum){:target="_blank"}*