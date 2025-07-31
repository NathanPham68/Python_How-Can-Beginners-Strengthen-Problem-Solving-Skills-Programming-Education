# 🐍 [Python] How Can Beginners Strengthen Problem-Solving Skills? - Programming Education

<img width="1111" height="528" alt="image" src="https://github.com/user-attachments/assets/47221320-425c-4aab-899b-2630e67dd953" />

Welcome to this Python practice project! This repository is designed to help beginners strengthen their problem-solving skills through a series of short, practical exercises. You'll learn to apply Python fundamentals such as data types, functions, loops, string manipulation, and basic data structures (lists, sets, dictionaries) in real-world scenarios.

## 🎯 **Project Goals**

By working through these exercises, you'll be able to:

✅ Choose and apply the right data types for real-world problems

✅ Define and use functions, loops, and conditions effectively

✅ Apply computational thinking: breaking down problems step-by-step

✅ Strengthen your confidence in basic coding and logical flow

If you get stuck or have any questions, feel free to reach out!

Happy coding 🎶

## 🧠 **Problem-Solving Mindset (Step-by-Step Guide)**

Each exercise follows a logical approach that you can use when solving any Python problem:

1. Read & Understand the Problem
→ Identify the goal, keywords, and the expected input/output

2. Clarify Input and Output
→ Know the required data type and format clearly

3. Sketch a Quick Plan
→ Outline your solution idea briefly

4. Link Back to What You've Learned
→ Map your plan to Python knowledge: loops, conditions, etc.

5. Break Down the Problem
→ Think in smaller steps:

    - Looping through data

    - Checking conditions

    - Updating variables or collections

6. Write a Function Skeleton
→ Example: def function_name(params): ...

7. Implement Step-by-Step Logic
→ Code exactly what you planned using loop → condition → update flow

8. Test with Sample Inputs
→ Compare actual output with the expected one

9. Refactor if Needed
→ Improve readability, fix bugs, or optimize performance

## 📚 [**Exercises Overview**](https://colab.research.google.com/drive/1dDV0jLbzYygT1BaeYsk6dmVe5R3QIfmr?usp=sharing)

### Exercise 1: Write a function count_vowels(s) that counts the number of vowels (a, e, i, o, u) in a given string 'This Is Just A String That We Use To Practice'

Objetives: Practice Problem Solving, String Manipulating, Loop, Define Function

* Code

```ruby
def count_vowels(given_string):
  vowels = 0

  # loop for given_string
  for i in given_string.lower():
    if i in ['a', 'e', 'i', 'o', 'u']:
      # update vowels
      vowels += 1
  return vowels

print("Number of vowels:", count_vowels('This Is Just A String That We Use To Practice'))
```

* Results

<img width="393" height="65" alt="image" src="https://github.com/user-attachments/assets/645eccb9-3718-4d5c-b99e-dc7f9b175bed" />

### Exercise 2a: You are managing a small library system and have a list of books. Each book has a title, author, and whether it is currently borrowed. Your task is to organize and analyze the data.

Input: A list of dictionaries, where each dictionary contains information about a book:

books = [ {"title": "1984", "author": "George Orwell", "borrowed": True}, {"title": "To Kill a Mockingbird", "author": "Harper Lee", "borrowed": False}, {"title": "The Great Gatsby", "author": "F. Scott Fitzgerald", "borrowed": True}, {"title": "Moby Dick", "author": "Herman Melville", "borrowed": False}, {"title": "War and Peace", "author": "Leo Tolstoy", "borrowed": True}, ]

Write a function that takes a title as input and checks if the book exists in the library. If it does, return 'Borrowed' else return 'Available'. If it doesn't return 'Not exist in the library'

* Code

```ruby
def check_book_status(title, library):
    for book in library:
        # Check if the title matches (case-insensitive)
        if book["title"].lower() == title.lower():
            return "Borrowed" if book["borrowed"] else "Available"
    return "Not exist in the library"

# Sample book list
books = [
    {"title": "1984", "author": "George Orwell", "borrowed": True},
    {"title": "To Kill a Mockingbird", "author": "Harper Lee", "borrowed": False},
    {"title": "The Great Gatsby", "author": "F. Scott Fitzgerald", "borrowed": True},
    {"title": "Moby Dick", "author": "Herman Melville", "borrowed": False},
    {"title": "War and Peace", "author": "Leo Tolstoy", "borrowed": True},
]

# Test cases
print(check_book_status('1984', books))
print(check_book_status("To Kill a Mockingbird", books))
print(check_book_status("A", books))
```

* Results

<img width="451" height="90" alt="image" src="https://github.com/user-attachments/assets/7d74f8f3-0c0a-4fda-a6de-eb4190387917" />

### Exercise 2b: Count Borrowed and Available Books from books in previous exercise.

* Code

