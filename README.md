Скрипт, який необхідно скопіювати і вставити у файл modal.js.

(() => {
  const refs = {
    openModalBtn: document.querySelector("[data-modal-open]"),
    closeModalBtn: document.querySelector("[data-modal-close]"),
    modal: document.querySelector("[data-modal]"),
  };

  refs.openModalBtn.addEventListener("click", toggleModal);
  refs.closeModalBtn.addEventListener("click", toggleModal);

  function toggleModal() {
    refs.modal.classList.toggle("is-hidden");
  }
})();

<body>
  <!-- Вся твоя розмітка, включно з розміткою модалки -->

  <!-- Ставимо перед закриваючим тегом body -->
  <script src="./js/modal.js"></script>
</body>

Відкриття/закриття модального вікна
Модальне вікно з формою заявки відкривається по натисканню на кнопку "Замовити послугу". Для того щоб скрипт спрацював, необхідно додати до розмітки спеціальні атрибути, за якими скрипт шукає елементи:

data-modal-open - на кнопку відкриття модального вікна.
data-modal-close - на кнопку закриття модального вікна.
data-modal - на бекдроп модального вікна.

.is-hidden {
  /* скриваємо вікно */
  visibility: hidden;
  opacity: 0;
  pointer-events: none;
}
