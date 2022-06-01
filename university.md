
1. Selezionare tutti gli studenti nati nel 1990 (160)
SELECT * FROM `students` WHERE `date_of_birth` LIKE "1990%"

2. Selezionare tutti i corsi che valgono più di 10 crediti (479)
SELECT * FROM `courses` WHERE cfu >= 11

3. Selezionare tutti gli studenti che hanno più di 30 anni
SELECT * FROM `students` WHERE date_of_birth <= "1991-12-31"

4. Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di laurea (286)
SELECT * FROM `courses` where `year` = 1 AND `period` = 'I semestre'

5. Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del 20/06/2020 (21)
SELECT * FROM `exams` where hour(`hour`) >= '14:00:00' AND `date` = '2020-06-20'

6. Selezionare tutti i corsi di laurea magistrale (38)
SELECT * FROM `degrees` where `level` = 'magistrale'

7. Da quanti dipartimenti è composta l'università? (12)
SELECT COUNT(id) FROM `departments`

8. Quanti sono gli insegnanti che non hanno un numero di telefono? (50)
SELECT * FROM `teachers` WHERE `phone` IS NULL