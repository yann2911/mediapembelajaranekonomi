# mediapembelajaranekonomi
<!doctype html>
<html lang="id">
 <head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Media Pembelajaran Ekonomi</title>
  <script src="/_sdk/element_sdk.js"></script>
  <script src="/_sdk/data_sdk.js"></script>
  <style>
        body {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            height: 100%;
            overflow-x: hidden;
        }
        
        html {
            height: 100%;
        }
        
        * {
            box-sizing: border-box;
        }
        
        .container {
            min-height: 100%;
            padding: 0;
        }
        
        .header {
            text-align: center;
            padding: 40px 20px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        
        .header h1 {
            margin: 0 0 10px 0;
            font-size: 42px;
            font-weight: 700;
        }
        
        .header p {
            margin: 0;
            font-size: 18px;
            opacity: 0.9;
        }
        
        .registration-screen {
            max-width: 600px;
            margin: 60px auto;
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.1);
        }
        
        .registration-screen h2 {
            margin: 0 0 30px 0;
            font-size: 32px;
            text-align: center;
        }
        
        .form-group {
            margin-bottom: 25px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-size: 16px;
            font-weight: 600;
        }
        
        .form-group input {
            width: 100%;
            padding: 14px;
            border: 2px solid;
            border-radius: 8px;
            font-size: 16px;
            transition: all 0.3s ease;
        }
        
        .form-group input:focus {
            outline: none;
            box-shadow: 0 0 0 3px rgba(59, 130, 246, 0.1);
        }
        
        .start-btn {
            width: 100%;
            padding: 16px;
            border: none;
            border-radius: 10px;
            font-size: 18px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            margin-top: 10px;
        }
        
        .start-btn:hover:not(:disabled) {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }
        
        .start-btn:disabled {
            opacity: 0.5;
            cursor: not-allowed;
        }
        
        .error-message {
            color: #ef4444;
            font-size: 14px;
            margin-top: 5px;
            display: none;
        }
        
        .error-message.show {
            display: block;
        }
        
        .nav-tabs {
            display: flex;
            justify-content: center;
            gap: 0;
            padding: 0;
            margin: 0;
            border-bottom: 3px solid;
            flex-wrap: wrap;
        }
        
        .nav-tab {
            padding: 18px 35px;
            cursor: pointer;
            font-size: 16px;
            font-weight: 600;
            border: none;
            transition: all 0.3s ease;
            flex: 1;
            min-width: 150px;
            max-width: 250px;
        }
        
        .nav-tab:hover {
            opacity: 0.8;
        }
        
        .nav-tab.active {
            border-bottom: 4px solid;
        }
        
        .content-wrapper {
            max-width: 1000px;
            margin: 0 auto;
            padding: 40px 20px;
        }
        
        .tab-content {
            display: none;
        }
        
        .tab-content.active {
            display: block;
            animation: fadeIn 0.5s ease;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .materi-section {
            margin-bottom: 40px;
            padding: 30px;
            border-radius: 15px;
            border-left: 5px solid;
        }
        
        .materi-section h2 {
            margin: 0 0 20px 0;
            font-size: 28px;
            font-weight: 700;
        }
        
        .materi-section h3 {
            margin: 25px 0 15px 0;
            font-size: 22px;
            font-weight: 600;
        }
        
        .materi-section p {
            margin: 0 0 15px 0;
            font-size: 16px;
            line-height: 1.8;
        }
        
        .materi-section ul {
            margin: 15px 0;
            padding-left: 25px;
        }
        
        .materi-section li {
            margin: 10px 0;
            font-size: 16px;
            line-height: 1.7;
        }
        
        .highlight-box {
            padding: 20px;
            border-radius: 10px;
            margin: 20px 0;
            border-left: 4px solid;
        }
        
        .quiz-container {
            padding: 30px;
            border-radius: 15px;
            margin-bottom: 30px;
        }
        
        .student-info {
            padding: 20px;
            border-radius: 10px;
            margin-bottom: 25px;
            text-align: center;
            font-size: 16px;
            font-weight: 600;
        }
        
        .quiz-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 30px;
            flex-wrap: wrap;
            gap: 15px;
        }
        
        .quiz-progress {
            font-size: 18px;
            font-weight: 600;
        }
        
        .quiz-score {
            font-size: 18px;
            font-weight: 600;
            padding: 10px 20px;
            border-radius: 25px;
        }
        
        .question-card {
            padding: 30px;
            border-radius: 12px;
            margin-bottom: 25px;
            border: 2px solid;
        }
        
        .question-number {
            font-size: 14px;
            font-weight: 600;
            margin-bottom: 15px;
            opacity: 0.8;
        }
        
        .question-text {
            font-size: 19px;
            font-weight: 600;
            margin-bottom: 25px;
            line-height: 1.6;
        }
        
        .options-grid {
            display: grid;
            gap: 12px;
        }
        
        .option-btn {
            padding: 18px 22px;
            border-radius: 10px;
            cursor: pointer;
            font-size: 16px;
            border: 2px solid;
            transition: all 0.3s ease;
            text-align: left;
            font-weight: 500;
        }
        
        .option-btn:hover:not(.correct):not(.wrong):not(:disabled) {
            transform: translateX(8px);
        }
        
        .option-btn.correct {
            border-color: #10b981;
            font-weight: 600;
        }
        
        .option-btn.wrong {
            border-color: #ef4444;
            opacity: 0.6;
        }
        
        .option-btn:disabled {
            cursor: not-allowed;
        }
        
        .feedback {
            margin-top: 20px;
            padding: 18px;
            border-radius: 10px;
            font-size: 16px;
            font-weight: 500;
            display: none;
        }
        
        .feedback.show {
            display: block;
        }
        
        .quiz-navigation {
            display: flex;
            justify-content: space-between;
            margin-top: 30px;
            gap: 15px;
        }
        
        .nav-btn {
            padding: 14px 30px;
            border-radius: 10px;
            cursor: pointer;
            font-size: 16px;
            font-weight: 600;
            border: none;
            transition: all 0.3s ease;
        }
        
        .nav-btn:hover:not(:disabled) {
            transform: scale(1.05);
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }
        
        .nav-btn:disabled {
            opacity: 0.5;
            cursor: not-allowed;
        }
        
        .result-card {
            text-align: center;
            padding: 50px 30px;
            border-radius: 15px;
            margin-top: 30px;
        }
        
        .result-card h2 {
            font-size: 36px;
            margin: 0 0 20px 0;
        }
        
        .result-score {
            font-size: 64px;
            font-weight: 700;
            margin: 20px 0;
        }
        
        .result-message {
            font-size: 20px;
            margin: 20px 0;
        }
        
        .result-details {
            margin: 30px 0;
            padding: 20px;
            border-radius: 10px;
            text-align: left;
        }
        
        .result-details p {
            margin: 10px 0;
            font-size: 16px;
        }
        
        .retry-btn {
            padding: 16px 40px;
            border-radius: 10px;
            cursor: pointer;
            font-size: 18px;
            font-weight: 600;
            border: none;
            margin-top: 30px;
            transition: all 0.3s ease;
        }
        
        .retry-btn:hover {
            transform: scale(1.05);
        }
        
        .loading-spinner {
            display: inline-block;
            width: 20px;
            height: 20px;
            border: 3px solid rgba(255,255,255,.3);
            border-radius: 50%;
            border-top-color: #fff;
            animation: spin 1s ease-in-out infinite;
        }
        
        @keyframes spin {
            to { transform: rotate(360deg); }
        }
        
        .success-message {
            padding: 20px;
            border-radius: 10px;
            margin: 20px 0;
            text-align: center;
            font-weight: 600;
            background-color: #d1fae5;
            color: #065f46;
        }
        
        .footer {
            text-align: center;
            padding: 30px 20px;
            margin-top: 50px;
        }
        
        .footer p {
            margin: 0;
            font-size: 16px;
            font-weight: 500;
        }
        
        @media (max-width: 768px) {
            .header h1 {
                font-size: 32px;
            }
            
            .registration-screen {
                margin: 30px 20px;
                padding: 30px 20px;
            }
            
            .nav-tab {
                padding: 15px 20px;
                font-size: 14px;
                min-width: 120px;
            }
            
            .materi-section {
                padding: 20px;
            }
            
            .materi-section h2 {
                font-size: 24px;
            }
            
            .question-text {
                font-size: 17px;
            }
            
            .result-score {
                font-size: 48px;
            }
        }
    </style>
  <style>@view-transition { navigation: auto; }</style>
  <script src="https://cdn.tailwindcss.com" type="text/javascript"></script>
 </head>
 <body>
  <div class="container">
   <div class="header" id="header">
    <h1 id="mainTitle">Pembelajaran Ekonomi: Permintaan &amp; Penawaran</h1>
    <p id="subtitle">Pahami konsep dasar ekonomi dengan materi lengkap dan kuis interaktif</p>
   </div>
   <div id="registrationScreen" class="registration-screen">
    <h2>📝 Daftar Sebelum Memulai</h2>
    <form id="registrationForm">
     <div class="form-group"><label for="studentName">Nama Lengkap</label> <input type="text" id="studentName" placeholder="Masukkan nama lengkap Anda" required>
      <div class="error-message" id="nameError">
       Nama harus diisi
      </div>
     </div>
     <div class="form-group"><label for="studentAbsen">Nomor Absen</label> <input type="text" id="studentAbsen" placeholder="Contoh: 01, 02, 15" required>
      <div class="error-message" id="absenError">
       Nomor absen harus diisi
      </div>
     </div><button type="submit" class="start-btn" id="startBtn"> 🚀 Mulai Belajar </button>
    </form>
   </div>
   <div id="mainContent" style="display: none;">
    <div class="nav-tabs" id="navTabs"><button class="nav-tab active" data-tab="materi">📚 Materi</button> <button class="nav-tab" data-tab="quiz">🎯 Kuis (20 Soal)</button>
    </div>
    <div class="content-wrapper">
     <div id="materi" class="tab-content active">
      <div class="materi-section" id="materi1">
       <h2>📊 1. Pengertian Permintaan (Demand)</h2>
       <p><strong>Permintaan</strong> adalah jumlah barang atau jasa yang ingin dan mampu dibeli oleh konsumen pada berbagai tingkat harga dalam periode waktu tertentu.</p>
       <h3>Faktor-faktor yang Mempengaruhi Permintaan:</h3>
       <ul>
        <li><strong>Harga Barang Itu Sendiri:</strong> Jika harga naik, permintaan cenderung turun (hukum permintaan)</li>
        <li><strong>Pendapatan Konsumen:</strong> Semakin tinggi pendapatan, semakin besar daya beli</li>
        <li><strong>Harga Barang Substitusi:</strong> Barang pengganti yang dapat menggantikan fungsi barang utama</li>
        <li><strong>Harga Barang Komplementer:</strong> Barang pelengkap yang digunakan bersama-sama</li>
        <li><strong>Selera Konsumen:</strong> Preferensi dan trend yang berkembang di masyarakat</li>
        <li><strong>Jumlah Penduduk:</strong> Semakin banyak penduduk, semakin besar permintaan</li>
        <li><strong>Ekspektasi Masa Depan:</strong> Harapan konsumen tentang harga dan kondisi ekonomi</li>
       </ul>
       <div class="highlight-box" id="highlight1"><strong>💡 Hukum Permintaan:</strong> "Jika harga suatu barang naik, maka jumlah barang yang diminta akan turun, dan sebaliknya (ceteris paribus - faktor lain tetap)"
       </div>
      </div>
      <div class="materi-section" id="materi2">
       <h2>📈 2. Pengertian Penawaran (Supply)</h2>
       <p><strong>Penawaran</strong> adalah jumlah barang atau jasa yang tersedia dan ditawarkan oleh produsen untuk dijual pada berbagai tingkat harga dalam periode waktu tertentu.</p>
       <h3>Faktor-faktor yang Mempengaruhi Penawaran:</h3>
       <ul>
        <li><strong>Harga Barang Itu Sendiri:</strong> Jika harga naik, produsen akan menawarkan lebih banyak</li>
        <li><strong>Biaya Produksi:</strong> Biaya bahan baku, tenaga kerja, dan overhead</li>
        <li><strong>Teknologi:</strong> Teknologi modern dapat meningkatkan efisiensi produksi</li>
        <li><strong>Harga Barang Lain:</strong> Produsen dapat beralih memproduksi barang yang lebih menguntungkan</li>
        <li><strong>Jumlah Produsen:</strong> Semakin banyak produsen, semakin besar penawaran</li>
        <li><strong>Ekspektasi Harga:</strong> Harapan produsen tentang harga di masa depan</li>
        <li><strong>Kebijakan Pemerintah:</strong> Pajak, subsidi, dan regulasi</li>
       </ul>
       <div class="highlight-box" id="highlight2"><strong>💡 Hukum Penawaran:</strong> "Jika harga suatu barang naik, maka jumlah barang yang ditawarkan akan naik, dan sebaliknya (ceteris paribus)"
       </div>
      </div>
      <div class="materi-section" id="materi3">
       <h2>⚖️ 3. Keseimbangan Pasar (Market Equilibrium)</h2>
       <p><strong>Keseimbangan pasar</strong> terjadi ketika jumlah barang yang diminta sama dengan jumlah barang yang ditawarkan pada tingkat harga tertentu.</p>
       <h3>Karakteristik Keseimbangan Pasar:</h3>
       <ul>
        <li><strong>Harga Keseimbangan (Equilibrium Price):</strong> Harga di mana permintaan = penawaran</li>
        <li><strong>Jumlah Keseimbangan (Equilibrium Quantity):</strong> Jumlah barang yang diperjualbelikan pada harga keseimbangan</li>
        <li><strong>Tidak Ada Kelebihan/Kekurangan:</strong> Pasar dalam kondisi stabil</li>
       </ul>
       <h3>Pergeseran Keseimbangan:</h3>
       <p><strong>Kelebihan Penawaran (Surplus):</strong> Terjadi ketika harga di atas harga keseimbangan, jumlah penawaran &gt; permintaan. Solusi: harga akan turun.</p>
       <p><strong>Kelebihan Permintaan (Shortage):</strong> Terjadi ketika harga di bawah harga keseimbangan, jumlah permintaan &gt; penawaran. Solusi: harga akan naik.</p>
       <div class="highlight-box" id="highlight3"><strong>💡 Mekanisme Pasar:</strong> "Pasar memiliki kemampuan untuk menyesuaikan diri (self-adjusting) menuju keseimbangan melalui mekanisme harga"
       </div>
      </div>
      <div class="materi-section" id="materi4">
       <h2>📉 4. Elastisitas Permintaan</h2>
       <p><strong>Elastisitas permintaan</strong> mengukur seberapa sensitif perubahan jumlah permintaan terhadap perubahan harga.</p>
       <h3>Jenis-jenis Elastisitas:</h3>
       <ul>
        <li><strong>Elastis (E &gt; 1):</strong> Permintaan sangat sensitif terhadap perubahan harga (contoh: barang mewah)</li>
        <li><strong>Inelastis (E &lt; 1):</strong> Permintaan kurang sensitif terhadap perubahan harga (contoh: kebutuhan pokok)</li>
        <li><strong>Uniter (E = 1):</strong> Perubahan harga sebanding dengan perubahan permintaan</li>
        <li><strong>Elastis Sempurna (E = ∞):</strong> Perubahan harga sedikit menyebabkan perubahan permintaan sangat besar</li>
        <li><strong>Inelastis Sempurna (E = 0):</strong> Permintaan tidak berubah meskipun harga berubah</li>
       </ul>
       <div class="highlight-box" id="highlight4"><strong>💡 Contoh Praktis:</strong> Harga beras naik 10%, permintaan hanya turun 3% (inelastis). Harga smartphone naik 10%, permintaan turun 15% (elastis).
       </div>
      </div>
     </div>
     <div id="quiz" class="tab-content">
      <div class="student-info" id="studentInfo"></div>
      <div class="quiz-container" id="quizContainer">
       <div class="quiz-header">
        <div class="quiz-progress" id="quizProgress">
         Soal 1 dari 20
        </div>
        <div class="quiz-score" id="quizScore">
         Skor: 0
        </div>
       </div>
       <div id="questionContainer"></div>
       <div class="quiz-navigation"><button class="nav-btn" id="prevBtn" disabled>← Sebelumnya</button> <button class="nav-btn" id="nextBtn">Selanjutnya →</button>
       </div>
      </div>
      <div id="resultContainer" style="display: none;">
       <div class="result-card" id="resultCard">
        <h2>🎉 Kuis Selesai!</h2>
        <div class="result-score" id="finalScore">
         0/20
        </div>
        <div class="result-message" id="resultMessage"></div>
        <div class="result-details" id="resultDetails"></div>
        <div id="saveStatus"></div><button class="retry-btn" id="retryBtn">🔄 Kembali ke Beranda</button>
       </div>
      </div>
     </div>
    </div>
   </div>
   <div class="footer" id="footer">
    <p id="footerText">💡 Terus belajar dan kuasai ilmu ekonomi!</p>
   </div>
  </div>
  <script>
        const quizData = [
            {
                question: "Apa yang dimaksud dengan permintaan dalam ilmu ekonomi?",
                options: [
                    "Jumlah barang yang tersedia di pasar",
                    "Jumlah barang yang ingin dan mampu dibeli konsumen pada berbagai tingkat harga",
                    "Jumlah barang yang diproduksi produsen",
                    "Jumlah barang yang dijual di toko"
                ],
                correct: 1,
                explanation: "Permintaan adalah jumlah barang/jasa yang ingin DAN mampu dibeli konsumen pada berbagai tingkat harga dalam periode tertentu."
            },
            {
                question: "Menurut hukum permintaan, jika harga barang naik maka...",
                options: [
                    "Permintaan akan naik",
                    "Permintaan akan turun",
                    "Permintaan tetap",
                    "Penawaran akan turun"
                ],
                correct: 1,
                explanation: "Hukum permintaan menyatakan bahwa jika harga naik, permintaan akan turun (hubungan berbanding terbalik), ceteris paribus."
            },
            {
                question: "Faktor yang BUKAN mempengaruhi permintaan adalah...",
                options: [
                    "Pendapatan konsumen",
                    "Selera konsumen",
                    "Teknologi produksi",
                    "Harga barang substitusi"
                ],
                correct: 2,
                explanation: "Teknologi produksi mempengaruhi PENAWARAN, bukan permintaan. Permintaan dipengaruhi oleh faktor dari sisi konsumen."
            },
            {
                question: "Barang yang dapat menggantikan fungsi barang lain disebut barang...",
                options: [
                    "Komplementer",
                    "Substitusi",
                    "Inferior",
                    "Normal"
                ],
                correct: 1,
                explanation: "Barang substitusi adalah barang pengganti yang dapat menggantikan fungsi barang lain, contoh: teh dan kopi."
            },
            {
                question: "Jika harga kopi naik, maka permintaan teh akan...",
                options: [
                    "Turun",
                    "Naik",
                    "Tetap",
                    "Tidak dapat diprediksi"
                ],
                correct: 1,
                explanation: "Teh dan kopi adalah barang substitusi. Jika harga kopi naik, konsumen beralih ke teh, sehingga permintaan teh naik."
            },
            {
                question: "Apa yang dimaksud dengan penawaran?",
                options: [
                    "Jumlah barang yang ingin dibeli konsumen",
                    "Jumlah barang yang tersedia dan ditawarkan produsen untuk dijual",
                    "Jumlah uang yang dimiliki konsumen",
                    "Jumlah toko yang menjual barang"
                ],
                correct: 1,
                explanation: "Penawaran adalah jumlah barang/jasa yang tersedia dan ditawarkan produsen untuk dijual pada berbagai tingkat harga."
            },
            {
                question: "Menurut hukum penawaran, jika harga barang naik maka...",
                options: [
                    "Penawaran akan turun",
                    "Penawaran akan naik",
                    "Permintaan akan naik",
                    "Penawaran tetap"
                ],
                correct: 1,
                explanation: "Hukum penawaran menyatakan bahwa jika harga naik, penawaran akan naik (hubungan berbanding lurus), karena produsen ingin untung lebih."
            },
            {
                question: "Faktor yang mempengaruhi penawaran adalah...",
                options: [
                    "Selera konsumen",
                    "Biaya produksi",
                    "Pendapatan konsumen",
                    "Jumlah penduduk"
                ],
                correct: 1,
                explanation: "Biaya produksi mempengaruhi penawaran. Jika biaya produksi naik, produsen akan mengurangi penawaran atau menaikkan harga."
            },
            {
                question: "Teknologi produksi yang lebih baik akan menyebabkan...",
                options: [
                    "Penawaran turun",
                    "Penawaran naik",
                    "Permintaan turun",
                    "Harga naik"
                ],
                correct: 1,
                explanation: "Teknologi yang lebih baik meningkatkan efisiensi produksi, sehingga produsen dapat menawarkan lebih banyak barang dengan biaya lebih rendah."
            },
            {
                question: "Keseimbangan pasar terjadi ketika...",
                options: [
                    "Harga sangat tinggi",
                    "Harga sangat rendah",
                    "Jumlah permintaan sama dengan jumlah penawaran",
                    "Produsen mendapat untung maksimal"
                ],
                correct: 2,
                explanation: "Keseimbangan pasar (equilibrium) terjadi ketika jumlah yang diminta sama dengan jumlah yang ditawarkan pada harga tertentu."
            },
            {
                question: "Jika harga di atas harga keseimbangan, maka akan terjadi...",
                options: [
                    "Kelebihan permintaan (shortage)",
                    "Kelebihan penawaran (surplus)",
                    "Keseimbangan sempurna",
                    "Inflasi"
                ],
                correct: 1,
                explanation: "Jika harga terlalu tinggi, penawaran > permintaan, terjadi surplus. Produsen akan menurunkan harga untuk menjual stok."
            },
            {
                question: "Jika harga di bawah harga keseimbangan, maka akan terjadi...",
                options: [
                    "Kelebihan penawaran (surplus)",
                    "Kelebihan permintaan (shortage)",
                    "Keseimbangan sempurna",
                    "Deflasi"
                ],
                correct: 1,
                explanation: "Jika harga terlalu rendah, permintaan > penawaran, terjadi shortage. Harga akan naik karena banyak yang ingin membeli."
            },
            {
                question: "Ceteris paribus artinya...",
                options: [
                    "Semua faktor berubah",
                    "Faktor lain tetap/tidak berubah",
                    "Harga selalu naik",
                    "Pasar tidak stabil"
                ],
                correct: 1,
                explanation: "Ceteris paribus adalah asumsi 'faktor lain tetap', digunakan untuk menganalisis pengaruh satu variabel tanpa gangguan variabel lain."
            },
            {
                question: "Barang yang permintaannya naik ketika pendapatan naik disebut barang...",
                options: [
                    "Inferior",
                    "Normal",
                    "Substitusi",
                    "Komplementer"
                ],
                correct: 1,
                explanation: "Barang normal adalah barang yang permintaannya naik ketika pendapatan konsumen naik, contoh: daging, smartphone."
            },
            {
                question: "Barang yang permintaannya turun ketika pendapatan naik disebut barang...",
                options: [
                    "Normal",
                    "Inferior",
                    "Mewah",
                    "Substitusi"
                ],
                correct: 1,
                explanation: "Barang inferior adalah barang yang permintaannya turun ketika pendapatan naik, contoh: mie instan, angkutan umum (diganti mobil pribadi)."
            },
            {
                question: "Elastisitas permintaan mengukur...",
                options: [
                    "Jumlah barang yang dijual",
                    "Sensitivitas perubahan permintaan terhadap perubahan harga",
                    "Keuntungan produsen",
                    "Jumlah konsumen"
                ],
                correct: 1,
                explanation: "Elastisitas permintaan mengukur seberapa sensitif/responsif perubahan jumlah permintaan terhadap perubahan harga."
            },
            {
                question: "Permintaan dikatakan elastis jika...",
                options: [
                    "E < 1",
                    "E > 1",
                    "E = 0",
                    "E = 1"
                ],
                correct: 1,
                explanation: "Permintaan elastis (E > 1) berarti permintaan sangat sensitif terhadap perubahan harga, biasanya pada barang mewah/tidak penting."
            },
            {
                question: "Contoh barang dengan permintaan inelastis adalah...",
                options: [
                    "Mobil mewah",
                    "Beras",
                    "Perhiasan",
                    "Liburan ke luar negeri"
                ],
                correct: 1,
                explanation: "Beras adalah kebutuhan pokok dengan permintaan inelastis (E < 1). Meskipun harga naik, orang tetap harus membeli."
            },
            {
                question: "Jika permintaan meningkat tetapi penawaran tetap, maka harga akan...",
                options: [
                    "Turun",
                    "Naik",
                    "Tetap",
                    "Tidak menentu"
                ],
                correct: 1,
                explanation: "Jika permintaan naik tapi penawaran tetap, terjadi kelangkaan relatif, sehingga harga akan naik untuk mencapai keseimbangan baru."
            },
            {
                question: "Subsidi dari pemerintah kepada produsen akan menyebabkan...",
                options: [
                    "Penawaran turun",
                    "Penawaran naik",
                    "Permintaan turun",
                    "Harga naik"
                ],
                correct: 1,
                explanation: "Subsidi mengurangi biaya produksi, sehingga produsen dapat menawarkan lebih banyak barang. Kurva penawaran bergeser ke kanan."
            }
        ];

        const defaultConfig = {
            background_color: "#f8fafc",
            card_color: "#ffffff",
            primary_color: "#3b82f6",
            text_color: "#1e293b",
            accent_color: "#10b981",
            font_family: "Segoe UI",
            font_size: 16,
            main_title: "Pembelajaran Ekonomi: Permintaan & Penawaran",
            subtitle: "Pahami konsep dasar ekonomi dengan materi lengkap dan kuis interaktif",
            footer_text: "💡 Terus belajar dan kuasai ilmu ekonomi!"
        };

        let currentQuestion = 0;
        let score = 0;
        let answers = new Array(quizData.length).fill(null);
        let studentData = { nama: '', no_absen: '' };
        let allResults = [];

        const dataHandler = {
            onDataChanged(data) {
                allResults = data;
                console.log('Data updated:', data.length, 'records');
            }
        };

        async function initApp() {
            if (window.dataSdk) {
                try {
                    const result = await window.dataSdk.init(dataHandler);
                    if (result.isOk) {
                        console.log("✅ Data SDK ready");
                    } else {
                        console.error("❌ Data SDK init failed:", result.error);
                    }
                } catch (error) {
                    console.error("❌ Data SDK error:", error);
                }
            }
        }

        window.addEventListener('load', initApp);

        async function onConfigChange(config) {
            const customFont = config.font_family || defaultConfig.font_family;
            const baseFontStack = 'Segoe UI, Tahoma, Geneva, Verdana, sans-serif';
            const baseSize = config.font_size || defaultConfig.font_size;
            
            const backgroundColor = config.background_color || defaultConfig.background_color;
            const cardColor = config.card_color || defaultConfig.card_color;
            const primaryColor = config.primary_color || defaultConfig.primary_color;
            const textColor = config.text_color || defaultConfig.text_color;
            const accentColor = config.accent_color || defaultConfig.accent_color;
            
            document.body.style.backgroundColor = backgroundColor;
            document.body.style.color = textColor;
            document.body.style.fontFamily = `${customFont}, ${baseFontStack}`;
            
            const header = document.getElementById('header');
            header.style.backgroundColor = primaryColor;
            header.style.color = '#ffffff';
            
            const mainTitle = document.getElementById('mainTitle');
            mainTitle.textContent = config.main_title || defaultConfig.main_title;
            mainTitle.style.fontSize = `${baseSize * 2.625}px`;
            mainTitle.style.fontFamily = `${customFont}, ${baseFontStack}`;
            
            const subtitle = document.getElementById('subtitle');
            subtitle.textContent = config.subtitle || defaultConfig.subtitle;
            subtitle.style.fontSize = `${baseSize * 1.125}px`;
            subtitle.style.fontFamily = `${customFont}, ${baseFontStack}`;
            
            const footerText = document.getElementById('footerText');
            footerText.textContent = config.footer_text || defaultConfig.footer_text;
            footerText.style.fontSize = `${baseSize}px`;
            footerText.style.fontFamily = `${customFont}, ${baseFontStack}`;
            
            const footer = document.getElementById('footer');
            footer.style.backgroundColor = primaryColor;
            footer.style.color = '#ffffff';
        }

        function mapToCapabilities(config) {
            return {
                recolorables: [
                    {
                        get: () => config.background_color || defaultConfig.background_color,
                        set: (value) => {
                            if (window.elementSdk) {
                                window.elementSdk.config.background_color = value;
                                window.elementSdk.setConfig({ background_color: value });
                            }
                        }
                    },
                    {
                        get: () => config.card_color || defaultConfig.card_color,
                        set: (value) => {
                            if (window.elementSdk) {
                                window.elementSdk.config.card_color = value;
                                window.elementSdk.setConfig({ card_color: value });
                            }
                        }
                    },
                    {
                        get: () => config.text_color || defaultConfig.text_color,
                        set: (value) => {
                            if (window.elementSdk) {
                                window.elementSdk.config.text_color = value;
                                window.elementSdk.setConfig({ text_color: value });
                            }
                        }
                    },
                    {
                        get: () => config.primary_color || defaultConfig.primary_color,
                        set: (value) => {
                            if (window.elementSdk) {
                                window.elementSdk.config.primary_color = value;
                                window.elementSdk.setConfig({ primary_color: value });
                            }
                        }
                    },
                    {
                        get: () => config.accent_color || defaultConfig.accent_color,
                        set: (value) => {
                            if (window.elementSdk) {
                                window.elementSdk.config.accent_color = value;
                                window.elementSdk.setConfig({ accent_color: value });
                            }
                        }
                    }
                ],
                borderables: [],
                fontEditable: {
                    get: () => config.font_family || defaultConfig.font_family,
                    set: (value) => {
                        if (window.elementSdk) {
                            window.elementSdk.config.font_family = value;
                            window.elementSdk.setConfig({ font_family: value });
                        }
                    }
                },
                fontSizeable: {
                    get: () => config.font_size || defaultConfig.font_size,
                    set: (value) => {
                        if (window.elementSdk) {
                            window.elementSdk.config.font_size = value;
                            window.elementSdk.setConfig({ font_size: value });
                        }
                    }
                }
            };
        }

        function mapToEditPanelValues(config) {
            return new Map([
                ["main_title", config.main_title || defaultConfig.main_title],
                ["subtitle", config.subtitle || defaultConfig.subtitle],
                ["footer_text", config.footer_text || defaultConfig.footer_text]
            ]);
        }

        if (window.elementSdk) {
            window.elementSdk.init({
                defaultConfig,
                onConfigChange,
                mapToCapabilities,
                mapToEditPanelValues
            });
        }

        document.getElementById('registrationForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const nameInput = document.getElementById('studentName');
            const absenInput = document.getElementById('studentAbsen');
            
            if (nameInput.value.trim() && absenInput.value.trim()) {
                studentData.nama = nameInput.value.trim();
                studentData.no_absen = absenInput.value.trim();
                
                document.getElementById('registrationScreen').style.display = 'none';
                document.getElementById('mainContent').style.display = 'block';
                document.getElementById('studentInfo').textContent = `👤 ${studentData.nama} | No. Absen: ${studentData.no_absen}`;
                
                renderQuestion();
            }
        });

        const tabBtns = document.querySelectorAll('.nav-tab');
        const tabContents = document.querySelectorAll('.tab-content');
        
        tabBtns.forEach(btn => {
            btn.addEventListener('click', function() {
                tabBtns.forEach(t => t.classList.remove('active'));
                this.classList.add('active');
                
                const targetTab = this.dataset.tab;
                tabContents.forEach(content => content.classList.remove('active'));
                document.getElementById(targetTab).classList.add('active');
            });
        });

        function renderQuestion() {
            const question = quizData[currentQuestion];
            const container = document.getElementById('questionContainer');
            
            container.innerHTML = `
                <div class="question-card">
                    <div class="question-number">Pertanyaan ${currentQuestion + 1} dari ${quizData.length}</div>
                    <div class="question-text">${question.question}</div>
                    <div class="options-grid">
                        ${question.options.map((option, index) => `
                            <button class="option-btn" data-index="${index}">${option}</button>
                        `).join('')}
                    </div>
                    <div class="feedback" id="feedback"></div>
                </div>
            `;
            
            const optionBtns = container.querySelectorAll('.option-btn');
            optionBtns.forEach(btn => {
                if (answers[currentQuestion] !== null) {
                    btn.disabled = true;
                    const index = parseInt(btn.dataset.index);
                    if (index === question.correct) {
                        btn.classList.add('correct');
                        btn.style.backgroundColor = '#10b981';
                        btn.style.color = '#ffffff';
                    } else if (index === answers[currentQuestion]) {
                        btn.classList.add('wrong');
                        btn.style.backgroundColor = '#ef4444';
                        btn.style.color = '#ffffff';
                    }
                }
                
                btn.addEventListener('click', function() {
                    if (answers[currentQuestion] === null) {
                        const selectedIndex = parseInt(this.dataset.index);
                        answers[currentQuestion] = selectedIndex;
                        
                        optionBtns.forEach(b => b.disabled = true);
                        
                        if (selectedIndex === question.correct) {
                            score++;
                            this.classList.add('correct');
                            this.style.backgroundColor = '#10b981';
                            this.style.color = '#ffffff';
                            showFeedback(true, question.explanation);
                        } else {
                            this.classList.add('wrong');
                            this.style.backgroundColor = '#ef4444';
                            this.style.color = '#ffffff';
                            optionBtns[question.correct].classList.add('correct');
                            optionBtns[question.correct].style.backgroundColor = '#10b981';
                            optionBtns[question.correct].style.color = '#ffffff';
                            showFeedback(false, question.explanation);
                        }
                        
                        updateScore();
                    }
                });
            });
            
            if (answers[currentQuestion] !== null) {
                showFeedback(answers[currentQuestion] === question.correct, question.explanation);
            }
            
            updateProgress();
            updateNavigationButtons();
        }

        function showFeedback(isCorrect, explanation) {
            const feedback = document.getElementById('feedback');
            if (isCorrect) {
                feedback.innerHTML = `✅ <strong>Benar!</strong> ${explanation}`;
                feedback.style.backgroundColor = '#d1fae5';
                feedback.style.color = '#065f46';
            } else {
                feedback.innerHTML = `❌ <strong>Kurang Tepat.</strong> ${explanation}`;
                feedback.style.backgroundColor = '#fee2e2';
                feedback.style.color = '#991b1b';
            }
            feedback.classList.add('show');
        }

        function updateProgress() {
            document.getElementById('quizProgress').textContent = `Soal ${currentQuestion + 1} dari ${quizData.length}`;
        }

        function updateScore() {
            document.getElementById('quizScore').textContent = `Skor: ${score}`;
        }

        function updateNavigationButtons() {
            const prevBtn = document.getElementById('prevBtn');
            const nextBtn = document.getElementById('nextBtn');
            
            prevBtn.disabled = currentQuestion === 0;
            nextBtn.textContent = currentQuestion === quizData.length - 1 ? 'Lihat Hasil 🎉' : 'Selanjutnya →';
        }

        document.getElementById('prevBtn').addEventListener('click', function() {
            if (currentQuestion > 0) {
                currentQuestion--;
                renderQuestion();
            }
        });

        document.getElementById('nextBtn').addEventListener('click', function() {
            if (currentQuestion < quizData.length - 1) {
                currentQuestion++;
                renderQuestion();
            } else {
                showResults();
            }
        });

        async function showResults() {
            document.getElementById('quizContainer').style.display = 'none';
            document.getElementById('resultContainer').style.display = 'block';
            
            const percentage = (score / quizData.length) * 100;
            let message = '';
            
            if (percentage >= 90) message = '🌟 Luar biasa! Anda menguasai materi dengan sangat baik!';
            else if (percentage >= 75) message = '👏 Bagus sekali! Pemahaman Anda sudah sangat baik!';
            else if (percentage >= 60) message = '👍 Cukup baik! Terus belajar untuk hasil lebih maksimal!';
            else message = '💪 Jangan menyerah! Baca kembali materinya dan coba lagi!';
            
            document.getElementById('finalScore').textContent = `${score}/${quizData.length}`;
            document.getElementById('resultMessage').textContent = message;
            document.getElementById('resultDetails').innerHTML = `
                <p><strong>Nama:</strong> ${studentData.nama}</p>
                <p><strong>No. Absen:</strong> ${studentData.no_absen}</p>
                <p><strong>Skor:</strong> ${score} dari ${quizData.length} (${percentage.toFixed(1)}%)</p>
                <p><strong>Waktu Selesai:</strong> ${new Date().toLocaleString('id-ID')}</p>
            `;
            
            await saveResultToSheet();
        }

        async function saveResultToSheet() {
            const saveStatus = document.getElementById('saveStatus');
            saveStatus.innerHTML = '<div class="loading-spinner"></div> Menyimpan hasil...';
            
            if (!window.dataSdk) {
                saveStatus.innerHTML = '⚠️ Data SDK tidak tersedia';
                saveStatus.style.color = '#ef4444';
                return;
            }
            
            const percentage = (score / quizData.length) * 100;
            
            const resultData = {
                nama: studentData.nama,
                no_absen: studentData.no_absen,
                skor: score,
                total_soal: quizData.length,
                persentase: parseFloat(percentage.toFixed(1)),
                waktu_selesai: new Date().toISOString()
            };
            
            try {
                const result = await window.dataSdk.create(resultData);
                
                if (result.isOk) {
                    saveStatus.innerHTML = '✅ Hasil berhasil disimpan ke Canva Sheet!';
                    saveStatus.className = 'success-message';
                } else {
                    saveStatus.innerHTML = `❌ Gagal menyimpan: ${result.error.message}`;
                    saveStatus.style.color = '#ef4444';
                }
            } catch (error) {
                saveStatus.innerHTML = `❌ Error: ${error.message}`;
                saveStatus.style.color = '#ef4444';
            }
        }

        document.getElementById('retryBtn').addEventListener('click', () => location.reload());
    </script>
 <script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'99d84936103db15c',t:'MTc2Mjk3NDE3MC4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
