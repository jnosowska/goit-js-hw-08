Kryteria przyjęcia
Utworzono repozytorium goit-js-hw-08.
Przy oddaniu pracy domowej dołączono linki: do plików źródłowych i strony roboczej na GitHub Pages.
Wiersz poleceń nie zawiera błędów i ostrzeżeń.
Projekt utworzono z pomocą parcel-project-template.
Sformatowano kod Prettier.
Pliki startowe
Pobierz pliki startowe z gotowymi znacznikami, stylami i załączonymi plikami skryptów dla każdego zadania. Skopiuj je do swojego projektu, całkowicie zastępując folder src w parcel-project-template.

Zadanie 1 - biblioteka SimpleLightbox
Wykonuj to zadanie w plikach 01-gallery.html i 01-gallery.js. Rozbij je na kilka podzadań:

Dodaj bibliotekę SimpleLightbox jako zależność projektu używając npm (link do CDN z Twojej poprzedniej pracy nie jest już potrzebny).
Użyj swojego kodu JavaScript z poprzedniej pracy domowej, ale zrealizuj refaktoryzację uwzględniając to, że biblioteka została zainstalowana przez npm (składnia import/export).
Aby umieścić kod CSS biblioteki w projekcie, należy dodać jeszcze jeden import, oprócz tego opisanego w dokumentacji.

// Opisany w dokumentacji
import SimpleLightbox from "simplelightbox";
// Dodatkowy import stylów
import "simplelightbox/dist/simple-lightbox.min.css";

Zadanie 2 - odtwarzacz wideo
W HTML znajduje się <iframe> z wideo na Vimeo. Napisz skrypt, który będzie zapisywał aktualny czas odtwarzania wideo w local storage i, podczas przeładowywania strony, kontynuuje odtwarzanie wideo od danego momentu.

<iframe
  id="vimeo-player"
  src="https://player.vimeo.com/video/236203659"
  width="640"
  height="360"
  frameborder="0"
  allowfullscreen
  allow="autoplay; encrypted-media"
></iframe>

Wykonuj to zadanie w plikach 02-video.html i 02-video.js. Rozbij je na kilka podzadań:

Zapoznaj się z dokumentacją biblioteki odtwarzacza Vimeo.
Dodaj bibliotekę jako zależność projektu poprzez npm.
Inicjalizuj odtwarzacz w pliku skryptu tak, jak opisano w sekcji pre-existing player, ale weź pod uwagę to, że odtwarzacz dodano jako pakiet npm, a nie poprzez CDN.
Zbadaj dokumentację metody on() i zacznij śledzić zdarzenie timeupdate - aktualizacja czasu odtwarzania.
Zapisuj czas odtwarzania w local storage. Niech kluczem do storage będzie "videoplayer-current-time".
Do przeładowywania strony używaj metody setCurrentTime() aby wznowić odtwarzanie od zapisanego momentu.
Dodaj do projektu bibliotekę lodash.throttle i zrób tak, aby czas odtwarzania aktualizował się w storage nie częściej niż raz na sekundę.
Zadanie 3 - formularz kontaktowy
W HTML znajduje się znacznik formularza. Napisz skrypt, który będzie zapisywał wartości pól w local storage, gdy użytkownik coś wpisuje.

<form class="feedback-form" autocomplete="off">
  <label>
    Email
    <input type="email" name="email" autofocus />
  </label>
  <label>
    Message
    <textarea name="message" rows="8"></textarea>
  </label>
  <button type="submit">Submit</button>
</form>

Wykonuj to zadanie w plikach 03-feedback.html i 03-feedback.js. Rozbij je na kilka podzadań:

Śledź w formularzu zdarzenie input, i za każdym razem zapisuj w local storage obiekt z polami email i message, w których przechowuj aktualne wartości pól formularza. Niech kluczem do storage będzie "feedback-form-state".
Podczas przeładowywania strony sprawdzaj stan storage i jeśli są tam zapisane dane, wypełniaj nimi pola formularza. W przeciwnym wypadku pola powinny być puste.
Po wysłaniu formularza wyczyść storage i pola formularza, a także wprowadź obiekt z polami email, message i ich aktualnymi wartościami do wiersza poleceń.
Zrób tak, aby storage aktualizował się nie częściej niż raz na 500 milisekund. Aby to zrobić, użyj biblioteki lodash.throttle i dodaj ją do projektu.
