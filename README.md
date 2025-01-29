declare

d number; 

begin

d:=&weekday1to7; 

case d

when 1 then dbms_output.put_line('Monday'); 

when 2 then dbms_output.put_line('Tuesday');

when 3 then dbms_output.put_line('Wednesday'); 

when 4 then dbms_output.put_line('Thursday'); 

when 5 then dbms_output.put_line('Friday'); 

when 6 then dbms_output.put_line('Saturday'); 

when 7 then dbms_output.put_line('Sunday'); 

elsedbms_output.put_line('not a valid week day number'); 

end case; 

end;

/
