<template>
  <section class="home">
    
    <header class="header">
      <img alt="Logo" class="logo" src="/img/logo.svg" />
    </header>

    <div class="hero-content">

    <div class="photo-frame">
      
    </div>

      <div class="text-block">
        <h1>WELCOME!</h1>
        <h2>I am Software Engineer</h2>
        <p>I'm an undergraduated Software Engineering Technology at IPB University with many experiences in web development and UI/UX design.</p>
        <div class="social-icons">
          <img src="/img/ig.svg" class="contact-icon" />
          <img src="/img/fb.svg" class="contact-icon" />
          <img src="/img/x.svg" class="contact-icon" />
          <img src="/img/li.svg" class="contact-icon" />
          <img src="/img/wa.svg" class="contact-icon" />
        </div>
      </div>

    </div>
  </section>

    <section>
      <div class="wave"></div>
    </section>

    <img src="@/assets/pop.png" class="pop" />
    <img src="@/assets/pop.png" class="popp" />

    <section id="about" class="about py-5">
    <div class="container">

      <h2 class="text-center fw-bold mb-2" style="color: #2b1911;">ABOUT ME</h2>
      <p style="color: #2b1911;">Hi! Get to know me better.</p>
        <div class="about-container">

          <div class="about-left">
              <img src="@/assets/4.png" class="about-photo" />
            </div>

            <div class="about-right">
                          <div class="about-row">
              <div class="card small-card">
                <h5>Who Am I</h5>
                <p>Halo, saya <strong>Luna Falya</strong>, mahasiswa di IPB University jurusan Teknologi Rekayasa Perangkat Lunak, fokus pada web front-end.</p>
              </div>

              <div class="card small-card">
                <h5>My Interest</h5>
                <p>Memiliki pengalaman manajemen logistik, serta mendalami UI/UX design dan front-end programming.</p>
              </div>
            </div>

            <div class="card big-card">
                <h5>Personal Info</h5>

                <div class="info-grid">
                  <div>
                    <p>
                      <img src="@/assets/dob (1).png" alt="Name Icon" class="contact-icon me-3">
                      <strong>Name :</strong> Luna Falya Iskandar
                    </p>
                    <p>
                      <img src="@/assets/dob (1).png" alt="Name Icon" class="contact-icon me-3">
                      <strong>Phone :</strong> +62 878 9850 5218
                    </p>
                    <p>
                      <img src="@/assets/dob (1).png" alt="Location Icon" class="contact-icon me-3">
                      <strong>Address :</strong> Bogor, Indonesia
                    </p>
                  </div>
                  <div>
                    <p>
                      <img src="@/assets/dob (1).png" alt="DOB Icon" class="contact-icon me-3">
                      <strong>DOB :</strong> Born in 2005
                    </p>
                    <p>
                      <img src="@/assets/dob (1).png" alt="Email Icon" class="contact-icon me-3">
                      <strong>Email :</strong> lunfaliswork@gmail.com
                    </p>
                    <p>
                      <img src="@/assets/dob (1).png" alt="Education Icon" class="contact-icon me-3">
                      <strong>Education :</strong> IPB University - Software Engineer
                    </p>
                  </div>
                </div>

                <a href="/certificate/CV.pdf" class="resume-btn">⬇ Download My Resume</a>
              </div>
            </div>

          </div>

          
        </div>
    </section>


    
      <section id="portfolio" class="py-5">
        <div class="container">

          <h2 class="text-center fw-bold mb-2" style="color: #2b1911;">Portofolio Showcase</h2>
          <p class="text-center mb-4" style="color: #2b1911;">Explore my journey through projects, certificates, and skills.</p>

          <!-- Tab Buttons -->
          <ul class="tabs">
            <li>
              <button 
                class="tab-btn" 
                :class="{ active: activeTab === 'projects' }" 
                @click="activeTab = 'projects'"
              >Projects</button>
            </li>

            <li>
              <button 
                class="tab-btn" 
                :class="{ active: activeTab === 'certificates' }" 
                @click="activeTab = 'certificates'"
              >Certificates</button>
            </li>

            <li>
              <button 
                class="tab-btn" 
                :class="{ active: activeTab === 'skills' }" 
                @click="activeTab = 'skills'"
              >Skills</button>
            </li>
          </ul>

          <!-- Tab Content -->
          <div class="tab-content">

            <!-- PROJECTS -->
            <div v-show="activeTab === 'projects'" class="portfolio-grid">

              <!-- === Portfolio Item 1 === -->

                <div class="portfolio-card p-3 text-center box">
                  <div class="media-wrapper">
                    <video class="portfolio-media"
                          controls
                          style="cursor: pointer;"
                          @click="openVideoModal(video1)">
                      <source :src="video1">
                    </video>
                  </div>
                  <h5 class="fw-semibold mt-3 captionport">Teka Teki Taki</h5>
                  <p class="captionport">Game Teka Teki dengan bobot nilai!</p>
                </div>


              <!-- === Portfolio Item 2 === -->

                <div class="portfolio-card p-3 text-center box">
                  <div class="media-wrapper">
                    <video class="portfolio-media"
                          controls
                          @click="openVideoModal(video2)">
                      <source :src="video2">
                    </video>
                  </div>
                  <h5 class="fw-semibold mt-3 captionport">Mush Room (Final Team Project)</h5>
                  <p class="captionport">Website Penjualan Jamur</p>
                  <a href="https://mushroom.miauwlan.com/" target="_blank" style="color: inherit;">Klik disini</a>
                </div>


              <!-- === Portfolio Item 3 === -->

                <div class="portfolio-card p-3 text-center box">
                  <div class="media-wrapper">
                    <video class="portfolio-media"
                          controls
                          @click="openVideoModal(video3)">
                      <source :src="video3">
                    </video>
                  </div>
                  <h5 class="fw-semibold mt-3 captionport">Deluxe Hotel</h5>
                  <p class="captionport">Aplikasi Reservasi Hotel</p>
                </div>


              <!-- === Portfolio Item 4 === -->

                <div class="portfolio-card p-3 text-center box">
                  <div class="media-wrapper">
                    <video class="portfolio-media"
                          controls
                          @click="openVideoModal(video2)">
                      <source :src="video2">
                    </video>
                  </div>
                  <h5 class="fw-semibold mt-3 captionport">SpaceXplorer</h5>
                  <p class="captionport">Gameboard Berbasis AR!</p>
                  <a href="https://drive.google.com/drive/folders/1a0npsiBXnJnNQqvjLSuUtFRKkIOV6Au-?usp=sharing"
                    target="_blank" style="color: inherit;">Klik disini</a>
                </div>


              <!-- === Portfolio Item 5 === -->

                <div class="portfolio-card p-3 text-center box">
                  <div class="media-wrapper">
                    <video class="portfolio-media"
                          controls
                          @click="openVideoModal(video2)">
                      <source :src="video2">
                    </video>
                  </div>
                  <h5 class="fw-semibold mt-3 captionport">Rahayu Konveksi</h5>
                  <p class="captionport">Website Manajemen Keuangan Digital</p>
                  <a href="https://mushroom.miauwlan.com/" target="_blank" style="color: inherit;">Klik disini</a>
                </div>


              <!-- === Portfolio Item 6 === -->

                <div class="portfolio-card p-3 text-center box">
                  <div class="media-wrapper">
                    <video class="portfolio-media"
                          controls
                          @click="openVideoModal(video2)">
                      <source :src="video2">
                    </video>
                  </div>
                  <h5 class="fw-semibold mt-3 captionport">Funelish AR</h5>
                  <p class="captionport">Aplikasi Belajar Bahasa Inggris</p>
                </div>
              </div>


            <!-- CERTIFICATES -->
            <div v-show="activeTab === 'certificates'" class="portfolio-grid">

              <div v-for="cert in certificates" :key="cert.title">
                <div class="card text-center p-3 shadow-sm">
                  <img :src="cert.img"
                      class="img-fluid certif-thumbnail"
                      style="cursor: pointer;"
                      @click="openImageModal(cert.img)">
                  <h5 class="mt-2">{{ cert.title }}</h5>
                </div>
              </div>

            </div>

            <!-- SKILLS -->
            <<div v-show="activeTab === 'skills'" class="portfolio-grid">

              <div v-for="skill in skills" :key="skill.name">
                <div class="card text-center p-3 shadow-sm">
                  <img :src="skill.icon" style="width: 50px;" class="mx-auto">
                  <h5 class="mt-2">{{ skill.name }}</h5>
                  <div class="progress mt-2" style="height: 8px;">
                    <div class="progress-bar bg-success" :style="{ width: skill.level + '%' }"></div>
                  </div>
                </div>
              </div>

              <!-- Other skills -->
              <div class="text-center mt-4">
                <h4 class="fw-bold mb-3" style="color: #36005B;">Other Skills</h4>

                <div class="d-flex justify-content-center flex-wrap gap-30">
                  <img v-for="icon in otherSkills" :src="icon" :key="icon" style="width: 50px;">
                </div>
              </div>

            </div>

          </div>
        </div>

        <!-- Modal Video -->
        <div v-if="showVideo" class="modal-backdrop-custom" @click="closeVideo">
          <video :src="currentVideo" controls autoplay class="modal-video"></video>
        </div>

        <!-- Modal Image -->
        <div v-if="showImage" class="modal-backdrop-custom" @click="closeImage">
          <img :src="currentImage" class="modal-image">
        </div>
      </section>

