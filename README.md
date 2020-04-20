# Python Mission Chief Bot Linux

This repo is specifically for use with Linux servers, so that you can run the bot for 24 hours a day.

## How to run the bot 24/7
Want to know how to run a bot for 24 hours a day? Sure, I can show you.

1. First of all I'd recommened setting up a Digital Ocean account, or any other cloud provider. You can set an account for Digital Ocean [here](https://m.do.co/c/741cf5923606) (It's a referral link)

(Make sure you install docker if you're going outside of DO)

2. Once you've signed up to Digital Ocean simply create a droplet. You can install docker straight to it via the marketplace so i'd suggest doing that. (You can use any droplet, this will work on the smallest $5 A month one)

3. Connect into the droplet, you can do this via going to the Access Console or alternatively SSH into the droplet.

4. Once you're in type in `docker pull jjbayliss/missionchief`, let it run it'll set up the image for the bot. 
 
5. Once the image is done simply run `docker run -it -d jjbayliss/missionchief`. This will create a container for you.

6. Run `docker ps -a` and copy the name of your container there should only be one, then run `docker exec -it [container name] bash` this will take you into the container in a bash.

7. You should be brought straight into a container, all you'll need to do is `cd missionchief/config` and then do `vim config.ini` 
You'll want to press the `I` key to edit the document, and add your username, password and region. Once done press `ESC` and type `:wq` this will save the document.

8. Run `cd ../ && bash run.sh` to run the base bot. If you require the despatcher please create another container, but instead run bash run-d.sh. (Just repeat from step 5) - Seems to be an issue if you try and run two chromium instances on one container.

9. To exit the docker container press `CTRL + D`, and if you need to enter the bot again just follow from step 6.

Did you find this useful? Why not buy me a beer!? [donate](https://www.paypal.me/jackbaylissdev)


## License
This work is licensed under the Creative Commons Attribution-NonCommercial 4.0 International License
see license [here](https://github.com/codesidian/Python-MissionChiefBot/blob/master/LICENSE.md)

## Disclaimer
Please be aware, this is simply a guide on how to get the bot running using docker to make it simple. I hold no responsibility on what you do with it.

Section 7.2 of the MissionChief official rules state:
`Use of tools, scripts, bots or other computer programs:Users are not allowed to use tools, scripts, bots or other computer programs which are suitable for the automatic execution of actions in a game.`

No developers of this bot hold any responsibility for your use of it. We make no warranties about the effectiveness, or performance of this bot. If you're banned, that's on you. 

**USE AT YOUR OWN RISK**
