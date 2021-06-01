Find Largest
==========================

This is finding largest

Sample table
----------------------------------------
table name: *employee_info*

.. code-block:: sql

    +--------+--------+
    | emp_id | salary |
    +--------+--------+
    |     10 |    100 |
    |     20 |    101 |
    |     30 |    102 |
    |     40 |    103 |
    +--------+--------+


Find third largest record using LIMIT
----------------------------------------

.. code-block:: sql

    SELECT *
    FROM employee_info
    ORDER BY salary
    LIMIT 2, 1

Here the key is *LIMIT*


Find third largest record without LIMIT
----------------------------------------

.. code-block:: sql

    SELECT *
    FROM employee_info e1
    WHERE N-1 =
    (
        SELECT COUNT(DISTINCT salary)
        FROM employee_info e2
        WHERE e1.salary < e2.salary
    )


Select records where salary of employee is greater than emp_id 30
--------------------------------------------------------------------------------

.. code-block:: sql

    SELECT *
    FROM employee_info
    WHERE salary > (
        SELECT salary
        FROM employee_info
        WHERE emp_id = 30
    )