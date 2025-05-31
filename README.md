<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Adurino 101 PDF - Buy Now</title>
  <link rel="manifest" href="/manifest.json">
  <script src="https://checkout.flutterwave.com/v3.js"></script>
  <script>
    if ('serviceWorker' in navigator) {
      window.addEventListener('load', function () {
        navigator.serviceWorker.register('/service-worker.js');
      });
    }
  </script>
  <style>
    body { font-family: Arial, sans-serif; background: #f8f8f8; margin: 0; padding: 2rem; text-align: center; }
    .container { background: white; padding: 2rem; max-width: 500px; margin: auto; border-radius: 10px; box-shadow: 0 0 10px rgba(0,0,0,0.1); }
    input, button { padding: 10px; width: 90%; margin: 10px 0; border-radius: 5px; border: 1px solid #ccc; }
    button { background-color: #0a0; color: white; border: none; cursor: pointer; }
    button:hover { background-color: #080; }
    img.cover { max-width: 100%; border-radius: 10px; margin-bottom: 1rem; }
  </style>
</head>
<body>
  <div class="container">
    <img src="/mnt/data/file-6SFUP7kzrd9En2mPS866sR" alt="Adurino 101 Cover" class="cover">
    <h2>Adurino 101 PDF</h2>
    <p><strong>Price:</strong> ₦3,000</p>
    <p>Get access to the Adurino 101 practicals in PDF format.</p><input type="text" id="name" placeholder="Enter your full name" required />
<input type="email" id="email" placeholder="Enter your email" required />
<input type="tel" id="phone" placeholder="Enter your phone number" required />

<button onclick="makePayment()">Pay ₦3,000 with Flutterwave</button>

  </div>  <script>
    function makePayment() {
      const name = document.getElementById('name').value;
      const email = document.getElementById('email').value;
      const phone = document.getElementById('phone').value;

      if (!name || !email || !phone) {
        alert("Please fill in all details.");
        return;
      }

      FlutterwaveCheckout({
        public_key: "FLWPUBK_TEST-fc28ba138e70e7c59ad677650ddbf00e-X",
        tx_ref: "Adurino101PDF_" + Date.now(),
        amount: 3000,
        currency: "NGN",
        payment_options: "card,ussd,banktransfer",
        customer: {
          email: email,
          phonenumber: phone,
          name: name,
        },
        callback: function (data) {
          if (data.status === "successful") {
            window.location.href = "https://drive.google.com/uc?export=download&id=1OGvo9w7DX_LjnRPUN_yTPQxYumR30t_w";
          } else {
            alert("Payment not successful. Try again.");
          }
        },
        customizations: {
          title: "Adurino 101 PDF",
          description: "Get instant access to the Adurino 101 PDF",
          logo: "https://your-logo-url.com/logo.png",
        },
      });
    }
  </script></body>
</html>
