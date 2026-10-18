# Temp Mail po polsku — tymczasowy e-mail na 60 minut

**[Otwórz działającą aplikację →](https://temp-mail.hubertmynarski.pl/)**

Projekt Huberta Mynarskiego, ucznia technikum informatycznego. Jednorazowa skrzynka pozwala odebrać pocztę bez zakładania konta i podawania codziennego adresu e-mail. Projekt jest rozwijany również z pomocą narzędzi AI.

## Funkcje działającej usługi

- Losowy adres z 10 znakami przed @, ważny przez 60 minut.
- Automatyczne sprawdzanie poczty co 5 sekund, gdy karta jest widoczna, i ręczne odświeżanie.
- Czytnik sformatowanych wiadomości HTML oraz alternatywny widok tekstowy.
- Kopiowanie rozpoznanego kodu weryfikacyjnego bezpośrednio z listy wiadomości.
- Oczyszczanie HTML i izolacja treści w ramce; zewnętrzne obrazy są blokowane.

## Jak zacząć?

1. Otwórz [Temp Mail](https://temp-mail.hubertmynarski.pl/) i skopiuj wygenerowany adres.
2. Podaj go w miejscu, w którym chcesz odebrać jednorazową wiadomość, zgodnie z zasadami nadawcy.
3. Wróć do skrzynki, otwórz wiadomość albo skopiuj rozpoznany kod z listy.

Strona działa pod `temp-mail.hubertmynarski.pl`, a adresy odbiorcze kończą się na `@inbox.serwerbb.win`. Nie zmieniaj domeny w skopiowanym adresie.

## Instrukcje i pomoc

- [Jak działa tymczasowy e-mail?](https://temp-mail.hubertmynarski.pl/jak-dziala)
- [Wszystkie poradniki](https://temp-mail.hubertmynarski.pl/poradniki)
- [Odbieranie i kopiowanie kodów weryfikacyjnych](https://temp-mail.hubertmynarski.pl/poradniki/kody-weryfikacyjne)
- [Co sprawdzić, gdy wiadomość nie przychodzi?](https://temp-mail.hubertmynarski.pl/poradniki/wiadomosc-nie-przychodzi)
- [O projekcie](https://temp-mail.hubertmynarski.pl/o-projekcie)
- [Prywatność](https://temp-mail.hubertmynarski.pl/prywatnosc) · [Regulamin](https://temp-mail.hubertmynarski.pl/regulamin)

## Ograniczenia

Usługa wyłącznie odbiera pocztę. Nie wysyła wiadomości i nie udostępnia zawartości załączników — pokazuje tylko ich nazwy i rozmiary. Rozpoznawanie kodów jest heurystyczne i może wskazać błędny fragment. Niektóre serwisy nie akceptują adresów tymczasowych; dostarczenie wiadomości nie jest gwarantowane.

Ważności skrzynki nie można przedłużyć. Po wygaśnięciu albo usunięciu wiadomości nie są przywracane. Dostęp zależy od cookie przeglądarki. Nie używaj jednorazowego adresu do poufnej korespondencji, ważnych kont ani odzyskiwania hasła.

## Technologie

Next.js, React, TypeScript, Tailwind CSS, Fastify, PostgreSQL, Docker Compose i Caddy. Odbiór internetowy korzysta z integracji Mailgun.

## Kod repozytorium a usługa produkcyjna

Powyższy opis dotyczy działającej aplikacji. Kod w tym repozytorium pochodzi ze starszej migawki projektu i może nie zawierać wszystkich funkcji obecnego wdrożenia. Aktualizacja tego README nie synchronizuje kodu ani konfiguracji produkcyjnej.

Dokumentacja techniczna wersji repozytorium: [PLAN.md](PLAN.md), [EMAIL_SETUP.md](EMAIL_SETUP.md), [KONTROLE.md](KONTROLE.md), [CHANGELOG.md](CHANGELOG.md). Te dokumenty mogą opisywać historyczne adresy i wyniki kontroli; nie traktuj ich jako bieżącej konfiguracji serwera.

Sekrety, pliki `.env` i dane skrzynek nie powinny trafiać do repozytorium. Baza tego projektu przechowuje krótkotrwałe dane w pamięci: jej restart usuwa wiadomości. Aktualizacja samego frontendu powinna dotyczyć tylko usługi `web`, bez restartu bazy i bez `down -v`.

## Hubert Mynarski

[Portfolio](https://portfolio.hubertmynarski.pl/) · [CV](https://cv.hubertmynarski.pl/) · [GitHub](https://github.com/mynarskih)

Repozytorium nie deklaruje licencji open source; ta aktualizacja jej nie dodaje.
