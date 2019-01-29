# simple-srd

An easy to use template for quickly creating SRD style documents and webpages. Minimum styling for customizable theming.

## Setup

> You may want to clone this tab to keep these instructions open while you follow along.

1. Fork this repository by clicking the fork button in the upper right. ![fork](https://github-images.s3.amazonaws.com/help/bootcamp/Bootcamp-Fork.png)
2. When your new repo opens, naviagte to your settings tab. ![settings](https://guides.github.com/features/pages/repo-settings.png)
3. Scroll down your settings page and set your GitHub pages source to  "master branch" ![settings](https://guides.github.com/features/pages/launch-theme-chooser.png)
4. Your site will be reachble from the link indicated in the "Your site is ready to be published at..." line

## Usage

Creating a great webpage doesn't require you to know any javascript, css or even html. The are only a couple types of files you will ever need to touch. The first type of file is called a YAML file with the .yml extension. It stores structured data in text format. 

Currently there is only a single file of this type called links.yml. It stores any links that you want to appear in your navigation menu. 

[file](https://github.com/non-binary-trees/simple-srd/blob/master/_data/links.yml)

```Yaml
- label: blades in the dark # This is the text that appears on your site for the link
  url: https://bladesinthedark.com # This is where the link goes to
- label: internal link
  type: internal # For links to your own site use this flag
  url: /index 
```

following that ppatern you can create links for anything you will need.

The other type of file is Markdown with the .md extension. This is mostly just like you would normally type with the addition of being able to mark things you want to be formatted a special way.

[file](https://github.com/non-binary-trees/simple-srd/blob/master/README.md)

```Markdown
# simple-srd

An easy to use template for quickly creating SRD style documents and webpages. Minimum styling for customizable theming.

test content shamelessly used without permission from the Gold ENnie award winning website [bladesinthedark.com](https://bladesinthedark.com/)
```

Is how the first section of this file is written using Markdown.

Your actual website will have some preset pages. These might include your homepage, a contact form and perhaps an about page. Initially you begin with just a home page called index.md

[file](https://github.com/non-binary-trees/simple-srd/blob/master/index.md)

```Markdown
---
title: Simple SRD
---

The easy way to make an SRD.
```

This file has two parts. The top section between the two '---' is YAML just like you saw before. It just defines a variable for when the page is rendered. For now you just need to know all our Markdown files should define a title variable. Following that section is just plain Markdown like in the previous example.

You can edit this using markdown to create a home page with whatever information you want visitors to see when they first visit your page.

The other page on your website will be rules. There are two types of rules pages. First is a rules section, this groups related sections of rules together under a heading in your navigation menu. Our section sample is called [the-basics.md](https://github.com/non-binary-trees/simple-srd/blob/master/_rules/the-basics.md)

```Markdown
---
title: The Basics
---

## System Reference Document Overview

This System Reference Document (SRD) contains the core mechanics derived from the Blades in the Dark rpg. If you'd like to use these mechanics in your own game, see the Licensing section of this website for details.

## The Game
Blades in the Dark is a game about a group of daring characters building an enterprising crew. We play to find out if the fledgling crew can thrive amidst the teeming threats that surround it.

## The Players
Each player creates a character and works with the other players to create the crew to which their characters belong. Each player strives to bring their character to life as an interesting, daring character who reaches boldly beyond their current safety and means.

The players work together with the Game Master to establish the tone and style of the game by making judgment calls about the mechanics, dice, and consequences of actions. The players take responsibility as co-authors of the game with the GM.

## The Characters
The characters attempt to develop their crew by performing scores and contending with threats from their enemies.

## The Crew
In addition to creating characters, you’ll also create the crew by choosing which type of criminal enterprise you’re interested in exploring.

## The Game Master
The GM establishes the dynamic world around the characters. The GM plays all the non-player characters in the world by giving each one a concrete desire and preferred method of action.

The GM helps organize the conversation of the game so it’s pointed toward the interesting elements of play. The GM isn’t in charge of the story and doesn’t have to plan events ahead of time. They present interesting opportunities to the players, then follow the chain of action and consequences wherever they lead.

## Playing A Session
A session of Blades in the Dark is like an episode of a TV show. There are one or two main events, plus maybe some side-story elements, which all fit into an ongoing series. A session of play can last anywhere from two to six hours, depending on the preferences of the group.

During a session, the crew of scoundrels works together to choose a score to accomplish, then they make a few dice rolls to jump into the action of the score in progress. The PCs take actions, suffer consequences, and finish the operation (succeed or fail). Then the crew has downtime, during which they recover, pursue side-projects, and indulge their vices. After downtime, the players once again look for a new opportunity or create their own goals and pursuits, and we play to find out what happens next.
```

Just like before we set a title in the first section. Then we, wrote our content with a few extras for formatting.

The other type of rules file is the kind that goes into a section. This sample is called [the-core-system.md](https://github.com/non-binary-trees/simple-srd/blob/master/_rules/the-core-system.md)

```Markdown
---
title: The Core System
category: the-basics.md
---
## Judgment calls

When you play, you’ll make several key judgment calls. Everyone contributes, but either the players or the GM gets final say for each:

* Which actions are reasonable as a solution to a problem? *Can this person be swayed? Must we get out the tools and tinker with this old rusty lock, or could it also be quietly finessed? The players have final say.*
* How dangerous and how effective is a given action in this circumstance? *How risky is this? Can this person be swayed very little or a whole lot? The GM has final say.*
* Which consequences are inflicted to manifest the dangers in a given circumstance? *Does this fall from the roof break your leg? Do the constables merely become suspicious or do they already have you trapped? The GM has final say.*
* Does this situation call for a dice roll, and which one? *Is your character in position to make an action roll or must they first make a resistance roll to gain initiative? The GM has final say.*
* Which events in the story match the experience triggers for character and crew advancement? *Did you express your character’s beliefs, drives, heritage, or background? You tell us. The players have final say.*

## Rolling the Dice

Blades in the Dark uses six-sided dice. You roll several at once and read the **single highest result**.

* If the highest die is a **6**, it’s a **full success**—things go well. If you roll more than one **6**, it’s a **critical success**—you gain some additional advantage.
* If the highest die is a **4 or 5**, that’s a **partial success**—you do what you were trying to do, but there are consequences: trouble, harm, reduced effect, etc.
* If the highest die is **1-3**, it’s a **bad outcome**. Things go poorly. You probably don’t achieve your goal and you suffer complications, too.

> *If you ever need to roll but you have zero (or negative) dice, roll two dice and take the single lowest result. You can’t roll a **critical** when you have zero dice.*

All the dice systems in the game are expressions of this basic format. When you’re first learning the game, you can always “collapse” back down to a simple roll to judge how things go. Look up the exact rule later when you have time.

To create a dice pool for a roll, you’ll use a **trait** (like your ***Finesse*** or your ***Prowess*** or your crew’s Tier) and take dice equal to its **rating**. You’ll usually end up with one to four dice. Even one die is pretty good in this game—a 50% chance of success. The most common traits you’ll use are the **action ratings** of the player characters. A player might roll dice for their ***Skirmish*** action rating when they fight an enemy, for example.

There are four types of rolls that you’ll use most often in the game:

* ***Action roll.*** When a PC attempts an action that’s dangerous or troublesome, you make an action roll to find out how it goes. Action rolls and their effects and consequences drive most of the game.
* ***Downtime roll.*** When the PCs are at their leisure after a job, they can perform downtime activities in relative safety. You make downtime rolls to see how much they get done.
* ***Fortune roll.*** The GM can make a fortune roll to disclaim decision making and leave something up to chance. *How loyal is an NPC? How much does the plague spread? How much evidence is burned before the constables kick in the door?*
* ***Resistance roll.*** A player can make a resistance roll when their character suffers a consequence they don’t like. The roll tells us how much stress their character suffers to reduce the severity of a consequence. *When you resist that “Broken Leg” harm, you take some stress and now it’s only a “Sprained Ankle” instead.*

## The Game Structure

Blades in the Dark has a structure to play, with four parts. By default, the game is in **free play**—characters talk to each other, they go places, they do things, they make rolls as needed.

When the group is ready, they choose a target for their next operation, then choose a type of plan to employ. This triggers the engagement roll (which establishes the situation as the operation starts) and then the game shifts into the **score** phase.

During the score, the PCs engage the target—they make rolls, overcome obstacles, call for flashbacks, and complete the operation (successfully or not). When the score is finished, the game shifts into the **downtime** phase.

During the downtime phase, the GM engages the systems for payoff, heat, and entanglements, to determine all the fallout from the score. Then the PCs each get their downtime activities, such as indulging their vice to remove stress or working on a long-term project. When all the downtime activities are complete, the game returns to **free play** and the cycle starts over again.

The phases are a conceptual model to help you organize the game. They’re not meant to be rigid structures that restrict your options (this is why they’re presented as amorphous blobs of ink without hard edges). Think of the phases as a menu of options to fit whatever it is you’re trying to accomplish in play. Each phase suits a different goal.
```

This is very similar to the last file with one notable exception. We defined a category variable in the YAML section. This has to match file name of the rules section this page belongs to.

If you are familiar with CSS you may want to check out the [custom css](https://github.com/non-binary-trees/simple-srd/blob/master/_sass/_custome.scss) file to modify the theme to your liking.

That should be enough to get you started on making your very own SRD document for the web.

## Attribution

I have used text from the Gold ENnie award winning website [bladesinthedark.com](https://bladesinthedark.com/) because it is a great example of how to make an SRD. I hope this project allows people publish their games without technology getting in the way. 

And heres the legal stuff...

This work is based on Blades in the Dark (found at http://www.bladesinthedark.com/), product of One Seven Design, developed and authored by John Harper, and licensed for our use under the Creative Commons Attribution 3.0 Unported license (http://creativecommons.org/licenses/by/3.0/).

The images in the setup section are from official GitHub guides. [forking](https://guides.github.com/activities/forking/) [pages](https://guides.github.com/features/pages/)
