# Hangman_Test__
A git error necessitated that the repo be remade

Milestone 1
*in milestone 1 a simple function was created which asks the user for an input

Milestone 2
*in milestone 2 object oriented programming (OOP) was used and the attributes were initialised, OOP was used due to the number of variables that will be repeatedly updated and used multiple times.
```python
   def __init__(self, word_list, num_lives=5):
        self.word = random.choice(word_list)
        self.word_guessed = list(len(self.word)*'_')
        self.num_letter = len(set(self.word))
        self.num_lives = num_lives
        self.list_letters = []

        print(f'the mystery word has {len(self.word)} characters')
        print(self.word_guessed)
```
Milestone 3:
*in milestone 3 the ask_letter method was completed, checks were put in to evaluate if the letter input by the user was present in the word
*If the letter input was indeed in the word blank spaces would be filled by the entered letter
*If the letter wasn't in the word the number of lives would go down by 1
```python
 def ask_letter(self):
        while True:
            letter = input('Enter a single character: ').lower()
            if len(letter) == 1 and letter in self.list_letters:
                print(f'{letter} was already tried')
            elif len(letter) == 1 and letter not in self.list_letters:
                print('Thank you')
                self.list_letters.append(letter)
                self.check_letter(letter)
                if self.num_lives == 4:
                    print('____')
                    print('|   |')
                    print('|    ')
                    print('|    ')
                    print('|    ')
                    print('|____')
                if self.num_lives == 3:
                    print('____')
                    print('|   |')
                    print('|   o')
                    print('|    ')
                    print('|    ')
                    print('|____')
                if self.num_lives == 2:
                    print('____')
                    print('|   |')
                    print('|   o')
                    print('|   |')
                    print('|    ')
                    print('|____')
                if self.num_lives == 1:
                    print('____')
                    print('|   |')
                    print('|   o')
                    print('|  \|/')
                    print('|    ')
                    print('|____')
                if self.num_lives == 0:
                    print(f'You ran out of lives. The word was {self.word}')
                    print('____')
                    print('|   |')
                    print('|   o')
                    print('|  \|/')
                    print('|  / \ ')
                    print('|____')
                    return
                if '_' not in self.word_guessed:
                    print('Congratulations, you won!')
                    return
        else:
            print('Please, enter just one character')
```
*as can be seen on line 33 the check_letter method is called which checks if the letter is in the word
note: the code for the hangman illustration is from the final milestone

Milestone 4:
*The logic of the game was programmed (please refer to the latter part of the code copied above), if the user entered a letter and it wasn't in the word a life was minued and the hangman diagram was cloder to being complete
*If it was in the word it would appear in the blank spaces of the word

![image](https://user-images.githubusercontent.com/99564434/177201477-460d355d-ea43-4661-b43a-991a8e6976ac.png)

        
