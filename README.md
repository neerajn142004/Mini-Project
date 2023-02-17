# Mini-Project
Aritificial Intelligence Minor Project 


import time

def countdown(t):
    while t:
        mins, secs = divmod(t, 60)
        time_left = "{:02d}:{:02d}".format(mins, secs)
        print(time_left, end='\r')
        time.sleep(1)
        t -= 1
    print('Countdown complete!')

def start_countdown(t):
    print('Starting countdown...')
    countdown(t)

def main():
    t = int(input("Enter the countdown time in seconds: "))
    start_countdown(t)
    while True:
        user_input = input('Enter "r" to reset, "s" to stop, "p" to pause/resume, "q" to quit: ')
        if user_input == 'r':
            t = int(input("Enter the new countdown time in seconds: "))
            start_countdown(t)
        elif user_input == 's':
            break
        elif user_input == 'p':
            if user_input == 'p':
                while True:
                    user_input = input('Enter "r" to resume, "s" to stop, "q" to quit: ')
                    if user_input == 'r':
                        break
                    elif user_input == 's':
                        return
                    elif user_input == 'q':
                        return

if _name_ == '_main_':
    main()
