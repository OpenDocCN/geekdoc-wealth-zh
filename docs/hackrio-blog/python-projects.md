# 30 个酷、简单、有趣的 Python 项目及其源代码[2023]

> 原文：<https://hackr.io/blog/python-projects>

今天，我们正在经历绝大多数商业部门对人工智能(AI)、机器学习(ML)和数据科学的不断采用。这些领域的一个主要共同点是它们以这样或那样的方式使用 [Python 编程语言](https://hackr.io/blog/python-programming-language)。

成为 Python 大师可以为你的职业生涯打开许多大门，让你获得世界上最好的工作机会。不管您当前的 Python 能力如何，知道如何构建 Python 项目是提高您的技能和构建您的投资组合的一种万无一失的方式。

虽然 [Python 书籍](https://hackr.io/blog/best-python-books-for-beginners-and-advanced-programmers)和 [Python 教程](https://hackr.io/tutorials/learn-python?ref=blog-post)非常有用，但是没有什么比亲自动手做一些实际的编码和尝试 Python 项目想法更好的了！

在本文中，我们列出了 30 个有趣的 Python 项目，从适合初学者的简单 Python 项目到中级和高级 Python 项目想法，您可以用它们来挑战自己或提高您的 Python 编程技能。

## **面向初学者的 Python 项目**

### **1。疯狂 Libs 发生器**

这是最有趣的初学 Python 项目之一，更不用说它让你练习如何使用字符串、变量和连接。

Mad Libs 生成器收集用户输入数据，并将其作为形容词、代词和动词进行处理。程序获取这些数据，并对其进行排列以构建一个故事。

**源代码:**

```
'''
Mad Libs Generator
-------------------------------------------------------------
'''

# Questions for the user to answer

noun = input('Choose a noun: ')

p_noun = input('Choose a plural noun: ')

noun2 = input('Choose a noun: ')

place = input('Name a place: ')

adjective = input('Choose an adjective (Describing word): ')

noun3 = input('Choose a noun: ')

# Print a story from the user input

print('------------------------------------------')

print('Be kind to your', noun, '- footed', p_noun)

print('For a duck may be somebody\'s', noun2, ',')

print('Be kind to your', p_noun, 'in', place)

print('Where the weather is always', adjective, '. \n')

print('You may think that is this the', noun3, ',')

print('Well it is.')

print('------------------------------------------') 
```

### **2。数字猜测**

这个初级 Python 项目是一个有趣的游戏，它生成一个随机数(在一定范围内)，用户在收到提示后必须猜出这个随机数。用户每猜错一次，就会收到额外的提示，但代价是降低最终分数。

这个程序是试验 Python 标准库的好方法，因为它使用 Python *random* 模块来生成随机数。您还可以获得一些关于条件语句、打印格式和用户定义函数的实践。

**源代码:**

```
'''
Number Guessing Game
-------------------------------------------------------------
'''

import random

attempts_list = []

def show_score():
  if not attempts_list:
      print('There is currently no high score, it\'s yours for the taking!')

  else:
      print(f'The current high score is {min(attempts_list)} attempts')

def start_game():
   attempts = 0
   rand_num = random.randint(1, 10)
   print('Hello traveler! Welcome to the game of guesses!')
   player_name = input('What is your name? ')
   wanna_play = input(
       f'Hi, {player_name}, would you like to play the guessing game?'
       '(Enter Yes/No): ')

   if wanna_play.lower() != 'yes':
      print('That\'s cool, Thanks!')
      exit()
   else:
       show_score()

   while wanna_play.lower() == 'yes':
       try:
           guess = int(input('Pick a number between 1 and 10: '))
           if guess < 1 or guess > 10:
               raise ValueError(
                   'Please guess a number within the given range')

           attempts += 1
           attempts_list.append(attempts)

           if guess == rand_num:
               print('Nice! You got it!')
               print(f'It took you {attempts} attempts')
               wanna_play = input(
                   'Would you like to play again? (Enter Yes/No): ')
               if wanna_play.lower() != 'yes':
                   print('That\'s cool, have a good one!')
                   break
               else:
                   attempts = 0
                   rand_num = random.randint(1, 10)
                   show_score()
                   continue
           else:
               if guess > rand_num:
                   print('It\'s lower')
               elif guess < rand_num:
                   print('It\'s higher')

       except ValueError as err:
           print('Oh no!, that is not a valid value. Try again...')
           print(err)

if __name__ == '__main__':
   start_game() 
```

### **3。石头剪刀布**

这个石头剪子布程序用函数和条件语句模拟了普遍流行的游戏。那么，有什么更好的方法来掌握这些关键概念呢？

作为许多导入额外库的 Python 编码项目之一，这个程序使用了标准库的 *random* 、 *os* 和 *re* 模块。

看一下下面的代码，您会发现这个 Python 项目思想要求用户通过传入一个代表石头、布或剪刀的字符来迈出第一步。在评估输入字符串之后，条件逻辑检查获胜者。

**源代码:**

```
'''
Rock Paper Scissors
-------------------------------------------------------------
'''

import random
import os
import re

def check_play_status():
  valid_responses = ['yes', 'no']
  while True:
      try:
          response = input('Do you wish to play again? (Yes or No): ')
          if response.lower() not in valid_responses:
              raise ValueError('Yes or No only')

          if response.lower() == 'yes':
              return True
          else:
              os.system('cls' if os.name == 'nt' else 'clear')
              print('Thanks for playing!')
              exit()

      except ValueError as err:
          print(err)

def play_rps():
   play = True
   while play:
       os.system('cls' if os.name == 'nt' else 'clear')
       print('')
       print('Rock, Paper, Scissors - Shoot!')

       user_choice = input('Choose your weapon'
                           ' [R]ock], [P]aper, or [S]cissors: ')

       if not re.match("[SsRrPp]", user_choice):
           print('Please choose a letter:')
           print('[R]ock, [P]aper, or [S]cissors')
           continue

       print(f'You chose: {user_choice}')

       choices = ['R', 'P', 'S']
       opp_choice = random.choice(choices)

       print(f'I chose: {opp_choice}')

       if opp_choice == user_choice.upper():
           print('Tie!')
           play = check_play_status()
       elif opp_choice == 'R' and user_choice.upper() == 'S':
           print('Rock beats scissors, I win!')
           play = check_play_status()
       elif opp_choice == 'S' and user_choice.upper() == 'P':
           print('Scissors beats paper! I win!')
           play = check_play_status()
       elif opp_choice == 'P' and user_choice.upper() == 'R':
           print('Paper beats rock, I win!')
           play = check_play_status()
       else:
           print('You win!\n')
           play = check_play_status()

if __name__ == '__main__':
   play_rps()
```

### **4。掷骰子发生器**

作为与代码初学者最相关的 Python 项目之一，这个程序模拟滚动一个或两个骰子。这也是巩固您对用户定义的函数、循环和条件语句的理解的好方法。

作为 Python easy 项目之一，这是一个相当简单的程序，它使用 Python *random* 模块来复制掷骰子的随机性。你还会注意到，在你掷骰子之后，我们使用*操作系统*模块来清空屏幕。

请注意，您可以将最大骰子值更改为任何数字，从而模拟许多棋盘和角色扮演游戏中经常使用的多面体骰子。

**源代码:**

```
'''
Dice Roll Generator
-------------------------------------------------------------
'''

import random
import os

def num_die():
  while True:
      try:
          num_dice = input('Number of dice: ')
          valid_responses = ['1', 'one', 'two', '2']
          if num_dice not in valid_responses:
              raise ValueError('1 or 2 only')
          else:
              return num_dice
      except ValueError as err:
          print(err)

def roll_dice():
   min_val = 1
   max_val = 6
   roll_again = 'y'

   while roll_again.lower() == 'yes' or roll_again.lower() == 'y':
       os.system('cls' if os.name == 'nt' else 'clear')
       amount = num_die()

       if amount == '2' or amount == 'two':
           print('Rolling the dice...')
           dice_1 = random.randint(min_val, max_val)
           dice_2 = random.randint(min_val, max_val)

           print('The values are:')
           print('Dice One: ', dice_1)
           print('Dice Two: ', dice_2)
           print('Total: ', dice_1 + dice_2)

           roll_again = input('Roll Again? ')
       else:
           print('Rolling the die...')
           dice_1 = random.randint(min_val, max_val)
           print(f'The value is: {dice_1}')

           roll_again = input('Roll Again? ')

if __name__ == '__main__':
   roll_dice()
```

### **5。刽子手游戏**

这是一个有趣的 Python 项目想法，用来模拟猜词游戏 Hangman。我们在猜测方面使用了一个预定义的单词列表，但是可以通过使用第三方字典 API 来改进它。

这个 Python 项目使用循环、函数和字符串格式来打印刽子手的进度。它还可以让你试验标准库的*随机*、*时间*和*操作系统*模块。

具体来说，我们使用了*随机*模块来选择要猜的单词，使用了*操作系统*模块来清空屏幕，使用了*时间*模块的*。sleep()* 功能引入暂停，增强游戏流程。

**源代码:**

```
'''
Hangman Game
-------------------------------------------------------------
'''

import random
import time
import os

def play_again():
  question = 'Do You want to play again? y = yes, n = no \n'
  play_game = input(question)
  while play_game.lower() not in ['y', 'n']:
      play_game = input(question)

  if play_game.lower() == 'y':
      return True
  else:
      return False

def hangman(word):
  display = '_' * len(word)
  count = 0
  limit = 5
  letters = list(word)
  guessed = []
  while count < limit:
      guess = input(f'Hangman Word: {display} Enter your guess: \n').strip()
      while len(guess) == 0 or len(guess) > 1:
          print('Invalid input. Enter a single letter\n')
          guess = input(
              f'Hangman Word: {display} Enter your guess: \n').strip()

      if guess in guessed:
          print('Oops! You already tried that guess, try again!\n')
          continue

      if guess in letters:
          letters.remove(guess)
          index = word.find(guess)
          display = display[:index] + guess + display[index + 1:]

      else:
          guessed.append(guess)
          count += 1
          if count == 1:
              time.sleep(1)
              print('   _____ \n'
                    '  |      \n'
                    '  |      \n'
                    '  |      \n'
                    '  |      \n'
                    '  |      \n'
                    '  |      \n'
                    '__|__\n')
              print(f'Wrong guess: {limit - count} guesses remaining\n')

          elif count == 2:
              time.sleep(1)
              print('   _____ \n'
                    '  |     | \n'
                    '  |     | \n'
                    '  |      \n'
                    '  |      \n'
                    '  |      \n'
                    '  |      \n'
                    '__|__\n')
              print(f'Wrong guess: {limit - count} guesses remaining\n')

          elif count == 3:
              time.sleep(1)
              print('   _____ \n'
                    '  |     | \n'
                    '  |     | \n'
                    '  |     | \n'
                    '  |      \n'
                    '  |      \n'
                    '  |      \n'
                    '__|__\n')
              print(f'Wrong guess: {limit - count} guesses remaining\n')

          elif count == 4:
              time.sleep(1)
              print('   _____ \n'
                    '  |     | \n'
                    '  |     | \n'
                    '  |     | \n'
                    '  |     O \n'
                    '  |      \n'
                    '  |      \n'
                    '__|__\n')
              print(f'Wrong guess: {limit - count} guesses remaining\n')

          elif count == 5:
              time.sleep(1)
              print('   _____ \n'
                    '  |     | \n'
                    '  |     | \n'
                    '  |     | \n'
                    '  |     O \n'
                    '  |    /|\ \n'
                    '  |    / \ \n'
                    '__|__\n')
              print('Wrong guess. You\'ve been hanged!!!\n')
              print(f'The word was: {word}')

      if display == word:
          print(f'Congrats! You have guessed the word \'{word}\' correctly!')
          break

def play_hangman():
   print('\nWelcome to Hangman\n')
   name = input('Enter your name: ')
   print(f'Hello {name}! Best of Luck!')
   time.sleep(1)
   print('The game is about to start!\nLet\'s play Hangman!')
   time.sleep(1)
   os.system('cls' if os.name == 'nt' else 'clear')

   words_to_guess = [
       'january', 'border', 'image', 'film', 'promise', 'kids',
       'lungs', 'doll', 'rhyme', 'damage', 'plants', 'hello', 'world'
   ]
   play = True
   while play:
       word = random.choice(words_to_guess)
       hangman(word)
       play = play_again()

   print('Thanks For Playing! We expect you back again!')
   exit()

if __name__ == '__main__':
  play_hangman() 
```

### **6。密码强度检查器**

这个 Python 项目让您检查您的密码是否足够强。

它通过检查给定密码中的字母、数字、特殊字符和空白字符的数量，并根据这些结果生成分数。因此，这是学习条件语句、函数和字符串格式的另一个好方法。

我们还使用 Python 标准库中的*字符串*和 *getpass* 模块。这允许我们访问全部的字符串字符来与我们的密码的字符组成进行比较，而*。getpass()* 函数让我们在输入密码时隐藏密码。

**源代码:**

```
'''
Password Strength Checker
-------------------------------------------------------------
'''

import string
import getpass

def check_password_strength():
   password = getpass.getpass('Enter the password: ')
   strength = 0
   remarks = ''
   lower_count = upper_count = num_count = wspace_count = special_count = 0

   for char in list(password):
       if char in string.ascii_lowercase:
           lower_count += 1
       elif char in string.ascii_uppercase:
           upper_count += 1
       elif char in string.digits:
           num_count += 1
       elif char == ' ':
           wspace_count += 1
       else:
           special_count += 1

   if lower_count >= 1:
       strength += 1
   if upper_count >= 1:
       strength += 1
   if num_count >= 1:
       strength += 1
   if wspace_count >= 1:
       strength += 1
   if special_count >= 1:
       strength += 1

   if strength == 1:
       remarks = ('That\'s a very bad password.'
           ' Change it as soon as possible.')
   elif strength == 2:
       remarks = ('That\'s a weak password.'
           ' You should consider using a tougher password.')
   elif strength == 3:
       remarks = 'Your password is okay, but it can be improved.'
   elif strength == 4:
       remarks = ('Your password is hard to guess.'
           ' But you could make it even more secure.')
   elif strength == 5:
       remarks = ('Now that\'s one hell of a strong password!!!'
           ' Hackers don\'t have a chance guessing that password!')

   print('Your password has:-')
   print(f'{lower_count} lowercase letters')
   print(f'{upper_count} uppercase letters')
   print(f'{num_count} digits')
   print(f'{wspace_count} whitespaces')
   print(f'{special_count} special characters')
   print(f'Password Score: {strength / 5}')
   print(f'Remarks: {remarks}')

def check_pwd(another_pw=False):
   valid = False
   if another_pw:
       choice = input(
           'Do you want to check another password\'s strength (y/n) : ')
   else:
       choice = input(
           'Do you want to check your password\'s strength (y/n) : ')

   while not valid:
       if choice.lower() == 'y':
           return True
       elif choice.lower() == 'n':
           print('Exiting...')
           return False
       else:
           print('Invalid input...please try again. \n')

if __name__ == '__main__':
   print('===== Welcome to Password Strength Checker =====')
   check_pw = check_pwd()
   while check_pw:
       check_password_strength()
       check_pw = check_pwd(True)
```

### **7。字数**

这个 Python 项目的思想是将用户输入的整数转换成等价的单词。这个程序被设置为支持最多 12 位的数字，但是可以随意修改程序来处理更大的数字(提示:需要条件语句和循环)。

作为基本 Python 项目的一个易于理解的例子，这个简单但有效的程序可以用循环、用户输入和条件语句扩展您的技能，更不用说 Python 元组和列表了。

您还可以尝试一些新的数学运算，比如用模(%)运算符来返回整数除法的余数。

**源代码:**

```
'''
Numbers To Words
-------------------------------------------------------------
'''

ones = (
   'Zero', 'One', 'Two', 'Three', 'Four',
   'Five', 'Six', 'Seven', 'Eight', 'Nine'
   )

twos = (
   'Ten', 'Eleven', 'Twelve', 'Thirteen', 'Fourteen',
    'Fifteen', 'Sixteen', 'Seventeen', 'Eighteen', 'Nineteen'
   )

tens = (
   'Twenty', 'Thirty', 'Forty', 'Fifty', 'Sixty',
    'Seventy', 'Eighty', 'Ninety', 'Hundred'
   )

suffixes = (
   '', 'Thousand', 'Million', 'Billion'
   )

def fetch_words(number, index):
   if number == '0': return 'Zero'

   number = number.zfill(3)
   hundreds_digit = int(number[0])
   tens_digit = int(number[1])
   ones_digit = int(number[2])

   words = '' if number[0] == '0' else ones[hundreds_digit]

   if words != '':
       words += ' Hundred '

   if tens_digit > 1:
       words += tens[tens_digit - 2]
       words += ' '
       words += ones[ones_digit]
   elif(tens_digit == 1):
       words += twos[((tens_digit + ones_digit) % 10) - 1]
   elif(tens_digit == 0):
       words += ones[ones_digit]

   if(words.endswith('Zero')):
       words = words[:-len('Zero')]
   else:
       words += ' '

   if len(words) != 0:
       words += suffixes[index]

   return words

def convert_to_words(number):
   length = len(str(number))
   if length > 12:
       return 'This program supports a maximum of 12 digit numbers.'

   count = length // 3 if length % 3 == 0 else length // 3 + 1
   copy = count
   words = []

   for i in range(length - 1, -1, -3):
       words.append(fetch_words(
           str(number)[0 if i - 2 < 0 else i - 2 : i + 1], copy - count))

       count -= 1

   final_words = ''
   for s in reversed(words):
       final_words += (s + ' ')

   return final_words

if __name__ == '__main__':
   number = int(input('Enter any number: '))
   print('%d in words is: %s' %(number, convert_to_words(number)))
```

### **8 .TIC-tac-toe〔t1〕**

井字游戏是一种经典的双人游戏，包含一个九方形的格子。每个玩家交替地用 O 或 X 标记他们的空间，无论哪个玩家设法对角地、水平地或垂直地标记三个 O 或 X，就获胜。每个玩家还必须阻止他们的对手，同时试图使他们的链。

这是最有趣的 Python 项目之一，对于初学者来说也是独一无二的，因为它使用面向对象编程来创建一个名为 TicTacToe 的新类。我们用这个通过类属性和方法来表示游戏的特性。

仔细研究这些方法，看看我们如何使用面向对象的编程来巧妙地包装模拟这个游戏所需的各种行为。

对于初学者来说，这个 Python 项目思想的一些新方面包括嵌套循环，用于检查网格的列、行和对角线，以及 Python *set* 数据类型，用于包含唯一值。这个程序也使用了 Python *random* 模块来选择一个随机玩家开始游戏，不过这个你现在更熟悉了。

**源代码:**

**9。计算器**

```
'''
Tic Tac Toe
-------------------------------------------------------------
'''

import random

class TicTacToe:

   def __init__(self):
       self.board = []

   def create_board(self):
       for i in range(3):
           row = []
           for j in range(3):
               row.append('-')
           self.board.append(row)

   def get_random_first_player(self):
       return random.randint(0, 1)

   def fix_spot(self, row, col, player):
       self.board[row][col] = player

   def has_player_won(self, player):
       n = len(self.board)
       board_values = set()

       # check rows
       for i in range(n):
           for j in range(n):
               board_values.add(self.board[i][j])

           if board_values == {player}:
               return True
           else:
               board_values.clear()

       # check cols
       for i in range(n):
           for j in range(n):
               board_values.add(self.board[j][i])

           if board_values == {player}:
               return True
           else:
               board_values.clear()

       # check diagonals
       for i in range(n):
           board_values.add(self.board[i][i])
       if board_values == {player}:
           return True
       else:
           board_values.clear()

       board_values.add(self.board[0][2])
       board_values.add(self.board[1][1])
       board_values.add(self.board[2][0])
       if board_values == {player}:
           return True
       else:
           return False

   def is_board_filled(self):
       for row in self.board:
           for item in row:
               if item == '-':
                   return False
       return True

   def swap_player_turn(self, player):
       return 'X' if player == 'O' else 'O'

   def show_board(self):
       for row in self.board:
           for item in row:
               print(item, end=' ')
           print()

   def start(self):
       self.create_board()
       player = 'X' if self.get_random_first_player() == 1 else 'O'
       game_over = False

       while not game_over:
           try:
               self.show_board()
               print(f'\nPlayer {player} turn')

               row, col = list(
                   map(int, input(
                       'Enter row & column numbers to fix spot: ').split()))
               print()

               if col is None:
                   raise ValueError(
                       'not enough values to unpack (expected 2, got 1)')

               self.fix_spot(row - 1, col - 1, player)

               game_over = self.has_player_won(player)
               if game_over:
                   print(f'Player {player} wins the game!')
                   continue

               game_over = self.is_board_filled()
               if game_over:
                   print('Match Draw!')
                   continue

               player = self.swap_player_turn(player)

           except ValueError as err:
               print(err)

       print()
       self.show_board()

if __name__ == '__main__':
  tic_tac_toe = TicTacToe()
  tic_tac_toe.start()
```

### 作为 easy Python 项目之一，这个程序创建了一个基本的计算器应用程序，具有加、减、乘和除的功能。

这是 Python 实践项目之一，对于学习如何使用循环、函数、条件语句、用户输入和字符串格式非常有用。我们还使用 Python *os* 模块在用户完成计算动作后清空屏幕。

**样本代码:**

10。倒计时钟和计时器

```
'''
Calculator
-------------------------------------------------------------
'''

import os

def addition():
   os.system('cls' if os.name == 'nt' else 'clear')
   print('Addition')

   continue_calc = 'y'

   num_1 = float(input('Enter a number: '))
   num_2 = float(input('Enter another number: '))
   ans = num_1 + num_2
   values_entered = 2
   print(f'Current result: {ans}')

   while continue_calc.lower() == 'y':
       continue_calc = (input('Enter more (y/n): '))
       while continue_calc.lower() not in ['y', 'n']:
           print('Please enter \'y\' or \'n\'')
           continue_calc = (input('Enter more (y/n): '))

       if continue_calc.lower() == 'n':
           break
       num = float(input('Enter another number: '))
       ans += num
       print(f'Current result: {ans}')
       values_entered += 1
   return [ans, values_entered]

def subtraction():
   os.system('cls' if os.name == 'nt' else 'clear')
   print('Subtraction')

   continue_calc = 'y'

   num_1 = float(input('Enter a number: '))
   num_2 = float(input('Enter another number: '))
   ans = num_1 - num_2
   values_entered = 2
   print(f'Current result: {ans}')

   while continue_calc.lower() == 'y':
       continue_calc = (input('Enter more (y/n): '))
       while continue_calc.lower() not in ['y', 'n']:
           print('Please enter \'y\' or \'n\'')
           continue_calc = (input('Enter more (y/n): '))

       if continue_calc.lower() == 'n':
           break
       num = float(input('Enter another number: '))
       ans -= num
       print(f'Current result: {ans}')
       values_entered += 1
   return [ans, values_entered]

def multiplication():
   os.system('cls' if os.name == 'nt' else 'clear')
   print('Multiplication')

   continue_calc = 'y'

   num_1 = float(input('Enter a number: '))
   num_2 = float(input('Enter another number: '))
   ans = num_1 * num_2
   values_entered = 2
   print(f'Current result: {ans}')

   while continue_calc.lower() == 'y':
       continue_calc = (input('Enter more (y/n): '))
       while continue_calc.lower() not in ['y', 'n']:
           print('Please enter \'y\' or \'n\'')
           continue_calc = (input('Enter more (y/n): '))

       if continue_calc.lower() == 'n':
           break
       num = float(input('Enter another number: '))
       ans *= num
       print(f'Current result: {ans}')
       values_entered += 1
   return [ans, values_entered]

def division():
   os.system('cls' if os.name == 'nt' else 'clear')
   print('Division')

   continue_calc = 'y'

   num_1 = float(input('Enter a number: '))
   num_2 = float(input('Enter another number: '))
   while num_2 == 0.0:
       print('Please enter a second number > 0')
       num_2 = float(input('Enter another number: '))

   ans = num_1 / num_2
   values_entered = 2
   print(f'Current result: {ans}')

   while continue_calc.lower() == 'y':
       continue_calc = (input('Enter more (y/n): '))
       while continue_calc.lower() not in ['y', 'n']:
           print('Please enter \'y\' or \'n\'')
           continue_calc = (input('Enter more (y/n): '))

       if continue_calc.lower() == 'n':
           break
       num = float(input('Enter another number: '))
       while num == 0.0:
           print('Please enter a number > 0')
           num = float(input('Enter another number: '))
       ans /= num
       print(f'Current result: {ans}')
       values_entered += 1
   return [ans, values_entered]

def calculator():
   quit = False
   while not quit:
       results = []
       print('Simple Calculator in Python!')
       print('Enter \'a\' for addition')
       print('Enter \'s\' for substraction')
       print('Enter \'m\' for multiplication')
       print('Enter \'d\' for division')
       print('Enter \'q\' to quit')

       choice = input('Selection: ')

       if choice == 'q':
           quit = True
           continue

       if choice == 'a':
           results = addition()
           print('Ans = ', results[0], ' total inputs: ', results[1])
       elif choice == 's':
           results = subtraction()
           print('Ans = ', results[0], ' total inputs: ', results[1])
       elif choice == 'm':
           results = multiplication()
           print('Ans = ', results[0], ' total inputs: ', results[1])
       elif choice == 'd':
           results = division()
           print('Ans = ', results[0], ' total inputs: ', results[1])
       else:
           print('Sorry, invalid character')

if __name__ == '__main__':
   calculator()
```

### 这个 Python 项目想法很好玩！在这里，我们创建了一个倒计时器，通过用户输入询问用户秒数，然后它一秒一秒地倒计时，直到显示一条消息。

我们已经使用了 Python *时间*模块的*。sleep()* 功能以 1 秒的间隔暂停。我们将它与一些漂亮的字符串格式结合起来，产生倒计时显示。

**源代码:**

**11。二分搜索法算法**

```
'''
Countdown Timer
-------------------------------------------------------------
'''

import time

def countdown(user_time):
   while user_time >= 0:
       mins, secs = divmod(user_time, 60)
       timer = '{:02d}:{:02d}'.format(mins, secs)
       print(timer, end='\r')
       time.sleep(1)
       user_time -= 1
   print('Lift off!')

if __name__ == '__main__':
   user_time = int(input("Enter a time in seconds: "))
   countdown(user_time)
```

### 对于所有有抱负的程序员来说，在某个时候在他们的 Python 编程项目中解决二分搜索法问题是一个必经之路！

这个针对二分搜索法的 Python 项目接收一个*排序的*列表(数组)，然后不断地将一个搜索值与数组的中间值进行比较。

根据搜索值是小于还是大于中间值，列表被分割(分而治之策略)以减少搜索空间，这集中在给定的搜索值上。这种连续的划分导致了对数时间复杂度。

如果你看下面的代码，你会发现我们实现了两个解决方案:条件循环和递归。这两种方法都很好，所以可以随意尝试。

如果你是递归的新手，这是一个很好的介绍，因为它展示了我们如何通过每次递归调用来“减少”问题的大小，即通过将列表分割到当前中间元素的一侧。

我们还将递归的基本情况定义为中间元素等于搜索元素的点。在这种情况下，递归将停止，并通过调用堆栈向上返回真值。

**源代码:**

**12。合并排序算法**

```
'''
Binary Search
-------------------------------------------------------------
'''

def binary_search(a_list, an_item):
   first = 0
   last = len(a_list) - 1

   while first <= last:
       mid_point = (first + last) // 2
       if a_list[mid_point] == an_item:
           return True
       else:
           if an_item < a_list[mid_point]:
               last = mid_point - 1
           else:
               first = mid_point + 1
   return False

def binary_search_rec(a_list, first, last, an_item):
   if len(a_list) == 0:
       return False
   else:
       mid_point = (first + last) // 2
       if a_list[mid_point] == an_item:
           return True
       else:
           if an_item < a_list[mid_point]:
               last = mid_point - 1
               return binary_search_rec(a_list, first, last, an_item)
           else:
               first = mid_point + 1
               return binary_search_rec(a_list, first, last, an_item)

if __name__ == '__main__':
   a_list = [1, 4, 7, 10, 14, 19, 102, 2575, 10000]

   print('Binary Search:', binary_search(a_list, 4))
   print('Binary Search Recursive:',
       binary_search_rec(a_list, 0, len(a_list) -1, 4))
```

### 合并排序是另一个流行的编码挑战，当有抱负的程序员在 Python 中寻找事情做的时候会面临这个挑战。

这种*分治*策略使用除法将一系列数字分成相等的部分，然后在重新组合生成排序列表之前对这些部分进行递归排序。

如果你刚刚完成了二分搜索法的例子，你可能会注意到除法和缩小问题规模的一些相似之处。你是对的，这意味着你可能已经意识到我们需要使用递归。

这个合并排序的 Python 实现使用递归来处理分而治之的过程。问题规模的不断缩小使得问题在达到递归基本情况时，即问题规模为一个元素或更少时，得以解决。

本质上，这个 Python 程序继续递归地划分列表，直到到达基本情况。此时，它开始对问题的较小部分进行排序，产生较小的排序数组，这些排序数组被重新组合，最终生成一个完全排序的数组。如果你熟悉大 O 符号，你会很好奇合并排序有一个大 O(n logn)。

**源代码:**

13。密码生成器

```
'''
Merge Sort
-------------------------------------------------------------
'''

def merge_sort(a_list):
   print("Dividing ", a_list)

   if len(a_list) > 1:
       mid_point = len(a_list)//2
       left_half = a_list[:mid_point]
       right_half = a_list[mid_point:]

       merge_sort(left_half)
       merge_sort(right_half)

       i=0
       j=0
       k=0

       while i < len(left_half) and j < len(right_half):
           if left_half[i] <= right_half[j]:
               a_list[k] = left_half[i]
               i += 1
           else:
               a_list[k] = right_half[j]
               j += 1
           k += 1

       while i < len(left_half):
           a_list[k] = left_half[i]
           i += 1
           k += 1

       while j < len(right_half):
           a_list[k] = right_half[j]
           j += 1
           k += 1

   print("Merging ", a_list)

if __name__ == '__main__':
   a_list = [45, 7, 85, 24, 60, 25, 38, 63, 1]
   merge_sort(a_list)
   print(a_list)
```

### 这是一个有趣的 Python 项目，它使用*秘密*和*字符串*模块来生成一个强大而安全的密码，就像您可以使用流行的密码管理器一样。

*string* 模块获取所有可能的字母、数字和特殊字符，而 *secrets* 模块允许我们获取加密安全的密码。

这个项目的代码相对简单，因为它使用一个循环来不断生成密码，直到它包含至少一个特殊字符和两个数字。当然，您可以修改它来适应您自己的超强密码规则！

**源代码:**

**14。货币转换器**

```
'''
Password Generator
-------------------------------------------------------------
'''

import secrets
import string

def create_pw(pw_length=12):
   letters = string.ascii_letters
   digits = string.digits
   special_chars = string.punctuation

   alphabet = letters + digits + special_chars
   pwd = ''
   pw_strong = False

   while not pw_strong:
       pwd = ''
       for i in range(pw_length):
           pwd += ''.join(secrets.choice(alphabet))

       if (any(char in special_chars for char in pwd) and
               sum(char in digits for char in pwd) >= 2):
           pw_strong = True

   return pwd

if __name__ == '__main__':
   print(create_pw())
```

### 这是几个 Python 项目想法之一，要求我们[安装一个新的 Python 库](https://hackr.io/blog/top-python-libraries)，在这种情况下，*请求*模块。Python 标准库不包括这个，所以使用源代码中显示的 pip 命令将其安装到您的系统上。

使用*请求*模块，我们可以向固定器 API 发出 *HTTP* 请求，允许我们将一种货币转换成另一种货币。你可能会注意到我们正在使用第三方 API，所以你需要注册来获得一个免费的 API 密钥[这里](https://apilayer.com/marketplace/fixer-api#pricing)。然后，您可以在源代码中显示的字段中输入您的 API 密钥，您就可以开始了！

这个项目允许您获得更多关于循环和用户输入的实践，但是它扩展了 HTTP 请求来检索 JSON 格式的 API 数据。

如果您不熟悉 JSON，它非常类似于 Python 字典，这意味着我们可以访问键值对来获取我们想要的数据。在本例中，我们从 API 调用中寻找货币转换结果。

查看 Fixer API 站点上的文档，了解可以检索的不同数据的更多详细信息。

**源代码:**

15。自动发送生日邮件

```
'''
Currency Converter
-------------------------------------------------------------
pip install requests
'''

import requests

def convert_currency():
   init_currency = input('Enter an initial currency: ')
   target_currency = input('Enter a target currency: ')

   while True:
       try:
           amount = float(input('Enter the amount: '))
       except:
           print('The amount must be a numeric value!')
           continue

       if not amount > 0:
           print('The amount must be greater than 0')
           continue
       else:
           break

   url = ('https://api.apilayer.com/fixer/convert?to='
          + target_currency + '&from=' + init_currency +
          '&amount=' + str(amount))

   payload = {}
   headers = {'apikey': 'YOUR API KEY'}
   response = requests.request('GET', url, headers=headers, data=payload)
   status_code = response.status_code

   if status_code != 200:
       print('Uh oh, there was a problem. Please try again later')
       quit()

   result = response.json()
   print('Conversion result: ' + str(result['result']))

if __name__ == '__main__':
   convert_currency()
```

### 这个 Python 项目使用了标准的 *smtplib* 、 *EmailMessage、*和 *datetime* 模块，此外还有 *pandas* 和 *openpyxl* (这些需要 pip 安装，如下所示)来发送自动化的生日邮件。

这个程序从一个包含你所有朋友的详细信息的 excel 表格中读取(见下面源代码中的 excel 表格格式)。如果今天是他们的大日子，它会给他们发一封电子邮件，然后在你的电子表格中注明他们已经收到了他们的电子邮件。

我们已经使用了 *smtplib* 和 *EmailMessage* 模块来创建到我们的电子邮件帐户和消息的 SSL 连接。然后，我们使用一个*熊猫*数据帧在 Python 程序中存储电子表格风格的数据(这是数据科学家的一项基本技能)。最后，我们在 *datetime* 模块的*中使用了日期格式。strftime()* 函数。

所以，有很多新技能需要掌握！

**重要提示:**自 2022 年 5 月以来，谷歌收紧了对“不太安全的应用”访问 Gmail 的限制。您需要遵循一些额外的步骤才能在您的 Gmail 帐户中使用此代码。但是不要担心，它们很容易做到，我们已经为你列出来了。

转到您的 google 帐户的“管理帐户”页面

*   点击安全
*   启用 2FA(使用您喜欢的任何方法)
*   点击“应用程序密码”
*   点击“选择应用程序”，然后选择“邮件”
*   点击“选择设备”并选择“其他(自定义名称)”，进入“Python 生日应用程序”
*   点击“生成”，然后保存该密码
*   现在，您可以在下面的代码中使用此应用程序密码来轻松访问您的 Gmail 帐户！

**源代码:**

16。队列

```
'''
Birthday Email Sender
-------------------------------------------------------------
pip install pandas openpyxl
excel file cols:
Name, Email, Birthday (MM/DD/YYYY), Last Sent (YYYY)
'''

import pandas as pd
from datetime import datetime
import smtplib
from email.message import EmailMessage

def send_email(recipient, subject, msg):
   GMAIL_ID = 'your_email_here'
   GMAIL_PWD = 'your_password_here'

   email = EmailMessage()
   email['Subject'] = subject
   email['From'] = GMAIL_ID
   email['To'] = recipient
   email.set_content(msg)

   with smtplib.SMTP_SSL('smtp.gmail.com', 465) as gmail_obj:
       gmail_obj.ehlo()
       gmail_obj.login(GMAIL_ID, GMAIL_PWD)
       gmail_obj.send_message(email)
   print('Email sent to ' + str(recipient) + ' with Subject: \''
         + str(subject) + '\' and Message: \'' + str(msg) + '\'')

def send_bday_emails(bday_file):
   bdays_df = pd.read_excel(bday_file)
   today = datetime.now().strftime('%m-%d')
   year_now = datetime.now().strftime('%Y')
   sent_index = []

   for idx, item in bdays_df.iterrows():
       bday = item['Birthday'].to_pydatetime().strftime('%m-%d')
       if (today == bday) and year_now not in str(item['Last Sent']):
           msg = 'Happy Birthday ' + str(item['Name'] + '!!')
           send_email(item['Email'], 'Happy Birthday', msg)
           sent_index.append(idx)

   for idx in sent_index:
       bdays_df.loc[bdays_df.index[idx], 'Last Sent'] = str(year_now)

   bdays_df.to_excel(bday_file, index=False)

if __name__ == '__main__':
   send_bday_emails(bday_file='your_bdays_list.xlsx')
```

### 这个 Python 项目创建了一个新类来实现一个*队列*。这是计算机科学中一种常见的数据结构，当你需要处理先进先出(FIFO)的情况时，比如消息队列、CPU 任务等。

代码简单明了，并提供了更多面向对象编程的实践。测试队列，了解它是如何工作的，然后就可以在其他项目中使用这个数据结构了。

**源代码:**

**17。帕斯卡三角形**

```
'''
Queue Data Structure
-------------------------------------------------------------
'''

class Queue:

   def __init__(self):
       self.items = []

   def __repr__(self):
       return f'Queue object: data={self.items}'

   def is_empty(self):
       return not self.items

   def enqueue(self, item):
       self.items.append(item)

   def dequeue(self):
       return self.items.pop(0)

   def size(self):
       return len(self.items)

   def peek(self):
       return self.items[0]

if __name__ == '__main__':
   q = Queue()
   print(q.is_empty())
   q.enqueue('First')
   q.enqueue('Second')
   print(q)
   print(q.dequeue())
   print(q)
   print(q.size())
   print(q.peek())
```

### 这个 Python 项目利用条件语句和循环打印出了帕斯卡三角形。它还使用标准库的*数学*模块和*阶乘*函数来计算用于生成三角形中的值的“组合数”等式。

试验三角形的种子数，以检查如何使用“组合”等式在三角形中生成连续值。

**源代码:**

18。二十一点

```
'''
Pascal's Triangle
-------------------------------------------------------------
Number of combinations via "n choose k" or nCk = n! / [k! * (n-k)!]
'''

from math import factorial

def pascal_triangle(n):
   for i in range(n):
       for j in range(n-i+1):
           print(end=' ')

       for j in range(i+1):

           print(factorial(i)//(factorial(j)*factorial(i-j)), end=' ')

       print()

if __name__ == '__main__':
   pascal_triangle(5)
```

### 作为最酷的 Python 项目之一，这将吸引任何喜欢纸牌游戏的人，因为我们将模仿 21 点。这是一个超级流行的纸牌游戏，规则相对简单:最重要的是你需要 21 分才能赢，或者你需要比庄家更高的分数才能不破产！

这是迄今为止列表中最大的项目。它结合了我们在以前的项目中已经介绍过的大部分技能，包括创建类、循环、条件语句、导入模块、接受用户输入和字符串格式化。

花点时间研究这段代码的不同部分，并将其与早期的项目联系起来，看看不同的技术如何协同工作。没有你没见过的；它只是被稍微不同地打包并组合在一起，以创建一个全功能的游戏模拟器。

我们应该说，尽量不要整天玩它！但是如果你做了，我们完全理解！

**源代码:**

**19 号。Reddit bot**

```
'''
Blackjack
-------------------------------------------------------------
'''

import random
import os

class Card:

   def __init__(self, card_face, value, symbol):
       self.card_face = card_face
       self.value = value
       self.symbol = symbol

def show_cards(cards, hidden):
   s = ''
   for card in cards:
       s = s + '\t ________________'
   if hidden:
       s += '\t ________________'
   print(s)

   s = ''
   for card in cards:
       s = s + '\t|                |'
   if hidden:
       s += '\t|                |'
   print(s)

   s = ''
   for card in cards:
       if card.card_face in ['J', 'Q', 'K', 'A']:
           s = s + '\t|  {}             |'.format(card.card_face)
       elif card.value == 10:
           s = s + '\t|  {}            |'.format(card.value)
       else:
           s = s + '\t|  {}             |'.format(card.value)

   if hidden:
       s += '\t|                |'
   print(s)

   s = ''
   for card in cards:
       s = s + '\t|                |'
   if hidden:
       s += '\t|      * *       |'
   print(s)

   s = ''
   for card in cards:
       s = s + '\t|                |'
   if hidden:
       s += '\t|    *     *     |'
   print(s)

   s = ''
   for card in cards:
       s = s + '\t|                |'
   if hidden:
       s += '\t|   *       *    |'
   print(s)

   s = ''
   for card in cards:
       s = s + '\t|                |'
   if hidden:
       s += '\t|   *       *    |'
   print(s)

   s = ''
   for card in cards:
       s = s + '\t|       {}        |'.format(card.symbol)
   if hidden:
       s += '\t|          *     |'
   print(s)

   s = ''
   for card in cards:
       s = s + '\t|                |'
   if hidden:
       s += '\t|         *      |'
   print(s)

   s = ''
   for card in cards:
       s = s + '\t|                |'
   if hidden:
       s += '\t|        *       |'
   print(s)

   s = ''
   for card in cards:
       s = s + '\t|                |'
   if hidden:
       s += '\t|                |'
   print(s)

   s = ''
   for card in cards:
       s = s + '\t|                |'
   if hidden:
       s += '\t|                |'
   print(s)

   s = ''
   for card in cards:
       if card.card_face in ['J', 'Q', 'K', 'A']:
           s = s + '\t|            {}   |'.format(card.card_face)
       elif card.value == 10:
           s = s + '\t|           {}   |'.format(card.value)
       else:
           s = s + '\t|            {}   |'.format(card.value)
   if hidden:
       s += '\t|        *       |'
   print(s)

   s = ''
   for card in cards:
       s = s + '\t|________________|'
   if hidden:
       s += '\t|________________|'
   print(s)
   print()

def deal_card(deck):
   card = random.choice(deck)
   deck.remove(card)
   return card, deck

def play_blackjack(deck):
   player_cards = []
   dealer_cards = []
   player_score = 0
   dealer_score = 0
   os.system('clear')

   while len(player_cards) < 2:
       player_card, deck = deal_card(deck)
       player_cards.append(player_card)
       player_score += player_card.value

       # If dealt a second Ace, adjust player score
       if len(player_cards) == 2:
           if player_cards[0].value == 11 and player_cards[1].value == 11:
               player_cards[0].value = 1
               player_score -= 10

       print('PLAYER CARDS: ')
       show_cards(player_cards, False)
       print('PLAYER SCORE = ', player_score)

       input('Continue...')

       dealer_card, deck = deal_card(deck)
       dealer_cards.append(dealer_card)
       dealer_score += dealer_card.value

       # If dealt a second Ace, adjust dealer score
       # Note: adjusts 2nd card to hide that the dealer has an Ace
       if len(dealer_cards) == 2:
           if dealer_cards[0].value == 11 and dealer_cards[1].value == 11:
               dealer_cards[1].value = 1
               dealer_score -= 10

       print('DEALER CARDS: ')
       if len(dealer_cards) == 1:
           show_cards(dealer_cards, False)
           print('DEALER SCORE = ', dealer_score)
       else:
           show_cards(dealer_cards[:-1], True)
           print('DEALER SCORE = ', dealer_score - dealer_cards[-1].value)

       input('Continue...')

   if player_score == 21:
       print('PLAYER HAS A BLACKJACK!!!!')
       print('PLAYER WINS!!!!')
       quit()
   os.system('clear')

   print('DEALER CARDS: ')
   show_cards(dealer_cards[:-1], True)
   print('DEALER SCORE = ', dealer_score - dealer_cards[-1].value)
   print()
   print('PLAYER CARDS: ')
   show_cards(player_cards, False)
   print('PLAYER SCORE = ', player_score)

   while player_score < 21:
       choice = input('Enter H to Hit or S to Stand: ').upper()
       if len(choice) != 1 or (choice not in ['H', 'S']):
           os.system('clear')
           print('Invalid choice!! Try Again...')
           continue

       if choice.upper() == 'S':
           break
       else:
           player_card, deck = deal_card(deck)
           player_cards.append(player_card)
           player_score += player_card.value
           card_pos = 0

           # If dealt an Ace, adjust score for each existing Ace in hand
           while player_score > 21 and card_pos < len(player_cards):
               if player_cards[card_pos].value == 11:
                   player_cards[card_pos].value = 1
                   player_score -= 10
                   card_pos += 1
               else:
                   card_pos += 1

           if player_score > 21:
               break

           os.system('clear')
           print('DEALER CARDS: ')
           show_cards(dealer_cards[:-1], True)
           print('DEALER SCORE = ', dealer_score - dealer_cards[-1].value)
           print()
           print('PLAYER CARDS: ')
           show_cards(player_cards, False)
           print('PLAYER SCORE = ', player_score)

   os.system('clear')
   print('PLAYER CARDS: ')
   show_cards(player_cards, False)
   print('PLAYER SCORE = ', player_score)
   print()
   print('DEALER IS REVEALING THEIR CARDS....')
   print('DEALER CARDS: ')
   show_cards(dealer_cards, False)
   print('DEALER SCORE = ', dealer_score)

   if player_score == 21:
       print('PLAYER HAS A BLACKJACK, PLAYER WINS!!!')
       quit()

   if player_score > 21:
       print('PLAYER BUSTED!!! GAME OVER!!!')
       quit()

   input('Continue...')
   while dealer_score < 17:
       os.system('clear')
       print('DEALER DECIDES TO HIT.....')
       dealer_card, deck = deal_card(deck)
       dealer_cards.append(dealer_card)
       dealer_score += dealer_card.value

       # If dealt an Ace, adjust score for each existing Ace in hand
       card_pos = 0
       while dealer_score > 21 and card_pos < len(dealer_cards):
           if dealer_cards[card_pos].value == 11:
               dealer_cards[card_pos].value = 1
               dealer_score -= 10
               card_pos += 1
           else:
               card_pos += 1

       print('PLAYER CARDS: ')
       show_cards(player_cards, False)
       print('PLAYER SCORE = ', player_score)
       print()
       print('DEALER CARDS: ')
       show_cards(dealer_cards, False)
       print('DEALER SCORE = ', dealer_score)
       if dealer_score > 21:
           break
       input('Continue...')

   if dealer_score > 21:
       print('DEALER BUSTED!!! YOU WIN!!!')
       quit()
   elif dealer_score == 21:
       print('DEALER HAS A BLACKJACK!!! PLAYER LOSES!!!')
       quit()
   elif dealer_score == player_score:
       print('TIE GAME!!!!')
   elif player_score > dealer_score:
       print('PLAYER WINS!!!')
   else:
       print('DEALER WINS!!!')

def init_deck():
   suits = ['Spades', 'Hearts', 'Clubs', 'Diamonds']
   # UNICODE values for card symbol images
   suit_symbols = {'Hearts': '\u2661', 'Diamonds': '\u2662',
                   'Spades': '\u2664', 'Clubs': '\u2667'}
   cards = {'A': 11, '2': 2, '3': 3, '4': 4, '5': 5, '6': 6,
            '7': 7, '8': 8, '9': 9, '10': 10, 'J': 10, 'Q': 10, 'K': 10}
   deck = []
   for suit in suits:
       for card, value in cards.items():
           deck.append(Card(card, value, suit_symbols[suit]))
   return deck

if __name__ == '__main__':
   deck = init_deck()
   play_blackjack(deck)
```

### 这个 Python 项目创建了一个带有一些新模块的自动化 reddit 机器人，即 *praw* 和 *enchant* (参见 pip 安装命令)。

这是一个相当简单的概念，因为程序会检查所选子编辑中的每个评论，然后回复任何包含预定义“触发短语”的评论。为此，我们使用 *praw* 模块与 reddit 交互，并使用 *enchant* 生成与评论相似的词，从而允许我们做出适当的回复。

如果你正在寻找 Python 项目来学习如何在你自己的 subreddit 中回答问题，这个想法真的很有用。您只需要扩展这段代码，使其包含对预定义问题的自动响应(您可能已经注意到 reddit 上的其他人正在使用它！).

**重要提示:**您需要查看[这些说明](https://github.com/reddit-archive/reddit/wiki/OAuth2-Quick-Start-Example#first-steps)以获得客户端 id、客户端密码、用户名、密码和用户代理。您将需要这些信息来通过 API 接口向 reddits 添加评论。

**源代码:**

20。斐波那契发生器

```
'''
Reddit Reply Bot
-------------------------------------------------------------
pip install praw pyenchant
'''

import praw
import enchant

def reddit_bot(sub, trigger_phrase):
   reddit = praw.Reddit(
       client_id='your_client_id',
       client_secret='your_client_secret',
       username='your_username',
       password='your_pw',
       user_agent='your_user_agent'
   )

   subreddit = reddit.subreddit(sub)
   dict_suggest = enchant.Dict('en_US')

   for comment in subreddit.stream.comments():
       if trigger_phrase in comment.body.lower():
           word = comment.body.replace(trigger_phrase, '')
           reply_text = ''
           similar_words = dict_suggest.suggest(word)
           for similar in similar_words:
               reply_text += (similar + ' ')
           comment.reply(reply_text)

if __name__ == '__main__':
   reddit_bot(sub='Python', trigger_phrase='useful bot')
```

### 斐波那契数列可能是我们生活中最重要的一些数字，因为它们在自然界中经常出现。

下面的 Python 代码使用递归生成特定长度的斐波那契数(是的，更多的递归！).为了防止计算时间失控，我们在计算时实现了内存化来缓存值。

您会注意到，对于这个递归算法，基本情况是检查给定的斐波那契数列值是否已经存储在缓存中。如果是这样的话，它返回这个(这是一个恒定时间复杂度的操作)，这节省了大量的计算时间。

**源代码:**

**高级 Python 项目创意**

```
'''
Fibonacci Sequence
-------------------------------------------------------------
'''

fib_cache = {}

def fib_memo(input_val):
   if input_val in fib_cache:
       return fib_cache[input_val]

   if input_val == 0:
       val = 0
   elif input_val < 2:
       val = 1
   else:
       val = fib_memo(input_val - 1) + fib_memo(input_val - 2)

   fib_cache[input_val] = val
   return val

if __name__ == '__main__':
   print('======== Fibonacci Series ========')
   for i in range(1, 11):
       print(f'Fibonacci ({i}) : {fib_memo(i)}')
```

## **21 号。聊天机器人〔t1〕**

### 这个 Python 项目使用 *chatterbot* 模块(参见下面的 pip 安装说明)来训练一个自动聊天机器人回答你提出的任何问题！我知道；我们现在用的是 AI！

您将看到该程序是这个列表中相对较小的 Python 项目之一，但是如果您想了解更多或扩展代码的功能，请随意探索 ChatterBot 文档以及更广泛的 AI 聊天机器人领域。

**重要提示:** ChatterBot 不再被主动维护。这意味着您需要对位于 Python 安装文件夹的“Lib/site-packages/chatterbot”目录中的 tagging.py 文件做一个小小的更改。

不用担心；这很容易做到，我们已经包含了您需要使用的确切源代码，如下所示。

**源代码:**

**修改 tagging.py:**

```
'''
Chat Bot
-------------------------------------------------------------
1) pip install ChatterBot chatterbot-corpus spacy
2) python3 -m spacy download en_core_web_sm
   Or... choose the language you prefer
3) Navigate to your Python3 directory
4) Modify Lib/site-packages/chatterbot/tagging.py
  to properly load 'en_core_web_sm'
'''

from chatterbot import ChatBot
from chatterbot.trainers import ChatterBotCorpusTrainer

def create_chat_bot():
   chatbot = ChatBot('Chattering Bot')
   trainer = ChatterBotCorpusTrainer(chatbot)
   trainer.train('chatterbot.corpus.english')

   while True:
       try:
           bot_input = chatbot.get_response(input())
           print(bot_input)

       except (KeyboardInterrupt, EOFError, SystemExit):
           break

if __name__ == '__main__':
   create_chat_bot()
```

查找属于 PosLemmaTagger 类的 __init__ 方法的第一段代码。将其替换为 *if/else* 语句。

**注意:**这个例子是针对我们在例子中使用的英语库的，但是如果你愿意的话，可以自由地将它切换到另一种语言。

**22。文本到语音转换**

```
# Replace this:
self.nlp = spacy.load(self.language.ISO_639_1.lower())

# With this:
if self.language.ISO_639_1.lower() == 'en':
   self.nlp = spacy.load('en_core_web_sm')
else:
   self.nlp = spacy.load(self.language.ISO_639_1.lower())
```

### 这个 Python 项目使用一系列新的库将现有的文章转换成可播放的 mp3 文件。您需要安装 *nltk* (自然语言工具箱)、*报业 3k、*和 *gtts* (参见 pip 安装说明)。

您会看到这个程序很简单，我们只需传入一个要转换的文章的 URL，然后让我们定义的函数用我们新安装的模块处理文本到语音的转换。

所以，下次你想把一篇文章变成一个可播放的播客时，考虑试试这个，因为它绝对是值得复制的很酷的 Python 代码之一！

**源代码:**

**23。图书馆管理系统**

```
'''
Text To Speech
-------------------------------------------------------------
pip install nltk newspaper3k gtts
'''

import nltk
from newspaper import Article
from gtts import gTTS

def text_to_speech(url):
   article = Article(url)
   article.download()
   article.parse()
   nltk.download('punkt')
   article.nlp()
   article_text = article.text
   language = 'en'
   my_obj = gTTS(text=article_text, lang=language, slow=False)
   my_obj.save("read_article.mp3")

if __name__ == '__main__':
   text_to_speech(
       url='https://hackr.io/blog/top-tech-companies-hiring-python-developers'
   )
```

### 作为更高级的 Python 项目之一，这个程序使用面向对象编程来模拟一个图书馆管理系统。

在这个例子中，我们创建了一个库和学生类，我们可以用它来创建我们的库系统及其用户。然后，我们实现了一个简单的用户界面，要求用户从一系列标准的图书馆操作中进行选择，比如借书或还书。

这是一个简单而强大的例子，说明了如何通过 Python 和面向对象编程构建真实世界的系统。请随意扩展这些类，以包含其他有用的特性，如唯一的图书 id、同一本书的多个副本、还书日期、延迟还书的费用，或者您认为图书馆应该具有的任何其他特性！

**源代码:**

**24。乒乓街机游戏**

```
'''
Library
-------------------------------------------------------------
'''

class Library:

   def __init__(self, books):
       self.books = books

   def show_avail_books(self):
       print('Our Library Can Offer You The Following Books:')
       print('================================================')
       for book, borrower in self.books.items():
           if borrower == 'Free':
               print(book)

   def lend_book(self, requested_book, name):
       if self.books[requested_book] == 'Free':
           print(
               f'{requested_book} has been marked'
               f' as \'Borrowed\' by: {name}')
           self.books[requested_book] = name
           return True
       else:
           print(
               f'Sorry, the {requested_book} is currently'
               f' on loan to: {self.books[requested_book]}')
           return False

   def return_book(self, returned_book):
       self.books[returned_book] = 'Free'
       print(f'Thanks for returning {returned_book}')

class Student:
   def __init__(self, name, library):
       self.name = name
       self.books = []
       self.library = library

   def view_borrowed(self):
       if not self.books:
           print('You haven\'t borrowed any books')
       else:
           for book in self.books:
               print(book)

   def request_book(self):
       book = input(
           'Enter the name of the book you\'d like to borrow >> ')
       if self.library.lend_book(book, self.name):
           self.books.append(book)

   def return_book(self):
       book = input(
           'Enter the name of the book you\'d like to return >> ')
       if book in self.books:
           self.library.return_book(book)
       else:
           print('You haven\'t borrowed that book, try another...')

def create_lib():
   books = {
       'The Last Battle': 'Free',
       'The Hunger Games': 'Free',
       'Cracking the Coding Interview': 'Free'
   }
   library = Library(books)
   student_example = Student('Your Name', library)

   while True:
       print('''
           ==========LIBRARY MENU===========
           1\. Display Available Books
           2\. Borrow a Book
           3\. Return a Book
           4\. View Your Books
           5\. Exit'''
             )

       choice = int(input('Enter Choice: '))
       if choice == 1:
           print()
           library.show_avail_books()
       elif choice == 2:
           print()
           student_example.request_book()
       elif choice == 3:
           print()
           student_example.return_book()
       elif choice == 4:
           print()
           student_example.view_borrowed()
       elif choice == 5:
           print('Goodbye')
           exit()

if __name__ == '__main__':
   create_lib()
```

### 这是一个非常有趣的项目，因为我们已经使用 Python *turtle* 模块来模拟经典街机游戏 Pong！

我们使用了来自*海龟*模块的各种方法来创建我们的游戏组件，并检测球与玩家球拍的碰撞。我们还定义了一系列键绑定来设置左右玩家控制。请随意试验游戏的设置，以更好地了解每个设置如何工作以及如何影响整个游戏。

除了这些新引入的 *turtle* 图形函数，我们还使用了字符串格式来输出当前的记分牌和用户定义的函数，以保持代码整洁。这些是你在这个阶段应该熟悉的概念。

**源代码:**

**25。速度打字测试**

```
'''
Pong Arcade Game
-------------------------------------------------------------
'''

import turtle

def update_score(l_score, r_score, player, score_board):
   if player == 'l':
       l_score += 1
   else:
       r_score += 1

   score_board.clear()
   score_board.write('Left Player: {} -- Right Player: {}'.format(
       l_score, r_score), align='center',
       font=('Arial', 24, 'normal'))
   return l_score, r_score, score_board

def setup_game():
   screen = turtle.Screen()
   screen.title('Pong Arcade Game')
   screen.bgcolor('white')
   screen.setup(width=1000, height=600)

   l_paddle = turtle.Turtle()
   l_paddle.speed(0)
   l_paddle.shape('square')
   l_paddle.color('red')
   l_paddle.shapesize(stretch_wid=6, stretch_len=2)
   l_paddle.penup()
   l_paddle.goto(-400, 0)

   r_paddle = turtle.Turtle()
   r_paddle.speed(0)
   r_paddle.shape('square')
   r_paddle.color('black')
   r_paddle.shapesize(stretch_wid=6, stretch_len=2)
   r_paddle.penup()
   r_paddle.goto(400, 0)

   ball = turtle.Turtle()
   ball.speed(40)
   ball.shape('circle')
   ball.color('blue')
   ball.penup()
   ball.goto(0, 0)
   ball.dx = 5
   ball.dy = -5

   score_board = turtle.Turtle()
   score_board.speed(0)
   score_board.color('blue')
   score_board.penup()
   score_board.hideturtle()
   score_board.goto(0, 260)
   score_board.write('Left Player: 0 -- Right Player: 0',
                     align='center', font=('Arial', 24, 'normal'))

   return screen, ball, l_paddle, r_paddle, score_board

def pong_game():
   game_components = setup_game()
   screen = game_components[0]
   ball = game_components[1]
   l_paddle = game_components[2]
   r_paddle = game_components[3]
   score_board = game_components[4]
   l_score = 0
   r_score = 0

   def l_paddle_up():
       l_paddle.sety(l_paddle.ycor() + 20)

   def l_paddle_down():
       l_paddle.sety(l_paddle.ycor() - 20)

   def r_paddle_up():
       r_paddle.sety(r_paddle.ycor() + 20)

   def r_paddle_down():
       r_paddle.sety(r_paddle.ycor() - 20)

   screen.listen()
   screen.onkeypress(l_paddle_up, 'e')
   screen.onkeypress(l_paddle_down, 'x')
   screen.onkeypress(r_paddle_up, 'Up')
   screen.onkeypress(r_paddle_down, 'Down')

   while True:
       screen.update()
       ball.setx(ball.xcor()+ball.dx)
       ball.sety(ball.ycor()+ball.dy)

       if ball.ycor() > 280:
           ball.sety(280)
           ball.dy *= -1

       if ball.ycor() < -280:
           ball.sety(-280)
           ball.dy *= -1

       if ball.xcor() > 500:
           ball.goto(0, 0)
           ball.dy *= -1
           l_score, r_score, score_board = update_score(
               l_score, r_score, 'l', score_board)
           continue

       elif ball.xcor() < -500:
           ball.goto(0, 0)
           ball.dy *= -1
           l_score, r_score, score_board = update_score(
               l_score, r_score, 'r', score_board)
           continue

       if ((ball.xcor() > 360) and
           (ball.xcor() < 370) and
           (ball.ycor() < r_paddle.ycor()+40) and
               (ball.ycor() > r_paddle.ycor()-40)):
           ball.setx(360)
           ball.dx *= -1

       if ((ball.xcor() < -360) and
               (ball.xcor() > -370) and
               (ball.ycor() < l_paddle.ycor()+40) and
               (ball.ycor() > l_paddle.ycor()-40)):
           ball.setx(-360)
           ball.dx *= -1

if __name__ == '__main__':
   pong_game()
```

### 这是一个有趣的 Python 项目，测试你能多快准确地打出一个句子。

该程序要求我们通过 *tkinter* 模块创建一个图形用户界面(GUI)。如果您不熟悉 GUI，这个例子是一个很好的介绍，因为我们使用了一系列简单的标签、按钮和输入字段来创建一个窗口。我们还使用 Python *timeit* 模块来处理我们的输入测试的计时方面，使用 *random* 模块来随机选择一个测试短语。

我们在这个例子中只添加了两个测试短语，但是可以尝试更多，甚至集成第三方字典来获得更多的例子。

**源代码:**

**26。文本编辑器**

```
'''
Speed Typing Test
-------------------------------------------------------------
'''

import tkinter
from timeit import default_timer as timer
import random

def speed_test():
   speed_test_sentences = [
       'This is a random sentence to check speed.',
       'Speed, I am lightning mcqueen.'
   ]

   sentence = random.choice(speed_test_sentences)
   start = timer()
   main_window = tkinter.Tk()
   main_window.geometry('600x400')

   label_1 = tkinter.Label(main_window, text=sentence, font='times 20')
   label_1.place(x=150, y=10)

   label_2 = tkinter.Label(main_window, text='Start Typing', font='times 20')
   label_2.place(x=10, y=50)

   entry = tkinter.Entry(main_window)
   entry.place(x=280, y=55)

   def check_result():
       if entry.get() == sentence:
           end = timer()
           label_3.configure(text=f'Time: {round((end-start), 4)}s')
       else:
           label_3.configure(text='Wrong Input')

   button_1 = tkinter.Button(main_window, text='Done',
                             command=check_result, width=12, bg='grey')
   button_1.place(x=150, y=100)

   button_2 = tkinter.Button(main_window, text='Try Again',
                             command=speed_test, width=12, bg='grey')
   button_2.place(x=250, y=100)

   label_3 = tkinter.Label(main_window, text='', font='times 20')
   label_3.place(x=10, y=300)

   main_window.mainloop()

if __name__ == '__main__':
   speed_test()
```

### 基于我们上一个 *tkinter* 例子，这个有趣的 Python 项目创建了一个 GUI 来模拟我们自己的文本编辑器。这个例子还使用了标准的 GUI 组件，包括标签、按钮和输入字段。

然而，我们也增加了像真正的文本编辑器一样打开和保存文件的能力。如果您是文件处理的新手，这个 Python 项目是理解如何读入和保存文件的一个很好的方式。

尝试下面的代码来巩固您的理解，看看您是否可以扩展这些代码来创建您习惯在文本编辑器中使用的其他功能，比如“查找单词”功能。

**源代码:**

**27。数独求解器**

```
'''
Text Editor
-------------------------------------------------------------
'''

import tkinter as tk
from tkinter.filedialog import askopenfilename, asksaveasfilename

def text_editor():
   def open_file():
       filepath = askopenfilename(
           filetypes=[('Text Files', '*.txt'), ('All Files', '*.*')]
       )

       if not filepath:
           return

       txt_edit.delete(1.0, tk.END)
       with open(filepath, 'r') as input_file:
           text = input_file.read()
           txt_edit.insert(tk.END, text)
       window.title(f'TextEditor - {filepath}')

   def save_file():
       filepath = asksaveasfilename(
           defaultextension='txt',
           filetypes=[('Text Files', '*.txt'), ('All Files', '*.*')],
       )

       if not filepath:
           return

       with open(filepath, 'w') as output_file:
           text = txt_edit.get(1.0, tk.END)
           output_file.write(text)
       window.title(f'Text Editor - {filepath}')

   window = tk.Tk()
   window.title('Text Editor')
   window.rowconfigure(0, minsize=800, weight=1)
   window.columnconfigure(1, minsize=800, weight=1)

   txt_edit = tk.Text(window)
   fr_buttons = tk.Frame(window, relief=tk.RAISED, bd=2)
   btn_open = tk.Button(fr_buttons, text='Open', command=open_file)
   btn_save = tk.Button(fr_buttons, text='Save As...', command=save_file)

   btn_open.grid(row=0, column=0, sticky='ew', padx=5, pady=5)
   btn_save.grid(row=1, column=0, sticky='ew', padx=5)

   fr_buttons.grid(row=0, column=0, sticky='ns')
   txt_edit.grid(row=0, column=1, sticky='nsew')

   window.mainloop()

if __name__ == '__main__':
  text_editor()
```

### 这个 Python 项目使用 *pygame* 库(参见 pip 安装说明)来实现一个自动解决数独难题的 GUI。我们使用几个用户定义的函数来创建 GUI，如下所示。

为了解决一个数独难题，这个程序使用一种回溯算法来递增地检查解决方案，如果当前的解决方案不可行，就采用或放弃它。

这种放弃解决方案的步骤是回溯方法的定义特征，因为程序*后退*以尝试新的解决方案，直到它找到一个有效的解决方案。这个过程递增地进行，直到整个网格被正确填充。

随意试验不同的数独问题，甚至考虑扩大问题网格的大小(如果你这样做，你将需要一个新的基础图像)。

**源代码:**

**28。站点连接检查器**

```
'''
Sudoku Solver
-------------------------------------------------------------
pip install pygame
image link:
https://www.pngitem.com/pimgs/m/210-2106648_empty-sudoku-grid-grid-6x6-png-transparent-png.png
'''

import pygame

pygame.font.init()
screen = pygame.display.set_mode((600, 600))
pygame.display.set_caption('SUDOKU SOLVER USING BACKTRACKING')
img = pygame.image.load('icon.png')
pygame.display.set_icon(img)
font1 = pygame.font.SysFont('comicsans', 40)
font2 = pygame.font.SysFont('comicsans', 20)
x = 0
y = 0
dif = 500 / 9
val = 0

# Default Sudoku Board
grid = [
   [7, 8, 0, 4, 0, 0, 1, 2, 0],
   [6, 0, 0, 0, 7, 5, 0, 0, 9],
   [0, 0, 0, 6, 0, 1, 0, 7, 8],
   [0, 0, 7, 0, 4, 0, 2, 6, 0],
   [0, 0, 1, 0, 5, 0, 9, 3, 0],
   [9, 0, 4, 0, 6, 0, 0, 0, 5],
   [0, 7, 0, 3, 0, 0, 0, 1, 2],
   [1, 2, 0, 0, 0, 7, 4, 0, 0],
   [0, 4, 9, 2, 0, 6, 0, 0, 7]
]

def get_coord(pos):
   x = pos[0] // dif
   y = pos[1] // dif

def draw_box():
   for i in range(2):
       pygame.draw.line(screen, (255, 0, 0), (x * dif-3, (y + i)
                        * dif), (x * dif + dif + 3, (y + i)*dif), 7)
       pygame.draw.line(screen, (255, 0, 0), ((x + i) * dif,
                        y * dif), ((x + i) * dif, y * dif + dif), 7)

def draw():
   for i in range(9):
       for j in range(9):
           if grid[i][j] != 0:
               pygame.draw.rect(screen, (0, 153, 153),
                                (i * dif, j * dif, dif + 1, dif + 1))
               text1 = font1.render(str(grid[i][j]), 1, (0, 0, 0))
               screen.blit(text1, (i * dif + 15, j * dif + 15))

   for i in range(10):
       if i % 3 == 0:
           thick = 7
       else:
           thick = 1
       pygame.draw.line(screen, (0, 0, 0), (0, i * dif),
                        (500, i * dif), thick)
       pygame.draw.line(screen, (0, 0, 0), (i * dif, 0),
                        (i * dif, 500), thick)

def draw_val(val):
   text1 = font1.render(str(val), 1, (0, 0, 0))
   screen.blit(text1, (x * dif + 15, y * dif + 15))

def raise_error_1():
   text1 = font1.render('WRONG !!!', 1, (0, 0, 0))
   screen.blit(text1, (20, 570))

def raise_error_2():
   text1 = font1.render('Wrong !!! Not a valid Key', 1, (0, 0, 0))
   screen.blit(text1, (20, 570))

def valid(m, i, j, val):
   for it in range(9):
       if m[i][it] == val:
           return False
       if m[it][j] == val:
           return False

   it = i // 3
   jt = j // 3

   for i in range(it * 3, it * 3 + 3):
       for j in range(jt * 3, jt * 3 + 3):
           if m[i][j] == val:
               return False
   return True

def solve(grid, i, j):
   while grid[i][j] != 0:
       if i < 8:
           i += 1
       elif i == 8 and j < 8:
           i = 0
           j += 1
       elif i == 8 and j == 8:
           return True

   pygame.event.pump()
   for it in range(1, 10):
       if valid(grid, i, j, it) == True:
           grid[i][j] = it
           x = i
           y = j
           screen.fill((255, 255, 255))
           draw()
           draw_box()
           pygame.display.update()
           pygame.time.delay(20)

           if solve(grid, i, j) == 1:
               return True
           else:
               grid[i][j] = 0
           screen.fill((255, 255, 255))

           draw()
           draw_box()
           pygame.display.update()
           pygame.time.delay(50)
   return False

def instruction():
  text1 = font2.render(
      'PRESS D TO RESET TO DEFAULT / R TO EMPTY\n', 1, (0, 0, 0))
  text2 = font2.render(
      'ENTER VALUES AND PRESS ENTER TO VISUALIZE\n', 1, (0, 0, 0))
  screen.blit(text1, (20, 520))
  screen.blit(text2, (20, 540))

def result():
  text1 = font1.render('FINISHED PRESS R or D\n', 1, (0, 0, 0))
  screen.blit(text1, (20, 570))

run = True
flag_1 = 0
flag_2 = 0
rs = 0
error = 0
while run:
   screen.fill((255, 255, 255))
   for event in pygame.event.get():
       if event.type == pygame.QUIT:
           run = False
       if event.type == pygame.MOUSEBUTTONDOWN:
           flag_1 = 1
           pos = pygame.mouse.get_pos()
           get_coord(pos)
       if event.type == pygame.KEYDOWN:
           if event.key == pygame.K_LEFT:
               x -= 1
               flag_1 = 1
           if event.key == pygame.K_RIGHT:
               x += 1
               flag_1 = 1
           if event.key == pygame.K_UP:
               y -= 1
               flag_1 = 1
           if event.key == pygame.K_DOWN:
               y += 1
               flag_1 = 1
           if event.key == pygame.K_1:
               val = 1
           if event.key == pygame.K_2:
               val = 2
           if event.key == pygame.K_3:
               val = 3
           if event.key == pygame.K_4:
               val = 4
           if event.key == pygame.K_5:
               val = 5
           if event.key == pygame.K_6:
               val = 6
           if event.key == pygame.K_7:
               val = 7
           if event.key == pygame.K_8:
               val = 8
           if event.key == pygame.K_9:
               val = 9
           if event.key == pygame.K_RETURN:
               flag_2 = 1

           # If R pressed clear sudoku board
           if event.key == pygame.K_r:
               rs = 0
               error = 0
               flag_2 = 0
               grid = [
                   [0, 0, 0, 0, 0, 0, 0, 0, 0],
                   [0, 0, 0, 0, 0, 0, 0, 0, 0],
                   [0, 0, 0, 0, 0, 0, 0, 0, 0],
                   [0, 0, 0, 0, 0, 0, 0, 0, 0],
                   [0, 0, 0, 0, 0, 0, 0, 0, 0],
                   [0, 0, 0, 0, 0, 0, 0, 0, 0],
                   [0, 0, 0, 0, 0, 0, 0, 0, 0],
                   [0, 0, 0, 0, 0, 0, 0, 0, 0],
                   [0, 0, 0, 0, 0, 0, 0, 0, 0]
               ]

           # If D pressed reset board to default
           if event.key == pygame.K_d:
               rs = 0
               error = 0
               flag_2 = 0
               grid = [
                   [7, 8, 0, 4, 0, 0, 1, 2, 0],
                   [6, 0, 0, 0, 7, 5, 0, 0, 9],
                   [0, 0, 0, 6, 0, 1, 0, 7, 8],
                   [0, 0, 7, 0, 4, 0, 2, 6, 0],
                   [0, 0, 1, 0, 5, 0, 9, 3, 0],
                   [9, 0, 4, 0, 6, 0, 0, 0, 5],
                   [0, 7, 0, 3, 0, 0, 0, 1, 2],
                   [1, 2, 0, 0, 0, 7, 4, 0, 0],
                   [0, 4, 9, 2, 0, 6, 0, 0, 7]
               ]

   if flag_2 == 1:
       if solve(grid, 0, 0) == False:
           error = 1
       else:
           rs = 1
       flag_2 = 0

   if val != 0:
       draw_val(val)
       if valid(grid, int(x), int(y), val) == True:
           grid[int(x)][int(y)] = val
           flag_1 = 0
       else:
           grid[int(x)][int(y)] = 0
           raise_error_2()
       val = 0

   if error == 1:
       raise_error_1()
   if rs == 1:
       result()
   draw()
   if flag_1 == 1:
       draw_box()
   instruction()

   pygame.display.update() 
```

### 这个 Python 项目使用 *urllib* 和 *tkinter* 模块来测试网站连接性。

我们已经使用 *tkinter* 模块创建了一个 GUI，允许用户输入网址。与我们前面的例子非常相似，这包括标签、按钮和输入字段。

在我们收集了用户的网址之后，我们将它传递给我们的用户定义函数，通过 *urllib* 模块的*返回当前网站的 HTTP 状态代码。getcode()* 函数。

对于这个例子，我们简单地确定 HTTP 代码是否是 200。如果是，我们知道该站点正在工作；否则，我们会通知用户它不可用。

您可以扩展这段代码，考虑一种更细粒度的方法来处理各种 HTTP 响应代码，所以可以随意添加！

**源代码:**

**29。语言检测器**

```
'''
Site Connectivity Checker
-------------------------------------------------------------
Enter websites as http(s)://www.yourwebsite.com
'''

import urllib.request
import tkinter as tk

def test_connectivity():
  window = tk.Tk()
  window.geometry('600x400')
  head = tk.Label(window, text='Website Connectivity Checker',
                  font=('Calibri 15'))
  head.pack(pady=20)

  def check_url():
      web = (url.get())
      status_code = urllib.request.urlopen(web).getcode()
      website_is_up = status_code == 200

      if website_is_up:
          tk.Label(window, text='Website Available',
                   font=('Calibri 15')).place(x=260, y=200)
      else:
          tk.Label(window, text='Website Not Available',
                   font=('Calibri 15')).place(x=260, y=200)

  url = tk.StringVar()
  tk.Entry(window, textvariable=url).place(x=200, y=80, height=30, width=280)
  tk.Button(window, text='Check', command=check_url).place(x=285, y=150)
  window.mainloop()

if __name__ == '__main__':
  test_connectivity()
```

### 这个 Python 项目使用 *langdetect* 模块(参见 pip 安装说明)来帮助我们识别已经输入的语言。如果你不确定你在处理哪种语言，这真的很有用。

这是另一个例子，我们使用 *tkinter* 创建了一个简单的 GUI，包括标签、按钮和输入框。然后，我们可以从输入字段中收集文本，并用 *langdetect* 进行处理，以确定输入了哪种语言。最后，我们将这个结果打印到 GUI 上，让用户知道结果。

注意， *langdetect* 返回的结果是缩写的语言代码。例如，如果我们输入英文文本，我们将看到' en '作为返回值。

**源代码:**

三十岁。网飞推荐系统

```
'''
Language Detector
-------------------------------------------------------------
pip install langdetect
'''

from langdetect import detect
import tkinter as tk

def detect_lang():
   window = tk.Tk()
   window.geometry('600x400')
   head = tk.Label(window, text='Language Detector', font=('Calibri 15'))
   head.pack(pady=20)

   def check_language():
       new_text = text.get()
       lang = detect(str(new_text))
       tk.Label(window, text=lang, font=('Calibri 15')).place(x=260, y=200)

   text = tk.StringVar()
   tk.Entry(window, textvariable=text).place(
       x=200, y=80, height=30, width=280)
   tk.Button(window, text='Check Language',
             command=check_language).place(x=285, y=150)
   window.mainloop()

if __name__ == '__main__':
   detect_lang()
```

### 最后，我们将一个特别激动人心的 Python 项目留到了最后！这是一个网飞推荐系统，非常适合有抱负的数据科学家或机器学习爱好者。

要创建这个项目，您需要导入一系列模块，包括 *tkinter、re、nltk、pandas 和 numpy* (请参阅新模块的 pip 安装说明)。你还需要从[这里](https://www.kaggle.com/datasets/satpreetmakhija/netflix-movies-and-tv-shows-2021?resource=download)下载一个包含网飞电影和电视节目的数据集。

我们将使用 *tkinter* 来创建 GUI，它将使用标签、按钮和输入字段。然后，用户可以在网飞上输入他们喜欢的电视节目或电影，根据他们的喜好返回推荐。

推荐引擎使用演员、导演、收视率、国家和流派作为机器学习(ML)“特征”。然后，代码使用“余弦相似度”方法根据用户输入找到相似的结果。这大量使用了 *pandas* 和 *numpy* 来清理数据并为处理做准备。

在这个例子中有很多东西需要解开。最好的方法是慢慢研究代码，然后对机器学习(ML)、“特征”和“余弦相似性”进行进一步的研究。

然后，您将能够理解如何使用数据集基于相似性得出建议。如果你是一个有抱负的数据科学家，这是一个非常好的尝试项目！

**源代码:**

**结论**

```
'''
Netflix Recommendation Engine
-------------------------------------------------------------
pip install pandas numpy nltk
'''

from nltk.tokenize import word_tokenize
import numpy as np
import pandas as pd
import re
import nltk
import tkinter as tk
from nltk.corpus import stopwords
nltk.download('stopwords')

data = pd.read_csv('netflixData.csv')
data = data.dropna(subset=['Cast', 'Production Country', 'Rating'])
movies = data[data['Content Type'] == 'Movie'].reset_index()
movies = movies.drop(['index', 'Show Id', 'Content Type', 'Date Added',
                    'Release Date', 'Duration', 'Description'], axis=1)
movies.head()
tv = data[data['Content Type'] == 'TV Show'].reset_index()
tv = tv.drop(['index', 'Show Id', 'Content Type', 'Date Added',
            'Release Date', 'Duration', 'Description'], axis=1)
tv.head()
actors = []
for i in movies['Cast']:
   actor = re.split(r', \s*', i)
   actors.append(actor)
flat_list = []

for sublist in actors:
   for item in sublist:
       flat_list.append(item)

actors_list = sorted(set(flat_list))
binary_actors = [[0] * 0 for i in range(len(set(flat_list)))]
for i in movies['Cast']:
   k = 0
   for j in actors_list:
       if j in i:
           binary_actors[k].append(1.0)
       else:
           binary_actors[k].append(0.0)
       k += 1

binary_actors = pd.DataFrame(binary_actors).transpose()
directors = []
for i in movies['Director']:
   if pd.notna(i):
       director = re.split(r', \s*', i)
       directors.append(director)

flat_list_2 = []
for sublist in directors:
   for item in sublist:
       flat_list_2.append(item)

directors_list = sorted(set(flat_list_2))
binary_directors = [[0] * 0 for i in range(len(set(flat_list_2)))]
for i in movies['Director']:
   k = 0
   for j in directors_list:
       if pd.isna(i):
           binary_directors[k].append(0.0)
       elif j in i:
           binary_directors[k].append(1.0)
       else:
           binary_directors[k].append(0.0)
       k += 1

binary_directors = pd.DataFrame(binary_directors).transpose()
countries = []
for i in movies['Production Country']:
   country = re.split(r', \s*', i)
   countries.append(country)

flat_list_3 = []
for sublist in countries:
   for item in sublist:
       flat_list_3.append(item)

countries_list = sorted(set(flat_list_3))
binary_countries = [[0] * 0 for i in range(len(set(flat_list_3)))]
for i in movies['Production Country']:
   k = 0
   for j in countries_list:
       if j in i:
           binary_countries[k].append(1.0)
       else:
           binary_countries[k].append(0.0)
       k += 1

binary_countries = pd.DataFrame(binary_countries).transpose()
genres = []
for i in movies['Genres']:
   genre = re.split(r', \s*', i)
   genres.append(genre)

flat_list_4 = []
for sublist in genres:
   for item in sublist:
       flat_list_4.append(item)

genres_list = sorted(set(flat_list_4))
binary_genres = [[0] * 0 for i in range(len(set(flat_list_4)))]
for i in movies['Genres']:
   k = 0
   for j in genres_list:
       if j in i:
           binary_genres[k].append(1.0)
       else:
           binary_genres[k].append(0.0)
       k += 1

binary_genres = pd.DataFrame(binary_genres).transpose()
ratings = []
for i in movies['Rating']:
   ratings.append(i)

ratings_list = sorted(set(ratings))
binary_ratings = [[0] * 0 for i in range(len(set(ratings_list)))]
for i in movies['Rating']:
   k = 0
   for j in ratings_list:
       if j in i:
           binary_ratings[k].append(1.0)
       else:
           binary_ratings[k].append(0.0)
       k += 1

binary_ratings = pd.DataFrame(binary_ratings).transpose()
binary = pd.concat([binary_actors, binary_directors,
                  binary_countries, binary_genres], axis=1, ignore_index=True)
actors_2 = []
for i in tv['Cast']:
  actor2 = re.split(r', \s*', i)
  actors_2.append(actor2)

flat_list_5 = []
for sublist in actors_2:
   for item in sublist:
       flat_list_5.append(item)

actors_list_2 = sorted(set(flat_list_5))
binary_actors_2 = [[0] * 0 for i in range(len(set(flat_list_5)))]
for i in tv['Cast']:
   k = 0
   for j in actors_list_2:
       if j in i:
           binary_actors_2[k].append(1.0)
       else:
           binary_actors_2[k].append(0.0)
       k += 1

binary_actors_2 = pd.DataFrame(binary_actors_2).transpose()
countries_2 = []
for i in tv['Production Country']:
   country2 = re.split(r', \s*', i)
   countries_2.append(country2)

flat_list_6 = []
for sublist in countries_2:
   for item in sublist:
       flat_list_6.append(item)

countries_list_2 = sorted(set(flat_list_6))
binary_countries_2 = [[0] * 0 for i in range(len(set(flat_list_6)))]
for i in tv['Production Country']:
   k = 0
   for j in countries_list_2:
       if j in i:
           binary_countries_2[k].append(1.0)
       else:
           binary_countries_2[k].append(0.0)
       k += 1

binary_countries_2 = pd.DataFrame(binary_countries_2).transpose()
genres_2 = []
for i in tv['Genres']:
   genre2 = re.split(r', \s*', i)
   genres_2.append(genre2)

flat_list_7 = []
for sublist in genres_2:
   for item in sublist:
       flat_list_7.append(item)

genres_list_2 = sorted(set(flat_list_7))
binary_genres_2 = [[0] * 0 for i in range(len(set(flat_list_7)))]
for i in tv['Genres']:
   k = 0
   for j in genres_list_2:
       if j in i:
           binary_genres_2[k].append(1.0)
       else:
           binary_genres_2[k].append(0.0)
       k += 1

binary_genres_2 = pd.DataFrame(binary_genres_2).transpose()
ratings_2 = []
for i in tv['Rating']:
   ratings_2.append(i)

ratings_list_2 = sorted(set(ratings_2))
binary_ratings_2 = [[0] * 0 for i in range(len(set(ratings_list_2)))]
for i in tv['Rating']:
   k = 0
   for j in ratings_list_2:
       if j in i:
           binary_ratings_2[k].append(1.0)
       else:
           binary_ratings_2[k].append(0.0)
       k += 1

binary_ratings_2 = pd.DataFrame(binary_ratings_2).transpose()
binary_2 = pd.concat([binary_actors_2, binary_countries_2,
                    binary_genres_2], axis=1, ignore_index=True)

window = tk.Tk()
window.geometry('600x600')
head = tk.Label(window, text='Enter Movie / TV Show on Netflix For Recommendations', font=('Calibri 15'))
head.pack(pady=20)

def netflix_recommender(search):
   cs_list = []
   binary_list = []

   if search in movies['Title'].values:
       idx = movies[movies['Title'] == search].index.item()
       for i in binary.iloc[idx]:
           binary_list.append(i)

       point_1 = np.array(binary_list).reshape(1, -1)
       point_1 = [val for sublist in point_1 for val in sublist]
       for j in range(len(movies)):
           binary_list_2 = []
           for k in binary.iloc[j]:
               binary_list_2.append(k)
           point_2 = np.array(binary_list_2).reshape(1, -1)
           point_2 = [val for sublist in point_2 for val in sublist]
           dot_product = np.dot(point_1, point_2)
           norm_1 = np.linalg.norm(point_1)
           norm_2 = np.linalg.norm(point_2)
           cos_sim = dot_product / (norm_1 * norm_2)
           cs_list.append(cos_sim)

       movies_copy = movies.copy()
       movies_copy['cos_sim'] = cs_list
       results = movies_copy.sort_values('cos_sim', ascending=False)
       results = results[results['title'] != search]
       top_results = results.head(5)
       return (top_results)

   elif search in tv['Title'].values:
       idx = tv[tv['Title'] == search].index.item()
       for i in binary_2.iloc[idx]:
           binary_list.append(i)

       point_1 = np.array(binary_list).reshape(1, -1)
       point_1 = [val for sublist in point_1 for val in sublist]
       for j in range(len(tv)):
           binary_list_2 = []
           for k in binary_2.iloc[j]:
               binary_list_2.append(k)

           point_2 = np.array(binary_list_2).reshape(1, -1)
           point_2 = [val for sublist in point_2 for val in sublist]
           dot_product = np.dot(point_1, point_2)
           norm_1 = np.linalg.norm(point_1)
           norm_2 = np.linalg.norm(point_2)
           cos_sim = dot_product / (norm_1 * norm_2)
           cs_list.append(cos_sim)

       tv_copy = tv.copy()
       tv_copy['cos_sim'] = cs_list
       results = tv_copy.sort_values('cos_sim', ascending=False)
       results = results[results['Title'] != search]
       top_results = results.head(5)
       return (top_results)

   else:
       return ('Title not in dataset. Please check spelling.')

def call_recommender():
  subject = text.get()
  recommendation = netflix_recommender(subject)
  txt = ''
  for i in recommendation.iterrows():
      txt += 'Title: ' + str(i[1][0]) + '\n'
  tk.Label(window, text=txt, font=('Calibri 15')).place(x=195, y=150)

text = tk.StringVar()
tk.Entry(window, textvariable=text).place(x=200, y=80, height=30, width=280)
tk.Button(window, text='Find Recommendations',
         command=call_recommender).place(x=285, y=150)
window.mainloop()
```

## 现在你知道了。我们已经用源代码介绍了 30 个很酷、有趣、令人兴奋的 Python 项目，从简单到高级都有。这些包括游戏、面向对象编程、图形用户界面、人工智能(AI)、机器学习(ML)、API、机器人、标准库模块和几个第三方库。

这些 Python 项目想法的一个共同点是，它们要求你将理论上的 Python 学习付诸实践。通过这样做，您可以测试自己，并在逐步成为更好的实用程序员的过程中提高您的 Python 技能。

想用 Python 构建更多的项目吗？查看 [**Python 巨型课程打造 10 个真实世界的应用**](https://click.linksynergy.com/deeplink?id=SeYHzlfZEmI&mid=39197&murl=https%3A%2F%2Fwww.udemy.com%2Fcourse%2Fthe-python-mega-course%2F&u1=blog%2Fpython-projects_amcid-b3q2sZUONFVMblmq7JUFI) **。**

**常见问题解答**

## **1。Python 适合大型项目吗？**

#### 尽管有人认为 Python 比其他流行语言(如 C 和 C++)要慢，但 Python 仍然被许多顶级科技公司广泛使用，因为它非常通用，易于维护，并且它提供了大量的库和来自社区的支持。

**2。我的第一个 Python 项目应该是什么？**

#### 查看我们上面提到的任何 Python 初学者项目，包括 Mad Libs、石头剪刀布、Hangman 或井字游戏！

**人也在读:**

**People are also reading:**