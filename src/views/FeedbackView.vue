<script setup>
    import Footer from '../components/Footer.vue'
    import { ref, reactive, computed, watch } from 'vue'
    import '@/assets/style.css';
  
    const messagea = ref(''); 
    const messageb = ref(''); 

    function say(message) { 
    alert(message)
  }

</script>

<template>
    <main>
        <h1 style="margin-left: 120px">Contact us</h1> 
        <div class="centered-container">
            <form>
                <h4>Please enter your name:</h4>
                <input v-model="messagea" placeholder="Jane Doe" />
                <p>Thank you! Your name is... <br>{{ messagea }}</p>

                <h4>Please enter your email:</h4>
                <input v-model="messageb" placeholder="email@email.com" />
                <p>Thank you! Your email is... <br>{{ messageb }}</p> <br>

                <h4>Please enter your question:</h4>
                <textarea>*Drag to resize</textarea>

                <button @click="say('Thank you! We will get back to you shortly.')">Submit</button>
            </form>
        </div>
        <Footer/>
    </main>
</template>
