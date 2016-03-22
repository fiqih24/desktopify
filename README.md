# desktopify

Easily create and display notifications using Notification API Standard.

Creates the object and binds 2 events: 

## click

Ask for permission and sets up.

## notify (title, body, [icon])

Shows the notification.

# Usage

	$('<button\/>')
		.attr('id','desktopify')
		.appendTo('body')
		.desktopify({
			callback: function() {
				$('<form>' +
					'<input name="title"\/>' +
					'<textarea name="body"\/>' +
					'<input name="btn" type="button" value="notify"\>' +
				'<\/form>')
					.appendTo('body')
					.find('input[name="btn"]')
					.click(function(){
						$('#desktopify').trigger('notify', [
							$('[name="body"]').val(),
							$('[name="title"]').val()
						]);
						return false;
					});
			},
			unsupported: function() {
				$('#destopify').remove();
			}
		});


# Reference

See http://j.mp/k7JHyF for demo and detailed information.

