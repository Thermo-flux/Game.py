import string
import random
import time
import readchar
green = "\033[92m"
red = "\033[91m"
grey = "\033[90m"
reset = "\033[0m"
print ("Welcome to Type-Racer!")
Name = input ("Please Enter Your Name And Press Enter:-")
print(f"Hi {Name}!")
difficulty = int(input("Please select difficulty:\n1 for Easy\n2 for Medium\n3 for Hard\n4 for INSANE\n5 for PRO-Grammer\n Choice: "))
if difficulty == 1 :
 characters = string.ascii_lowercase
 word_length = 5
elif difficulty == 2 :
 characters = string.ascii_letters
 word_length = 8
elif difficulty == 3 :
 characters = string.ascii_letters + string.digits
 word_length = 10
elif difficulty == 4 :
 characters = string.ascii_letters + string.digits + string.punctuation
 word_length = 15
elif difficulty == 5 :
   characters = string.punctuation
   word_length = 22  
   print(f"Be Ready to Shit your Pants Dear {Name}!!")
else :
 print("Please Retry and Enter a Valid Difficulty!")
round_number = 1
score = 0
streak = 0
completed_rounds = 0
total_WPM = 0
level = 1
while True :
    if round_number == 1:
        print("\nGet ready!")
        time.sleep(2)
    else:
        time.sleep (1.5)
        print("\nReady for the next round?")
        print("3...") 
        time.sleep (1)
        print ("2...") 
        time.sleep (1)
        print ("1..") 
        time.sleep(1)

    round_number += 1
    Word = "".join(random.choices(characters, k=word_length)) 
    print (f"here you go!:- {Word}")
    typed_characters = []
    total_keystrokes = 0
    start_time = None
    Word_Boilerplate = "".join ([f"{grey}{char}{reset}" for char in Word])
    print(f"\r Go!:- {Word_Boilerplate}", end="", flush=True)
    while len(typed_characters) < len(Word):
        key = readchar.readkey()

        if start_time is None:
            start_time = time.time()

        if key == readchar.key.BACKSPACE:
            if len(typed_characters) > 0:
                typed_characters.pop()
        elif key.isprintable() and len(key) == 1:
            total_keystrokes += 1
            typed_characters.append(key)

        Display = []
        for position_number, character in enumerate(Word):
            if position_number < len(typed_characters):
                if typed_characters[position_number] == character:
                    Display.append(f"{green}{character}{reset}")
                else:
                    Display.append(f"{red}{typed_characters[position_number]}{reset}")
            else:
                Display.append(f"{grey}{character}{reset}")

        print("\r GO!:- " + " ".join(Display), end="", flush=True)

    print()
    end_time = time.time()
    typed_word = "".join(typed_characters)
    total_time = end_time - start_time
    if typed_word == Word :
        print ("PERFECT MATCH! Good Job!")
        WPM = (len(typed_word) / 5 / total_time) * 60
        accuracy = (len(Word) / max(total_keystrokes, len(Word))) * 100
        print (f"\nYou Typed it in {total_time:.2f} Seconds!\n With A Speed of {WPM:.0f} WPM\n And {accuracy} Accuracy! ")
    else :
        user_answer = input ("OOPS! Wrong Word Entered! press y to Retry!")
        if user_answer.lower() != "y" :
            print ("Thank You for Playing!")
            break

       


            
        


        
        

        
        

        


      
  



 


   



