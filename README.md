# JSWebCam
Stream webcam using javascript

With this project I will show you how to stream your webcam using javascript.
To do this I'm going to use javascript,
navigator.mediaDevices  function.


<!DOCTYPE html>
	<head>
		<meta content="charset=utf-8" http-equiv="Content-Type">
	</head>

	<body>
		<div id="content">
			<video autoplay="true" id="video"></video>
		</div>

		<script>
			var videoObject = document.querySelector("#video");
 
			if (navigator.mediaDevices.getUserMedia) {       
				navigator.mediaDevices.getUserMedia({video: true}).then(function(stream) {
					videoObject.srcObject = stream;
				}).catch(function(err0r) {
					console.log("Something went wrong!");
				});
			}
		</script>
	</body>
</html>

