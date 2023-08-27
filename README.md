# CGPA-Calculator-TAS-Task-1
def calculate_grade_point(grade):
    if grade == 'A':
        return 4.0
    elif grade == 'A-':
        return 3.7
    elif grade == 'B+':
        return 3.3
    elif grade == 'B':
        return 3.0
    elif grade == 'B-':
        return 2.7
    elif grade == 'C+':
        return 2.3
    elif grade == 'C':
        return 2.0
    elif grade == 'C-':
        return 1.7
    elif grade == 'D+':
        return 1.3
    elif grade == 'D':
        return 1.0
    else:
        return 0.0

def main():
    num_subjects = int(input("Enter the number of subjects: "))
    
  total_credit_hours = 0
  total_weighted_grade_points = 0
    
  for _ in range(num_subjects):
       grade = input("Enter the grade obtained (e.g., A, B+, C-): ")
      credit_hours = int(input("Enter the credit hours for this subject: "))
        
   grade_point = calculate_grade_point(grade)
   weighted_grade_points = grade_point * credit_hours
        
  total_credit_hours += credit_hours
  total_weighted_grade_points += weighted_grade_points
    
  if total_credit_hours > 0:
       cgpa = total_weighted_grade_points / total_credit_hours
       print(f"Your CGPA is: {cgpa:.2f}")
   else:
       print("No subjects entered.")
    
if _name_ == "_main_":
    main()
