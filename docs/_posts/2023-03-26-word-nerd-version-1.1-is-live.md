---
layout: post
title:  "Word Nerd v1.1.0 Released"
categories: gamedev
author: groundh0g
---

I don't know about you, but I love the game, Wordle, hosted by the NY Times. Maybe "obsessed" is a better word. It's so dang addicting. And it's equally as frustrating since you can only play once a day. So, I decided to make a clone of it, with a few new features.

Enter "[Word Nerd!](https://games.joehall.net/wordnerd)", stage left. It has configurable levels of difficulty. It supports themeing and high-contrast modes (like Wordle). And it allows you to use the scrabble-like word lists for validation (limited to 5-letter words, minus a simple naughty word filter).

<img src='{{ "/assets/images/blog/word-nerd-themes.png" | relative_url }}' style="width:512px;" />

Wordle's method of playing against your friends is that you and your friends have to play the same word on the same day. With Word Nerd, you can play as many words per day as you'd like, so there needs to be some other method of pitting your friends against you. Word Nerd generates a unique token for each word, so you can give that token to your opponent (via the "Share" button) at any time to challenge them.

<img src='{{ "/assets/images/blog/word-nerd-shared-games.png" | relative_url }}' style="width:512px;" />

Word Nerd was designed mobile-first, so it should work well on phone and desktop. There are even desktop applications for Windows and MacOS (not yet released).

![Joe's Signature]({{ "/assets/images/signature-joe.png" | relative_url }})
