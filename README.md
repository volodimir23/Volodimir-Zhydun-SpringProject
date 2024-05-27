System Behaviors:

User Management:

•	Create user account (student or teacher)
•	Authenticate user (login)
•	Retrieve user profile
•	Update user profile
•	Delete user account (optional)

Test Management (Teacher):

•	Create new test
•	Retrieve test details
•	Update test details
•	Delete test
•	Add question to test
•	Remove question from test
•	Retrieve list of tests (with optional filtering/sorting)

Test Taking (Student):

•	Retrieve available tests (for a subject)
•	Start test
•	Submit answer for a question
•	Complete test
•	Retrieve test results

Results and Analytics:

•	Retrieve test results for a student (teacher view)
•	Retrieve test results for all students (teacher view)
•	Retrieve aggregated test statistics (e.g., average score, distribution)

Scheduling and Notifications:

•	Create test schedule
•	Retrieve test schedule
•	Send notification to students about upcoming tests
•	Send notification to teachers about completed tests
•	Reporting

User Management

POST /api/users: Create a new user (student or teacher).
POST /api/users/login: Authenticate a user (login).
GET /api/users/{userId}: Retrieve a user's profile.
PUT /api/users/{userId}: Update a user's profile.
DELETE /api/users/{userId}: Delete a user account (optional).
Test Management (Teacher)

POST /api/tests: Create a new test.
GET /api/tests/{testId}: Retrieve details of a specific test.
PUT /api/tests/{testId}: Update details of a specific test.
DELETE /api/tests/{testId}: Delete a specific test.
POST /api/tests/{testId}/questions: Add a question to a specific test.
DELETE /api/tests/{testId}/questions/{questionId}: Remove a question from a specific test.
GET /api/tests: Retrieve a list of all tests (with optional filtering and sorting).
Test Taking (Student)

GET /api/tests/available: Retrieve available tests for a student (filtered by subject).
POST /api/tests/{testId}/start: Start a specific test.
POST /api/tests/{testId}/submit: Submit an answer for a question in a specific test.
POST /api/tests/{testId}/complete: Complete a specific test.
GET /api/results/{testId}: Retrieve the results of a specific test for the student.
Results and Analytics

GET /api/results/{testId}: (Teacher) Retrieve the results of a specific test for a specific student.
GET /api/results: (Teacher) Retrieve the results of all tests for all students.
GET /api/statistics/{testId}: (Teacher) Retrieve aggregated statistics for a specific test.
Scheduling and Notifications

POST /api/schedule: Create a new test schedule.
GET /api/schedule: Retrieve the test schedule.
POST /api/notifications: Send a notification (to students or teachers).
Reporting

GET /api/reports/{reportType}: Generate a report (e.g., individual results, group results).
