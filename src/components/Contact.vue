<template>
     <section class="contact" id="cta">
    <div class="contact-content">
      <h2>Nous contacter</h2>
      <form action="#" method="POST">
        <div class="form-group">
          <label for="name">Nom :</label>
          <input type="text" id="name" name="name" required>
        </div>
        <div class="form-group">
          <label for="email">Email :</label>
          <input type="email" id="email" name="email" required>
        </div>
        <div class="form-group">
          <label for="message">Message :</label>
          <textarea id="message" name="message" rows="4" required></textarea>
        </div>
        <div class="form-group">
          <label for="message">Téléphone : 00000000</label>
          
        </div>
        <button type="submit" class="submit-button">Envoyer</button>
      </form>
    </div>
  </section>
</template>

<script>

export default{
    name: 'Contact',
}
</script>

<style>
@import '../style.css';
</style>