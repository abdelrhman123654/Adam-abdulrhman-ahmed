<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>هاي انا آدم عبدالرحمن</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Tajawal', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #e0f7fa 0%, #b3e5fc 100%);
            color: #01579b;
            min-height: 100vh;
            overflow-x: hidden;
            padding: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        
        .container {
            max-width: 1000px;
            width: 100%;
            background: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
            overflow: hidden;
            position: relative;
        }
        
        .header {
            background: linear-gradient(135deg, #4fc3f7 0%, #0288d1 100%);
            padding: 25px;
            text-align: center;
            color: white;
            position: relative;
        }
        
        .baby-character {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 5px solid white;
            margin: 0 auto 15px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        .baby-character img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2);
        }
        
        .stats {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-top: 15px;
        }
        
        .score-display, .timer-display {
            font-size: 1.5rem;
            background: rgba(255, 255, 255, 0.2);
            display: inline-block;
            padding: 8px 20px;
            border-radius: 50px;
        }
        
        .timer-display.warning {
            background: rgba(255, 193, 7, 0.3);
            color: #ffc107;
        }
        
        .timer-display.danger {
            background: rgba(244, 67, 54, 0.3);
            color: #f44336;
            animation: pulse 1s infinite;
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        
        .game-content {
            padding: 30px;
        }
        
        .question-section {
            background: #f8fdff;
            border-radius: 15px;
            padding: 25px;
            margin-bottom: 25px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            border: 2px solid #e1f5fe;
        }
        
        .question-text {
            font-size: 1.6rem;
            margin-bottom: 20px;
            color: #0277bd;
            text-align: center;
            line-height: 1.5;
        }
        
        .options-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
            margin-top: 20px;
        }
        
        .option-btn {
            background: linear-gradient(135deg, #e3f2fd 0%, #bbdefb 100%);
            border: none;
            border-radius: 15px;
            padding: 18px;
            font-size: 1.2rem;
            color: #01579b;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 5px 10px rgba(0, 0, 0, 0.08);
            text-align: center;
        }
        
        .option-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 15px rgba(0, 0, 0, 0.1);
            background: linear-gradient(135deg, #bbdefb 0%, #90caf9 100%);
        }
        
        .option-btn.correct {
            background: linear-gradient(135deg, #c8e6c9 0%, #a5d6a7 100%);
            color: #2e7d32;
        }
        
        .option-btn.incorrect {
            background: linear-gradient(135deg, #ffcdd2 0%, #ef9a9a 100%);
            color: #c62828;
        }
        
        .feedback-section {
            text-align: center;
            margin: 20px 0;
            min-height: 80px;
        }
        
        .feedback-text {
            font-size: 1.4rem;
            padding: 15px;
            border-radius: 15px;
            display: inline-block;
            margin-bottom: 15px;
        }
        
        .next-btn, .restart-btn, .start-btn, .submit-btn {
            background: linear-gradient(135deg, #4fc3f7 0%, #0288d1 100%);
            color: white;
            border: none;
            padding: 15px 40px;
            border-radius: 50px;
            font-size: 1.3rem;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            margin: 10px auto;
            display: block;
        }
        
        .next-btn:hover, .restart-btn:hover, .start-btn:hover, .submit-btn:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
        }
        
        .restart-btn {
            background: linear-gradient(135deg, #ff9800 0%, #f57c00 100%);
        }
        
        .start-btn {
            font-size: 1.8rem;
            padding: 20px 60px;
            margin: 40px auto;
        }
        
        .rewards-section {
            background: #e1f5fe;
            border-radius: 15px;
            padding: 20px;
            margin-top: 30px;
            text-align: center;
        }
        
        .rewards-title {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: #0288d1;
        }
        
        .rewards-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
        }
        
        .reward-item {
            text-align: center;
            opacity: 0.3;
            transition: opacity 0.5s ease;
            flex: 0 0 calc(25% - 15px);
            cursor: pointer;
        }
        
        .reward-item.unlocked {
            opacity: 1;
        }
        
        .reward-image {
            width: 100px;
            height: 100px;
            border-radius: 15px;
            overflow: hidden;
            margin: 0 auto 8px;
            box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
        }
        
        .reward-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .reward-video {
            width: 100px;
            height: 100px;
            border-radius: 15px;
            overflow: hidden;
            margin: 0 auto 8px;
            box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
            background: #000;
            position: relative;
        }
        
        .reward-video i {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: white;
            font-size: 2rem;
        }
        
        .reward-label {
            font-size: 0.9rem;
            color: #01579b;
        }
        
        .music-control {
            position: absolute;
            top: 20px;
            left: 20px;
            background: rgba(255, 255, 255, 0.2);
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            color: white;
            cursor: pointer;
            box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
            z-index: 10;
        }
        
        .time-up-message {
            text-align: center;
            padding: 30px;
            display: none;
        }
        
        .time-up-message h2 {
            font-size: 2.5rem;
            color: #f44336;
            margin-bottom: 20px;
        }
        
        .time-up-message p {
            font-size: 1.5rem;
            margin-bottom: 30px;
            color: #555;
        }
        
        .start-screen {
            text-align: center;
            padding: 50px 30px;
        }
        
        .start-screen h2 {
            font-size: 2.2rem;
            color: #0288d1;
            margin-bottom: 20px;
        }
        
        .start-screen p {
            font-size: 1.3rem;
            margin-bottom: 30px;
            color: #555;
            line-height: 1.6;
        }
        
        /* شاشة الدفع */
        .payment-screen {
            text-align: center;
            padding: 30px;
            display: none;
        }
        
        .payment-screen h2 {
            font-size: 2rem;
            color: #0288d1;
            margin-bottom: 20px;
        }
        
        .payment-screen p {
            font-size: 1.2rem;
            margin-bottom: 15px;
            color: #555;
        }
        
        .payment-details {
            background: #e1f5fe;
            border-radius: 15px;
            padding: 20px;
            margin: 20px 0;
            text-align: right;
        }
        
        .payment-details h3 {
            color: #0288d1;
            margin-bottom: 15px;
        }
        
        .payment-info {
            text-align: right;
            margin-bottom: 15px;
        }
        
        .payment-info p {
            margin: 8px 0;
            font-size: 1.1rem;
        }
        
        .form-group {
            margin-bottom: 20px;
            text-align: right;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-size: 1.1rem;
            color: #01579b;
        }
        
        .form-group input, .form-group textarea {
            width: 100%;
            padding: 12px;
            border: 2px solid #b3e5fc;
            border-radius: 10px;
            font-size: 1rem;
        }
        
        .file-upload {
            background: #f1f8fe;
            border: 2px dashed #4fc3f7;
            border-radius: 10px;
            padding: 20px;
            text-align: center;
            cursor: pointer;
            margin-bottom: 20px;
        }
        
        .file-upload i {
            font-size: 2rem;
            color: #4fc3f7;
            margin-bottom: 10px;
        }
        
        .file-upload p {
            color: #0288d1;
        }
        
        .file-name {
            margin-top: 10px;
            font-size: 0.9rem;
            color: #555;
        }
        
        /* شاشة كود التفعيل */
        .activation-screen {
            text-align: center;
            padding: 50px 30px;
            display: none;
        }
        
        .activation-screen h2 {
            font-size: 2rem;
            color: #0288d1;
            margin-bottom: 20px;
        }
        
        .activation-screen p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            color: #555;
        }
        
        .activation-form {
            max-width: 400px;
            margin: 0 auto;
        }
        
        /* تصميم متجاوب */
        @media (max-width: 768px) {
            .options-container {
                grid-template-columns: 1fr;
            }
            
            h1 {
                font-size: 2rem;
            }
            
            .question-text {
                font-size: 1.3rem;
            }
            
            .option-btn {
                padding: 15px;
                font-size: 1.1rem;
            }
            
            .baby-character {
                width: 120px;
                height: 120px;
            }
            
            .stats {
                flex-direction: column;
                gap: 15px;
            }
            
            .reward-item {
                flex: 0 0 calc(50% - 15px);
            }
            
            .payment-info p {
                font-size: 1rem;
            }
        }
        
        /* تأثيرات الحركة */
        @keyframes float {
            0%, 100% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-10px);
            }
        }
        
        .floating {
            animation: float 4s ease-in-out infinite;
        }
        
        .celebrate {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 100;
            display: flex;
            justify-content: center;
            align-items: center;
            opacity: 0;
            transition: opacity 0.5s ease;
        }
        
        .confetti {
            position: absolute;
            width: 15px;
            height: 15px;
            background: #f44336;
            opacity: 0.7;
        }

        /* نافذة الجائزة المنبثقة */
        .reward-popup {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            z-index: 1000;
            justify-content: center;
            align-items: center;
        }
        
        .reward-popup-content {
            background: white;
            padding: 20px;
            border-radius: 15px;
            max-width: 90%;
            max-height: 90%;
            text-align: center;
        }
        
        .reward-popup-close {
            position: absolute;
            top: 10px;
            right: 10px;
            background: #f44336;
            color: white;
            border: none;
            width: 30px;
            height: 30px;
            border-radius: 50%;
            cursor: pointer;
        }
        
        .reward-popup-image {
            max-width: 100%;
            max-height: 70vh;
            border-radius: 10px;
        }
        
        .reward-popup-video {
            max-width: 100%;
            max-height: 70vh;
            border-radius: 10px;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="music-control">
            <i class="fas fa-volume-up"></i>
        </div>
        
        <div class="header">
            <div class="baby-character floating">
                <img src="https://c.top4top.io/p_3530429a81.png" alt="آدم عبدالرحمن">
            </div>
            <h1>لعبة آدم عبدالرحمن</h1>
            <div class="stats">
                <div class="score-display">النقاط: <span id="score">0</span></div>
                <div class="timer-display" id="timer">الوقت: 01:10</div>
            </div>
        </div>
        
        <div class="start-screen" id="start-screen">
            <h2>مرحباً بك في لعبة آدم عبدالرحمن!</h2>
            <p>هذه اللعبة تحتوي على 20 سؤالاً حول رعاية الأطفال الرضع. لديك 70 ثانية للإجابة على أكبر عدد ممكن من الأسئلة. كل إجابة صحيحة تعطيك 35 نقطة. يمكنك كسب جوائز عند الوصول إلى نقاط معينة!</p>
            <p>لبدء اللعبة، حولي 10 جنيه عشان عايز بامبرز </p>
            <button class="start-btn" id="start-btn">ابدأ اللعبة</button>
        </div>
        
        <div class="payment-screen" id="payment-screen">
            <h2>عايز تلعب</h2>
            <p>لتفعيل اللعبة، هات 10 جنيه عشان اجيب بامبرز </p>
            
            <div class="payment-details">
                <h3>بيانات التحويل</h3>
                <div class="payment-info">
                    <p><strong>رقم الهاتف:</strong> 01009234166</p>
                    <p><strong>المبلغ:</strong> 10 جنيه</p>
                </div>
            </div>
            
            <form id="payment-form">
                <div class="form-group">
                    <label for="sender-name">الاسم بالكامل</label>
                    <input type="text" id="sender-name" required>
                </div>
                
                <div class="form-group">
                    <label for="sender-number">رقم الهاتف المحول منه</label>
                    <input type="text" id="sender-number" required>
                </div>
                
                <div class="form-group">
                    <label>صورة إثبات التحويل (اختياري)</label>
                    <div class="file-upload" id="upload-area">
                        <i class="fas fa-cloud-upload-alt"></i>
                        <p>انقر لرفع صورة التحويل</p>
                        <div class="file-name" id="file-name"></div>
                    </div>
                    <input type="file" id="payment-proof" accept="image/*" style="display: none;">
                </div>
                
                <button type="submit" class="submit-btn">تأكيد التحويل</button>
            </form>
        </div>
        
        <div class="activation-screen" id="activation-screen">
            <h2>أدخل كود التفعيل</h2>
            <p>بابا هيبعتلك كود التفعيل على الواتساب ، ممكن تدخله في الخانة دي</p>
            
            <div class="activation-form">
                <div class="form-group">
                    <label for="activation-code">كود التفعيل</label>
                    <input type="text" id="activation-code" placeholder="أدخل الكود المكون من 6 أحرف/أرقام" required>
                </div>
                
                <button class="submit-btn" id="activate-btn">تفعيل اللعبة</button>
            </div>
        </div>
        
        <div class="game-content" id="game-content" style="display: none;">
            <div class="question-section">
                <div class="question-text" id="question-text">
                    <!-- سيتم تعبئة السؤال هنا بواسطة JavaScript -->
                </div>
                
                <div class="options-container" id="options-container">
                    <!-- سيتم تعبئة الخيارات هنا بواسطة JavaScript -->
                </div>
            </div>
            
            <div class="feedback-section">
                <div class="feedback-text" id="feedback-text"></div>
            </div>
            
            <div class="rewards-section">
                <div class="rewards-title">الجوائز المُكتسبة</div>
                <div class="rewards-container" id="rewards-container">
                    <!-- سيتم تعبئة الجوائز هنا بواسطة JavaScript -->
                </div>
            </div>
        </div>
        
        <div class="time-up-message" id="time-up-message">
            <h2>انتهى الوقت!</h2>
            <p>لقد جمعت <span id="final-score">0</span> نقطة</p>
            <div class="rewards-section">
                <div class="rewards-title">الجوائز التي حصلت عليها</div>
                <div class="rewards-container" id="final-rewards-container">
                    <!-- سيتم تعبئة الجوائز هنا بواسطة JavaScript -->
                </div>
            </div>
            <button class="restart-btn" id="restart-btn">إعادة البدء</button>
        </div>
    </div>
    
    <div class="celebrate" id="celebrate">
        <!-- سيتم إنشاء الكونفيتي هنا بواسطة JavaScript -->
    </div>

    <!-- نافذة الجائزة المنبثقة -->
    <div class="reward-popup" id="reward-popup">
        <div class="reward-popup-content">
            <button class="reward-popup-close" id="reward-popup-close">
                <i class="fas fa-times"></i>
            </button>
            <div id="reward-popup-body"></div>
        </div>
    </div>
    
    <audio id="bg-music" loop>
        <source src="https://cdn.pixabay.com/download/audio/2022/06/04/audio_11d4323329.mp3?filename=the-last-piano-112677.mp3" type="audio/mpeg">
    </audio>
    
    <audio id="correct-sound">
        <source src="https://cdn.pixabay.com/download/audio/2025/04/23/audio_5a1eca1fdf.mp3?filename=sonido-correcto-331225.mp3" type="audio/mpeg">
    </audio>
    
    <audio id="wrong-sound">
        <source src="https://cdn.pixabay.com/download/audio/2022/03/10/audio_8b0fae46ef.mp3?filename=wrong-47985.mp3" type="audio/mpeg">
    </audio>
    
    <audio id="reward-sound">
        <source src="https://cdn.pixabay.com/download/audio/2025/06/10/audio_53c4a3417d.mp3?filename=11l-victory_sound_with_t-1749487045383-357608.mp3" type="audio/mpeg">
    </audio>
    
    <audio id="time-up-sound">
        <source src="https://cdn.pixabay.com/download/audio/2025/06/24/audio_fb68e85054.mp3?filename=clock-ticking-365218.mp3" type="audio/mpeg">
    </audio>

    <script>
        // بيانات الأسئلة (20 سؤالاً)
        const questions = [
            {
                question: "متى يجب تغيير حفاض آدم؟",
                options: [
                    "بعد كل رضاعة",
                    "عندما يكون متسخًا أو مبللاً",
                    "مرة واحدة يوميًا",
                    "عندما يبكي"
                ],
                correctIndex: 1
            },
            {
                question: "كم عدد ساعات نوم آدم البالغ من العمر شهرًا؟",
                options: [
                    "8-10 ساعات يوميًا",
                    "12-16 ساعة يوميًا",
                    "6-8 ساعات يوميًا",
                    "20 ساعة يوميًا"
                ],
                correctIndex: 1
            },
            {
                question: "ما هو أفضل وضع لنوم آدم؟",
                options: [
                    "على بطنه",
                    "على ظهره",
                    "على جانبه",
                    "في حضن والدته"
                ],
                correctIndex: 1
            },
            {
                question: "كم مرة يجب أن يستحم آدم؟",
                options: [
                    "يوميًا",
                    "مرتين في الأسبوع",
                    "مرة واحدة في الشهر",
                    "عندما يتسخ فقط"
                ],
                correctIndex: 1
            },
            {
                question: "ما هي درجة حرارة الماء المناسبة لاستحمام آدم؟",
                options: [
                    "باردة مثل ماء الصنبور",
                    "دافئة (حوالي 37 درجة مئوية)",
                    "حارة جدًا",
                    "باردة جدًا"
                ],
                correctIndex: 1
            },
            {
                question: "كيف يمكن تهدئة آدم عندما يبكي؟",
                options: [
                    "تركه يبكي حتى يتوقف",
                    "هزه بقوة",
                    "احتضانه والتحدث إليه بصوت هادئ",
                    "إعطاءه طعامًا صلبًا"
                ],
                correctIndex: 2
            },
            {
                question: "ما هي كمية الحليب التي يحتاجها آدم في كل رضعة؟",
                options: [
                    "120-150 مل",
                    "50-70 مل",
                    "200-250 مل",
                    "300 مل"
                ],
                correctIndex: 1
            },
            {
                question: "ما هي العلامات التي تدل على أن آدم جائع؟",
                options: [
                    "البكاء والتململ",
                    "الضحك واللعب",
                    "النوم العميق",
                    "التحديق في السقف"
                ],
                correctIndex: 0
            },
            {
                question: "كيف يمكن مساعدة آدم على التجشؤ بعد الرضاعة؟",
                options: [
                    "وضعه على ظهره فورًا",
                    "هزه بقوة",
                    "التربيت على ظهره بلطف",
                    "إعطاءه الماء"
                ],
                correctIndex: 2
            },
            {
                question: "ما هي الأنشطة المناسبة لآدم البالغ شهرًا؟",
                options: [
                    "مشاهدة التلفزيون",
                    "اللعب بالألعاب الإلكترونية",
                    "التحدث إليه والغناء له",
                    "الركض في الحديقة"
                ],
                correctIndex: 2
            },
            {
                question: "ما هو الوزن الطبيعي لآدم في عمر الشهر؟",
                options: [
                    "2-3 كجم",
                    "3.5-4.5 كجم",
                    "5-6 كجم",
                    "7-8 كجم"
                ],
                correctIndex: 1
            },
            {
                question: "كم مرة يجب إرضاع آدم في اليوم؟",
                options: [
                    "3-4 مرات",
                    "6-8 مرات",
                    "10-12 مرة",
                    "مرة واحدة فقط"
                ],
                correctIndex: 2
            },
            {
                question: "ما هي أفضل طريقة لحمل آدم؟",
                options: [
                    "من ذراعه",
                    "دعم رأسه ورقبته",
                    "من ساقيه",
                    "من بطنه"
                ],
                correctIndex: 1
            },
            {
                question: "متى يبدأ آدم في الابتسام؟",
                options: [
                    "من أول يوم",
                    "بعد أسبوع",
                    "بعد شهرين",
                    "بعد 6 أشهر"
                ],
                correctIndex: 2
            },
            {
                question: "ما هي درجة حرارة الغرفة المناسبة لآدم؟",
                options: [
                    "15-18 درجة مئوية",
                    "18-20 درجة مئوية",
                    "22-24 درجة مئوية",
                    "30 درجة مئوية"
                ],
                correctIndex: 2
            },
            {
                question: "كيف يمكن معرفة إذا كان آدم مريضًا؟",
                options: [
                    "إذا كان يلعب",
                    "إذا كان ينام كثيرًا",
                    "إذا كان يعاني من الحمى أو refuses to eat",
                    "إذا كان يبتسم"
                ],
                correctIndex: 2
            },
            {
                question: "ما هو اللقاح الأول الذي يجب أن يحصل عليه آدم؟",
                options: [
                    "شهرين",
                    "6 أشهر",
                    "سنة واحدة",
                    "لا يحتاج إلى تطعيمات"
                ],
                correctIndex: 0
            },
            {
                question: "كم عدد الحفاضات التي يحتاجها آدم يوميًا؟",
                options: [
                    "2-3 حفاضات",
                    "6-8 حفاضات",
                    "10-12 حفاضة",
                    "حفاضة واحدة"
                ],
                correctIndex: 1
            },
            {
                question: "ما هو أفضل وقت للخروج مع آدم؟",
                options: [
                    "في منتصف النهار تحت الشمس",
                    "في الصباح الباكر أو وقت العصر",
                    "في الليل",
                    "لا يجب الخروج به أبدًا"
                ],
                correctIndex: 1
            },
            {
                question: "كيف يمكن تنمية رابطة مع آدم؟",
                options: [
                    "تركه وحيدًا",
                    "التحدث إليه واللمس بلطف",
                    "إعطاءه هدايا",
                    "السفر معه"
                ],
                correctIndex: 1
            }
        ];

        // بيانات الجوائز
        const rewards = [
            { points: 100, type: 'image', source: 'https://e.top4top.io/p_3530l2jli3.png', label: 'صورة 1' },
            { points: 150, type: 'image', source: 'https://d.top4top.io/p_3530kmfpv2.png', label: 'صورة 2' },
            { points: 200, type: 'image', source: 'https://f.top4top.io/p_3530tx22d4.png', label: 'صورة 3' },
            { points: 250, type: 'image', source: 'https://g.top4top.io/p_3530m53u65.png', label: 'صورة 4' },
            { points: 300, type: 'image', source: 'https://h.top4top.io/p_3530dscch6.png', label: 'صورة 5' },
            { points: 350, type: 'image', source: 'https://i.top4top.io/p_3530disjg7.png', label: 'صورة 6' },
            { points: 400, type: 'image', source: 'https://j.top4top.io/p_3530zkx9h8.png', label: 'صورة 7' },
            { points: 450, type: 'image', source: 'https://k.top4top.io/p_3530j0hkb9.png', label: 'صورة 8' },
            { points: 500, type: 'image', source: 'https://l.top4top.io/p_35302x8oq10.png', label: 'صورة 9' },
            { points: 550, type: 'video', source: 'https://j.top4top.io/m_3527h41tj7.mp4', label: 'فيديو 1' },
            { points: 600, type: 'video', source: 'https://k.top4top.io/m_352762eb68.mp4', label: 'فيديو 2' },
            { points: 650, type: 'video', source: 'https://a.top4top.io/m_3527dx88710.mp4', label: 'فيديو 3' },
            { points: 700, type: 'video', source: 'https://f.top4top.io/m_3527kwosw1.mp4', label: 'فيديو 4' }
        ];

        // إنشاء 50 كود تفعيل عشوائي
        const activationCodes = Array.from({ length: 50 }, () => generateRandomCode(6));
        
        // عناصر DOM
        const questionText = document.getElementById('question-text');
        const optionsContainer = document.getElementById('options-container');
        const feedbackText = document.getElementById('feedback-text');
        const scoreDisplay = document.getElementById('score');
        const timerDisplay = document.getElementById('timer');
        const rewardsContainer = document.getElementById('rewards-container');
        const finalRewardsContainer = document.getElementById('final-rewards-container');
        const celebrateDiv = document.getElementById('celebrate');
        const musicControl = document.querySelector('.music-control');
        const gameContent = document.getElementById('game-content');
        const timeUpMessage = document.getElementById('time-up-message');
        const finalScoreDisplay = document.getElementById('final-score');
        const restartBtn = document.getElementById('restart-btn');
        const startScreen = document.getElementById('start-screen');
        const startBtn = document.getElementById('start-btn');
        const paymentScreen = document.getElementById('payment-screen');
        const activationScreen = document.getElementById('activation-screen');
        const paymentForm = document.getElementById('payment-form');
        const uploadArea = document.getElementById('upload-area');
        const paymentProof = document.getElementById('payment-proof');
        const fileName = document.getElementById('file-name');
        const activationCodeInput = document.getElementById('activation-code');
        const activateBtn = document.getElementById('activate-btn');
        const rewardPopup = document.getElementById('reward-popup');
        const rewardPopupClose = document.getElementById('reward-popup-close');
        const rewardPopupBody = document.getElementById('reward-popup-body');
        
        const bgMusic = document.getElementById('bg-music');
        const correctSound = document.getElementById('correct-sound');
        const wrongSound = document.getElementById('wrong-sound');
        const rewardSound = document.getElementById('reward-sound');
        const timeUpSound = document.getElementById('time-up-sound');

        // متغيرات اللعبة
        let currentQuestionIndex = 0;
        let score = 0;
        let answered = false;
        let unlockedRewards = [];
        let timeLeft = 70; // 70 ثانية
        let timerInterval;
        let gameStarted = false;
        let shuffledQuestions = [];
        let nextQuestionTimeout;

        // دالة لإنشاء كود عشوائي
        function generateRandomCode(length) {
            const characters = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789';
            let result = '';
            for (let i = 0; i < length; i++) {
                result += characters.charAt(Math.floor(Math.random() * characters.length));
            }
            return result;
        }

        // تهيئة اللعبة
        function initGame() {
            currentQuestionIndex = 0;
            score = 0;
            unlockedRewards = [];
            timeLeft = 70;
            
            // خلط الأسئلة بشكل عشوائي
            shuffledQuestions = [...questions];
            shuffleArray(shuffledQuestions);
            
            loadQuestion();
            createRewardsDisplay();
            updateScore(0);
            updateTimerDisplay();
            
            // إخفاء شاشات البدء والتفعيل وإظهار محتوى اللعبة
            startScreen.style.display = 'none';
            paymentScreen.style.display = 'none';
            activationScreen.style.display = 'none';
            gameContent.style.display = 'block';
            timeUpMessage.style.display = 'none';
            
            // بدء المؤقت
            startTimer();
            
            // تشغيل الموسيقى الخلفية
            bgMusic.volume = 0.3;
            correctSound.volume = 0.5;
            wrongSound.volume = 0.5;
            rewardSound.volume = 0.7;
            timeUpSound.volume = 0.7;
            
            gameStarted = true;
        }

        // دالة لخلط المصفوفة (لجعل الأسئلة عشوائية)
        function shuffleArray(array) {
            for (let i = array.length - 1; i > 0; i--) {
                const j = Math.floor(Math.random() * (i + 1));
                [array[i], array[j]] = [array[j], array[i]];
            }
            return array;
        }

        // بدء المؤقت
        function startTimer() {
            clearInterval(timerInterval);
            timeLeft = 70;
            updateTimerDisplay();
            timerInterval = setInterval(() => {
                timeLeft--;
                updateTimerDisplay();
                
                if (timeLeft <= 0) {
                    clearInterval(timerInterval);
                    timeUp();
                }
            }, 1000);
        }
        
        // تحديث عرض المؤقت
        function updateTimerDisplay() {
            const minutes = Math.floor(timeLeft / 60);
            const seconds = timeLeft % 60;
            timerDisplay.textContent = `الوقت: ${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;
            
            // تغيير اللون عند اقتراب الوقت من النفاد
            if (timeLeft <= 20) {
                timerDisplay.classList.add('warning');
            } else {
                timerDisplay.classList.remove('warning');
            }
            
            if (timeLeft <= 10) {
                timerDisplay.classList.add('danger');
            } else {
                timerDisplay.classList.remove('danger');
            }
        }
        
        // انتهاء الوقت
        function timeUp() {
            timeUpSound.play();
            gameContent.style.display = 'none';
            timeUpMessage.style.display = 'block';
            finalScoreDisplay.textContent = score;
            
            // عرض الجوائز المكتسبة
            showFinalRewards();
            
            // إضافة مستمعي الأحداث للجوائز النهائية
            addRewardsEventListeners(finalRewardsContainer);
            
            // إيقاف الموسيقى الخلفية
            bgMusic.pause();
        }

        // تحميل السؤال الحالي
        function loadQuestion() {
            answered = false;
            const question = shuffledQuestions[currentQuestionIndex];
            questionText.textContent = question.question;
            
            optionsContainer.innerHTML = '';
            question.options.forEach((option, index) => {
                const button = document.createElement('button');
                button.className = 'option-btn';
                button.textContent = option;
                button.addEventListener('click', () => checkAnswer(index));
                optionsContainer.appendChild(button);
            });
            
            feedbackText.textContent = '';
        }

        // التحقق من الإجابة
        function checkAnswer(selectedIndex) {
            if (answered || timeLeft <= 0) return;
            answered = true;
            
            const question = shuffledQuestions[currentQuestionIndex];
            const options = optionsContainer.querySelectorAll('.option-btn');
            
            options.forEach((button, index) => {
                if (index === question.correctIndex) {
                    button.classList.add('correct');
                } else if (index === selectedIndex) {
                    button.classList.add('incorrect');
                }
            });
            
            if (selectedIndex === question.correctIndex) {
                feedbackText.textContent = 'إجابة صحيحة! أحسنت!';
                feedbackText.style.color = '#2e7d32';
                feedbackText.style.background = '#e8f5e9';
                updateScore(score + 35); // 35 نقطة لكل إجابة صحيحة
                correctSound.play();
            } else {
                feedbackText.textContent = 'إجابة خاطئة. حاول مرة أخرى!';
                feedbackText.style.color = '#c62828';
                feedbackText.style.background = '#ffebee';
                wrongSound.play();
            }
            
            // الانتقال التلقائي للسؤال التالي بعد 2 ثانية (بدون زر)
            clearTimeout(nextQuestionTimeout);
            nextQuestionTimeout = setTimeout(() => {
                currentQuestionIndex = (currentQuestionIndex + 1) % shuffledQuestions.length;
                loadQuestion();
            }, 2000);
        }

        // تحديث النقاط
        function updateScore(newScore) {
            score = newScore;
            scoreDisplay.textContent = score;
            
            // التحقق من الجوائز المكتسبة
            checkRewards();
        }

        // التحقق من الجوائز
        function checkRewards() {
            rewards.forEach(reward => {
                if (score >= reward.points && !unlockedRewards.includes(reward.points)) {
                    unlockedRewards.push(reward.points);
                    unlockReward(reward);
                }
            });
        }

        // فتح الجائزة
        function unlockReward(reward) {
            const rewardElement = document.querySelector(`.reward-item[data-points="${reward.points}"]`);
            if (rewardElement) {
                rewardElement.classList.add('unlocked');
                rewardElement.addEventListener('click', () => showReward(reward));
                
                // عرض رسالة تهنئة
                feedbackText.textContent = `مبارك! لقد فزت بجائزة ${reward.label}!`;
                feedbackText.style.color = '#ff9800';
                feedbackText.style.background = '#fff3e0';
                
                // تأثير الاحتفال
                celebrate();
                rewardSound.play();
            }
        }

        // عرض الجائزة
        function showReward(reward) {
            rewardPopup.style.display = 'flex';
            
            if (reward.type === 'image') {
                rewardPopupBody.innerHTML = `
                    <h3>${reward.label}</h3>
                    <img src="${reward.source}" alt="${reward.label}" class="reward-popup-image">
                `;
            } else if (reward.type === 'video') {
                rewardPopupBody.innerHTML = `
                    <h3>${reward.label}</h3>
                    <video controls autoplay class="reward-popup-video">
                        <source src="${reward.source}" type="video/mp4">
                        متصفحك لا يدعم تشغيل الفيديو
                    </video>
                `;
            }
        }

        // إضافة مستمعي الأحداث للجوائز
        function addRewardsEventListeners(container) {
            const rewardItems = container.querySelectorAll('.reward-item.unlocked');
            rewardItems.forEach(item => {
                const points = parseInt(item.getAttribute('data-points'));
                const reward = rewards.find(r => r.points === points);
                if (reward) {
                    item.addEventListener('click', () => showReward(reward));
                }
            });
        }

        // إنشاء عرض الجوائز
        function createRewardsDisplay() {
            rewardsContainer.innerHTML = '';
            rewards.forEach(reward => {
                const rewardItem = document.createElement('div');
                rewardItem.className = 'reward-item';
                rewardItem.setAttribute('data-points', reward.points);
                
                if (reward.type === 'image') {
                    rewardItem.innerHTML = `
                        <div class="reward-image">
                            <img src="${reward.source}" alt="${reward.label}">
                        </div>
                        <div class="reward-label">${reward.points} نقطة</div>
                    `;
                } else {
                    rewardItem.innerHTML = `
                        <div class="reward-video">
                            <i class="fas fa-play"></i>
                        </div>
                        <div class="reward-label">${reward.points} نقطة</div>
                    `;
                }
                
                rewardsContainer.appendChild(rewardItem);
            });
        }

        // عرض الجوائز النهائية
        function showFinalRewards() {
            finalRewardsContainer.innerHTML = '';
            rewards.forEach(reward => {
                const rewardItem = document.createElement('div');
                rewardItem.className = 'reward-item';
                rewardItem.setAttribute('data-points', reward.points);
                
                if (score >= reward.points) {
                    rewardItem.classList.add('unlocked');
                }
                
                if (reward.type === 'image') {             
                    rewardItem.innerHTML = `
                        <div class="reward-image">
                            <img src="${reward.source}" alt="${reward.label}">
                        </div>
                        <div class="reward-label">${reward.points} نقطة</div>
                    `;
                } else {
                    rewardItem.innerHTML = `
                        <div class="reward-video">
                            <i class="fas fa-play"></i>
                        </div>
                        <div class="reward-label">${reward.points} نقطة</div>
                    `;
                }
                
                finalRewardsContainer.appendChild(rewardItem);
            });
        }

        // تأثير الاحتفال
        function celebrate() {
            celebrateDiv.style.opacity = '1';
            
            // إنشاء عناصر الكونفيتي
            for (let i = 0; i < 50; i++) {
                const confetti = document.createElement('div');
                confetti.className = 'confetti';
                confetti.style.left = Math.random() * 100 + 'vw';
                confetti.style.animationDelay = Math.random() * 2 + 's';
                confetti.style.background = `hsl(${Math.random() * 360}, 100%, 50%)`;
                confetti.style.transform = `rotate(${Math.random() * 360}deg)`;
                celebrateDiv.appendChild(confetti);
            }
            
            setTimeout(() => {
                celebrateDiv.style.opacity = '0';
                setTimeout(() => {
                    celebrateDiv.innerHTML = '';
                }, 500);
            }, 3000);
        }

        // التحكم بالموسيقى
        function toggleMusic() {
            if (bgMusic.paused) {
                bgMusic.play();
                musicControl.innerHTML = '<i class="fas fa-volume-up"></i>';
            } else {
                bgMusic.pause();
                musicControl.innerHTML = '<i class="fas fa-volume-mute"></i>';
            }
        }

        // إعادة بدء اللعبة
        restartBtn.addEventListener('click', () => {
            initGame();
        });
        
        // بدء عملية الدفع
        startBtn.addEventListener('click', () => {
            startScreen.style.display = 'none';
            paymentScreen.style.display = 'block';
        });

        // تحكم بالموسيقى
        musicControl.addEventListener('click', toggleMusic);

        // رفع صورة التحويل
        uploadArea.addEventListener('click', () => {
            paymentProof.click();
        });

        paymentProof.addEventListener('change', (e) => {
            if (e.target.files.length > 0) {
                fileName.textContent = e.target.files[0].name;
            }
        });

        // تقديم نموذج الدفع
        paymentForm.addEventListener('submit', (e) => {
            e.preventDefault();
            
            const senderName = document.getElementById('sender-name').value;
            const senderNumber = document.getElementById('sender-number').value;
            
            if (!senderName || !senderNumber) {
                alert('يرجى ملء جميع الحقول المطلوبة');
                return;
            }
            
            // الانتقال إلى شاشة إدخال كود التفعيل
            paymentScreen.style.display = 'none';
            activationScreen.style.display = 'block';
        });
// أكواد التفعيل الصحيحة
const validActivationCodes = new Set([
    "Adam906", "Adam802K", "Adam9L1Q", "Adam4R1M", "Adam2F8Q",
    "Adam1T5V", "Adam6J9W", "Adam3K7S", "Adam8N4D", "Adam5G1C",
    "Adam0H6B", "Adam7Z3X", "Adam2V8N", "Adam4M6L", "Adam9P5K",
    "Adam3Q7J", "Adam6T9H", "Adam8Y4G", "Adam1W5F", "Adam7U3D",
    "Adam2S8A", "Adam4E6Z", "Adam9I5X", "Adam3O7C", "Adam6L9V",
    "Adam8B4N", "Adam1M5Q", "Adam7C3W", "Adam2A8S", "Adam4D6F",
    "Adam9G5R", "Adam3H7T", "Adam6K9Y", "Adam8J4U", "Adam1P5I",
    "Adam7W3O", "Adam2E8L", "Adam4N6B", "Adam9V5M", "Adam3X7Z",
    "Adam6F9C", "Adam8Q4D", "Adam1Z5A", "Adam7R3S", "Adam2T8G",
    "Adam4Y6E", "Adam9U6J", "Adam3I2A", "Adam6O8P", "Adam814L"
]);
// التحقق من كود التفعيل
function checkActivationCode(code) {
    // تحميل الأكواد المستخدمة من localStorage
    const usedCodes = JSON.parse(localStorage.getItem('usedActivationCodes') || '[]');
    
    // التحقق إذا كان الكود صحيحاً ولم يُستخدم من قبل
    if (validActivationCodes.has(code) && !usedCodes.includes(code)) {
        // إضافة الكود إلى قائمة الأكواد المستخدمة
        usedCodes.push(code);
        localStorage.setItem('usedActivationCodes', JSON.stringify(usedCodes));
        return true;
    }
    
    return false;
}
// تفعيل اللعبة بالكود
activateBtn.addEventListener('click', () => {
    const code = activationCodeInput.value.trim();
    
    if (!code) {
        alert('يرجى إدخال كود التفعيل');
        return;
    }
    
    if (checkActivationCode(code)) {
        // الكود صحيح، بدء اللعبة
        initGame();
    } else {
        alert('كود التفعيل غير صحيح أو تم استخدامه من قبل. يرجى المحاولة مرة أخرى');
    }
});
       

        // إغلاق نافذة الجائزة المنبثقة
        rewardPopupClose.addEventListener('click', () => {
            rewardPopup.style.display = 'none';
            // إيقاف الفيديو إذا كان يعمل
            const video = rewardPopupBody.querySelector('video');
            if (video) {
                video.pause();
            }
        });

        // إغلاق النافذة المنبثقة بالنقر خارج المحتوى
        rewardPopup.addEventListener('click', (e) => {
            if (e.target === rewardPopup) {
                rewardPopup.style.display = 'none';
                // إيقاف الفيديو إذا كان يعمل
                const video = rewardPopupBody.querySelector('video');
                if (video) {
                    video.pause();
                }
            }
        });

        // إضافة مستمعي الأحداث للجوائز عند التحميل
        document.addEventListener('DOMContentLoaded', () => {
            createRewardsDisplay();
            addRewardsEventListeners(rewardsContainer);
            
            // عرض أكواد التفعيل في console لأغراض الاختبار
            console.log('أكواد التفعيل المتاحة:', activationCodes);
        });

    </script>
</body>
</html>
