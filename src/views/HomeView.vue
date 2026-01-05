<template>
  <section class="home">
    
    <header class="header">
      <img alt="Logo" class="logo" src="/img/logo.svg" />
      <img alt="Brand" class="wv" src="/img/wv.svg" />
    </header>

    
    <div class="hero-content">
      
      <div class="text-block">
        <h1>WELCOME!</h1>
        <h2>I am Software Engineer</h2>
        <p>I'm an undergraduated Software Engineering Technology at IPB University with many experiences in web development and UI/UX design.</p>
        <div class="social-icons">
          <a href="https://www.instagram.com/lunfalis/" target="_blank">
            <img src="/img/ig.svg" class="contact-icon" />
          </a>
          <a href="https://www.facebook.com" target="_blank">
            <img src="/img/fb.svg" class="contact-icon" />
          </a>
          <a href="https://www.x.com" target="_blank">
            <img src="/img/x.svg" class="contact-icon" />
          </a>
          <a href="https://www.linkedin.com/in/lunfalis/" target="_blank">
            <img src="/img/li.svg" class="contact-icon" />
          </a>
          <a href="https://wa.me/6287898505218" target="_blank">
            <img src="/img/wa.svg" class="contact-icon" />
          </a>
        </div>
      </div>

          <div class="photo-frame">
            <img alt="Luna Falya" class="photo" src="/img/lucu.svg" />
         </div>

    </div>
  </section>

    <section>
      <div class="wave"></div>
        <img src="/img/3.svg" class="pop" />
        <img src="/img/3.svg" class="popp" />
        <img src="/img/bung.svg" class="bung" />
        <img src="/img/bungs.png" class="bungs" />
    </section>

    <section id="about" class="about py-5">
    <div class="container">

      <h2 class="text-center fw-bold mb-2" style="color: #2b1911;">ABOUT ME</h2>
      <p style="color: #2b1911;">Hi! Get to know me better.</p>
        <div class="about-container">

          <div class="about-left">
              <img src="/img/guehp.png" class="about-photo" />
            </div>

            <div class="about-right">
            <div class="about-row">
              <div class="card small-card">
                <h3>Who Am I</h3>
                <p>Halo, saya <strong>Luna Falya</strong>, mahasiswa di IPB University jurusan Teknologi Rekayasa Perangkat Lunak, fokus pada web front-end.</p>
              </div>

              <div class="card small-card">
                <h3>My Interest</h3>
                <p>Memiliki pengalaman manajemen logistik, serta mendalami UI/UX design dan front-end programming.</p>
              </div>
            </div>

            <div class="card big-card">
                <h3>Personal Info</h3>

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

              <div v-for="project in projects" :key="project.title">
                <div class="portfolio-card p-3 text-center box">

                  <div class="media-wrapper">
                    <video
                      class="portfolio-media"
                      controls
                      style="cursor: pointer;"
                      @click="openVideoModal(project.video)"
                    >
                      <source :src="project.video" type="video/mp4">
                    </video>
                  </div>

                  <h3 class="fw-semibold captionport">
                    {{ project.title }}
                  </h3>

                  <h5 class="captionport">
                    {{ project.description }}
                  </h5>

                </div>
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
                  <h3 class="fw-semibold captionport">{{ cert.title }}</h3>
                </div>
              </div>

            </div>

            <!-- SKILLS -->
            <<div v-show="activeTab === 'skills'" class="portfolio-grid">


              <!-- Other skills -->
              <div class="text-center mt-4">

                <div class="other-skills">
                  <img
                    v-for="icon in otherSkills"
                    :key="icon"
                    :src="icon"
                    class="skill-icon"
                    alt="skill"
                  />
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
    <h2 class="text-center fw-bold mb-4" style="color:#2b1911">Contact Me</h2>

    <p class="lead text-center mb-5" style="color:#2b1911">
      Saya selalu terbuka untuk diskusi, kolaborasi, atau peluang baru.
    </p>

    <!-- FLEX WRAPPER -->
    <div class="contact-wrapper">

      <!-- LEFT -->
      <div class="contact-left">
        <div class="contact-details">

          <div class="d-flex align-items-center mb-3">
            <img src="@/assets/img/10.png" class="contact-icon me-3" />
            <p class="mb-0">
              Email :
              <a href="mailto:lunfaliswork@gmail.com">lunfaliswork@gmail.com</a>
            </p>
          </div>

          <div class="d-flex align-items-center mb-3">
            <img src="@/assets/img/11.png" class="contact-icon me-3" />
            <p class="mb-0">
              Phone :
              <a href="https://wa.me/6287898505218">+62 878 9850 5218</a>
            </p>
          </div>

          <div class="d-flex align-items-center mb-3">
            <img src="@/assets/img/13.png" class="contact-icon me-3" />
            <p class="mb-0">
              Address :
              <a href="https://www.google.com/maps/place/Tegal+Gundil,+Bogor+Utara,+Bogor+City,+West+Java/@-6.5809898,106.8041303,15z/data=!3m1!4b1!4m6!3m5!1s0x2e69c4297bc8178f:0x7519ce71230296c4!8m2!3d-6.5788507!4d106.8148879!16s%2Fg%2F121k2x_h?entry=ttu&g_ep=EgoyMDI1MTIwOS4wIKXMDSoASAFQAw%3D%3D">Tegal Gundil, Bogor Utara</a>
            </p>
          </div>

          <p class="lead mt-3">
            Atau, Anda dapat mengirimkan pesan melalui formulir di samping.
          </p>
        </div>

        <img src="/img/5.svg" class="pipp" />

      </div>

    <div class="contact-wrapper">
      <img src="/img/4.svg" class="pip" />

      <div class="contact-right">
        <div class="contact-form p-4 rounded">
          <form @submit.prevent="submitContact">
            <div class="mb-3">
              <label>Name</label>
              <input class="form-control" required />
            </div>

            <div class="mb-3">
              <label>Email</label>
              <input class="form-control" required />
            </div>

            <div class="mb-3">
              <label>Message</label>
              <textarea class="form-control" rows="4"></textarea>
            </div>

            <button class="btn active custom-tab">Send Message</button>
          </form>
        </div>
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
        <img src="/img/li.svg" class="social-icon" />
      </a>

      <a href="https://twitter.com" target="_blank">
        <img src="/img/x.svg"  class="social-icon" />
      </a>

      <a href="https://www.instagram.com/lunfalis" target="_blank">
        <img src="/img/ig.svg" class="social-icon" />
      </a>

      <a href="https://www.facebook.com" target="_blank">
        <img src="/img/fb.svg" class="social-icon" />
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
  position: relative;
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
  position: relative;
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
  color: #bd8723;
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
  right: 20px;
  top: calc(25vh - 280px); 
  width: 160px;
  z-index: 5;
}

