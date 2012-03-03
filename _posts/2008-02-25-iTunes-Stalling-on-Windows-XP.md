---
layout: post
title: "iTunes Stalling on Windows XP"
category:
tags: []
---
{% include JB/setup %}
I have been meaning to write this little tutorial ever since I fixed my iTunes on windows XP. I have a pretty good computer (3.4 ghz 1Gb ram), so I was confused when switching from WinAmp to iTunes to find my music randomly stalling. If i was running something process intensive like compiling or even just loading a new program my music would stutter on XP. I search around the web and found that others were having this problem, but not many had a good solution. After browsing around the web, I found that the stuttering in my music was caused when iTunes didn't get enough of the CPU to process the music file. So when something would jump up and use 90% of my CPU iTunes would happily stop processing the music because it didn't have a high enough process priority to keep a couple percent of CPU for itself. When playing music in the background iTunes only needs 3%-4% to play the music.

So now knowing the problem I searched for solutions and many just said that every time they started iTunes they would open the Windows Task Manager go to the processes tab and right click on iTunes to set the priority of the process to high. This did in fact work, but now I had to do that every time that I openned iTunes which was really annoying. So I continued looking for a better solution. There are special windows programs out there, most of them cost money, that will monitor which processes are running on the system and automatically change the process priority on any app you tell the system to increase the priority to whatever settings you choose. This seemed like and OK solution but now having an app running all the time checking my processes and just some other app that could cause problems, seemed bad. It also seems that processes aren't as stable if you switch their priority after they begin, it is best to set the priority as they are started. So off searching for a solution I found that you can start processes in does and pass what priority you want to start the process. So I decided to just hack up a little script which would launch iTunes from dos with a process priority of 'High'.

to run a windows app at a different process priority than the default you can create a file named "appName.bat" (in this case iTunes.bat), place this file in the same directory as the executable you want to run with a higher priority. Then edit the bat file (you can edit it in notepad). Add this line to the file

start /high iTunes.exe

(or start /priority_setting application.exe)

Save your bat file... Now all you have to do is create shortcuts to the new bat file instead of the shortcuts pointing directly the application.

To create a shortcut right click on your bat file and select 'Create Shortcut'. If you want the shortcut to have the same icon as the original app instead of the dos icon, right click the shortcut and got to properties, then the 'Shortcut' tab, and click Change Icon. Select browse an application to search for an icon in, then select the application you are creating a shortcut for (in this case iTunes.exe), it will display the available icons select the one your want.

Anyways, I hope this helps anyone else having trouble getting audio to play smooth on windows XP with iTunes. I have also used this method to speed up some other processes that I always want running full speed on windows, with pretty good success.