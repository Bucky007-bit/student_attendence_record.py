from datetime import datetime

# Dictionary to store student attendance
attendance_record = {}

def mark_attendance(student_name):
    """Mark attendance for a student."""
    date_today = datetime.now().date()
    if student_name in attendance_record:
        attendance_record[student_name].append(date_today)
    else:
        attendance_record[student_name] = [date_today]
    print(f"Attendance marked for {student_name} on {date_today}.")

def view_attendance(student_name):
    """View attendance for a specific student."""
    if student_name in attendance_record:
        print(f"Attendance for {student_name}: {attendance_record[student_name]}")
    else:
        print(f"No attendance record found for {student_name}.")

def generate_attendance_report():
    """Generate a report of attendance percentages for all students."""
    total_classes = len(set(date for dates in attendance_record.values() for date in dates))
    report = {}
    
    for student, dates in attendance_record.items():
        attendance_count = len(dates)
        attendance_percentage = (attendance_count / total_classes) * 100 if total_classes > 0 else 0
        report[student] = attendance_percentage
    
    print("Attendance Report:")
    for student, percentage in report.items():
        print(f"{student}: {percentage:.2f}%")

def main():
    while True:
        print("\nAttendance System")
        print("1. Mark Attendance")
        print("2. View Attendance")
        print("3. Generate Attendance Report")
        print("4. Exit")
        
        choice = input("Choose an option (1-4): ")
        
        if choice == '1':
            student_name = input("Enter the student's name: ")
            mark_attendance(student_name)
        elif choice == '2':
            student_name = input("Enter the student's name: ")
            view_attendance(student_name)
        elif choice == '3':
            generate_attendance_report()
        elif choice == '4':
            print("Exiting the program.")
            break
        else:
            print("Invalid choice. Please try again.")

if _name_ == "_main_":
    main()
