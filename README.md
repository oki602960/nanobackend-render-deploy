# nanobackend-render-deploy

To repozytorium zawiera konfigurację do wdrożenia aplikacji na platformie Render, budując obraz Docker na podstawie pliku `Dockerfile`.

## Wdrożenie na Render

Plik `render.yaml` definiuje usługę webową, która używa obrazu Docker z GitHub Container Registry. Automatyczne wdrożenie jest włączone, co oznacza, że każda zmiana w tym repozytorium (jeśli jest połączone z Render) spowoduje ponowne wdrożenie.

### Konfiguracja Render

Usługa jest skonfigurowana do:
- Budowania obrazu Docker na podstawie pliku `Dockerfile` znajdującego się w repozytorium.
- Nasłuchiwania na porcie `8080`.
- Posiadania ścieżki sprawdzania kondycji (`healthCheckPath`) ustawionej na `/`.

Aby wdrożyć:
1. Utwórz nowe konto na [Render](https://render.com/).
2. Połącz swoje konto GitHub z Render.
3. Utwórz nową usługę `Web Service` na Render.
4. Wybierz to repozytorium.
5. Render automatycznie wykryje plik `render.yaml` i skonfiguruje usługę.

