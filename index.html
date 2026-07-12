<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Pi Ecosystem App</title>
    
    <!-- Pi Network ရဲ့ တရားဝင် SDK ကို ချိတ်ဆက်ခြင်း -->
    <script src="https://sdk.minepi.com/pi-sdk.js"></script>

    <style>
        /* Pi ရဲ့ Theme အရောင်ဖြစ်တဲ့ ခရမ်းရောင်ကို အခြေခံထားပါတယ် */
        :root {
            --pi-purple: #e2b43c; /* Pi Gold */
            --pi-bg: #57207c;     /* Pi Purple */
        }

        body {
            font-family: 'Segoe UI', Arial, sans-serif;
            background-color: #f5f5f9;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            color: #333;
        }

        .container {
            width: 100%;
            max-width: 480px; /* ဖုန်းမျက်နှာပြင်အရွယ်အစား သတ်မှတ်ခြင်း */
            min-height: 100vh;
            background: white;
            box-shadow: 0 0 10px rgba(0,0,0,0.05);
            display: flex;
            flex-direction: column;
            position: relative;
        }

        .header {
            background-color: var(--pi-bg);
            color: white;
            padding: 20px;
            text-align: center;
            border-bottom-left-radius: 20px;
            border-bottom-right-radius: 20px;
        }

        .header h1 {
            margin: 0;
            font-size: 22px;
        }

        .content {
            padding: 20px;
            flex: 1;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
        }

        /* လော့ဂ်အင် ဝင်ရန် ခလုတ် */
        .btn-login {
            background-color: var(--pi-bg);
            color: white;
            border: 2px solid var(--pi-purple);
            padding: 14px 30px;
            font-size: 16px;
            font-weight: bold;
            border-radius: 30px;
            cursor: pointer;
            width: 80%;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }

        .btn-login:active {
            transform: scale(0.98);
        }

        /* App ရဲ့ ပင်မ Content (လော့ဂ်အင်ဝင်ပြီးမှ ပြမည့်အပိုင်း) */
        #main-app {
            display: none; /* အစပိုင်းမှာ ဖျောက်ထားမယ် */
            width: 100%;
        }

        .user-card {
            background: #f0ebf7;
            padding: 15px;
            border-radius: 12px;
            margin-bottom: 20px;
            border-left: 5px solid var(--pi-bg);
        }
    </style>
</head>
<body>

    <div class="container">
        <!-- Header ပိုင်း -->
        <div class="header">
            <h1>My First Pi App</h1>
        </div>

        <!-- အလယ် Content ပိုင်း -->
        <div class="content">
            
            <!-- ၁။ လော့ဂ်အင် မဝင်ရသေးခင် ပြသမည့် မျက်နှာပြင် -->
            <div id="login-screen">
                <p style="margin-bottom: 30px; color: #666;">သင့်ရဲ့ Pi Account နဲ့ ချိတ်ဆက်ပြီး App ကို စတင်အသုံးပြုပါ</p>
                <button class="btn-login" id="login-button">Pi အကောင့်ဖြင့် ဝင်မည်</button>
            </div>

            <!-- ၂။ လော့ဂ်အင် ဝင်ပြီးမှ ပေါ်လာမည့် ပင်မအက်ပ်မျက်နှာပြင် -->
            <div id="main-app">
                <div class="user-card">
                    <p style="margin: 0; font-size: 14px; color: #555;">လက်ရှိအသုံးပြုသူ</p>
                    <h3 style="margin: 5px 0 0 0; color: var(--pi-bg);" id="username-text">@username</h3>
                </div>
                
                <div style="padding: 40px 20px; border: 2px dashed #ccc; border-radius: 12px;">
                    <h4>သင့် App ရဲ့ လုပ်ဆောင်ချက်များကို ဒီနေရာမှာ ထည့်သွင်းပါ</h4>
                    <p style="font-size: 14px; color: #777;">ဥပမာ - ဂိမ်းဆော့တဲ့နေရာ၊ Pi Coin နဲ့ ပစ္စည်းဝယ်တဲ့ နေရာ စသဖြင့်...</p>
                </div>
            </div>

        </div>
    </div>

    <!-- JavaScript လုံခြုံရေးနှင့် ချိတ်ဆက်မှုပိုင်း -->
    <script>
        // Pi SDK စတင်ပွင့်စေခြင်း (Sandbox Mode)
        Pi.init({ version: "2.0", sandbox: true });

        const loginScreen = document.getElementById('login-screen');
        const mainApp = document.getElementById('main-app');
        const usernameText = document.getElementById('username-text');
        const loginButton = document.getElementById('login-button');

        // ခလုတ်နှိပ်ရင် လုပ်ဆောင်မယ့်အချက်
        loginButton.addEventListener('click', async () => {
            try {
                loginButton.innerText = "ချိတ်ဆက်နေသည်...";
                loginButton.disabled = true;

                // ခွင့်ပြုချက်တောင်းခံခြင်း
                const scopes = ['username', 'payments'];
                
                // တန်းလန်းဖြစ်နေသော Payment များရှိပါက ကိုင်တွယ်ရန် Function
                const onIncompletePaymentFound = (payment) => {
                    console.log("Incomplete payment found:", payment);
                };

                // Pi SDK သို့ လော့ဂ်အင် တောင်းဆိုခြင်း
                const auth = await Pi.authenticate(scopes, onIncompletePaymentFound);
                
                // အောင်မြင်ပါက မျက်နှာပြင်များ ပြောင်းလဲခြင်း
                loginScreen.style.display = 'none';
                mainApp.style.display = 'block';
                usernameText.innerText = `@${auth.user.username}`;

            } catch (error) {
                console.error("Error standard:", error);
                alert("ချိတ်ဆက်မှု မအောင်မြင်ပါ။ Pi Browser ထဲကနေ ဝင်ရောက်နေတာ ဟုတ်မဟုတ် ပြန်စစ်ပေးပါ။");
                loginButton.innerText = "Pi အကောင့်ဖြင့် ဝင်မည်";
                loginButton.disabled = false;
            }
        });
    </script>
</body>
</html>
