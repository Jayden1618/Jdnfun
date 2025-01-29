declare

sname varchar2(20); 

grade char(1); 

begin 

sname:='&name'; 

grade:='&grade'; 

case grade 

when 'a' then dbms_output.put_line('remarks : excellent'); 

when 'b' then dbms_output.put_line(' remarks : very good'); 

when 'c' then dbms_output.put_line(' remarks : well done'); 

when 'd' then dbms_output.put_line(' remarks : you passed'); 

when 'f' then dbms_output.put_line(' remarks : better try again'); 

else dbms_output.put_line(' remarks : no such grade'); 

end case; 

end;

/
