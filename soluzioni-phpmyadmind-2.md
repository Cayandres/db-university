Soluzioni
===

1. SELECT `degrees`.`name`, `students`.`name`, `students`.`surname`
   FROM `students`
   INNER JOIN `degrees`
   ON `students`.`degree_id` = `degrees`.`id`
   WHERE `degrees`.`name`= 'Corso di laurea in economia' ;

2. SELECT  `departments`.`name` AS `departments_name`,`degrees`.`name`, `degrees`.`level`
   FROM  `degrees`
   INNER JOIN  `departments`
   ON  `departments`.`id` =  `degrees`.`department_id`
   WHERE `degrees`.`level` = 'magistrale'
   AND `departments`.`name` = 'dipartimento di neuroscienze'

3. SELECT `degrees`.`name` AS `Corsi di laurea`,`teachers`.`name`, `teachers`.`surname`
   FROM `teachers`
   INNER JOIN `course_teacher`
   ON `teachers`.`id` = `course_teacher`.`teacher_id`
   INNER JOIN `courses`
   ON `course_teacher`.`course_id` = `courses`.`id`
   INNER JOIN `degrees`
   ON `courses`.`degree_id` = `degrees`.`id`
   WHERE `teachers`.`name`="fulvio"
   AND `teachers`.`surname`="amato"

4. SELECT `students`.`surname`,`students`.`name`, `degrees`.`name`, `departments`.`name`
   FROM `students`
   JOIN `degrees`
   ON `students`.`degree_id` = `degrees`.`id`
   JOIN `departments`
   ON `degrees`.`department_id` = `departments`.`id`
   ORDER BY `students`.`surname`;

5. SELECT `degrees`.`name` AS `Corso Di Laurea`,`departments`.`name`  AS `Dipartimento`
   FROM `degrees`
   JOIN `departments`
   ON `degrees`.`department_id` = `departments`.`id`