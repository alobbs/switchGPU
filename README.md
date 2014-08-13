#switchGPU
If your Mac has two graphic cards, switchGPU makes your Mac automatically use the integrated GPU when you login. This is useful for people who want to save energy, but also for people who face issues with their discrete GPU, e.g. [a lot of Macbook Pro 2011 owners][1] of who the discrete GPU causes lots of trouble (like crashes, reboots, etc.)

This program is just a wrapper for gfxCardStatus, but the latter doesn't have an option to set a default and it has an frustrating bug that requires the user to tick a GPU version twice; switchGPU addresses those problems.

Tested on a late 2011 Macbook with Mavericks, but it should work on most models.

##Installation
Download the Automator file and drag it to your programs folder. Go to 'System settings > Users and groups > Log in' and add switchGPU from the programs folder using the plus sign. Tick the box in the dialog and you're good to go: switchGPU will start the next time you login.

##How it works
When you login, the automator program will start the integrated switchGPU script that installs gfxCardStatus at its first run. Next, the script will start gfxCardStatus three times consecutively to address the problem of the selection (which GPU) not being preserved immediately.

##Credits
[gfxCardStatus][2]

[MacOH][3] - The switchGPU script is actually a stripped and slightly edited version of the macoh.sh script.


  [1]: http://www.mbp2011.com/
  [2]: http://gfx.io/
  [3]: https://github.com/qnxor/macoh
