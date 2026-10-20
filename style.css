// Ganti data kontak di bawah ini dengan akun milikmu sebelum dipublikasikan.
const profile = {
  email: "aziazril4@gmail.com",
  github: "https://github.com/username",
  linkedin: "Muh Adzril Aziz"
};

// 1. Update Tahun Footer
const yearElement = document.getElementById("year");
if (yearElement) {
  yearElement.textContent = new Date().getFullYear();
}

// 2. Update Data Kontak (Email)
const emailLink = document.getElementById("emailLink");
const emailText = document.getElementById("emailText");
if (emailLink && emailText) {
  emailLink.href = `mailto:${profile.email}`;
  emailText.textContent = profile.email;
}

// 3. Update Data Kontak (GitHub)
const githubLink = document.getElementById("githubLink");
const githubText = document.getElementById("githubText");
if (githubLink && githubText) {
  githubLink.href = profile.github;
  githubText.textContent = profile.github.replace(/^https?:\/\//, "").replace(/\/$/, "");
}

// 4. Update Data Kontak (LinkedIn)
const linkedinLink = document.getElementById("linkedinLink");
const linkedinText = document.getElementById("linkedinText");
if (linkedinLink && linkedinText) {
  linkedinLink.href = profile.linkedin;
  linkedinText.textContent = profile.linkedin.includes("username")
    ? "Ganti dengan profil LinkedIn"
    : profile.linkedin.replace(/^https?:\/\//, "").replace(/\/$/, "");
}

// 5. Menu Navigasi Mobile
const menuToggle = document.getElementById("menuToggle");
const navMenu = document.getElementById("navMenu");

if (menuToggle && navMenu) {
  menuToggle.addEventListener("click", () => {
    const isOpen = navMenu.classList.toggle("open");
    menuToggle.setAttribute("aria-expanded", String(isOpen));
    menuToggle.textContent = isOpen ? "✕" : "☰";
  });

  navMenu.querySelectorAll("a").forEach(link => {
    link.addEventListener("click", () => {
      navMenu.classList.remove("open");
      menuToggle.setAttribute("aria-expanded", "false");
      menuToggle.textContent = "☰";
    });
  });
}

// 6. Filter Project (Grid Proyek)
const filterButtons = document.querySelectorAll(".filter-btn");
const projectCards = document.querySelectorAll(".project-card");

if (filterButtons.length > 0 && projectCards.length > 0) {
  filterButtons.forEach(button => {
    button.addEventListener("click", () => {
      const filter = button.dataset.filter;
      filterButtons.forEach(item => item.classList.toggle("active", item === button));
      projectCards.forEach(card => {
        const shouldShow = filter === "all" || card.dataset.category === filter;
        card.classList.toggle("hidden", !shouldShow);
      });
    });
  });
}