<section id="contact" class="mt-5 space">
  <div class="container">
    <h2 class="text-center fw-bold mb-4" style="color: #2b1911;">Contact Me</h2>

    <p class="lead" style="color: #2b1911;">
      Saya selalu terbuka untuk diskusi, kolaborasi, atau peluang baru.
      Jangan ragu untuk menghubungi saya melalui kontak di bawah ini:
    </p>

    <div class="row">
      <!-- Contact Details -->
      <div class="col-md-6">
        <div class="contact-details">

          <div class="d-flex align-items-center mb-3">
            <img src="@/assets/img/10.png" class="contact-icon me-3" />
            <p class="mb-0">
              Email :
              <a href="mailto:lunfaliswork@gmail.com" target="_blank">
                lunfaliswork@gmail.com
              </a>
            </p>
          </div>

          <div class="d-flex align-items-center mb-3">
            <img src="@/assets/img/11.png" class="contact-icon me-3" />
            <p class="mb-0">
              Phone :
              <a href="https://wa.me/6287898505218" target="_blank">
                +62 878 9850 5218
              </a>
            </p>
          </div>

          <div class="d-flex align-items-center mb-3">
            <img src="@/assets/img/13.png" class="contact-icon me-3" />
            <p class="mb-0">
              Address :
              <a href="https://maps.app.goo.gl/vKGhVkY4x3NH7hop7" target="_blank">
                Tegal Gundil, Bogor Utara, Jawa Barat
              </a>
            </p>
          </div>

          <p class="lead mt-3">
            Atau, Anda dapat mengirimkan pesan langsung melalui formulir kontak ini.
            Saya akan segera merespons!
          </p>
        </div>
      </div>

      <!-- Contact Form -->
      <div class="col-md-6">
        <div class="contact-form p-3 rounded">
          <form @submit.prevent="submitContact">
            <div class="mb-3">
              <label class="form-label">Name</label>
              <input v-model="form.name" type="text" class="form-control" placeholder="Your Name" required>
            </div>

            <div class="mb-3">
              <label class="form-label">E-mail</label>
              <input v-model="form.email" type="email" class="form-control" placeholder="Your Email" required>
            </div>

            <div class="mb-3">
              <label class="form-label">Message</label>
              <textarea v-model="form.message" class="form-control" rows="4" placeholder="Message" required></textarea>
            </div>

            <button type="submit" class="btn active custom-tab">Send Message</button>
          </form>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- Footer -->
