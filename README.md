# CompanyOrg
🔧 Mini-Project Challenge: "Company Org & Insights"
💼 Scenario:
You're building a lightweight company tool that analyzes employees, managers, and departments. This version introduces multi-role employees, missing managers, and dynamic input (like searching by name or department).

📌 Setup Requirements
1. Declare These Arrays
ts
Copy
Edit
const departments = [
  { id: 1, name: "Engineering" },
  { id: 2, name: "Marketing" },
  { id: 3, name: "HR" },
  { id: 4, name: "Sales" },
];

const managers = [
  { id: 1, name: "Alice", departmentId: 1 },
  { id: 2, name: "Bob", departmentId: 2 },
  // Notice: No manager for department 3 (HR)
  { id: 4, name: "Diana", departmentId: 4 },
];

const employees = [
  { id: 1, name: "Eli", departmentId: 1, salary: 5000 },
  { id: 2, name: "Dana", departmentId: 1, salary: 5200 },
  { id: 3, name: "Frank", departmentId: 2, salary: 4700 },
  { id: 4, name: "Grace", departmentId: 2, salary: 4600 },
  { id: 5, name: "Hank", departmentId: 3, salary: 4000 },
  { id: 6, name: "Ivy", departmentId: 3, salary: 4100 },
  { id: 7, name: "Jack", departmentId: 4, salary: 4800 },
  { id: 8, name: "Kara", departmentId: 4, salary: 4700 },
  // Extra twist: Employee who works in two departments (dual role)
  { id: 9, name: "Leo", departmentId: 1, salary: 2500 },
  { id: 9, name: "Leo", departmentId: 4, salary: 2500 },
];
✅ Functional Requirements
1. printEmployeesByDepartmentName(departmentName: string)
Find the department by name (case insensitive).

Print all employees in that department.

2. printFullCompanyReport()
Loop over all departments.

For each:

Print department name

Print manager name (or "No Manager Assigned")

Print total salary

Print number of employees

3. findEmployeeDepartments(employeeName: string)
Find all departments an employee works in (they may appear more than once).

Print a list of those departments and their total combined salary.

🌶 Bonus Challenges (Stretch Goals)
a. getTopEarningDepartment()
Find which department has the highest total salary payout.

b. listManagersWithoutEmployees()
Identify if any manager is managing a department with 0 employees.

c. getSalaryRangeByDepartment(departmentId: number)
Print min, max, and average salary in that department.

