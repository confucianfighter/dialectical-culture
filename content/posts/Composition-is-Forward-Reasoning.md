---
title: "Composition Is Forward Reasoning"
date: 2023-06-24T00:19:40Z
draft: true
categories:
  -  AI
  -  Philosophy
  -  Psychology
image: "cyber-punk-all-seeing-eye.jpeg"
---
There is an ongoing conversation as to wether GPT-4 is developing its own reasoning, or if this is all just mimicry over a vast dataset. 

Geoffrey Hinton believes that GPT-4 can reason. He explains so much in the video at the bottom of this page.

And he doesn't just think it is using some kind of cheat based on similar texts. He believes it has evolved it's own way of solving problems.

He raises the question as to how this is possible given that the model can only move forward, one word at a time. I'm sure he has some pretty good theories, but he didn't suggest any.

I have been pondering this and I think I have somewhat of a gist of what is happening. I'm sure it's nothing novel.

### Stephen Wolfram on ChatGPT and LLMs 
Most of my thought on this is based on this lecture by Stephen Wolfram. There are parts of the lecture that get a little technical in the middle, but anyone can get a good enough idea of what is going on by taking what they can from this lecture. It is long, but I think it is worth most people's time so that they have a grasp on what is actually going on and so that they can have more general discernment on all the important issues comming up involving AI. Below the video I attempt to explain and refine my own view of exactly what is happening. I hope it adds something helpful for anyone who wants a good sense of what might be happening. 

{{< youtube flXrLGPY3SU >}}

### Changing State
In the above video, Stephen Wolfram moves from a very boring "word space" in the beginning, to a rich layer of abstraction in meaning space. This is key.

That these LLMs do not direct their own state in any meaningful way is based on several common misconceptions:

1. That the probability of the next word is based on words alone: Instead it is based on the preceding set of varied and rich constellations of ideas.

2. That ***next word*** is based off of ***previous word***: Consider that the model ***looks**** at the ***entire context*** all at once each time that is chooses the next word based on some probability. So if the model has an 8000 token context window, it looks at the preceding 8000 words each time it chooses the next word. Transformer models also direct different kinds of attention to different parts of the text based on certain gramatical ontologies. 

3. There is some difference between external and internal state. Since the model holds no internal state it is thought of as stateless. I disagree with this. While technically this is true that it does not save an internal state, the text itself holds plenty of state, it changes the text by adding to it, and that text changes what it sees in the context window, which influences the next behavior 100%, is that not the very definition of state? Does it matter that state is stored in the very output it is proposing? 

So as it adds words it is essentially modifying the context and therefore the state from which it chooses the next word. And really it can be pictured as choosing the next concept, that concept stretching over several dozen words. So GPT-4 is most certainly changing state in a controlled way by what it chooses as the next word. It's not so much that one word usually would change the whole state, but a certain cluster in ***meaning space*** may remain active over a dozen or so words. 

### Forward Compositional Thought
I think it's useful to think of it in terms of a similar mode of reasoning when we compose something in ink or with a typewriter. It's similar in that the LLM is in the same predicament: it can't go back, it can only go forward. Writing in this way is usually just thought of as cathartic, but I think it also has a certain effectiveness to it that is lacking in, say, a text editor. Liebniz's journal is a prime example. After reading it and seeing how he used the compositional style to his advantage in solving problems, it's hard for me to imagine that he would have come to any of his insights in mathematics without it. I think that the reason why this works so well, is that it forces the writer to procede in a tentative fasion and it brings in other ideas which at first might seem irrelevant, but might also turn out to be key. 

### Meandering Inductive Reasoning
Stephen Worlfram stated in his youtube lecture on ChatGPT that if it picks the ***most*** probable next word, it doesn't work so well. I think he knew why, but he didn't explain it. I think the randomness is needed because just like us, its thread of thought needs to meander about the constellations of neighboring ideas in what he calls ***meaning space*** in order to enlist other key concepts. By doing so it is able to explore and recruit other pertinent ideas into the thread that might be helpful towards coming to a solution. And in my own experience with the GPT-3.5 api, when I have reduced the randomness to 0, it seems to talk itself in circles like a person with some kind of OCD or schizophrenia.  

### Conclusion
So I propose that LLMs reasons by way of composition. They indeed hold state because each word added gets fed back through. Those states aren't usually changed instantly by adding one word, but instead over sequences of words constellations of ideas in meaning space illuminate and delluminate. It is still a matter of intensive research as to how this leads to it's ability to make such sharp inferences and to solve such complex problems, but it seems to me that this would be the general mechanism. I don't think this is any kind of breakthrough in how LLMs are understood, but simply a very intuitive way to grasp what is fundamentally at play.
### The lecture by Geoffrey Hinton referenced at the top of this page. 
{{< youtube rGgGOccMEiY >}}
