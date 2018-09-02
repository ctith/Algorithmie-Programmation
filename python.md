# Introduction data science - code academy

Kenny's first job out of college is teaching high-school algebra. It's a normal day in school and Kenny needs to break the class up into pairs for a project. Sounds easy enough, but Kenny wants to match the students who are struggling with those who understand the material.
Kenny looks at the problem and thinks to himself, "You know what? I'll use an algorithm to pair up these students!"

Kenny quickly writes up his class roster using the Python programming language and writes a program that pairs the highest scoring student with the lowest scoring student, the second highest scoring student with the second lowest scoring student, and so on.

What does that mean?
An algorithm is a step-by-step solution to a general type of problem. To solve this student-pairing problem, Kenny needs to write a sorting algorithm

![](https://github.com/ctith/Algorithmie-Programmation/blob/master/2018-09-02%2020_12_49-Survey%20of%20Computer%20Science%20_%20Codecademy.png?raw=truevg)

```python
# This is a Python Dictionary that contains all of the students in Kenny's class as well as their grades.
student_grades = {"Jeremy" : 87, "Kyla" : 82, "Ayesha" : 90, "Aleida" : 94, "Todd" : 79, "Maxwell" : 98, "Yolonda" : 81, "Kiyoko" : 71, "Dagmar" : 73, "Laura" : 91, "Shimeah" : 81, "Songqiao" : 92, "Frankie" : 87, "Natalia" : 95, "Gonzalo" : 82, "Pavel" : 78}

# This is a function that determines the student with the highest grade given a dictionary
def highest_grade(grades):
	top_of_class = list(grades.keys())[0]
	for student_a in grades:
		for student_b in grades:
			if (grades[student_a] > grades[student_b]) and (grades[student_a] > grades[top_of_class]):
				top_of_class = student_a
			elif (grades[student_b] > grades[student_a]) and (grades[student_b] > grades[top_of_class]):
				top_of_class = student_b
	return top_of_class

# This is a function that determines the student with the lowest grade given a dictionary
def lowest_grade(grades):
	bottom_of_class = list(grades.keys())[0]
	for student_a in grades:
		for student_b in grades:
			if (grades[student_a] < grades[student_b]) and (grades[student_a] < grades[bottom_of_class]):
				bottom_of_class = student_a
			elif (grades[student_b] < grades[student_a]) and (grades[student_b] < grades[bottom_of_class]):
				bottom_of_class = student_b
	return bottom_of_class

# This is Kenny's Algorithm! It sorts the students into pairs based on their grades.
def kennys_algorithm(grade_dict):
	student_pairs = []
	while len(grade_dict) > 0:
		student_pairs.append([highest_grade(grade_dict), lowest_grade(grade_dict)])
		grade_dict.pop(highest_grade(grade_dict))
		grade_dict.pop(lowest_grade(grade_dict))
	print(student_pairs)
  
# Paste the code below!
# This is a Python Dictionary that contains all of the students in Kenny's class as well as their grades.
student_grades = {"Jeremy" : 87, "Kyla" : 82, "Ayesha" : 90, "Aleida" : 94, "Todd" : 79, "Maxwell" : 98, "Yolonda" : 81, "Kiyoko" : 71, "Dagmar" : 73, "Laura" : 91, "Shimeah" : 81, "Songqiao" : 92, "Frankie" : 87, "Natalia" : 95, "Gonzalo" : 82, "Pavel" : 78}

# This is a function that determines the student with the highest grade given a dictionary
def highest_grade(grades):
	top_of_class = list(grades.keys())[0]
	for student_a in grades:
		for student_b in grades:
			if (grades[student_a] > grades[student_b]) and (grades[student_a] > grades[top_of_class]):
				top_of_class = student_a
			elif (grades[student_b] > grades[student_a]) and (grades[student_b] > grades[top_of_class]):
				top_of_class = student_b
	return top_of_class

# This is a function that determines the student with the lowest grade given a dictionary
def lowest_grade(grades):
	bottom_of_class = list(grades.keys())[0]
	for student_a in grades:
		for student_b in grades:
			if (grades[student_a] < grades[student_b]) and (grades[student_a] < grades[bottom_of_class]):
				bottom_of_class = student_a
			elif (grades[student_b] < grades[student_a]) and (grades[student_b] < grades[bottom_of_class]):
				bottom_of_class = student_b
	return bottom_of_class

# This is Kenny's Algorithm! It sorts the students into pairs based on their grades.
def kennys_algorithm(grade_dict):
	student_pairs = []
	while len(grade_dict) > 0:
		student_pairs.append([highest_grade(grade_dict), lowest_grade(grade_dict)])
		grade_dict.pop(highest_grade(grade_dict))
		grade_dict.pop(lowest_grade(grade_dict))
	print(student_pairs)
  
# Paste the code below!
kennys_algorithm(student_grades)
```
