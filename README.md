# leadshooktime

create the following custom fields

'test_date_1'
'test_date_2'
'test_date_3'

add decision node to filter out those that don't meet criteria

Deny Past
When did you leave is less than or equal to 'test_date_1'

Deny Future
When did you leave is greater than  or equal 'test_date_3'

Accept 
When did you leave is greater than  or equal 'test_date_1'
