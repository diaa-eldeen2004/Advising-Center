🎓 Project Title: Academic Course Advisor
🧩 Purpose:
The program reads a student's academic transcript and compares it to available courses across academic levels (100, 200, 300, and 400). Based on the student's total completed credit hours and course prerequisites, it recommends suitable courses for the upcoming term.

📂 Key Files Used:
transcript.txt — Contains the student's completed courses.

course_1.txt — First-year (100 level) courses.

course_2.txt — Second-year (200 level) courses.

course_3.txt — Third-year (300 level) courses.

course_4.txt — Fourth-year (400 level) courses.

ADVISE CENTER.txt — Output file with recommended courses.

🧱 Data Structures:
struct courses
Holds information about a single course:

name: Course name

code: Course code

hour: Credit hour

pre: Prerequisite course code

struct student
Holds information about a single student:

name, id, year, type: Basic student info

crs[n_crs]: Array of completed courses (max 6)

🧠 Core Functions:
Get_student_data()
Collects student data via user input.

Reads 6 completed courses from transcript.txt.

Get_courses_data_1/2/3/4()
Loads available courses for each academic level from the respective files.

totall()
Calculates total credit hours from the completed courses.

check(int total)
Based on the total credit hours:

0–33 → Recommends 100-level courses.

34–69 → Recommends 200-level.

70–101 → Recommends 300-level.

101 → Recommends 400-level.

Filters out already-taken courses and checks if prerequisites are satisfied.

Writes the suggested courses into ADVISE CENTER.txt.

🖥️ Main Flow in main()
cpp
Copy
Edit
1. Get_student_data();
2. Load all course levels (1 to 4);
3. Calculate total credit hours;
4. Generate course recommendations;
5. Notify user of generated recommendations.
📌 Features:
Reads structured text files to gather course and student data.

Validates course prerequisites.

Outputs human-readable recommendations to a file.

🔍 Limitations:
Hardcoded limits: 6 courses max, 1 student only.

Doesn’t check if a prerequisite has already been taken in prior semesters robustly.

File reading is rigidly structured and lacks error recovery.

No dynamic memory or support for multiple students.