.bung {
  position: relative;
  left: -320px;
  top: calc(25vh - 370px); 
  width: 200px;
  z-index: 6;
}

.bungs {
  position: relative;
  right: -482px;
  top: calc(25vh - 370px); 
  width: 200px;
  z-index: 6;
}

.wv {
  position: absolute;
  top: 0vh;
  width: 1202px;
  z-index: 0;
  pointer-events: none; /* opsional: biar ga ganggu klik */
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
  position: relative;
  margin-left: 100px;
  margin-top: 10px; /* NAIKIN TEKS */
  object-fit: cover;
  width: 600px;
  height: auto;
}

.text-block h1 {
  font-size: 60px;
  color: #bd8723;
  font-weight: bold;
  z-index: 10;
}

.text-block h2 {
  font-size: 20px;
  color: #bd8723;
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
  padding: 10px 0px;         /* bisa 0 kalau mau tanpa jarak */
  box-sizing: border-box;
}

.about-container {
  width: 95%;
  max-width: 1400px;
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  gap: 40px;
}

.about-left {
  width: 50%;
  display: flex;
  justify-content: flex-start;
}

.about-right {
  width: 80%;
  display: flex;
  flex-direction: column;
  gap: 7px;
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

.card h3 {
  color: #2b1911;
  margin-top: 10px;
  font-weight: 900;
  text-align: center;

  line-height: 1.2;
  height: 2.4em;  /* 2 baris */
  overflow: hidden;
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

.about-photo {
  width: 650px;
  height: auto;
  align-items: flex-start;   /* ⬅ Konten pindah ke kiri */
}

.about-row {
  display: flex;
  gap: 10px;
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
  max-width: 90vw;
  max-height: 90vh;
  width: auto;
  height: auto;
  object-fit: contain;   /* ⬅ ini kuncinya */
  border-radius: 12px;
  background: black;
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
  background: #bec1a6;
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
  background: #b6966a;
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

.skill-card{
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.skill-card h3{
    text-align: center;
  line-height: 1.2;
  max-height: 2.4em;
  overflow: hidden;

  display: -webkit-box;
  -webkit-line-clamp: 2;   /* max 2 baris */
  -webkit-box-orient: vertical;
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

.pip {
  position: absolute;
  top: -105px;        /* naik ke atas form */
  right: 280px;       /* atau left: 40px */
  width: 160px;
  z-index: 10;
}

.contact-wrapper {
  position: relative;
  color: #2b1911;
}

/* Form Container */

.contact-form {
    max-width: 320px; /* Controls the width */
    margin: 0 auto; /* Centers the form */
    border: 2px solid #2b191143;
    background-color: #2b191100;
    padding: 50px;
    box-shadow: 0 8px 8px 10px rgba(0, 42, 87, 0.1);
    border-radius: 30px !important; /* Makes the form container rounded */
    justify-content: flex-end;  
}

.contact-form input,
.contact-form textarea {
    border: 1px solid #342d00;
    border-radius: 5px; /* Rounds input fields and textarea */
    padding: 8px 10px;
    width: 100%;
    box-sizing: border-box; /* Ensures padding doesn't add to width */
    margin-bottom: 10px; /* Adds spacing between fields */
    background-color: #928c71;
}

.contact-form textarea {
    resize: none; /* Prevents resizing */
}

.contact-form button {
    display: inline-block;
    font-size: 14px;
    padding: 8px 12px;
    background-color: #442700;
    color: rgb(252, 253, 176);
    border: none;
    border-radius: 7px; /* Rounds the button */
    cursor: pointer;
}

.contact-form button:hover {
    background-color: #7b805c;
    color: #d2e4ff;
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

.contact-wrapper {
  display: flex;
  gap: 40px;
  align-items: flex-start;
}

/* LEFT */
.contact-left {
  flex: 1;
}

/* RIGHT */
.contact-right {
  flex: 1;
  margin-right: 220px;
}

#contact h2 {
  font-size: 36px;
  font-weight: 800;
  color: #2b1911 !important;
  justify-content: center;    /* ⬅ tab di tengah */
  align-items: center; 
}

/* Responsive */
@media (max-width: 768px) {
  .contact-wrapper {
    flex-direction: column;
  }
}

.pipp {
  position: relative;
  left: 120px;
  top: calc(25vh - 180px); 
  width: 260px;
  z-index: 5;

}


/* other skills */
.other-skills {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 24px;
}

/* icon default */
.skill-icon {
  width: 50px;
  height: 50px;
  object-fit: contain;
  transition: transform 0.3s ease, filter 0.3s ease;
  cursor: pointer;
}

/* icon yang di-hover */
.skill-icon:hover {
  transform: scale(1.6);
  z-index: 2;
  filter: drop-shadow(0 6px 10px rgba(0,0,0,0.25));
}

/* optional: biar fokus ke icon yang di-hover */
.other-skills:hover .skill-icon:not(:hover) {
  filter: grayscale(60%) opacity(0.6);
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
const showVideo = ref(false);
const currentVideo = ref("");

const openVideoModal = (src) => {
  currentVideo.value = src;
  showVideo.value = true;
};
const closeVideo = () => (showVideo.value = false);

const projects = [
  {
    video: "/video/tekateki.mp4",
    title: "Teka Teki Taki",
    description: "Game Teka Teki dengan bobot nilai!"
  },
  {
    video: "/video/mushroom.mp4",
    title: "Mush Room (Final Team Project)",
    description: "Website Penjualan Jamur"
  },
  {
    video: "/video/deluxe.mp4",
    title: "Deluxe Hotel",
    description: "Aplikasi Reservasi Hotel"
  },
  {
    video: "/video/mushroom.mp4",
    title: "SpaceXplorer",
    description: "Gameboard Berbasis AR!"
  },
  {
    video: "/video/mushroom.mp4",
    title: "Rahayu Konveksi",
    description: "Website Manajemen Keuangan Digital"
  },
  {
    video: "/video/elashie.mp4",
    title: "Lashie Lust",
    description: "Website E-commerce Lashie Lust"
  },
    {
    video: "/video/alashie.mp4",
    title: "Admin Lashie Lust",
    description: "Website Admin Lashie Lust"
  }
];

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
  { icon: "/img/html.png", name: "HTML" },
  { icon: "/img/css.png", name: "CSS"},
  { icon: "/img/js.png", name: "JavaScript" },
  { icon: "/img/androidstudio.png", name: "MySQL" },
  { icon: "/img/mysql.png", name: "PHP" },
  { icon: "/img/scratch.jpg", name: "Scratch" },
];

// Other skills icons
const otherSkills = [
  "/img/word.png", "/img/ppt.png", "/img/figma.jpg", "/img/canva.png",
  "/img/excel.png", "/img/capcut.png", "/img/thunkable.png",
  "/img/rstudio.png", "/img/postman.png", "/img/html.png", "/img/css.png", "/img/js.png",
  "/img/androidstudio.png", "/img/mysql.png",  "/img/scratch.jpg"
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
