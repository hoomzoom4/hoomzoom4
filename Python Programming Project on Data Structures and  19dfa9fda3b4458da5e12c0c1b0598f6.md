# Python Programming Project on Data Structures and Algorithms

## **Report: Python Programming Project on Data Structures and Algorithms**

## **Executive Summary**

This report outlines the development and execution of a Python-based project centered on data structures and algorithms. The project involved creating a quiz application that processes a text file containing multiple-choice questions (MCQs), presents them to users, and evaluates their responses. The application highlights the use of Python's built-in data structures and demonstrates algorithmic thinking in shuffling and organizing data.

## **Introduction**

**Objective**

: To develop a Python application that manages and administers a quiz based on a set of MCQs, utilizing fundamental data structures and algorithms to ensure functionality and user interaction.

**Context**

: The project was part of a module on Python Programming, focusing on Data Structures and Algorithms. It served as a practical application of theoretical concepts learned in the course.

## **Project Overview**

```jsx
import random

# Process the text file to extract the questions, options, and correct answers.
def process_file(file_name):
    mcq_test = []
    with open(file_name, 'r') as file:
        lines = file.readlines()
        current_question = {}
        for line in lines:
            # Check if the line starts with a number followed by a period, indicating a question
            if line.split('. ')[0].isdigit():
                # If there is an existing question, add it to the list before starting a new one
                if current_question:
                    mcq_test.append(current_question)
                # Initialize a new question dictionary
                current_question = {'question': line.strip(), 'options': [], 'answer': None}
            # Check if the line contains an asterisk, indicating a correct answer
            elif '*' in line:
                # Remove the asterisk and any trailing whitespace
                clean_option = line.replace('*', '').strip()
                # Add the option to the list and mark it as the correct answer
                current_question['options'].append(clean_option)
                current_question['answer'] = clean_option
            # Otherwise, it's a regular option line
            else:
                # Add the option to the list
                current_question['options'].append(line.strip())
        # Add the last question to the list if it exists
        if current_question:
            mcq_test.append(current_question)
    return mcq_test

# Run the quiz with the given parameters.
def run_quiz(mcq_test, num_questions, randomize_questions, randomize_options):
    # Randomize the order of questions if requested
    if randomize_questions:
        random.shuffle(mcq_test)
    score = 0
    # Loop through the specified number of questions
    for i in range(min(num_questions, len(mcq_test))):
        question = mcq_test[i]
        print(question['question'])
        options = question['options']
        # Randomize the order of options if requested
        if randomize_options:
            random.shuffle(options)
        # Display the options to the user
        for j, option in enumerate(options):
            print(f"{j+1}. {option}")
        # Get the user's answer
        user_input = input("Your answer: ").strip()
        # Convert the user's input to the corresponding option if it's a digit
        if user_input.isdigit() and int(user_input) - 1 < len(options):
            user_answer = options[int(user_input) - 1]
        else:
            user_answer = user_input
        # Check if the user's answer is correct
        if user_answer == question['answer']:
            score += 1
        else:
            # Inform the user of the correct answer if they are wrong
            print(f"Wrong answer. The correct answer is: {question['answer']}")
    # Display the user's total score at the end of the quiz
    print(f"Your total score is: {score}/{num_questions}")

# Main function to run the quiz.
def main():
    # Process the quiz questions file
    mcq_test = process_file('quiz_questions.txt')
    # Prompt the user for the number of questions and randomization preferences
    num_questions = int(input("Enter the number of questions: "))
    randomize_questions = input("Randomize questions? (yes/no): ") == "yes"
    randomize_options = input("Randomize options? (yes/no): ") == "yes"
    # Start the quiz with the user's preferences
    run_quiz(mcq_test, num_questions, randomize_questions, randomize_options)

# Entry point of the script
if __name__ == "__main__":
    main()
```

## **Data Structures Employed**

- **Lists**: Used to store collections of questions, options, and correct answers, allowing for easy access and manipulation.
- **Dictionaries**: Served as the primary data structure for organizing each question with its associated options and the correct answer.

## **Algorithms Implemented**

- **Text File Processing**: Developed an algorithm to parse a text file, extract questions and options, and identify correct answers.
- **Randomization**: Implemented the **`random.shuffle`** method to randomize the order of questions and options, enhancing the quiz experience.

## **Development Process**

1. **File Parsing**: Designed a function to read a text file line by line, identify questions and options, and store them in a structured format.
2. **Quiz Administration**: Created an interactive quiz function that presents questions to the user, accepts responses, and provides immediate feedback.
3. **Scoring Mechanism**: Developed a scoring algorithm that tallies correct answers and presents the user with their final score.

## **Challenges and Solutions**

- **File Processing**: Encountered challenges in distinguishing between questions, options, and correct answers. Overcame this by implementing conditional checks based on line content and formatting.
- **User Interaction**: Ensured robust input handling to accommodate various user input formats and prevent errors during the quiz.

## **Conclusion**

The completion of this Python programming project demonstrates my ability to apply data structures and algorithms to create practical, user-centric applications. The skills honed during this project, such as code organization, algorithmic thinking, and problem-solving, are essential for any software development role and are particularly valuable in the field of cybersecurity. I am confident that this experience, along with my passion for continuous learning, makes me a strong candidate for the Poly Cyber Work-Learn Scheme by the Digital and Intelligence Service.