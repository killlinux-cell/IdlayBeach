<template>

  <nav class="navbar">
    <div class="company-logo">Etoile du Sud</div>
    <div class="nav-links">
      <a href="#hero">Accueil</a>
      <a href="#about">À propos</a>
      <a href="#cta">Contact</a>
    </div>
    <div class="social-icons">
      <a href="#"><i class="fab fa-facebook"></i></a>
      <a href="#"><i class="fab fa-instagram"></i></a>
      <a href="#"><i class="fab fa-twitter"></i></a>
    </div>


      <div class="hamburger-menu-container" @click="openMenu">
				<div
					class="hamburger-menu"
					:class="{ close: isActive }"
					id="toggle-menu"
				></div>
			</div>
  </nav>



  <div class="nav-mobile">
			<a href="#hero-section" class="mobile-element" @click="openMenu">Accueil</a>
			<a href="#about-section" class="mobile-element" @click="openMenu">A propos</a>
			<a href="#menu-section" class="mobile-element" @click="openMenu">Menu</a>
			<a href="#cta-section" class="mobile-element" @click="openMenu">Contact</a>
		</div>

</template>

<script>

export default{
    name: 'Navbar',
    data() {
		return {
			isScrolled: false,
			isActive: false,
			isDropdownVisible: false,
		};
	},
	created() {
		window.addEventListener("scroll", this.onScroll);
	},
	destroyed() {
		window.removeEventListener("scroll", this.onScroll);
	},
	methods: {
		onScroll(event) {
			this.isScrolled = window.scrollY > 0;
		},

		openMenu(event) {
			const toggleButton = document.getElementsByClassName("hamburger-menu")[0];
			const navLinks = document.getElementsByClassName("nav-mobile")[0];

			if (this.isActive == false) {
				navLinks.style.transform = "translate(-100%, 0)";
				this.isActive = true;
			} else if (this.isActive == true) {
				navLinks.style.transform = "translate(100%, 0)";
				this.isActive = false;
			}
		},
		showDropdown() {
			this.isDropdownVisible = true;
		},
		hideDropdown() {
			this.isDropdownVisible = false;
		},
		triggerModal() {
			this.$emit("showModal");
		},
	},
}
</script>

<style>
@import '../style.css';

</style>