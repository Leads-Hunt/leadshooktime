# leadshooktime<br>

create the following custom fields<br>

'test_date_1'<br>
'test_date_2'<br>
'test_date_3'<br>

add decision node to filter out those that don't meet criteria<br>

Deny Past<br>
When did you leave is less than or equal to 'test_date_1'<br>

Deny Future<br>
When did you leave is greater than  or equal 'test_date_3'<br>

Accept <br>
When did you leave is greater than  or equal 'test_date_1'<br>