```ruby
def count_books_status(books):
    borrowed_count = 0
    available_count = 0

    for book in books:
        if book["borrowed"]:
            borrowed_count += 1
        else:
            available_count += 1
    return {"borrowed": borrowed_count, "available": available_count}

# Book list (same as before)
books = [
    {"title": "1984", "author": "George Orwell", "borrowed": True},
    {"title": "To Kill a Mockingbird", "author": "Harper Lee", "borrowed": False},
    {"title": "The Great Gatsby", "author": "F. Scott Fitzgerald", "borrowed": True},
    {"title": "Moby Dick", "author": "Herman Melville", "borrowed": False},
    {"title": "War and Peace", "author": "Leo Tolstoy", "borrowed": True},
]

# Test the function
result = count_books_status(books)
print(result)  # Output: {'borrowed': 3, 'available': 2}
```

* Results

<img width="516" height="56" alt="image" src="https://github.com/user-attachments/assets/ac24ccfd-1500-49c5-8ee0-d5ed7f1f89f6" />

### Exercise 2c: Group Books by Author.

* Code

```ruby
def group_books(books):
    book_dictionary = {}

    for book in books:
        author = book["author"]
        title = book["title"]

        if author not in book_dictionary:
            book_dictionary[author] = []
        book_dictionary[author].append(title)

    return book_dictionary

# Book list
books = [
    {"title": "1984", "author": "George Orwell", "borrowed": True},
    {"title": "To Kill a Mockingbird", "author": "Harper Lee", "borrowed": False},
    {"title": "The Great Gatsby", "author": "F. Scott Fitzgerald", "borrowed": True},
    {"title": "Moby Dick", "author": "Herman Melville", "borrowed": False},
    {"title": "War and Peace", "author": "Leo Tolstoy", "borrowed": True},
]

# Test the function
result = group_books(books)
print(result)
```

* Results

<img width="1068" height="77" alt="image" src="https://github.com/user-attachments/assets/879fa540-cb30-4639-971b-99fe37b1e1e2" />

### Exercise 3: Get the first name of input full name.

Input: name = Nguyễn Văn An

name = Nguyễn Văn an

name = an

* Code

```ruby
def process_name(name):
    # Remove extra spaces and split into parts
    words = name.strip().split()

    # Capitalize each word
    formatted_words = [word.capitalize() for word in words]

    # Check if it's a full name (2+ words)
    if len(formatted_words) >= 2:
        last_name = formatted_words[-1]
        full_name = ' '.join(formatted_words)
        return f"{last_name} # {full_name}"
    else:
        short_name = ' '.join(formatted_words)
        return f"Please input suitable format name # {short_name}"

# Test cases
print(process_name("Nguyễn Văn An"))
print(process_name("Nguyễn Văn an"))
print(process_name("an"))
```

* Results

<img width="627" height="100" alt="image" src="https://github.com/user-attachments/assets/ec5fe2d3-8775-45ea-a597-4bf59f4ab49d" />

### Exercise 4: Count Character Occurrences.

Objectives: Practice Problem Solving, String & List manipulating, Loops, Define functions

Write a function count_characters(s) that takes a string s and returns 2 lists. The first list is the list of distinct characters from the string. The second list contains the equivalent frequency for each distinct characters.

Input: "This is a string"

* Code

```ruby
def count_characters(s):
    # Bước 1: Làm sạch dữ liệu - chuyển về chữ thường
    s = s.lower()
    
    # Bước 2: Khởi tạo hai danh sách kết quả
    distinct_chars = []
    frequencies = []
    
    # Bước 3: Duyệt từng ký tự trong chuỗi
    for char in s:
        # Bỏ qua dấu cách
        if char == ' ':
            continue
        if char not in distinct_chars:
            distinct_chars.append(char)
            frequencies.append(s.count(char))
    
    return [distinct_chars, frequencies]

# Thử chạy với ví dụ
input_str = "This is a string"
result = count_characters(input_str)
print(result)
```

* Results

<img width="757" height="63" alt="image" src="https://github.com/user-attachments/assets/be859bfe-a083-4081-954d-5a83855b8404" />

### Exercise 5: Anna is submitting a requirement on a platform. Howerver, there are limitations about the number of words and number of characters for the submission. Particularly, the number of world should be under 50 words, and number of character should be under 200 characters. characters don't include special characters as '

Objective: Problem Solving, Loop, Function, List, Set, Dictionary, Define Function.

Please help Anna create a function to do this and check this function with the following submissions!

Submission 1: "I am very excited about the opportunity to work with your company. My skills in data analysis and programming make me confident that I would be a valuable addition to your team. I look forward to the chance to contribute and grow with your company.

Submission 2: "I recently bought this product, and I must say, I'm really impressed. The quality is exceptional, and it works just as advertised. I especially appreciate the ease of use, which makes it perfect for both beginners and experts. I would definitely recommend it to others who are looking for something similar."

* Code

```ruby
import re

def check_submission(text):
    # Remove apostrophes and similar special characters
    cleaned_text = re.sub(r"[’']", "", text)

    # Count words
    words = cleaned_text.split()
    word_count = len(words)

    # Count characters (excluding special ones)
    char_count = len(cleaned_text)

    # Check limits
    is_valid = word_count < 50 and char_count < 200

    status = "Valid" if is_valid else "Invalid"
    return {
        "status": status,
        "word_count": word_count,
        "character_count": char_count
    }
```

