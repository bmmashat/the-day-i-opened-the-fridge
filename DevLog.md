# Dev & Feelings Log

Yup. Log of my developemet AND _feelings_, because, yeah.. feelings. 

### Day 0 (Someday in June, 2018) 
The game idea came to me.

### Day 1 (Feb 16, 2019) 
First real actionable task towards bringing this game idea to life. Set up docs. GitHub, GDD in Notion, and experimented with Ink. [GDD here.](https://www.notion.so/bmmashat/The-Day-I-Opened-The-Fridge-Game-69d833d91b7f473e9475f9eceaeb8a05)

### Day 2 (Feb 19, 2019)
Wrote a rough draft for part 1! Includes the full conversation. You can access it [here](https://docs.google.com/spreadsheets/d/16gAga-8uIu6R6mer9m4d9gmwYIOU6H50HAn1Ma33y58/edit#gid=1559134232) <br>
Stat: full original converstaion: 333 lines. Reduced to: 196 lines.

### Day 3 (Apr 16, 2019) 
Okay.. Finally back phew! So, I prototyped the first part of the game using Ren'Py. Totally not as originially planned, but I made it as part of an assignment in my writing in games class (TCS 191). You can access the horribly made version [here.](https://bmmashat.itch.io/the-day-i-opened-the-fridge). Even though I got a very good feedback from my professor, I believe the dialogue is too long and draining so I definitly need to cut it down even more. Here's my professor's feedback: 
> _Excellent work! Much like Project 1, this story is thinking through the ways in which characters reach across the mediated channels of consciousness, speech, and communication devices to try (and fail) to make meaningful contact with one another. I don't know if I mentioned this in my previous comments, but have you read Waiting for Godot--a two-person dialogue built around existential anxiety and the attempts of two character to try (and fail) to communicate with each other? If you plan on building this world out, it might be interesting to look at some theatre, short stories, and film that is built around the psychic drama of quotidian conversation. Make sure to proofread the text and cut and paste the dialogue into a spell check before uploading--there are a few minor grammatical errors and typos that (I don't think) are deliberate. For ex, ninty instead of ninety, teproary, missing apostrophes, etc._

### Day 4 (May 7, 2019) 
Alright. I decided to make this game as my final project for my writing in games class (TCS 191). I just pitched it and people seem to be very excited.. Which makes me nervous! [Here is my pitch](https://docs.google.com/presentation/d/1YInIJs9fiFnqte8Hz3Ug0oyNnVhcQ6Ftg02fu3GRNAI/edit?usp=sharing). <br>
I'm now having second thoughts.. Shall I make it using Ren'Py or? Well, for now I will just focus on the writing and then worry later about the UI. 

### Day 5 (May 10, 2019)
I spent more time polishing part one and reducing it to 113 lines! (was 196 lines). I still think it's too long though. Need to do some playtesting. I made a prototype on ink. It's accessible [here](https://bmmashat.itch.io/the-day-i-opened-the-fridge-part-one). 

### Day 6 (May 18, 2019)
Based on some feedvack (3 people), they felt the conversation flow was natural, so I decided to keep it as it is for now and start working on part 2. But before that, I added some styles to make it easier for reading (see picture below). I changed the background to dark, and I finally managed to change the color of the text! Phew! Thanks to Chrome's "Inspect" option, I was able to see how [this game](https://h-anklebone.itch.io/a-song-for-kharon) had styles. Turns out ink already had support of tags (#CLASS: <whatever>) and then you just add the class customization in the CSS file. 

![screenshot](https://github.com/bmmashat/the-day-i-opened-the-fridge/blob/master/screenshots/darkcolors.jpg "screenshot of colros")


### Day 7 (May 19, 2019) 
I started and FINISHED part two. It's a draft though, I'm still not satisfied with it. And it's not like what I originally planned. This part you play from the perspective of one character (Blue), and players will have some choices to reveal more about the story. But I decided not to change the conversation and just add Blue's thoughts as the source of the "additional info" the player can get from this level. I might change this later but after testing to see how people react to it. Next step: write part 3! Part 2 is accessible [here](https://bmmashat.itch.io/the-day-i-opened-the-fridge-part-two). 

### Day 8 (May 24, 2019) 
Finished part 3. I'm not very satisified with it. I wrote it in rush. But at this point, I just want to finish the whole game, and then I will work on changing/improving the conversation. Part 3 is accessible [here](https://bmmashat.itch.io/the-day-i-opened-the-fridge-part-three). Next: combine part 1,2,3 together in one bulid.

### Day 9 (May 25, 2019) 
Okay.. I'm very embarrassed for using Ink in a very dumb way. I created a "knot" for nearly every line. Yup, I kept knoting and diverting the whole conversation =) Yup, like this: 
```
== start == 
-> next0

+ [(I wasn't supposed to see it)] -> blueThink0

== blueThink0 == 
+ [(This wasn't supposed to happen)] -> blueThink1

== blueThink1 == 
+ [(Ah.. My head.. My heart.. My hand.. I'm literally shaking..)] -> blueThink2

```

Turns out Ink had a speical formatting called [weave](https://github.com/inkle/ink/blob/master/Documentation/WritingWithInk.md#part-2-weave), which gives the ability to "connect" lines if it's a "normal" line, which I did for the rest of the conversation. It doesn't work if it's a choice though. The only way I could make it work is to use nested choices like following: 
```
+ [(I wasn't supposed to see it)] 
++ [(This wasn't supposed to happen)] 
+++ [(Ah.. My head.. My heart.. My hand.. I'm literally shaking..)] 
```
This way each line can be displayed at once on the screen then proceed to the next, without having to knot anything. <br>
Another problem I didn't account for from the very beginning is when the player finishes from one part, the entire part should disappear and move to a new one. Ink currently doesn't support that (as far as I know). Fortunately, I found someone developed a "Twine-Like" feeling [template](https://github.com/wickedlyethan/ink-soaked) for Ink, where the entire text on screen disappear after making a choice. <br>
That being said, I have a new build of the first 3 parts combined. It is accessible [here](https://bmmashat.itch.io/the-day-i-opened-the-fridge-three-parts). Next: write part 4!

### Day 10 (May 26, 2019)
I realized this game is taking me longer than I expected.. Yeah.. Game dev.. Anyways, I send the first 3 parts to some friends and got pretty good feedback. I also started writing part 4 and I didn't expect it would affect me emotionally a lot.. I couldn't sleep until I finished one ending. And yes, I stayed up all night, and all morning. I went to bed at 8 am. It was very intense on me. Although I wasn't satisified with it, finishing it gave me the feeling of victory.. It is accessible [here](https://bmmashat.itch.io/the-day-i-opened-the-fridge-part-4).

### Day 11 (May 27, 2019)
This is the first thing I headed towards once I woke up. Part 4 felt very rushed so I spend some time editing and ploishing it until I reached an appropriate level of satisifaction. I sent it to more friends and received couple of amazing feedback from amazing friends. It was very intense on them as well, which is good, because that was my itention. I felt suceess. Also, I decided not to write another ending (the happy ending). The ending I wrote felt more suitable to the story and to the emotions and feelings I wanted to convey. <br>
Damn.. That was hell of a ride.. I can't beleive I made this.. 

### Days XX (May 28 - Jun 4, 2019)
So.. I shared the game with ~70 people, got feedback from ~34 people. They were all rich and genuine and I'm very grateful for that. I got feedback for both the story/script, and gameplay mechanics. They made me very very very happy. However, to be very very very honest, the feedback that made me the happiest was from the CREATOR OF BURY ME MY LOVE!!!!!!!!!!!!!!! I still can't believe it. I DMed him on Twitter and he was nice and kind enough to play it and give me his sincere opinion. I will be forerver flattered. <br> 
The most common feedback were:
- add more choices
- maybe reduce the text a little bit
- add audio
<a/>
Minor things I changed based on feedback: 
- Polished Act 4. Added more detailes and streched it a little bit because it felt so rushed. 
- Some spelling mistakes. 
<a/>
Next, I just need to make final grammar & spelling fixes, write a postmortem, make a public itchio page for it, and submit it to my final project TCS class! <br>
Also, I decided to stop sharing and collecting feedback for this version.. I will work on some improvments before I share it again. Proabably that's the plan for the summer! 

#### TODO: 
- [ ] proofread (grammar & spelling)
- [ ] fix audio issue in Act 4
- [ ] release a public beta (?) in itchio 
- [ ] choose better colors (blue & purple)