<footer class="footer text-center py-3">
  <div class="container">
    <p>&copy; 2024 Luna Falya Iskandar. All Rights Reserved.</p>
    <p>Follow me on:</p>

    <div class="social-icons">
      <a href="https://www.linkedin.com/in/lunfalis/" target="_blank">
        <img src="@/assets/img/8.png" class="social-icon" />
      </a>

      <a href="https://twitter.com" target="_blank">
        <img src="@/assets/img/7.png" class="social-icon" />
      </a>

      <a href="https://www.instagram.com/lunfalis" target="_blank">
        <img src="@/assets/img/6.png" class="social-icon" />
      </a>

      <a href="https://wa.me/6287898505218" target="_blank">
        <img src="@/assets/img/9.png" class="social-icon" />
      </a>
    </div>
  </div>
</footer>

      
      
</template>

<script setup>
</script>

<style scoped>
.home {
  width: 100%;
  height: 100vh;
  background: #2b1911;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  padding: 0px 0px;
  box-sizing: border-box;
}

.hero-content {
  display: flex;
  flex-direction: row;
  width: 80%;
  max-width: 1400px;
  justify-content: flex-start;
  align-items: center;
  gap: 40px;
}

.wave {
  width: 100%;
  height: 35vh;
  display: flex;
  background-image: url("/img/wave.svg");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: bottom;
  margin-top: auto;
}

.text-block {
  position: relative;
  margin-left: 50px;
  margin-top: 170px; /* NAIKIN TEKS */
  object-fit: cover;
  width: 400px;
  height: auto;

}

.pop {
  position: relative;
  left: 1000px;
  top: calc(25vh - 280px); 
  width: 160px;
  z-index: 5;

}

.popp {
  position: relative;
  right: 120px;
  top: calc(25vh - 280px); 
  width: 160px;
  z-index: 5;

}

