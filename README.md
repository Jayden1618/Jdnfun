declare

studid number; days number; fine number; 

begin

studid:=&studid; 

days:=&days; 

if days < 7 then 

fine:=0; 

else

fine:=days-7; 

end if; 

dbms_output.put_line('student id number -> '||studid); 

dbms_output.put_line('fine to be paid -> '||fine); 

end;

/
