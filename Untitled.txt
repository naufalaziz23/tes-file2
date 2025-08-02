<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Naufal Aziz Budiandra - Portfolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #1a73e8;
            --secondary-color: #4285f4;
            --accent-color: #fbbc05;
            --text-color: #333;
            --light-bg: #f8f9fa;
            --white: #ffffff;
            --gray: #6c757d;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            line-height: 1.6;
            color: var(--text-color);
            background-color: var(--white);
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header Styles */
        header {
            background-color: var(--white);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }
        
        .logo {
            font-size: 24px;
            font-weight: bold;
            color: var(--primary-color);
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 30px;
        }
        
        .nav-links a {
            text-decoration: none;
            color: var(--text-color);
            font-weight: 500;
            transition: color 0.3s ease;
        }
        
        .nav-links a:hover {
            color: var(--primary-color);
        }
        
        /* Hero Section */
        .hero {
            display: flex;
            align-items: center;
            min-height: 100vh;
            padding: 100px 0 50px;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
        }
        
        .hero-content {
            display: flex;
            align-items: center;
            justify-content: space-between;
            width: 100%;
        }
        
        .hero-text {
            flex: 1;
            padding-right: 50px;
        }
        
        .hero-text h1 {
            font-size: 48px;
            margin-bottom: 20px;
            color: var(--primary-color);
        }
        
        .hero-text p {
            font-size: 18px;
            margin-bottom: 30px;
            color: var(--gray);
        }
        
        .btn {
            display: inline-block;
            padding: 12px 30px;
            background-color: var(--primary-color);
            color: var(--white);
            text-decoration: none;
            border-radius: 30px;
            font-weight: 600;
            transition: all 0.3s ease;
            margin-right: 15px;
            margin-bottom: 15px;
        }
        
        .btn:hover {
            background-color: var(--secondary-color);
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        .btn-outline {
            background-color: transparent;
            border: 2px solid var(--primary-color);
            color: var(--primary-color);
        }
        
        .btn-outline:hover {
            background-color: var(--primary-color);
            color: var(--white);
        }
        
        .hero-image {
            flex: 1;
            display: flex;
            justify-content: center;
        }
        
        .profile-img {
            width: 350px;
            height: 350px;
            border-radius: 50%;
            object-fit: cover;
            border: 8px solid var(--white);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            animation: float 6s ease-in-out infinite;
        }
        
        @keyframes float {
            0% {
                transform: translateY(0px);
            }
            50% {
                transform: translateY(-20px);
            }
            100% {
                transform: translateY(0px);
            }
        }
        
        /* Section Styles */
        section {
            padding: 80px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }
        
        .section-title h2 {
            font-size: 36px;
            color: var(--primary-color);
            position: relative;
            display: inline-block;
        }
        
        .section-title h2:after {
            content: '';
            position: absolute;
            width: 60px;
            height: 4px;
            background-color: var(--accent-color);
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
        }
        
        /* About Section */
        .about {
            background-color: var(--light-bg);
        }
        
        .about-content {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }
        
        .about-text {
            flex: 2;
            padding-right: 50px;
        }
        
        .about-text p {
            margin-bottom: 20px;
            font-size: 16px;
            color: var(--gray);
        }
        
        .about-image {
            flex: 1;
            display: flex;
            justify-content: center;
        }
        
        .about-img {
            width: 300px;
            height: 300px;
            border-radius: 10px;
            object-fit: cover;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }
        
        /* Education Section */
        .education-item {
            background-color: var(--white);
            border-radius: 10px;
            padding: 30px;
            margin-bottom: 30px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s ease;
        }
        
        .education-item:hover {
            transform: translateY(-5px);
        }
        
        .education-item h3 {
            font-size: 22px;
            color: var(--primary-color);
            margin-bottom: 10px;
        }
        
        .education-item .institution {
            font-size: 18px;
            font-weight: 600;
            margin-bottom: 5px;
        }
        
        .education-item .date {
            color: var(--gray);
            font-size: 14px;
            margin-bottom: 15px;
        }
        
        /* Skills Section */
        .skills {
            background-color: var(--light-bg);
        }
        
        .skills-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
        }
        
        .skill-item {
            background-color: var(--white);
            border-radius: 10px;
            padding: 20px;
            width: 250px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: all 0.3s ease;
        }
        
        .skill-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        .skill-item i {
            font-size: 40px;
            color: var(--primary-color);
            margin-bottom: 15px;
        }
        
        .skill-item h3 {
            font-size: 18px;
            margin-bottom: 10px;
        }
        
        .skill-item p {
            color: var(--gray);
            font-size: 14px;
        }
        
        /* Experience Section */
        .experience-item {
            background-color: var(--white);
            border-radius: 10px;
            padding: 30px;
            margin-bottom: 30px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            position: relative;
            transition: transform 0.3s ease;
        }
        
        .experience-item:hover {
            transform: translateY(-5px);
        }
        
        .experience-item h3 {
            font-size: 22px;
            color: var(--primary-color);
            margin-bottom: 10px;
        }
        
        .experience-item .company {
            font-size: 18px;
            font-weight: 600;
            margin-bottom: 5px;
        }
        
        .experience-item .date {
            color: var(--gray);
            font-size: 14px;
            margin-bottom: 15px;
        }
        
        .experience-item ul {
            list-style-type: none;
            padding-left: 0;
        }
        
        .experience-item ul li {
            margin-bottom: 10px;
            position: relative;
            padding-left: 20px;
        }
        
        .experience-item ul li:before {
            content: '✓';
            position: absolute;
            left: 0;
            color: var(--accent-color);
            font-weight: bold;
        }
        
        /* Activities Section */
        .activities {
            background-color: var(--light-bg);
        }
        
        .activities-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
        }
        
        .activity-item {
            background-color: var(--white);
            border-radius: 10px;
            padding: 20px;
            width: 300px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: all 0.3s ease;
        }
        
        .activity-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        .activity-item i {
            font-size: 30px;
            color: var(--primary-color);
            margin-bottom: 15px;
        }
        
        .activity-item h3 {
            font-size: 18px;
            margin-bottom: 10px;
        }
        
        .activity-item p {
            color: var(--gray);
            font-size: 14px;
        }
        
        /* Contact Section */
        .contact-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 30px;
        }
        
        .contact-info {
            flex: 1;
            min-width: 300px;
        }
        
        .contact-form {
            flex: 1;
            min-width: 300px;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 20px;
        }
        
        .contact-item i {
            font-size: 24px;
            color: var(--primary-color);
            margin-right: 15px;
            width: 30px;
            text-align: center;
        }
        
        .contact-item p {
            margin: 0;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 16px;
        }
        
        .form-group textarea {
            height: 150px;
            resize: vertical;
        }
        
        /* Footer */
        footer {
            background-color: var(--primary-color);
            color: var(--white);
            padding: 30px 0;
            text-align: center;
        }
        
        .social-links {
            margin-bottom: 20px;
        }
        
        .social-links a {
            display: inline-block;
            width: 40px;
            height: 40px;
            line-height: 40px;
            text-align: center;
            border-radius: 50%;
            background-color: rgba(255, 255, 255, 0.2);
            color: var(--white);
            margin: 0 10px;
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            background-color: var(--white);
            color: var(--primary-color);
            transform: translateY(-3px);
        }
        
        /* Responsive */
        @media (max-width: 992px) {
            .hero-content {
                flex-direction: column;
            }
            
            .hero-text {
                padding-right: 0;
                margin-bottom: 40px;
                text-align: center;
            }
            
            .about-content {
                flex-direction: column;
            }
            
            .about-text {
                padding-right: 0;
                margin-bottom: 40px;
            }
            
            .contact-container {
                flex-direction: column;
            }
        }
        
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero-text h1 {
                font-size: 36px;
            }
            
            .profile-img {
                width: 250px;
                height: 250px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <nav>
                <div class="logo">Naufal A.B.</div>
                <ul class="nav-links">
                    <li><a href="#home">Beranda</a></li>
                    <li><a href="#about">Tentang</a></li>
                    <li><a href="#education">Pendidikan</a></li>
                    <li><a href="#skills">Keahlian</a></li>
                    <li><a href="#experience">Pengalaman</a></li>
                    <li><a href="#activities">Aktivitas</a></li>
                    <li><a href="#contact">Kontak</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container">
            <div class="hero-content">
                <div class="hero-text">
                    <h1>Naufal Aziz Budiandra</h1>
                    <p>Mahasiswa Teknik Industri | UI/UX Designer | Web Developer</p>
                    <p>Halo! Saya Naufal Aziz Budiandra, mahasiswa aktif semester 4 Teknik Industri Universitas Negeri Yogyakarta. Saya memiliki minat tinggi di bidang Keselamatan dan Kesehatan Kerja (K3), UI/UX Design, dan Teknologi Industri.</p>
                    <a href="#contact" class="btn">Hubungi Saya</a>
                    <a href="#experience" class="btn btn-outline">Lihat Portfolio</a>
                </div>
                <div class="hero-image">
                    <img src="https://via.placeholder.com/350" alt="Profile Picture" class="profile-img">
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <div class="section-title">
                <h2>Tentang Saya</h2>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <p>Saya adalah mahasiswa Teknik Industri di Universitas Negeri Yogyakarta yang memiliki minat tinggi di bidang Keselamatan dan Kesehatan Kerja (K3), UI/UX Design, dan Teknologi Industri. Saya aktif dalam berbagai kegiatan organisasi dan proyek kreatif.</p>
                    <p>Saya percaya bahwa kombinasi antara keterampilan teknis, kreatif, dan ketekunan adalah kunci untuk berkembang di dunia industri saat ini. Saya terbuka untuk kolaborasi, freelance, atau proyek pengembangan skill bersama.</p>
                    <p>Selain fokus pada pengembangan profesional, saya juga aktif dalam kegiatan non-akademik seperti lari dan olahraga tim, yang membantu saya menjaga keseimbangan antara kehidupan akademik dan kesehatan fisik.</p>
                </div>
                <div class="about-image">
                    <img src="https://via.placeholder.com/300" alt="About Image" class="about-img">
                </div>
            </div>
        </div>
    </section>

    <!-- Education Section -->
    <section id="education" class="education">
        <div class="container">
            <div class="section-title">
                <h2>Pendidikan</h2>
            </div>
            <div class="education-item">
                <h3>S1 Teknik Industri</h3>
                <div class="institution">Universitas Negeri Yogyakarta</div>
                <div class="date">2022 - Sekarang</div>
                <p>Mahasiswa aktif semester 4 dengan fokus pada bidang Keselamatan dan Kesehatan Kerja (K3), UI/UX Design, dan Teknologi Industri.</p>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="skills">
        <div class="container">
            <div class="section-title">
                <h2>Keahlian</h2>
            </div>
            <div class="skills-container">
                <div class="skill-item">
                    <i class="fas fa-paint-brush"></i>
                    <h3>UI/UX Design</h3>
                    <p>Figma, Canva</p>
                </div>
                <div class="skill-item">
                    <i class="fas fa-cube"></i>
                    <h3>CAM Dasar</h3>
                    <p>Fusion 360</p>
                </div>
                <div class="skill-item">
                    <i class="fas fa-video"></i>
                    <h3>Editing Konten</h3>
                    <p>Lightroom, CapCut, VN</p>
                </div>
                <div class="skill-item">
                    <i class="fas fa-hard-hat"></i>
                    <h3>K3 Dasar</h3>
                    <p>Industrial Engineering Tools</p>
                </div>
                <div class="skill-item">
                    <i class="fas fa-laptop-code"></i>
                    <h3>Web Design</h3>
                    <p>WordPress, HTML dasar</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Experience Section -->
    <section id="experience" class="experience">
        <div class="container">
            <div class="section-title">
                <h2>Pengalaman Kerja & Proyek</h2>
            </div>
            <div class="experience-item">
                <h3>Staf Desain</h3>
                <div class="company">PT Simpul Desain Grafis</div>
                <div class="date">Jan 2025 – Mei 2025</div>
                <ul>
                    <li>Membuat berbagai materi promosi visual dan konten media sosial</li>
                    <li>Bekerja dengan Canva dan Adobe Lightroom untuk menjaga identitas visual klien</li>
                    <li>Terlibat dalam pengembangan ide kreatif dan presentasi desain ke klien</li>
                </ul>
            </div>
            <div class="experience-item">
                <h3>Landing Page Developer</h3>
                <div class="company">PT Jawara Multi Usaha</div>
                <div class="date">April 2025 – Juni 2025</div>
                <ul>
                    <li>Merancang dan membangun landing page untuk promosi layanan perusahaan</li>
                    <li>Menggunakan WordPress dan Elementor untuk desain yang responsif</li>
                    <li>Mengoptimasi struktur konten agar mudah diakses dan ramah pengguna</li>
                </ul>
            </div>
            <div class="experience-item">
                <h3>UI/UX Design</h3>
                <div class="company">Aplikasi Tiket Pintar</div>
                <div class="date">Proyek Akademik</div>
                <ul>
                    <li>Membuat tampilan user-friendly untuk sistem pemesanan tiket</li>
                    <li>Tools: Figma, Canva</li>
                    <li>Fokus pada kemudahan pengguna, visual minimalis, dan warna yang nyaman</li>
                </ul>
            </div>
            <div class="experience-item">
                <h3>CAM Fusion 360</h3>
                <div class="company">Project Komponen Mekanik</div>
                <div class="date">Proyek Akademik</div>
                <ul>
                    <li>Mendesain dan menyetting CAM dasar 2D & 3D</li>
                    <li>Membuat simulasi pemotongan dan perencanaan manufacturing</li>
                    <li>Cocok untuk pemula yang ingin memahami dasar CAM</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Activities Section -->
    <section id="activities" class="activities">
        <div class="container">
            <div class="section-title">
                <h2>Aktivitas Non-Akademik</h2>
            </div>
            <div class="activities-container">
                <div class="activity-item">
                    <i class="fas fa-running"></i>
                    <h3>Olahraga</h3>
                    <p>Lari 5K & Trail Run (PB: 22:25)<br>Race Pack Kompa Trail Run UNY</p>
                </div>
                <div class="activity-item">
                    <i class="fas fa-futbol"></i>
                    <h3>Ekstrakurikuler</h3>
                    <p>Futsal dan Basket semasa SMP</p>
                </div>
                <div class="activity-item">
                    <i class="fas fa-mosque"></i>
                    <h3>Organisasi</h3>
                    <p>Organisasi Rohis SMA 8 Pekanbaru</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="container">
            <div class="section-title">
                <h2>Kontak</h2>
            </div>
            <div class="contact-container">
                <div class="contact-info">
                    <div class="contact-item">
                        <i class="fas fa-envelope"></i>
                        <p>naufal@email.com</p>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-phone"></i>
                        <p>08xxxxxxxxxx</p>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-map-marker-alt"></i>
                        <p>Pekanbaru / Yogyakarta</p>
                    </div>
                    <div class="contact-item">
                        <i class="fab fa-linkedin"></i>
                        <p>LinkedIn</p>
                    </div>
                    <div class="contact-item">
                        <i class="fab fa-behance"></i>
                        <p>Behance/Dribbble</p>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-globe"></i>
                        <p>Website Portofolio</p>
                    </div>
                </div>
                <div class="contact-form">
                    <form id="contactForm">
                        <div class="form-group">
                            <input type="text" placeholder="Nama Lengkap" required>
                        </div>
                        <div class="form-group">
                            <input type="email" placeholder="Email" required>
                        </div>
                        <div class="form-group">
                            <input type="text" placeholder="Subjek">
                        </div>
                        <div class="form-group">
                            <textarea placeholder="Pesan" required></textarea>
                        </div>
                        <button type="submit" class="btn">Kirim Pesan</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="social-links">
                <a href="#"><i class="fab fa-linkedin"></i></a>
                <a href="#"><i class="fab fa-behance"></i></a>
                <a href="#"><i class="fab fa-github"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
            </div>
            <p>&copy; 2023 Naufal Aziz Budiandra. All Rights Reserved.</p>
        </div>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Form submission
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Get form values
            const name = this.querySelector('input[type="text"]').value;
            const email = this.querySelector('input[type="email"]').value;
            const subject = this.querySelector('input[type="text"]:nth-of-type(2)').value;
            const message = this.querySelector('textarea').value;
            
            // Here you would normally send the form data to a server
            // For this example, we'll just show a success message
            alert(`Terima kasih ${name}! Pesan Anda telah terkirim. Saya akan menghubungi Anda segera.`);
            
            // Reset form
            this.reset();
        });

        // Add animation on scroll
        const observerOptions = {
            root: null,
            rootMargin: '0px',
            threshold: 0.1
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('animate');
                }
            });
        }, observerOptions);

        // Observe all sections
        document.querySelectorAll('section').forEach(section => {
            observer.observe(section);
        });
    </script>
</body>
</html>