# Portal acoGO! - Jak zacząć ?

Aby rozpocząć korzystanie z Ekosystemu acoGO!, należy wykonać kilka kroków:

1. **Rejestracja**: Zarejestruj się w systemie acoGO! poprzez aplikację mobilną ([Android](https://play.google.com/store/apps/details?id=pl.aco.acogo){target=_blank}, [iOS](https://apps.apple.com/pl/app/acogo-2-0/id1544715142?l=pl){target=_blank}) lub [stronę internetową](https://portal.acogo.pl){target=_blank}.
2. **Potwierdzenie konta**: Po rejestracji otrzymasz e-mail z linkiem do potwierdzenia konta. Kliknij w link, aby aktywować swoje konto.
3. **Generowanie tokena**: Po zalogowaniu się w portalu, wygeneruj swój token API [link]. Token ten będzie potrzebny do autoryzacji w API acoGO!.

## Jak używać tokena API portalu acoGO! ?

Twój osobisty token API jest kluczem dostępu do zasobów acoGO!. Należy go traktować jak hasło i nie udostępniać go publicznie. Token ten jest wymagany do autoryzacji w API acoGO! i umożliwia dostęp do Twoich danych oraz zarządzanie urządzeniami.

Za pomocą tokena dokonujesz autoryzacji w API acoGO! poprzez dodanie go do nagłówka żądania HTTP. 

Nagłówek autoryzacji powinien wyglądać następująco:

```
Authorization: Bearer <twój_token_api>
```

=== "HTTP"
    ```http
    GET /api/v2/devices HTTP/1.1
    Host: api.acogo.pl
    Authorization: Bearer <twój_token_api>
    ```

=== "cURL"
    ```bash
    curl -X GET "https://api.acogo.pl/api/v2/devices" -H "Authorization: Bearer <twój_token_api>"
    ```

=== "Python"
    ```python
    import requests
    headers = {
        'Authorization': 'Bearer <twój_token_api>'
    }
    response = requests.get('https://api.acogo.pl/api/v2/devices', headers=headers)
    if response.status_code == 200:
        devices = response.json()
        print(devices)
    else:
        print(f'Error: {response.status_code}')
    ```
