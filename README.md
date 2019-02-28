# BookReaderwithTurnJS
Implementing Turn.JS to create a basic web reader
Turn.JS 
Turn.JS is a javascript library that gives our content a book like feel.Its easy to implement when compared to animating it using css files.

Pseudo Code: 
Step 1 : $(window).ready(function() -- This is  a jQuery function, $(window).ready(function(){ - here ready is used so that the program doesnot run before the complete webpage is loaded.
Step 2 : 	$('#flipbook').turn({ - flipbook is a class in the div where the content of the book is stored, and .turn is used to turn the page.
Step 3: $(window).bind('keydown', function(e){ - This is used to give access to the keyboard arrow keys.

Sample Code :

<script type="text/javascript"> 

		$(window).ready(function() {     
			$('#flipbook').turn({
								display: 'double',
								acceleration: true,
								gradients: !$.isTouch,
								elevation:200,
								when: {
									turned: function(e, page) {
										/*console.log('Current view: ', $(this).turn('view'));*/
									}
								}
							});
		});
		
		
		$(window).bind('keydown', function(e){
			
			if (e.keyCode==37)
				$('#flipbook').turn('previous');
			else if (e.keyCode==39)
				$('#flipbook').turn('next');
				
		});

	</script>
