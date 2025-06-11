// Copy ke clipboard
navigator.clipboard.writeText("text to copy");

// Cek apakah elemen ada
if (document.querySelector('#myid')) {}

// Debounce function
function debounce(fn, delay) {
  let timeout;
  return function () {
    clearTimeout(timeout);
    timeout = setTimeout(() => fn.apply(this, arguments), delay);
  };
}
