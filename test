import random

def generate_math_question(a, b):
    num1 = random.randint(a, b)
    num2 = random.randint(a, b)
    operator = random.choice(['+','-', '/', '*'])
    return f'{num1} {operator} {num2}  '

print(generate_math_question(1, 10))


def check_answer(a, b):
    try:
       b = float(b)
       return b == eval(a)   
    except ValueError:
        return False

print(check_answer("2 + 3", "5"))
print(check_answer("5 * 3", "10"))
print(check_answer("10-3", "семь"))



def math_quiz(number_of_questions=5):
    print("Добро пожаловать в математический тест!")
    correct_answers = 0

    for i in range(number_of_questions):
        q =  generate_math_question(1, 5)
        user_answer = input(f'{q}= ')
        if check_answer(q, user_answer):
            correct_answers += 1

    print("Тест завершен.")
    print(f"Вы правильно решили {correct_answers} из {number_of_questions} вопросов.")

    if correct_answers>= number_of_questions*0.8:
        print("Отлично! Вы получаете оценку A.")
    elif correct_answers>number_of_questions*0.6:
        print("Хорошо! Вы получаете оценку B.")
    else:
        print("Попробуйте еще раз. Вы получаете оценку C.")


# Запуск теста
math_quiz(7)
