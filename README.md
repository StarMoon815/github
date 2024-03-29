# github
TASK 1:
i. CREATE TABLE STUDENT(
ID BIGINT NOT NULL PRIMARY KEY,
 birthday_date DATE NOT NULL,
group_number INT
);
ii. CREATE TABLE SUBJECT(
ID BIGSERIAL NOT NULL PRIMARY KEY,
name VARCHAR(60) NOT NULL,
describtion VARCHAR(60) NOT NULL,
grade INT );

iii. 
CREATE TABLE PaymentTime(
id BIGSERIAL NOT NULL PRIMARY KEY,
name VARCHAR(60) NOT NULL
);
iv.
CREATE TABLE PAYMENT(
ID BIGSERIAL NOT NULL PRIMARY KEY,
type_id BIGINT REFERENCES PaymentTime(id),
student_id BIGINT REFERENCES STUDENT(id),
payment_date DATE );

v.
CREATE TABLE MARK(
ID BIGSERIAL NOT NULL PRIMARY KEY,
student_id BIGINT REFERENCES STUDENT(id),
subject_id BIGINT REFERENCES SUBJECT(id),
mark INT );


TASK 2:
1.

INSERT INTO Student(name, group) VALUES ('John', '1');
INSERT INTO Student(name, group) VALUES ('Chris', '1');
INSERT INTO Student(name, group) VALUES ('Carl', '1');

INSERT INTO Student(name, group) VALUES ('Oliver', '2');
INSERT INTO Student(name, group) VALUES ('James', '2');
INSERT INTO Student(name, group) VALUES ('Lucas', '2');
INSERT INTO Student(name, group) VALUES ('Henry', '2');

INSERT INTO Student(name, group) VALUES ('Jacob', '3');
INSERT INTO Student(name, group) VALUES ('Logan', '3');

INSERT INTO Student(name, group) VALUES ('Diyor', '4');
INSERT INTO Student(name, group) VALUES ('Saidazim', '4');

INSERT INTO Student(name, group) VALUES ('Amir', '5');
INSERT INTO Student(name, group) VALUES ('Farrux', '5');
INSERT INTO Student(name, group) VALUES ('John', '1');
INSERT INTO Student(name, group) VALUES ('Chris', '1');
INSERT INTO Student(name, group) VALUES ('Carl', '1');

INSERT INTO Student(name, group) VALUES ('Oliver', '2');
INSERT INTO Student(name, group) VALUES ('James', '2');
INSERT INTO Student(name, group) VALUES ('Lucas', '2');
INSERT INTO Student(name, group) VALUES ('Henry', '2');

INSERT INTO Student(name, group) VALUES ('Jacob', '3');
INSERT INTO Student(name, group) VALUES ('Logan', '3');

INSERT INTO Student(name, group) VALUES ('Diyor', '4');
INSERT INTO Student(name, group) VALUES ('Saidazim', '4');

INSERT INTO Student(name, group) VALUES ('Amir', '5');
INSERT INTO Student(name, group) VALUES ('Farrux', '5');

2. 
INSERT INTO Subject(name, grade) VALUES ('Art', '1');
INSERT INTO Subject(name, grade) VALUES ('Music', '1');

INSERT INTO Subject(name, grade) VALUES ('Geography', '2');
INSERT INTO Subject(name, grade) VALUES ('History', '2');

INSERT INTO Subject(name, grade) VALUES ('PE', '3');
INSERT INTO Subject(name, grade) VALUES ('Math', '3');

INSERT INTO Subject(name, grade) VALUES ('Science', '4');
INSERT INTO Subject(name, grade) VALUES ('IT', '4');

INSERT INTO Subject(name, grade) VALUES ('English', '5');
INSERT INTO Subject(name, grade) VALUES ('Social Studies', '5');



3.
INSERT INTO PaymentTypes(name) VALUES('DAILY');
INSERT INTO PaymentTypes(name) VALUES('WEEKLY');
INSERT INTO PaymentTypes(name) VALUES('MONTHLY');



4. INSERT INTO Mark (StudentName, Subject, Mark) VALUES('Chris', 'Art', 8);
INSERT INTO Mark (StudentName, Subject, Mark) VALUES('Oliver', 'History', 5);
INSERT INTO Mark (StudentName, Subject, Mark) VALUES('James', 'Geography', 9);
INSERT INTO Mark (StudentName, Subject, Mark) VALUES('Jacob', 'Math', 4);
INSERT INTO Mark (StudentName, Subject, Mark) VALUES('Logan', 'PE', 9);

TASK 3:
ALTER TABLE Student ALTER COLUMN birthday DATE NOT NULL;

ALTER TABLE Mark ALTER COLUMN mark INT CHECK (mark BETWEEN 1 AND 10);
ALTER TABLE Mark ALTER COLUMN student_id BIGINT NOT NULL;
ALTER TABLE Mark ALTER COLUMN subject_id BIGINT NOT NULL;

ALTER TABLE Subject ALTER COLUMN grade INT CHECK (grade BETWEEN 1 AND 5);

ALTER TABLE PaymentType ADD unique_name UNIQUE (name);

ALTER TABLE Payment ALTER COLUMN type_id BIGINT NOT NULL;
ALTER TABLE Payment ALTER COLUMN amount DECIMAL NOT NULL;
ALTER TABLE Payment ALTER COLUMN payment_date DATE NOT NULL;


TASK 4:
1. 
SELECT * FROM student;
2. 
SELECT * FROM student LIMIT 50;
3.
 SELECT name FROM student;
4.
 SELECT DISTINCT amount FROM payment;





























