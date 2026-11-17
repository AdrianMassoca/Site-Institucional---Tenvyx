
<script setup>
import { ref } from 'vue'
import {
  Mail,
  MessageSquareText,
  Send,
  CheckCircle2
} from 'lucide-vue-next'

import SectionHeading from './SectionHeading.vue'

const form = ref({
  name: '',
  email: '',
  company: '',
  message: ''
})

const feedback = ref('')
const submitted = ref(false)

function submitForm() {
  submitted.value = true

  feedback.value =
    'Validação concluída! Este formulário ainda está em modo demonstrativo. Em breve, você poderá enviar sua mensagem diretamente para a TENVYX.'
}
</script>

<template>
  <section id="contato" class="section contact-section">
    <div class="contact-aura" aria-hidden="true"></div>

    <div class="container contact-layout">
      <div class="contact-copy">
        <SectionHeading
          eyebrow="FALE COM A TENVYX"
          title="Vamos transformar sua ideia em uma solução."
          description="Cada projeto começa com uma boa conversa. Compartilhe seu desafio e descubra como a tecnologia pode contribuir para a evolução do seu negócio."
        />

        <div class="contact-detail">
          <span>
            <Mail :size="18" />
          </span>

          <div>
            <b>Contato institucional</b>
            <small>
              Um canal dedicado para apresentar seu projeto e suas necessidades.
            </small>
          </div>
        </div>

        <div class="contact-detail">
          <span>
            <MessageSquareText :size="18" />
          </span>

          <div>
            <b>Atendimento direcionado</b>
            <small>
              Entendemos seu contexto para identificar possibilidades e soluções.
            </small>
          </div>
        </div>
      </div>

      <form class="contact-form" @submit.prevent="submitForm">
        <div class="form-heading">
          <span>INICIAR UMA CONVERSA</span>
          <small>
            <i></i>
            FORMULÁRIO DEMONSTRATIVO
          </small>
        </div>

        <label for="name">Nome completo</label>
        <input
          id="name"
          v-model.trim="form.name"
          autocomplete="name"
          placeholder="Como podemos chamar você?"
          required
        />

        <label for="email">E-mail profissional</label>
        <input
          id="email"
          v-model.trim="form.email"
          type="email"
          autocomplete="email"
          placeholder="voce@empresa.com"
          required
        />

        <label for="company">
          Empresa <span>(opcional)</span>
        </label>
        <input
          id="company"
          v-model.trim="form.company"
          autocomplete="organization"
          placeholder="Nome da sua empresa"
        />

        <label for="message">Conte sobre seu projeto</label>
        <textarea
          id="message"
          v-model.trim="form.message"
          rows="4"
          placeholder="Descreva sua ideia, necessidade ou desafio..."
          required
        ></textarea>

        <button
          class="button button-primary form-submit"
          type="submit"
          :disabled="submitted"
        >
          {{ submitted ? 'Mensagem validada' : 'Validar mensagem' }}

          <CheckCircle2 v-if="submitted" :size="17" />
          <Send v-else :size="17" />
        </button>

        <p
          v-if="feedback"
          class="form-feedback"
          role="status"
        >
          {{ feedback }}
        </p>

        <p v-else class="form-note">
          Ambiente demonstrativo: suas informações não são enviadas nem armazenadas.
        </p>
      </form>
    </div>
  </section>
</template>
