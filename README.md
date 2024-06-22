# Pythpn
MCQ
question_data = {
    "QUESTION1": {
        "question": "which is the silicon valley of india?",
        "options": {"A": "delhi", "B":"hyderabad", "C":"chennai","D": "bengaluru"},
        "correct_ans": "D"
    },
    "QUESTION2": {
        "question": "Who invented exam?",
        "options": {"A": "Issac newton", "B": "galelio galeli", "C": "Henry Fischel","D":"jack ma"},
        "correct_ans": "C"
    },
     "QUESTION3": {
        "question": "What is the capital of Telangana?",
        "options": {"A": "Delhi", "B": "Hyderabad", "C": "Mysore","D":"Mumbai"},
        "correct_ans": "B"
    }
}

def result(answer, score):
    user_answer = input("Enter your option: ")
    if user_answer.upper() == answer:
        print("Correct answer!")
        score += 1
    else:
        print("Incorrect")
    return score

def func(question_data):
    score = 0
    print("WELCOME TO THE QUIZZ !")
    print("INSTRUCTIONS-1.enter only option not the whole answer")
    print("2.question will be three in  row you will get one after other")
    print("3.you  not allowed to take quizz if you not agree with instructions ")
    choice=int(input("if you agree enter \"YES=1\" otherwise \"NO=0\""))
    if choice==1:
        print(f"{question_data['QUESTION1']['question']}\n{question_data['QUESTION1']['options']}")
        score = result(question_data['QUESTION1']['correct_ans'], score)
        print(f"{question_data['QUESTION2']['question']}\n{question_data['QUESTION2']['options']}")
        score = result(question_data['QUESTION2']['correct_ans'], score)
        print(f"{question_data['QUESTION3']['question']}\n{question_data['QUESTION3']['options']}")
        score = result(question_data['QUESTION3']['correct_ans'], score)
        print(f"Student scored: {score} marks")
    else:
        print("you need to agree for instruction to take quizz")

func(question_data)