.header {
  display: flex;
  align-items: center;
  width: 85%;
  max-width: 1400px;
  margin-bottom: 30px;
  gap: 10px;
}

.logo {
  width: 100px;
}

.brand {
  color: #fff;
  font-size: 22px;
  font-weight: 500;
}

.photo-frame img.photo {
  width: 700px;
  height: auto;
  border-radius: 20px;
  object-fit: cover;
  left: 100px;
}

.text-block h1 {
  font-size: 60px;
  color: #d5eaf1;
  font-weight: bold;
  z-index: 10;
}

.overlay {
  position: absolute;
  top: 10px;
  left: 0;
  font-size: 60px;
  line-height: 1.15;
  color: rgba(255, 255, 255, 0.06);
  pointer-events: none;
}


/* ABOUT */

.about {
  width: 100%;
  min-height: 100vh;
  display: flex;  /* dorong container ke kanan */
  padding: 10px 10px;         /* bisa 0 kalau mau tanpa jarak */
  box-sizing: border-box;
}

.about-container {
  width: 85%;
  max-width: 1400px;
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  gap: 40px;
}

.about-left {
  width: 40%;
  display: flex;
  justify-content: flex-end;
}

#about h2 {
  font-size: 36px;
  font-weight: 800;
  color: #2b1911 !important;
  justify-content: center;    /* ⬅ tab di tengah */
  align-items: center; 
}

.card {
  background: #ffffffb5;
  padding: 20px;
  border-radius: 16px;
  box-shadow: 0 4px 10px rgba(0,0,0,0.1);
}

.card h5 {
  color: #2b1911;
  margin-bottom: 10px;
  font-weight: 900;
}

.card p {
  color: #2b1911;
  margin-bottom: 10px;
  font-weight: 300;
}

.info-grid {
  display: flex;
  justify-content: space-between;
  gap: 70px;
}

.resume-btn {
  display: inline-block;
  margin-top: 15px;
  padding: 10px 18px;
  background: #2b1911;
  color: white;
  text-decoration: none;
  border-radius: 10px;
}

.about-right {
  width: 60%;
  display: flex;
  flex-direction: column;
  gap: 30px;

}

.about-photo {
  width: 550px;
  height: auto;
  align-items: flex-end;   /* ⬅ Konten pindah ke kiri */
}

.about-row {
  display: flex;
  gap: 20px;
}

.small-card {
  flex: 1;   
}

.big-card {
  width: 100%;
}

.contact-icon {
    width: 30px;
    height: 30px;
    object-fit: contain;
    background-color: transparent !important;
    margin-right: 7px;
}



/* porto */
.modal-backdrop-custom {
  position: fixed;
  inset: 0;
  background: rgba(0,0,0,0.7);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 9999;
}

.modal-video {
  width: 80%;
  border-radius: 12px;
}

.modal-image {
  max-width: 80%;
  border-radius: 12px;
}

.box {
  border: 1px solid #ddd;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0,0,0,0.1);
}

#portfolio .container {
  max-width: 1300px;
}

/* Judul */
#portfolio h2 {
  font-size: 36px;
  font-weight: 800;
  color: #2b1911 !important;
}

.tabs {
  display: flex;
  justify-content: center;    /* ⬅ tab di tengah */
  align-items: center;        /* ⬅ sejajar vertikal */
  gap: 20px;                  /* ⬅ jarak antar tab */
  list-style: none;
  padding: 0;
  margin: 20px 0 40px;
}

.tab-btn {
  background: #e7f6ff;
  color: #2b1911;
  border: none;
  padding: 10px 24px;
  border-radius: 10px;
  font-size: 16px;
  font-weight: 600;
  cursor: pointer;
  transition: 0.2s;
}

.tab-btn:hover {
  background: #d1efff;
}

.tab-btn.active {
  background: #2b1911;
  color: white;
}

.portfolio-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 25px;
}

.portfolio-card {
  background: white;
  border-radius: 14px;
  box-shadow: 0 4px 10px rgba(0,0,0,0.1);
  padding: 15px;
  transition: 0.3s;
  height: 100%;
}

.portfolio-card:hover {
  transform: translateY(-5px);
}

.media-wrapper {
  width: 100%;
  height: 220px;
  overflow: hidden;
  border-radius: 10px;
}

