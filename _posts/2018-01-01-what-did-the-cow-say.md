---
layout: post
title:  "Have kids use the terminal"
date:   2017-12-01 19:00:00
categories: Kids fortune cowsay lolcat
cover: /images/cover-cowsay-lolcat.png
---

Making the terminal console interesting for kids, near impossible? Here's a
possible hack. *(kids age 9 - 11 years)*

This Christmas my kids wished for a `Minecraft` server. I wanted to be sure they
could actually use the server without my help. They should get familiar with the
terminal first, small steps = small risk of failing completely.

### Kids in the terminal

One day I was working on the computer and my kids asked what I was working on.
*(They were being polite, they don't actually want an answer and will start
rolling their eyes of pure boredom if they get one.)*

This time I was prepared - I had installed `cowsay`! Now what does the `cowsay`
do? It basically draws a cow using plain text characters.

Example:

```
$ cowsay Dad is the best
 _________________
< Dad is the best >
 -----------------
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||
```

The kids were almost fighting to get to the keyboard and they wanted to write
all kinds of things - they took the __bait__!

Naturally I showed them the `cowsay --help` and the `cowsay -l`, when they read
the output they got __excited__ - cowsay can render other fabel animals.

Example:
```
$ cowsay -f sheep Meh
 _________________
< Meh >
 -----------------
  \
   \
       __
      UooU\.'@@@@@@`.
      \__/(@@@@@@@@@@)
           (@@@@@@@@)
           `YY~~~~YY'
            ||    ||
```

Sure it's a pointless command, and you have to wonder who and why anybody would
foster a command like that. Well there's more...

#### Next command `fortune`

So I wanted to show them how to pipe data from one command to the next - it
might be more advanced, but I didn't let them know.

Now the there is a command called `fortune`, each time you run this it will
output a message sort of like from a fortune cookie.

Example:
```
$ fortune
I fell asleep reading a dull book, and I dreamt that I was reading on,
so I woke up from sheer boredom.
```

We can pipe the output from
`fortune` to `cowsay`.

Example:
```
$ fortune | cowsay -f flaming-sheep
 _______________________________________
/ What on earth would a man do with     \
| himself if something did not stand in |
| his way?                              |
|                                       |
\ -- H.G. Wells                         /
 ---------------------------------------
  \            .    .     .
   \      .  . .     `  ,
    \    .; .  : .' :  :  : .
     \   i..`: i` i.i.,i  i .
      \   `,--.|i |i|ii|ii|i:
           UooU\.'@@@@@@`.||'
           \__/(@@@@@@@@@@)'
                (@@@@@@@@)
                `YY~~~~YY'
                 ||    ||
```


#### Next command is `lolcat`

It's yet a command that makes you wonder - it basically adds rainbow'ish colors
to the output... But they really liked this command - it made the text area
beautiful, right.

And lets pipe the output from `cowsay` on to `lolcat`.

![fortune-cowsay-lolcat](/images/fortune-cowsay-lolcat.png){:width="100%"}

### Conclusion

Given that exploration is within reach and motivation is greater than 0, formula
for learning:

$$
    Learning=fun(exploration)^{motivation}
$$

Next blog post will be about setting up a linux server and running Minecraft in
docker.
