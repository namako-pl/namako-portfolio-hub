# Portfolio: Budowa Imersyjnego Portalu Operacyjnego [NAMAKO](https://www.namako.eu/)

Projekt polegał na zaprojektowaniu i pełnym wdrożeniu responsywnego portalu typu **One-Page Application**, łączącego zaawansowaną warstwę wizualną z autorską architekturą backendową.

## 🛠️ Zakres zrealizowanych prac technicznych:

### 1. Frontend Engineering & Immersive UI
*   **Implementacja WebGL:** Integracja biblioteki `Vanta.js` (opartej na `Three.js`) do renderowania generatywnych, interaktywnych teł działających w czasie rzeczywistym.
*   **System Synchronizacji Stanów (Cross-fade):** Opracowanie mechanizmu płynnego przełączania między trzema trybami aplikacji (Systems, Business, Soul). Logika zarządza jednoczesną zmianą parametrów WebGL, treści DOM oraz stylów CSS bez przeładowania strony.
*   **Zaawansowany CSS & Animacje:** 
    *   Zastosowanie technik **Glassmorphism** (mrożone szkło) przy użyciu `backdrop-filter`.
    *   Implementacja autorskiego efektu świetlnego na krawędziach kart (Spark Effect) przy użyciu **CSS Masking** (`mask-composite`) oraz dynamicznych gradientów stożkowych (`conic-gradient`).
    *   Opracowanie kinematograficznego systemu wejścia (**Portal Gateway**) wykorzystującego transformacje 3D i animacje skalowania (`Tunnel Zoom`).

### 2. Integracje API i Zarządzanie Stanem (Persistence)
*   **YouTube IFrame API:** Pełna integracja odtwarzacza audio z zaawansowaną obsługą zdarzeń (`onStateChange`, `onError`).
*   **Persystencja danych (LocalStorage):** Zaprojektowanie systemu zapisu stanu sesji, który synchronizuje postęp odtwarzania (numer utworu i znacznik czasu) w przeglądarce użytkownika, umożliwiając kontynuację sesji po odświeżeniu strony.

### 3. Backend & Data Architecture (PHP)
*   **Autorska Baza Danych (File-based DB):** Zaprojektowanie bezpiecznej architektury przechowywania danych w chronionych plikach PHP (z nagłówkami blokującymi dostęp bezpośredni). Dane są przetwarzane w formacie JSON, co eliminuje zależność od zewnętrznych serwerów SQL i zwiększa prywatność danych.
*   **Moduł Rezerwacyjny AJAX:** Implementacja skryptów PHP obsługujących asynchroniczne żądania `fetch` do weryfikacji dostępności terminów w czasie rzeczywistym oraz zapisu nowych rekordów.
*   **System Powiadomień (Auto-responder):** Opracowanie logiki wysyłki dwukierunkowych powiadomień e-mail w formacie HTML (MIME 1.0) z dynamicznym wstrzykiwaniem treści.

### 4. Security & Logic Validation
*   **Quantum Logic Captcha:** Autorski mechanizm weryfikacji botów "Human-to-Server". System generuje zadania matematyczne po stronie klienta, a ich poprawność jest walidowana przez backend przed przetworzeniem formularza.
*   **Data Sanitization:** Wdrożenie filtracji danych wejściowych (`filter_var`, `htmlspecialchars`) w celu ochrony przed atakami typu XSS i Injection.

## 🤖 Metodologia pracy (AI Orchestration)
Projekt został zrealizowany w modelu **AI-assisted Development**. Jako główny architekt zarządzałam pracą zespołu modeli AI (Gemini aiStudio, Cline, Claude), wykorzystując **Prompt Engineering** i **Agentic Workflows** do optymalizacji kodu źródłowego, debugowania skomplikowanych funkcji JavaScript oraz automatyzacji powtarzalnych zadań deweloperskich.

---
**Technologie:** JavaScript (ES6+), PHP, CSS3 (Custom Properties), HTML5, Three.js, YouTube API, AJAX.
