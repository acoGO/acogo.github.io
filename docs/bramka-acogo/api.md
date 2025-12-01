# API bramki acoGO!

Aby wykonać integrację z bramką acoGO!, należy wygenerować token API, który będzie służył do autoryzacji w API bramki acoGO!. Poniżej przedstawiamy kroki, które należy wykonać:

1. **Logowanie**: Zalguj się na bramce acoGO! z wykorzystaniem nazwy użytkownika i hasła bramki. <br>_Uwaga: Dane dostępowe do bramki nie są tymi samymi danymi, którch używasz do logowania się na portalu acoGO!_
2. [**Generowanie tokena**](generowanie-tokena.md): Po zalogowaniu się, przejdź do sekcji "API" w ustawieniach bramki i wygeneruj nowy token API.

## Jak używać tokena API do bramki acoGO! ?

Twój osobisty token API jest kluczem dostępu do bramki acoGO!. Należy go traktować jak hasło i nie udostępniać go publicznie. Token ten jest wymagany do autoryzacji w API bramki acoGO! i umożliwia dostęp do Twoich danych oraz zarządzanie bramką i podłączonymi urządzeniami.

!!! danger "Bezpieczeństwo tokena"
    Pamiętaj, aby nie udostępniać swojego tokena API publicznie. Traktuj go jak hasło i przechowuj w bezpiecznym miejscu. Jeśli podejrzewasz, że Twój token został skompromitowany, natychmiast go zresetuj i wygeneruj nowy.

Za pomocą tokena dokonujesz autoryzacji w API bramki acoGO! poprzez dodanie go do nagłówka żądania HTTP.

!!! warning "Nagłówek autoryzacji"
    Treść nagłówka autoryzacji należy podać zależnie od używanego systemu integracji. Niektóre systemy uwzględniają już słowo "Token" w nagłówku, inne wymagają jego dodania. Pamiętaj, że w przypadku bramki acoGO! słowo "Token" musi być w **treści nagłówka, przed wartością tokena.**

Nagłówek autoryzacji powinien wyglądać następująco:

=== "HTTP"
    ```http
    GET /api/order/ezOpen HTTP/1.1
    Host: <adres_IP_bramki>
    Authorization: Token <twój_token_api>
    ```

=== "cURL"
    ```bash
    curl -X GET "http://<adres_IP_bramki>/api/order/ezOpen" -H "Authorization: Token <twój_token_api>"
    ```

=== "Python"
    ```python
    import requests
    headers = {
        'Authorization': 'Token <twój_token_api>'
    }
    response = requests.get('http://<adres_IP_bramki>/api/order/ezOpen', headers=headers)
    if response.status_code == 200:
        devices = response.json()
        print(Drzwi otwarte)
    else:
        print(f'Error: {response.status_code}')
    ```
