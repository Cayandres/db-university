Soluzioni
===
1. SELECT *
  FROM `students`
  WHERE YEAR(`date_of_birth`) = 1990;

  Oppure

  SELECT *
  FROM `students`
  WHERE `date_of_birth` LIKE '1990%';

2. SELECT *
  FROM `courses`
  WHERE `cfu` > 10;

3. SELECT *
  FROM `students`
  WHERE (2023 - YEAR(`date_of_birth`)) = 30;

4. SELECT *
  FROM `courses`
  WHERE `period` = 'I semestre'
  AND `year` = 1;

5. SELECT *
  FROM `exams`
  WHERE HOUR(`hour`) >= 14
  AND `date` = '2020-06-20';

6. SELECT *
  FROM `degrees`
  WHERE `level` = 'magistrale';

7. SELECT COUNT(*) AS `number_of_departments`
  FROM `departments`;

8. SELECT COUNT(*) AS `number_of_teachers_without_number`
  FROM `teachers`
  WHERE `phone` IS NULL;
