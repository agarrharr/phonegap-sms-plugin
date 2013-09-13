phonegap-sms-plugin
=====================

Note! I'm currently testing this plugin. but if it doesn't work, and you know how to make it work, please let me know how to fix it or send me a pull request.

This Android Phonegap plugin allows you to easily send SMS in android using both native SMS Manager or by invoking the default android SMS app. This plugin works with PhoneGap 3.x version.

This was forked from https://github.com/javatechig/phonegap-sms-plugin so that I could upgreade it to phonegap 3.0.

Example Usage
=================

	<script type="text/javascript">
	$(document).ready(function() {
		//leave empty for sending sms using default intent
		$("#btnDefaultSMS").click(function(){
			var number = $("#numberTxt").val();
			var message = $("#messageTxt").val();
			SmsPlugin.prototype.send(number, message, '',
				function () { 
					alert('Message sent successfully');
				},
				function (e) {
					alert('Message Failed:' + e);
				}
			);
		});
	});
	</script>

	<input name="" id="numberTxt" placeholder="Enter mobile number" value="" type="tel" data-mini="true">
	<br/>
	<textarea name="" id="messageTxt" placeholder="Enter message" data-mini="false"></textarea>
	<br/>
	<input id="btnDefaultSMS" type="submit" data-theme="e" value="Send SMS" data-mini="false">
