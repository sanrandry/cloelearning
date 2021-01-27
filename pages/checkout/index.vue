<template>
  <div>
    <div class="container">
      <!-- logo -->
      <div class="columns mt-5 logo">
        <div class="column">
          <img
            src="https://da32ev14kd4yl.cloudfront.net/versioned/bioresonance/BRS_Logo/paiement-scuris-avec-stripe-carte-bleue-min.jpg"
            alt=""
            class="logo__img"
          />
        </div>
        <div class="column">
          <img
            src="https://da32ev14kd4yl.cloudfront.net/versioned/bioresonance/BRS_Logo/satisfait-rembourse-30j-2.png"
            alt=""
            class="logo__img"
            id="rebourse_image"
          />
        </div>
      </div>
      <!-- //logo -->

      <!-- card -->
      <div class="columns">
        <div class="column">
          <div class="card form-card">
            <div class="card-content">
              <h2 class="form-card__title mb-3">
                Solde Thérapeute Quantique 2033 Formule Diamant
              </h2>
              <div class="form-card__description columns">
                <div class="column">
                  <h4 class="form-card__description__title">Formule Diamant</h4>
                  <p class="form-card__description_paragraph">
                    Thérapeute Quantique 2033
                  </p>
                </div>
                <div class="column">
                  <span class="form-card__price">2690€</span>
                </div>
              </div>
              <h2 class="form-card__title mb-3">Coordonnées</h2>
              <!-- inputs -->
              <div class="">
                <b-field>
                  <b-input placeholder="Votre nom"></b-input>
                </b-field>
                <b-field>
                  <b-input placeholder="Votre prénom"></b-input>
                </b-field>
                <b-field>
                  <b-input placeholder="Votre email"></b-input>
                </b-field>
                <b-field>
                  <b-input placeholder="Votre adresse"></b-input>
                </b-field>
                <b-field>
                  <b-input placeholder="Ville"></b-input>
                </b-field>
                <b-field>
                  <b-input placeholder="France"></b-input>
                </b-field>
                <b-field>
                  <b-input placeholder="No label"></b-input>
                </b-field>
                <b-field>
                  <b-input placeholder="Votre société"></b-input>
                </b-field>
                <b-field>
                  <b-input
                    placeholder="Numéro de TVA Intracommunautaire"
                  ></b-input>
                </b-field>
              </div>
              <!-- //inputs -->
              <!-- checkboxs -->
              <div>
                <p class="is-size-5 mt-3">Conditions Générales de Vente</p>
                <div class="mt-2">
                  <label for="chekcbox-accept">
                    <input type="checkbox" id="chekcbox-accept" /> J'ai lu les
                    conditions générales de vente et j'y adhère sans réserve.
                    Lire les conditions générales de vente.
                  </label>
                </div>
                <div class="mt-2">
                  <label for="chekcbox-email">
                    <input type="checkbox" id="chekcbox-email" /> En indiquant
                    votre adresse mail, vous acceptez de recevoir des offres
                    commerciales de notre part. Vous pouvez vous désinscrire à
                    tout moment en nous adressant un mail et à travers les liens
                    de désinscription.
                  </label>
                </div>
              </div>
              <!-- //checkboxs -->
              <!-- payment type radio -->
              <h2 class="form-card__title mb-3">Moyen de paiement</h2>
              <div>
                <b-field>
                  <div class="columns">
                    <div class="column">
                      <b-radio-button
                        v-model="from_data.mode_payment"
                        native-value="credit"
                        type="active"
                        class="payment-type-radio"
                      >
                        <div>
                          <img
                            src="https://da32ev14kd4yl.cloudfront.net/assets/images/payments/stripe.png?v=396"
                            alt=""
                          />
                          <br />
                          2 690 € par carte de crédit
                        </div>
                      </b-radio-button>
                    </div>
                    <div class="column">
                      <b-radio-button
                        v-model="from_data.mode_payment"
                        native-value="bank"
                        type="active"
                        class="payment-type-radio"
                      >
                        <div>
                          <img
                            src="https://da32ev14kd4yl.cloudfront.net/assets/images/payments/virement.png?v=396"
                            alt=""
                          />
                          <br />
                          2 690 € par virement bancaire
                        </div>
                      </b-radio-button>
                    </div>
                  </div>
                </b-field>
                {{ from_data.mode_payment }}
              </div>
              <!-- payment type radio -->
              <div class="form-card__submit">
                <b-button
                  type=""
                  class="is-large form-card__submit__btn"
                  expanded
                  inverted
                  >Valider la commande</b-button
                >
              </div>
            </div>
          </div>
        </div>
      </div>
      <!-- //card -->
    </div>
    <div class="footer">
      <p class="footer__paragraph has-text-centered column is-half">
        CGV © 2010- 2018 Philippe Wattiez – Tous Droits Réservés – CLOE-LEARNING
        SPRL 33 Rue de l’Aigle, 7640 ANTOING, BELGIQUE – Numéro de TVA :
        BE0681578319
      </p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      from_data: {
        mode_payment: "credit",
      },
    };
  },
};
</script>

<style>
.logo__img {
  max-width: 100%;
}
#rebourse_image {
  height: 198px;
  width: 266px;
  margin: 0 auto;
  display: block;
}
.form-card__title {
  background-color: #1b79c2 !important;
  color: #fff;
  letter-spacing: 0px;
  font-weight: 700;
  padding: 20px;
  font-size: 22px;
  line-height: 70px;
}
.form-card__description {
  padding: 35px;
  color: #5c6566;
}
.form-card__description__title {
  font-size: 28px;
}
.form-card__description_paragraph {
  font-size: 14px;
}
.form-card__price {
  float: right;
}
.payment-type-radio .b-radio {
  height: auto !important;
}
.payment-type-radio .active {
  border: 2px solid #1b79c2;
}
.form-card__submit {
  padding: 0px 75px;
}
.form-card__submit__btn {
  color: white;
  background: #fca301;
}
.form-card__submit__btn:hover {
  color: white;
}
.footer {
  background-color: #1b79c2 !important;
  color: white;
}
.footer__paragraph {
  margin: auto;
}
</style>
