<script src="https://checkout.stripe.com/checkout.js"></script>

.myButton {
	-moz-box-shadow:inset 0px 39px 0px -24px #d54b7b;
	-webkit-box-shadow:inset 0px 39px 0px -24px #d54b7b;
	box-shadow:inset 0px 39px 0px -24px #d54b7b;
	background:-webkit-gradient(linear, left top, left bottom, color-stop(0.05, #d54b7b), color-stop(1, #d54b7b));
	background:-moz-linear-gradient(top, #d54b7b 5%, #d54b7b 100%);
	background:-webkit-linear-gradient(top, #d54b7b 5%, #d54b7b 100%);
	background:-o-linear-gradient(top, #d54b7b 5%, #d54b7b 100%);
	background:-ms-linear-gradient(top, #d54b7b 5%, #d54b7b 100%);
	background:linear-gradient(to bottom, #d54b7b 5%, #d54b7b 100%);
	filter:progid:DXImageTransform.Microsoft.gradient(startColorstr='#d54b7b', endColorstr='#d54b7b',GradientType=0);
	background-color:#d54b7b;
	display:inline-block;
	cursor:pointer;
	color:#ffffff;
	font-family:Verdana;
	font-size:13px;
	padding:24px 45px;
	text-decoration:none;
	text-shadow:0px 1px 0px #d54b7b;
}
.myButton:hover {
	background:-webkit-gradient(linear, left top, left bottom, color-stop(0.05, #d54b7b), color-stop(1, #d54b7b));
	background:-moz-linear-gradient(top, #d54b7b 5%, #d54b7b 100%);
	background:-webkit-linear-gradient(top, #d54b7b 5%, #d54b7b 100%);
	background:-o-linear-gradient(top, #d54b7b 5%, #d54b7b 100%);
	background:-ms-linear-gradient(top, #d54b7b 5%, #d54b7b 100%);
	background:linear-gradient(to bottom, #d54b7b 5%, #d54b7b 100%);
	filter:progid:DXImageTransform.Microsoft.gradient(startColorstr='#d54b7b', endColorstr='#d54b7b',GradientType=0);
	background-color:#d54b7b;
}
.myButton:active {
	position:relative;
	top:1px;
}

<script>
  var handler = StripeCheckout.configure({
    key: 'pk_test_hAcACdMvW5MG6TfYJ6o0dpMm',
    image: '/img/documentation/checkout/marketplace.png',
    locale: 'auto',
    token: function(token) { 
    }
  });

  $('#customButton').on('click', function(e) {
    handler.open({
      name: '90-Day VIP Love Coaching',
      description: 'LoveSmart with Coach Daniella',
      amount: 2000
    });
    e.preventDefault();
  });

  // Close Checkout on page navigation:
  $(window).on('popstate', function() {
    handler.close();
  });
</script>
