
# Integracja acoGO! z Home Assistant

## O acoGO!

acoGO! to niestandardowy komponent dla Home Assistant umożliwiający integrację z ekosystemem acoGO!.<br>
Komponent pozwala na:

- Sterowanie urządzeniami acoGO! bezpośrednio z Home Assistant
- Monitorowanie stanu urządzeń w czasie rzeczywistym
- Automatyzację procesów domowych
- Integrację z innymi komponentami Home Assistant

## Instalacja za pomocą HACS

### Wymagania wstępne

- Zainstalowany [Home Assistant](https://www.home-assistant.io/)
- Zainstalowany [HACS](https://hacs.xyz/)
- Konto w systemie [acoGO!](https://portal.acogo.pl){target=_blank}

### Kroki instalacji i konfiguracji



1. Kliknij przycisk "Dodaj do HACS" poniżej.<br>
[![Dodaj do HACS](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=acoGO&repository=HomeAssistant-acoGO&category=integration)
2. Dodaj niestandardowe repozytorium. <br>
![dodaj repozytorium](../img/Instrukcja_HA/2.png){ width=70% }
3. Pobierz acoGO! i zrestartuj Home Assistant.<br>
![pobierz acoGO!](../img/Instrukcja_HA/3.png){ width=70% }
4. Dodaj integrację "acoGo!" w Ustawienia -> Urządzenia oraz usługi -> Integracje.
![przejście do ustawień](../img/Instrukcja_HA/7.png){ width=70% }
5. Kliknij **Dodaj integrację** i wybierz acoGO!<br>
![dodawanie integracji](../img/Instrukcja_HA/9.png){ width=70% }
6. Podaj token do systemu acoGo! ([generowanie tokena](../portal-acogo/generowanie-tokena.md))
![wpisanie tokena](../img/Instrukcja_HA/10.png){ width=70% }
7. Potwierdź konfigurację<br>
![dodawanie integracji](../img/Instrukcja_HA/16.png){ width=70% }

Po pomyślnej instalacji urządzenia acoGo będą dostępne w Home Assistant.

---

**Dokumentacja**: [acoGO/HomeAssistant-acoGo](https://github.com/acoGO/HomeAssistant-acoGo/tree/master)
