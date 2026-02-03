# School-Shedule-Maker
while True:
    from datetime import datetime, timedelta # Импортируем правильно для краткости
    a = input("Start of the lesson: ")
    b = int(input("Break time: "))
    c = int(input("How many lessons: "))
    d = int(input("How long is one lesson: "))

    start_lesson = datetime.strptime(a, '%H:%M')
    print('Time Shedule:')

    for i in range(1, c + 1): 
        end_lesson = start_lesson + timedelta(minutes=d)
        print(f"{start_lesson.strftime('%H:%M')} - {end_lesson.strftime('%H:%M')}")
        start_lesson = end_lesson + timedelta(minutes=b)
