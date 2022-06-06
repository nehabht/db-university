
##  QUERY GROUP BY:
### 1. Contare quanti iscritti ci sono stati ogni anno
```
SELECT count(`id`) AS `new_students`, YEAR(`enrolment_date`) AS `year_of_enrolment`
FROM `students`
GROUP by year(`enrolment_date`)
```
### 2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio
```
SELECT COUNT(`id`) as `teachers_same_bulding`, `office_address`
FROM `teachers`
GROUP BY `office_address`
```
### 3. Calcolare la media dei voti di ogni appello d'esame
```
SELECT AVG(`exam_student`.`vote`) AS `average_votes`, `exams`.`date` AS `exam_date`, `courses`.`name` AS `course_name`
FROM `exam_student`
JOIN `exams` ON `exams`.`id` = `exam_student`.`exam_id`
JOIN `courses` ON `courses`.`id` = `exams`.`course_id`
GROUP BY `exams`.`id`
```
### 4. Contare quanti corsi di laurea ci sono per ogni dipartimento
```
SELECT count(`degrees`.`id`) AS `number_of_degrees`, `departments`.`name` AS `departments_name`
FROM `degrees`
JOIN `departments` ON `departments`.`id` = `degrees`.`department_id` 
GROUP BY `departments`.`id`
```