<!DOCTYPE html>
<html lang="en">
<head>
 <meta charset="UTF-8">
 <meta name="viewport" content="width=device-width, initial-scale=1.0">
 <title>QR Code Generator</title>
 <script src="https://cdn.rawgit.com/davidshimjs/qrcodejs/gh-pages/qrcode.min.js"></script>
 <style>
   /* CSS styles */
   body {
     font-family: Arial, sans-serif;
     background-color: #ffe5ec; /* Light pink background */
     display: flex;
     flex-direction: column;
     justify-content: center;
     align-items: center;
     height: 100vh;
     margin: 0;
   }
   
   h1 {
     color: black; /* Black heading color */
     text-align: center;
     text-shadow: 2px 2px 5px #ff66b2; /* Pink shadow */
     margin-bottom: 20px; /* Add margin between heading and QR code */
   }
   
   #qrcode-container {
     text-align: center;
     border: 10px solid #ff66b2; /* Pink border */
     border-radius: 20px;
     padding: 20px;
     background-color: white; /* White background */
   }
   
   #qrcode {
     display: block;
     margin: 0 auto; /* Center horizontally */
   }
 </style>
</head>
<body>
 <h1>Scan the QR Code</h1>
 <div id="qrcode-container">
   <!-- Insert your QR code image below -->
   <div id="qrcode"></div>
   <!-- End of QR code image -->
 </div>

 <script>
   // JavaScript to generate QR code
   document.addEventListener('DOMContentLoaded', function() {
     // Get values for the QR code
     var googleLink = "https://aditi381.github.io/employeeforms/";
     var data = googleLink;

     // Generate QR code
     var qrcode = new QRCode(document.getElementById('qrcode'), {
       text: data,
       width: 256,
       height: 256
     });
   });
 </script>
</body>
</html>