.portfolio-media,
.certif-thumbnail {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.captionport {
  color: #00364d;
  margin: 8px 0;
}

@media (max-width: 992px) {
  .portfolio-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 600px) {
  .portfolio-grid {
    grid-template-columns: 1fr;
  }
}


/* Contact Section */
.space {
    margin-bottom: 40px; /* Adds space below the contact section */
    margin-top: 40px;
}
/* Form Container */

.contact-form {
    max-width: 320px; /* Controls the width */
    margin: 0 auto; /* Centers the form */
    border: 2px solid #2b1911;
    background-color: #2b1911;
    padding: 50px;
    box-shadow: 0 8px 8px 10px rgba(0, 42, 87, 0.1);
    border-radius: 30px !important; /* Makes the form container rounded */
    justify-content: flex-end;  
}

.contact-form input,
.contact-form textarea {
    border: 1px solid #e4ff8d;
    border-radius: 5px; /* Rounds input fields and textarea */
    padding: 8px 10px;
    width: 100%;
    box-sizing: border-box; /* Ensures padding doesn't add to width */
    margin-bottom: 10px; /* Adds spacing between fields */
    background-color: #fdffe1;
}

.contact-form textarea {
    resize: none; /* Prevents resizing */
}

.contact-form button {
    display: inline-block;
    font-size: 14px;
    padding: 8px 12px;
    background-color: #7b805c;
    color: #d2e4ff;
    border: none;
    border-radius: 12px; /* Rounds the button */
    cursor: pointer;
}

.contact-form button:hover {
    background-color: #e1ffff;
    color: rgb(0, 53, 76);
}


/* Contact Icons */
.contact-icon {
    width: 40px;
    height: 40px;
    object-fit: contain;
    background-color: transparent !important;
}

/* Contact Text */
.contact-details p {
    font-size: 16px;
    color: #333;
    margin: 0;
}

.contact-details {
    margin-top: 20px;
    font-size: 16px;
    color: #333;
}

.contact-details i {
    color: #006666;
    font-size: 20px;
}

.contact-details div {
    display: flex;
    align-items: center;
    font-size: 18px;
    color: #006666;
    font-weight: 500;
}




/* footer */
.footer {
    background-color: #2b1911; /* Set the background color of the footer */
    color: #fff; /* Set the text color */
    font-size: 14px;
}

.footer p {
    margin: 0; /* Remove margin */
    padding: 5px;
}

.social-icons {
    margin-top: 10px;
}

.social-icon {
    width: 30px; /* Set the size of social media icons */
    margin: 0 10px; /* Space between icons */
    transition: transform 0.3s ease;
}

.social-icon:hover {
    transform: scale(1.2); /* Hover effect to enlarge icons */
}
</style>

<script setup>
import { ref } from "vue";

const activeTab = ref("projects");
const video1 = "/video/tekateki.mp4";
const video2 = "/video/mushroom.mp4";
const video3 = "/video/deluxe.mp4";
const showVideo = ref(false);
const currentVideo = ref("");

const openVideoModal = (src) => {
  currentVideo.value = src;
  showVideo.value = true;
};
const closeVideo = () => (showVideo.value = false);

// Certificates
const certificates = [
  { img: "/certificate/pendikar.png", title: "Finalis Business Plan PENDIKAR 2025" },
  { img: "/certificate/webmas.jpg", title: "Anggota Web Master HIMAVO MICRO IT 2023-2024" },
  { img: "/certificate/essai fkmpi.jpg", title: "Peserta Fair Essai Competition" },
  { img: "/certificate/logsumpermira.jpg", title: "Anggota Divisi Logistik" },
  { img: "/certificate/mpkmb60.png", title: "Anggota Divisi Logistik" },
  { img: "/certificate/itfest1.png", title: "Anggota Divisi Logistik" },
];

// Skills
const skills = [
  { icon: "/img/html.png", name: "HTML", level: 70 },
  { icon: "/img/css.png", name: "CSS", level: 68 },
  { icon: "/img/js.png", name: "JavaScript", level: 60 },
  { icon: "/img/androidstudio.png", name: "MySQL", level: 55 },
  { icon: "/img/mysql.png", name: "PHP", level: 50 },
  { icon: "/img/scratch.jpg", name: "Scratch", level: 45 },
];

// Other skills icons
const otherSkills = [
  "/img/word.png", "/img/ppt.png", "/img/figma.jpg", "/img/canva.png",
  "/img/excel.png", "/img/capcut.png", "/img/thunkable.png",
  "/img/rstudio.png", "/img/postman.png"
];

// Modal image logic
const showImage = ref(false);
const currentImage = ref("");

const openImageModal = (img) => {
  currentImage.value = img;
  showImage.value = true;
};
const closeImage = () => (showImage.value = false);



const form = ref({
  name: "",
  email: "",
  message: ""
});

const submitContact = () => {
  alert(`Thank you, ${form.value.name}! Pesan kamu sudah terkirim.`);
  form.value = { name: "", email: "", message: "" };
};
</script>
