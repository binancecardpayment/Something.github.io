<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>INTERPOL Recovery Service</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0a1a32, #0d2b4d);
            color: #ffffff;
            line-height: 1.6;
            padding: 20px;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        
        .email-container {
            max-width: 700px;
            width: 100%;
            background: linear-gradient(135deg, #0d2b4d, #0a1a32);
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            border: 1px solid rgba(30, 144, 255, 0.2);
        }
        
        .header {
            background: linear-gradient(90deg, #1a3a5f, #0d2b4d);
            padding: 30px 40px;
            text-align: center;
            border-bottom: 3px solid #1e90ff;
            position: relative;
            overflow: hidden;
        }
        
        .header::before {
            content: "";
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(30, 144, 255, 0.1) 0%, transparent 70%);
            transform: rotate(30deg);
        }
        
        .header h1 {
            font-size: 32px;
            letter-spacing: 2px;
            text-transform: uppercase;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.5);
            color: #ffffff;
            position: relative;
        }
        
        .content {
            padding: 40px;
        }
        
        .message {
            background: rgba(13, 43, 77, 0.6);
            padding: 30px;
            border-radius: 10px;
            margin-bottom: 30px;
            border-left: 4px solid #1e90ff;
            position: relative;
            overflow: hidden;
        }
        
        .message::after {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, #1e90ff, #0d2b4d);
        }
        
        .message p {
            font-size: 18px;
            margin-bottom: 20px;
            color: #e6f0ff;
        }
        
        .whatsapp-section {
            background: rgba(37, 211, 102, 0.15);
            border: 1px solid rgba(37, 211, 102, 0.3);
            border-radius: 10px;
            padding: 25px;
            text-align: center;
            margin: 25px 0;
            position: relative;
            overflow: hidden;
        }
        
        .whatsapp-section::before {
            content: "";
            position: absolute;
            top: -20px;
            right: -20px;
            width: 80px;
            height: 80px;
            background: rgba(37, 211, 102, 0.1);
            border-radius: 50%;
        }
        
        .whatsapp-section::after {
            content: "";
            position: absolute;
            bottom: -20px;
            left: -20px;
            width: 60px;
            height: 60px;
            background: rgba(37, 211, 102, 0.1);
            border-radius: 50%;
        }
        
        .whatsapp-icon {
            display: inline-block;
            background-color: #25d366;
            width: 70px;
            height: 70px;
            border-radius: 50%;
            margin-bottom: 15px;
            position: relative;
            z-index: 2;
            box-shadow: 0 4px 10px rgba(37, 211, 102, 0.4);
        }
        
        .whatsapp-icon::before {
            content: '';
            position: absolute;
            width: 34px;
            height: 34px;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path fill="white" d="M380.9 97.1C339 55.1 283.2 32 223.9 32c-122.4 0-222 99.6-222 222 0 39.1 10.2 77.3 29.6 111L0 480l117.7-30.9c32.4 17.7 68.9 27 106.1 27h.1c122.3 0 224.1-99.6 224.1-222 0-59.3-25.2-115-67.1-157zm-157 341.6c-33.2 0-65.7-8.9-94-25.7l-6.7-4-69.8 18.3L72 359.2l-4.4-7c-18.5-29.4-28.2-63.3-28.2-98.2 0-101.7 82.8-184.5 184.6-184.5 49.3 0 95.6 19.2 130.4 54.1 34.8 34.9 56.2 81.2 56.1 130.5 0 101.8-84.9 184.6-186.6 184.6zm101.2-138.2c-5.5-2.8-32.8-16.2-37.9-18-5.1-1.9-8.8-2.8-12.5 2.8-3.7 5.6-14.3 18-17.6 21.8-3.2 3.7-6.5 4.2-12 1.4-32.6-16.3-54-29.1-75.5-66-5.7-9.8 5.7-9.1 16.3-30.3 1.8-3.7.9-6.9-.5-9.7-1.4-2.8-12.5-30.1-17.1-41.2-4.5-10.8-9.1-9.3-12.5-9.5-3.2-.2-6.9-.2-10.6-.2-3.7 0-9.7 1.4-14.8 6.9-5.1 5.6-19.4 19-19.4 46.3 0 27.3 19.9 53.7 22.6 57.4 2.8 3.7 39.1 59.7 94.8 83.8 35.2 15.2 49 16.5 66.6 13.9 10.7-1.6 32.8-13.4 37.4-26.4 4.6-13 4.6-24.1 3.2-26.4-1.3-2.5-5-3.9-10.5-6.6z"></path></svg>') no-repeat center;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
        }
        
        .whatsapp-section h3 {
            font-size: 22px;
            margin-bottom: 15px;
            color: #25d366;
            position: relative;
            z-index: 2;
        }
        
        .whatsapp-section p {
            font-size: 18px;
            margin-bottom: 20px;
            position: relative;
            z-index: 2;
        }
        
        .contact-btn {
            display: inline-block;
            background: linear-gradient(to right, #25d366, #128c7e);
            color: white;
            text-decoration: none;
            font-weight: bold;
            padding: 14px 35px;
            border-radius: 50px;
            font-size: 18px;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(37, 211, 102, 0.3);
            margin-top: 10px;
            position: relative;
            z-index: 2;
            border: none;
            cursor: pointer;
        }
        
        .contact-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(37, 211, 102, 0.5);
            background: linear-gradient(to right, #128c7e, #25d366);
        }
        
        .masked-number {
            position: relative;
            display: inline-block;
            margin-top: 15px;
            padding: 8px 20px;
            background: rgba(0, 0, 0, 0.3);
            border-radius: 6px;
            font-size: 16px;
            cursor: pointer;
            transition: all 0.3s;
            z-index: 2;
        }
        
        .masked-number .hidden {
            display: none;
        }
        
        .masked-number:hover {
            background: rgba(0, 0, 0, 0.5);
        }
        
        .masked-number:hover .hidden {
            display: inline;
        }
        
        .masked-number:hover .visible {
            display: none;
        }
        
        .contact-info {
            display: flex;
            justify-content: space-around;
            margin-top: 25px;
            flex-wrap: wrap;
        }
        
        .contact-item {
            margin: 10px 15px;
            text-align: center;
            min-width: 200px;
            padding: 15px;
            background: rgba(13, 43, 77, 0.4);
            border-radius: 8px;
            transition: transform 0.3s;
        }
        
        .contact-item:hover {
            transform: translateY(-5px);
            background: rgba(13, 43, 77, 0.6);
        }
        
        .contact-item span {
            display: block;
            font-weight: bold;
            color: #4dabf7;
            margin-bottom: 8px;
            font-size: 16px;
        }
        
        .contact-item a {
            color: #ffffff;
            text-decoration: none;
            transition: color 0.3s;
            word-break: break-all;
            font-size: 15px;
        }
        
        .contact-item a:hover {
            color: #25d366;
            text-decoration: underline;
        }
        
        .footer {
            background: #0a1a32;
            padding: 25px;
            text-align: center;
            font-size: 14px;
            color: #a0b1c5;
            border-top: 1px solid #1a3a5f;
            position: relative;
        }
        
        .footer::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 1px;
            background: linear-gradient(90deg, transparent, #1e90ff, transparent);
        }
        
        .disclaimer {
            font-size: 12px;
            color: #7f8fa4;
            margin-top: 20px;
            padding-top: 20px;
            border-top: 1px solid #1a3a5f;
            line-height: 1.5;
        }
        
        .interpol-badge {
            display: inline-block;
            background: rgba(30, 144, 255, 0.1);
            padding: 5px 15px;
            border-radius: 30px;
            margin-top: 15px;
            font-size: 12px;
            color: #4dabf7;
            border: 1px solid rgba(30, 144, 255, 0.3);
        }
        
        @media (max-width: 600px) {
            .header {
                padding: 20px;
            }
            
            .header h1 {
                font-size: 24px;
            }
            
            .content {
                padding: 20px;
            }
            
            .contact-info {
                flex-direction: column;
                align-items: center;
            }
            
            .message, .whatsapp-section {
                padding: 20px;
            }
            
            .contact-item {
                width: 100%;
                margin: 10px 0;
            }
        }
    </style>
</head>
<body>
    <div class="email-container">
        <div class="header">
            <h1>INTERPOL RECOVERY SERVICE</h1>
        </div>
        
        <div class="content">
            <div class="message">
                <p>Dear refunder,</p>
                
                <p>To facilitate the timely recovery of your funds, we request that you contact our designated agent who has been dispatched to South Africa to conduct the necessary investigation.</p>
                
                <div class="whatsapp-section">
                    <div class="whatsapp-icon"></div>
                    <h3>CONTACT OUR AGENT VIA WHATSAPP</h3>
                    <p>Please contact her on WhatsApp for inquiries regarding the processing of your form and payment requirements.</p>
                    <p>This step is essential to prevent any delays in recovering your money.</p>
                    
                    <a href="https://wa.me/27643098567" class="contact-btn">Contact via WhatsApp</a>
                    
                    <div class="masked-number">
                        <span class="visible">Click to reveal contact number</span>
                        <span class="hidden">+27 64 309 8567</span>
                    </div>
                </div>
                
                <p>We appreciate your cooperation and assure you that we are committed to resolving your case efficiently.</p>
            </div>
            
            <div class="contact-info">
                <div class="contact-item">
                    <span>INTERPOL Recovery Service</span>
                    Lyon, France
                </div>
                <div class="contact-item">
                    <span>24/7 Support</span>
                    <a href="mailto:interpolrecoveryservice@paymentrefund.info">interpolrecoveryservice@paymentrefund.info</a>
                </div>
                <div class="contact-item">
                    <span>WhatsApp Contact</span>
                    <div class="masked-number">
                        <span class="visible">Click to reveal number</span>
                        <span class="hidden">+27 64 309 8567</span>
                    </div>
                </div>
            </div>
            
            <div class="disclaimer">
                <p>This is an automated message. Please do not reply to this email. For security reasons, all communications regarding your case should be conducted through our official WhatsApp channel with the designated agent.</p>
                <p>INTERPOL Recovery Service operates in strict compliance with international financial regulations. All recovery procedures are subject to verification and authentication protocols.</p>
            </div>
        </div>
        
        <div class="footer">
            <p>INTERPOL Recovery Service &copy; 2023 | Lyon, France | All Rights Reserved</p>
            <p>This email is confidential and intended solely for the recipient.</p>
            <div class="interpol-badge">Official INTERPOL Communication</div>
        </div>
    </div>

    <script>
        // Add functionality to masked number elements
        document.querySelectorAll('.masked-number').forEach(element => {
            element.addEventListener('click', function() {
                this.classList.toggle('revealed');
                
                const visible = this.querySelector('.visible');
                const hidden = this.querySelector('.hidden');
                
                if (visible.style.display === 'none') {
                    visible.style.display = 'inline';
                    hidden.style.display = 'none';
                } else {
                    visible.style.display = 'none';
                    hidden.style.display = 'inline';
                }
            });
        });
    </script>
</body>
</html>