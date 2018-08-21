Declare
Cursor cur_first_dept (N_Row NUMBER DEFAULT 1) IS
select dpt_id,dpt_Name from
department where ROWNUM<=N_Row;

cur_var_dept cur_first_dept%ROWTYPE;
Begin
open cur_first_dept(4);
LOOP
Fetch cur_first_dept INTO
cur_var_dept;
EXIT when cur_first_dept%NOTFOUND;
DBMS_OUTPUT.PUT_LINE ('Dpt_id:' || cur_var_dept.dpt_id);
DBMS_OUTPUT.PUT_LINE ('Dpt_name' ||  cur_var_dept.dpt_name);
DBMS_OUTPUT.PUT_LINE ('ROW_Number' || cur_first_dept%ROWCOUNT );
END loop;
if (cur_first_dept%isopen) then
close cur_first_dept;
END If;
END;