* Results

<img width="910" height="237" alt="image" src="https://github.com/user-attachments/assets/aa0b3797-ee22-4321-b2be-7121a850c7cb" />

<img width="910" height="267" alt="image" src="https://github.com/user-attachments/assets/9585ad1b-9646-4727-a6a7-5471fcf0fabd" />

### Exercise 6a: Given the participants' score sheet for your University Sports Day, you are required to find the runner-up score. You are given scores. Store them in a list and find the score of the runner-up.

Sample Input [2,3,6,6,5]

* Code

```ruby
def find_runner_up_score(scores):
    # Loại bỏ điểm trùng lặp
    unique_scores = list(set(scores))
    
    # Sắp xếp giảm dần
    unique_scores.sort(reverse=True)
    
    # Trả về phần tử thứ hai nếu tồn tại
    if len(unique_scores) >= 2:
        return unique_scores[1]
    else:
        return None  # Không có runner-up nếu chỉ có 1 điểm duy nhất

# Test mẫu
sample_scores = [2, 3, 6, 6, 5]
result = find_runner_up_score(sample_scores)
print(result) 
```

* Results

<img width="476" height="68" alt="image" src="https://github.com/user-attachments/assets/0bbfa472-a237-45d7-aef4-c6b37c4274ff" />

### Exercise 6b: Given the participants' score sheet for your University Sports Day, you are required to find the runner-up score. You are given scores. Store them in a list and find the score of the runner-up.

The first line contains number of participants. The second line contains an array of integers each separated by a space.

* Code

```ruby
def find_runner_up_score():
    n = int(input("Enter number of participants: "))
    scores = list(map(int, input("Enter the scores separated by space: ").split()))
    
    # Bước 1: Loại bỏ các điểm trùng lặp bằng set
    unique_scores = list(set(scores))
    
    # Bước 2: Sắp xếp giảm dần
    unique_scores.sort(reverse=True)
    
    # Bước 3: Lấy phần tử thứ 2
    if len(unique_scores) >= 2:
        runner_up = unique_scores[1]
        print(runner_up)
    else:
        print("Not enough unique scores for a runner-up.")

# Ví dụ test
# Input: 5 + newline + 2 3 6 6 5
find_runner_up_score()
```

* Results

<img width="649" height="107" alt="image" src="https://github.com/user-attachments/assets/17c8bec0-671c-4f17-88f1-3142cf3b7d6f" />

### Exercise 7: In this challenge, the user enters a string and a substring. You have to print the number of times that the substring occurs in the given string. String traversal will take place from left to right, not from right to left.

NOTE: String letters are case-sensitive.

Sample Input

ABCDCDC

CDC

* Code

```ruby
def count_substring(string, sub_string):
    count = 0
    for i in range(len(string) - len(sub_string) + 1):
        if string[i:i+len(sub_string)] == sub_string:
            count += 1
    return count

# Test với ví dụ mẫu
string = "ABCDCDC"
sub_string = "CDC"
result = count_substring(string, sub_string)
print(result)
```

* Results

<img width="385" height="68" alt="image" src="https://github.com/user-attachments/assets/d90f632a-0870-4fcb-9660-475699b6af9e" />

### Exercise 8: Write a function count_character(s, char) that takes a string s and a character char as input and returns the number of times char appears in s.

Sample Input: "Programming is fun", "m"

* Code

```ruby
def count_character(s, char):
    count = 0
    for c in s:
        if c == char:
            count += 1
    return count

# Test với ví dụ mẫu
input_string = "Programming is fun"
input_char = "m"
result = count_character(input_string, input_char)
print(result)
```

* Results

<img width="463" height="63" alt="image" src="https://github.com/user-attachments/assets/0205e085-7034-4e73-a2d2-92fe8b0179e3" />

### Exercise 9: Write a function is_palindrome(s) that checks if a given string s is a palindrome (reads the same backward as forward), ignoring case and spaces.

Sample Input: "Racecar"

* Code

```ruby
def is_palindrome(s):
    # Bỏ khoảng trắng và chuyển thành chữ thường
    cleaned = s.replace(" ", "").lower()
    
    # So sánh với chuỗi đảo ngược
    return cleaned == cleaned[::-1]

# Test ví dụ
input_str = "Racecar"
print(is_palindrome(input_str))
```

* Results

<img width="418" height="52" alt="image" src="https://github.com/user-attachments/assets/5881578d-3e23-4ce5-9281-15d3510ec309" />

### Exercise 10: Write a function reverse_string(s) that takes a string s as input and returns the reversed string.

Input: "Python"

* Code

```ruby
def reverse_string(s):
    return s[::-1]

# Test ví dụ
input_str = "Python"
result = reverse_string(input_str)
print(result) 
```

* Results

<img width="349" height="55" alt="image" src="https://github.com/user-attachments/assets/a92f9b0c-5977-45cb-99b5-5d66fb8d2b58" />

## 🤝 **Contributing**

Feel free to fork this repo and add more beginner-friendly exercises or suggest improvements to existing ones. 

Collaboration is welcome!

