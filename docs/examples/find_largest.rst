Find Largest
==========================

This is finding largest


Find third largest record using LIMIT
----------------------------------------

.. code-block:: sql

    SELECT *
    FROM employee_info
    ORDER BY salary
    LIMIT 2, 1
