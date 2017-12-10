# easycard
Jquery credit card animation for payment forms

[DEMO](http://demos.onuraltinsoy.com/en/easycard/example.html)

### required##
 - jQuery Javascript Library
 - Font Awesome Icon Library
 - Bootstrap (Optional)
 
### Install##

> Create HTML5 document that including easycard stylesheet and jQuery plugin, don't forget font awesome

	<!-- bootstrap stylesheet -->
	<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-alpha.6/css/bootstrap.min.css" integrity="sha384-rwoIResjU2yc3z8GV/NPeZWAv56rSmLldC3R/AZzGRnGxQQKnKkoFVhFQhNUwEyJ" crossorigin="anonymous">

	<!-- font awesome -->
	<link rel="stylesheet" type="text/css" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css">

	<!-- easycard stylesheet -->
	<link rel="stylesheet" type="text/css" href="css/easycard.min.css">

> add payment form

						<div class="form-group">
							<label>Full Name</label>
							<input type="text" class="form-control" id="name">
						</div>
						<div class="form-group">
							<label>Credit Card Number</label>
							<div class="input-group">
								<input type="text" class="form-control" id="number">
								<div class="input-group-addon"><i class="fa fa-credit-card"></i></div>
							</div>
						</div>
						<div class="form-group">
							<div class="row">
								<div class="col-md-8">
									<label>Expiry Date</label>
									<div class="input-group">
										<select class="form-control" id="date-m">
											<option>MM</option>
											<option value="01">01</option>
											<option value="02">02</option>
											<option value="03">03</option>
											<option value="04">04</option>
											<option value="05">05</option>
										</select>
										<select class="form-control" id="date-y">
											<option>YY</option>
											<option value="20">20</option>
											<option value="21">21</option>
											<option value="22">22</option>
											<option value="23">23</option>
											<option value="24">24</option>
										</select>
									</div>
								</div>
								<div class="col-md-4">
									<label>CVC</label>
									<input type="text" class="form-control" id="cvc">
								</div>
							</div>
						</div>
						<div class="form-group">
						<button class="btn btn-custom">PAY</button>
						</div>

> finally call the jQuery, Bootstrap and easycard plugin

	<!-- bootstrap javascripts -->
	<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
	<script src="https://cdnjs.cloudflare.com/ajax/libs/tether/1.4.0/js/tether.min.js" integrity="sha384-DztdAPBWPRXSA/3eYEEUWrWCy7G5KFbe8fFjk5JAIxUYHKkDx6Qin1DkWx51bBrb" crossorigin="anonymous"></script>
	<script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-alpha.6/js/bootstrap.min.js" integrity="sha384-vBWWzlZJ8ea9aCX4pEW3rVHjgjt7zpkNpZk+02D9phzyeVkE+jo0ieGizqPLForn" crossorigin="anonymous"></script>

	<!-- easycard plugin -->
	<script type="text/javascript" src="js/easycard.min.js"></script>

	<script type="text/javascript">
	$('.cc-wrapper').easycard();
	</script>

> example.html is full template sample

### Options and defaults##

		nameInput: '#name',
		numberInput: '#number',
		cvcInput: '#cvc',
		dateMonthInput: '#date-m',
		dateYearInput: '#date-y',
		cardWidth: '100%',
		backgroundCode: '#333',
		numberMask: true (switch to false if you used another input mask plugin),
		defaultName: 'full name',
		defaultNumber: '**** **** **** ****',
		defaultDate: 'MM / YY',
		defaultCvc: '***'
