# Webhooki bramki acoGO!

Webhooki w bramce acoGO! umożliwiają wysyłanie powiadomień do zewnętrznych systemów, takich jak systemy alarmowe, monitoring czy inne aplikacje, które obsługują webhooki. Dzięki temu możesz otrzymywać informacje o zdarzeniach związanych z bramką, takich jak otwarcie drzwi, bramy czy inne istotne zdarzenia.

## Jak to działa?

1. [**Rejestracja webhooka**](rejestracja-webhooka.md): Aby rozpocząć korzystanie z webhooków, musisz zarejestrować adres URL, na który będą wysyłane powiadomienia. Można to zrobić za pomocą interfejsu konfiguracyjnego bramki, poprzez przeglądarkę internetową.
2. **Wysyłanie powiadomień**: Gdy wystąpi zdarzenie, bramka acoGO! wyśle powiadomienie na zarejestrowany adres URL.
3. **Obsługa powiadomień**: Twój system zewnętrzny powinien być w stanie odebrać powiadomienie i odpowiednio na nie zareagować, na przykład aktualizując stan urządzenia lub informując użytkownika o zdarzeniu.

!!! info "Format powiadomień"
    Bramka acoGO! wywołuje adres webhook'a zawsze metodą `GET`. Do zapytania nie są dołączane żadne dodatkowe parametry ani nagłówki.

!!! tip "Autentykacja i parametry"
    Jeżeli potrzebujesz uwierzytelnienia lub dodatkowych parametrów, możesz zawrzeć je w adresie URL webhooka. Na przykład, możesz dodać token autoryzacyjny jako parametr zapytania: `https://example.com/webhook?token=your_token&bramka=id_bramki`.

## Obsługiwane zdarzenia

Webhooki mogą być używane do monitorowania różnych zdarzeń, takich jak:

- Otwarcie elektrozaczepu (EZ Open)
- Otwarcie wyjścia F2 (F2 Open)
  
Tylko w systemie PRO:

- Przełączenie przełącznika video z określonym adresem (Video Switch with address)
- Dzwonienie z modułu PRO-I/O (IO Module ring)

!!! Pamiętaj
    Ze względu na specyfikę systemu domofonowego, bramka acoGO! może zgłaszać tylko zdarzenia, które zostały wywołane za jej pośrednictwem. System nie będzie zgłaszał zdarzeń, które miały miejsce bezpośrednio na urządzeniach podłączonych do bramki, takich jak panele domofonowe czy moduły rozszerzeń.
