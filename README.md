# codexercises
lloyd = {
    "name": "Lloyd",
    "homework": [90.0, 97.0, 75.0, 92.0],
    "quizzes": [88.0, 40.0, 94.0],
    "tests": [75.0, 90.0]
}
alice = {
    "name": "Alice",
    "homework": [100.0, 92.0, 98.0, 100.0],
    "quizzes": [82.0, 83.0, 91.0],
    "tests": [89.0, 97.0]
}
tyler = {
    "name": "Tyler",
    "homework": [0.0, 87.0, 75.0, 22.0],
    "quizzes": [0.0, 75.0, 78.0],
    "tests": [100.0, 100.0]
}

# Add your function below!
student = ["lloyd", "alice", "tyler"]


def average(numbers):
    total = 0
    for number in student:
        total = int(sum(numbers))
    return total / len(numbers)


def get_average(student):
    result = 0
    result = average(student["homework"]) * .1 \
             + average(student["quizzes"]) * .3 \
             + average(student["tests"]) * .6
    return result


def get_letter_grade(score):
    if score >= 90:
        return "A"
    elif score < 90 and score >= 80:
        return "B"
    elif score < 80 and score >= 70:
        return "C"
    elif score < 70 and score >= 60:
        return "D"
    else:
        return "F"


print get_letter_grade(get_average(lloyd))


def get_class_average(student):
    results = []
    for child in student:
        grade = get_average(student)
        results.append(grade)
        return results


print get_class_average(student)
