# leadshooktime<br>

Add Script to Decision Treee Head <br>

<script>
  var monthNames = ["January", "February", "March", "April", "May", "June",
  "July", "August", "September", "October", "November", "December"
];
var n = new Date();
var y = n.getFullYear();
var m = n.getMonth() + 1;
var d = n.getDate();
var date = monthNames[n.getMonth()] + ' ' + d + ', ' + y;
var setDate = setInterval(function () {
  if (typeof $ === 'undefined') return;
  var $date = $('.app #date')
  if($date.length > 0) {
    $date.val(date).trigger('change');
    clearInterval(setDate);
  }
}, 500);
</script><br><br>


create the following custom fields<br>

'test_date_1'<br>
'test_date_2'<br>
'test_date_3'<br>

Add Date Node to Capture date you want to use as your base date eg 'when did you leave?"<br>

Add Script to that node.<br>

<script>
  console.log('test');
  DT.setField('test_date_1', moment.utc().startOf('day').subtract(6, 'months').valueOf())
  DT.setField('test_date_2', moment.utc().startOf('day').subtract(6, 'years').valueOf())
  DT.setField('test_date_3', moment.utc().startOf('day').add(1, 'day').valueOf())
</script><br><br>

add decision node to filter out those that don't meet criteria<br>

Deny Past<br>
When did you leave is less than or equal to 'test_date_1'<br>

Deny Future<br>
When did you leave is greater than  or equal 'test_date_3'<br>

Accept <br>
When did you leave is greater than  or equal 'test_date_1'<br>

