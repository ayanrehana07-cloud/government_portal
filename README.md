<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Islamic Republic of Ansico - Portal</title>
    <style>
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; background-color: #e9f5ee; margin: 0; padding: 0; }
        header { background-color: #004d40; color: white; padding: 20px; text-align: center; border-bottom: 5px solid #ffd700; }
        .container { max-width: 600px; margin: 30px auto; background: white; padding: 30px; border-radius: 10px; box-shadow: 0 4px 15px rgba(0,0,0,0.2); }
        h2 { color: #004d40; text-align: center; border-bottom: 2px solid #eee; padding-bottom: 10px; }
        label { font-weight: bold; display: block; margin-top: 15px; color: #333; }
        input, select, textarea { width: 100%; padding: 12px; margin-top: 5px; border: 1px solid #ccc; border-radius: 5px; box-sizing: border-box; }
        .btn { background-color: #004d40; color: white; padding: 15px; border: none; border-radius: 5px; width: 100%; margin-top: 25px; font-size: 18px; cursor: pointer; transition: 0.3s; }
        .btn:hover { background-color: #00695c; }
        .contact-box { text-align: center; margin-top: 20px; font-size: 14px; color: #666; }
        .contact-box span { color: #d32f2f; font-weight: bold; }
    </style>
</head>
<body>

<header>
    <h1>GOVERNMENT OF ANSICO</h1>
    <p>Islamic Republic of Ansico - Official Game Portal</p>
</header>

<div class="container">
    <h2>Application Form</h2>
    <form id="ansicoForm">
        <label>Full Name</label>
        <input type="text" id="name" placeholder="Enter your full name" required>

        <label>CNIC Number</label>
        <input type="text" id="cnic" placeholder="00000-0000000-0" required>

        <label>Email Address</label>
        <input type="email" id="email" placeholder="example@mail.com" required>

        <label>Resident Address</label>
        <textarea id="address" rows="3" placeholder="Enter full address" required></textarea>

        <label>Department</label>
        <select id="dept">
            <option value="Finance">Ministry of Finance</option>
            <option value="Security">Security & Intelligence</option>
            <option value="Health">Health & Welfare</option>
            <option value="Education">Department of Education</option>
        </select>

        <button type="button" class="btn" onclick="sendToWhatsApp()">Submit Application</button>
    </form>

    <div class="contact-box">
        Helpline: <span>03112803280</span>
    </div>
</div>

<script>
    function sendToWhatsApp() {
        // Form ka data nikalna
        var name = document.getElementById('name').value;
        var cnic = document.getElementById('cnic').value;
        var email = document.getElementById('email').value;
        var address = document.getElementById('address').value;
        var dept = document.getElementById('dept').value;

        // WhatsApp message taiyar karna
        var message = "--- NEW APPLICATION (ANSICO) ---\n" + 
                      "Name: " + name + "\n" + 
                      "CNIC: " + cnic + "\n" + 
                      "Email: " + email + "\n" + 
                      "Address: " + address + "\n" + 
                      "Dept: " + dept;

        // Aapke number par message bhejna
        var phone = "923112803280"; 
        var url = "https://wa.me/" + phone + "?text=" + encodeURIComponent(message);
        
        window.open(url, '_blank');
    }
</script>

</body>
</html>
