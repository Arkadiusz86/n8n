# 📬 Automatyczny Newsletter IT – n8n Workflow

Ten projekt to w pełni zautomatyzowany workflow oparty na [n8n](https://n8n.io), który generuje newsletter HTML z najnowszymi wpisami z kanałów RSS związanych z IT, devops, bezpieczeństwem i open source.

## 🔧 Funkcje

- Codzienne pobieranie newsów z ponad 50 kanałów RSS
- Wybór 3–5 najnowszych artykułów
- Formatowanie treści w stylu newslettera HTML
- Opcjonalna integracja z OpenAI (wersja pełna)
- Opcjonalna integracja z SerpAPI (wersja pełna)
- Wysyłka maila do wskazanych odbiorców

## 📁 Pliki w repozytorium

- `Newsletter.json` – pełna wersja z OpenAI + SerpAPI
- `Newsletter_bez_google.json` – wersja bez Google SerpAPI
- `Newsletter_bez_google_i_AI_copy.json` – wersja minimalna bez AI
- `lista kanałów RSS.txt` – lista źródeł RSS

## 📦 Wymagania

- 🐳 n8n (zalecana wersja: najnowsza stable)
- Konto SMTP (np. Mailgun, Gmail, Sendinblue)
- (Opcjonalnie) konto OpenAI z kluczem API
- (Opcjonalnie) konto SerpAPI

## 🚀 Instalacja

1. Uruchom instancję n8n (Docker lub lokalnie)
2. Zaimportuj jeden z plików `.json` do n8n
3. Ustaw dane SMTP w node `Send Email`
4. (Opcjonalnie) Dodaj dane API OpenAI i SerpAPI
5. W node `SSH` ustaw polecenie odczytujące Twój plik z URL-ami RSS
6. Ustaw harmonogram uruchamiania (`Schedule Trigger`)
7. Aktywuj workflow

## 📥 Przykładowy wynik

Wiadomość e-mail z:
- nagłówkiem newslettera,
- 3–5 najnowszymi newsami z kanałów RSS,
- podsumowaniem i linkami.

## 🛡️ Uwagi bezpieczeństwa

Plik `lista kanałów RSS.txt` nie zawiera danych wrażliwych. Upewnij się jednak, że dane API i SMTP nie są zapisane w repozytorium.

## 📚 Źródła RSS (fragment)

- https://blog.zabbix.com/feed/
- https://grafana.com/blog/rss/
- https://linuxsecurity.com/rss/news
- https://kubernetes.io/feed.xml
- … (pełna lista w pliku `lista kanałów RSS.txt`)

## 📄 Licencja

MIT

---

