import random
import time

class KAILASH:
    def __init__(self):
        self.greetings = ["Hello, I am KAILASH. How can I assist you today?",
                          "Greetings! This is KAILASH. How may I help you?",
                          "Welcome! I'm KAILASH. What can I do for you today?"]
    
    def greet_user(self):
        print(random.choice(self.greetings))
    
    def process_command(self, command):
        if "hello" in command.lower():
            print("Hello! How can I assist you?")
        elif "time" in command.lower():
            current_time = time.strftime("%H:%M:%S", time.localtime())
            print(f"The current time is {current_time}")
        elif "thank you" in command.lower() or "thanks" in command.lower():
            print("You're welcome!")
        elif "goodbye" in command.lower() or "bye" in command.lower():
            print("Goodbye! Have a great day!")
            return True
        else:
            print("I'm sorry, I didn't understand that command.")

def main():
    kailash = KAILASH()
    kailash.greet_user()
    
    while True:
        command = input("Your command: ")
        if kailash.process_command(command):
            break

if __name__ == "__main__":
    main()
