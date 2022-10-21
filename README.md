import os
from libraryArsein.Arsein import Robot_Rubika
os.system("clear")
from random import choice
import pyfiglet
from start import program
red = '\033[31m' 
green = '\033[32m' 
blue = '\033[36m' 
pink = '\033[35m' 
yellow = '\033[93m' 
darkblue = '\033[34m' 
white = '\033[00m'
text = "  YASIN BOT"

bot = Robot_Rubika("YOUR_AUTH")
link="GROUP_LINK"
program()
group_guid=bot.joinGroup(link)["data"]["group"]["group_guid"]
group_name=bot.joinGroup(link)["data"]["group"]['group_title']
group_members=bot.joinGroup(link)["data"]["group"]['count_members']
print(f"{darkblue}group name : {red}{group_name} \n {darkblue}group guid : {red}{group_guid} \n {darkblue}group count_members : {red}{group_members}")
while (1):
	bot.joinGroup(link)
	print(yellow+"bot join group !!!")
	bot.leaveGroup(group_guid)
	print(green+"bot leave group !!!")
