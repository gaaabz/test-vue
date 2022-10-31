<script setup>
import Header from './components/Header.vue'
import Wizard from './components/Wizard.vue'
import Alert from './components/Alert.vue'
</script>

<template>
  <Header />

  <main>
      <Wizard
        :message="'Por favor verifica o actualiza tus datos antes de continuar'"
      ></Wizard>

      <div class="wizard-form">
        <div class="wizard-form__step">
          <h5 class="wizard-form__message">En caso mantengas tus mismo datos de contacto, podrás continuar, de lo contrario, te pediremos que actualices la información.</h5>

          <div class="input-group">
            <label class="input-group__label">
              ¿A quién podemos contactar en caso de emergencia?
            </label>
            <div class="input-control input-control--flex-full">
              <input type="text" placeholder="Nombre completo">
              <span class="input-control__error-message"></span>
            </div>
            <div class="input-control input-control--flex-1-1-0">
              <input type="tel" placeholder="Número de Teléfono">
              <span class="input-control__error-message"></span>
            </div>
            <div class="input-control input-control--flex-1-1-0">
              <select name="" id="">
                <option value="">Seleccionar</option>
                <option value="1">Mi tío/a</option>
              </select>
            </div>
          </div>

          <div class="input-group">
            <label class="input-group__label">
              ¿Tu correo electrónico personal sigue siendo el mismo? 
            </label>
            <div class="input-control input-control--flex-1-1-0">
              <input type="email" placeholder="Correo electrónico">
              <span class="input-control__error-message"></span>
            </div>
            <div class="input-control input-control--button">
              <button type="button" class="button" disabled>
                <i class="button__icon">
                  <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M14 0.666656H2C1.46957 0.666656 0.960859 0.87737 0.585786 1.25244C0.210714 1.62752 0 2.13622 0 2.66666L0 15.3333H16V2.66666C16 2.13622 15.7893 1.62752 15.4142 1.25244C15.0391 0.87737 14.5304 0.666656 14 0.666656ZM13.8493 2.66666L9.09267 7.42332C8.79834 7.70443 8.407 7.86129 8 7.86129C7.593 7.86129 7.20166 7.70443 6.90733 7.42332L2.15067 2.66666H13.8493ZM2 13.3333V5.34466L5.49267 8.83732C5.82184 9.16664 6.21267 9.42787 6.64283 9.6061C7.07299 9.78434 7.53405 9.87607 7.99967 9.87607C8.46529 9.87607 8.92635 9.78434 9.35651 9.6061C9.78666 9.42787 10.1775 9.16664 10.5067 8.83732L14 5.34466V13.3333H2Z" fill="#171717"/>
                  </svg>
                </i>
                <span class="button__text">Verificar</span>
              </button>
            </div>
          </div>

          <Alert
            :iconUrl="'../src/assets/info-icon.svg'"
            :title="'Si cambias tu correo electrónico'"
            :text="'Te enviaré un enlace de confirmación.'"
          ></Alert>

          <div class="input-group">
            <label class="input-group__label">
              ¿Has cambiado de número de celular?
            </label>
            <div class="input-control input-control--flex-1-1-0">
              <input type="email" placeholder="Correo electrónico">
              <span class="input-control__error-message"></span>
            </div>
            <div class="input-control input-control--button">
              <button type="button" class="button" disabled>
                <i class="button__icon">
                  <svg width="12" height="16" viewBox="0 0 12 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path d="M0.666687 0V14C0.666687 14.5304 0.877401 15.0391 1.25247 15.4142C1.62755 15.7893 2.13625 16 2.66669 16H9.33335C9.86379 16 10.3725 15.7893 10.7476 15.4142C11.1226 15.0391 11.3334 14.5304 11.3334 14V0H0.666687ZM6.67002 14.6767H5.32869V13.3333H6.67002V14.6767ZM2.66669 12V2H9.33335V12H2.66669Z" fill="#262626"/>
                  </svg>
                </i>
                <span class="button__text">Verificar</span>
              </button>
            </div>
          </div>

          <Alert
            :iconUrl="'../src/assets/info-icon.svg'"
            :title="'Si actualizas, ten tu celular a la mano'"
            :text="'Te enviaré un SMS con un código de confirmación.'"
          ></Alert>
        </div>
      </div>
  </main>
</template>
