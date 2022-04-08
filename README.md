# Daily-task-assistant
#This repository contains simple codes to carry out minor day-to-day tasks (in python).

#ACTUAL CODE BEGINS HERE ON!!!!!!!
#Executable (Error-free) python program for while-exam countdown
name = input("Enter your name (Advisable to capitalise whole name): ")
import datetime
now = datetime.datetime.now()


import time

def countdown(time_sec):
    while time_sec:
        mins, secs = divmod(time_sec, 60)
        timeformat = '{:02d}:{:02d}'.format(mins, secs)
        print(timeformat, end='\r')
        time.sleep(1)
        time_sec -= 1

    print("Hello", name, "\nYour time is up!!")
print("              Note: If you wanna start the test then click ENTER!!")
timeneeded = int(input("What is the duration of the exam? (Advisable to give time in MINUTES): "))
inminutes = timeneeded * 60
print ("\nExam debuted time: ", now.strftime("%d-%m-%Y %H:%M:%S"))
print("\nREMAINING!!")
countdown(inminutes)
now = datetime.datetime.now()
print ("\nExam terminated time: ", now.strftime("%d-%m-%Y %H:%M:%S"))
