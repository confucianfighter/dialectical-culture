---
title: "Nvim Makes Code a Joy Again"
date: 2023-06-26T03:08:44Z
draft: false
categories:
  -  Code
image: "nvim-screenshot-2.png"
---
I spent some time setting up neovim on my server, and man was it worth it. It has all the functionality of VSCode, and really, it puts it to shame. I like it better than any editor I've ever used. Usually I'm fussing around with the mouse, and moaning and complaining. But once I set up nvim and got used to the basic vim style navigation, I will never use another code editor. I'm currently using it to write this blog. Even as a blog editor it blows all others out of the water. 

{{< picture "nvim-screenshot-2.png" "nvim-screenshot-2.png" "Screenshot of my NEOVIM setup">}}
***My Neovim Setup Running in a standard terminal***

### Vim Basics
If you haven't used vim before, you should learn the basic vim commands. They work the same within neovim.
It takes a little while to get used to, but trust me, it's worth practicing. I usually do not enjoy text editing, but vim makes text editing a joy instead of a hassle. I can be pretty dyslexic sometimes, and vim makes it much easier for me to find things, get where I need to be and it helps me avoid the usual clumsy mistakes I make in the standard editors like VSCode. No kidding. When you first see how it works, tit is not intuitively obvious that vim is a better system. But people swear by it, and now I see why.

#### After learning the basics try a few of these!

My favorite standard vim command is "c", then "i", then '"' (change in quote). 
You can also do ci{, or ci(, or ci[. It removes anything within the delimeter and enters you into edit mode. 
c,i,w will change the word under the cursor. 

Go to previous edit position, whichever file it was, with ctrl-o, and next with ctrl-i

### The Tutorial for setting up Neovim

Follow the tutorial at the bottom for a setup that will put vscode to shame. It includes language support for all the major languages and file formats. Nvim is notoriously difficult to set up, but I followed the tutorial step by step. It only took about an hour and there was not one glitch. I got a few error messages for my own typos, but the error messages were very clear as to the problem. He explains everything too.  

#### NOTE: I lied. There was one mistake in the tutorial that I forgot.  
**nvim-tree.lua should look like the code below:**
~/.config/nvim/lua/core/plugin_config/nvim-tree.lua
```lua
vim.g.loaded_netrw = 1
vim.g.loaded_netrwPlugin = 1

require('nvim-tree').setup() 
vim.keymap.set('n', '<c-n>', ':NvimTreeToggle<CR>')
```
He had put ':NvimFileTreeToggle<CR>' in the last line. All the rest is the same.
Don't worry about remembering that, just follow the turorial. The error message will make it pretty obvious when to come back and take a look at the above code.

### Intellisense and Copilot
Neovim also supports Intellisense and Copilot.
I managed to install both but it took a few days. But I wasn't using the methods outlined in this tutorial. I suspect it would have been pretty easy if I watched this tutorial first, and then looked up how to install them using lua like he is doing.

{{< youtube J9yqSdvAKXY>}}
