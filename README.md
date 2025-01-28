# 📌 Test PAI - Setup Server Local

Acest ghid explică pas cu pas cum să descarci și să rulezi fișierul HTML al testului într-un server local folosind **Python**.

---

## 📥 1. Descărcare și Salvare Fișier

1. **Creează un fișier nou** pe calculatorul tău.
2. **Copiază codul HTML** al testului.
3. **Salvează-l ca `test.html`** într-un folder ales de tine, de exemplu:
   ```
   C:\TestQuiz\test.html
   ```

---

## 🐍 2. Instalarea Python (dacă nu este instalat)

Dacă nu ai Python instalat, urmează acești pași:

1. **Descarcă Python** de pe site-ul oficial:
   👉 [https://www.python.org/downloads/](https://www.python.org/downloads/)
2. **Instalează-l** și **bifează opțiunea**:  
   ✅ **"Add Python to PATH"** (foarte important!)
3. **Verifică instalarea** deschizând Command Prompt (`cmd`) și rulând:
   ```sh
   python --version
   ```
   Dacă apare ceva de genul `Python 3.x.x`, instalarea a fost realizată cu succes.

---

## 📂 3. Navigarea la Folderul cu Fișierul

### 🔹 **Metoda 1: Direct din Explorer**
1. Mergi în folderul unde ai salvat `test.html`.
2. Ține apăsată tasta **Shift** și **clic dreapta** într-un spațiu gol.
3. Alege **"Open PowerShell window here"** sau **"Open Command Prompt here"**.

### 🔹 **Metoda 2: Folosind Command Prompt**
1. Deschide **Command Prompt** (`cmd`):
   - Apasă **Win + R**, scrie `cmd` și apasă **Enter**.
2. Navighează la folderul unde ai salvat `test.html`:
   ```sh
   cd C:\TestQuiz
   ```

---

## 🚀 4. Pornirea Serverului Local

În terminal (`cmd` sau `PowerShell`), rulează comanda:
```sh
python -m http.server 8000
```
🔹 Această comandă va porni un server web pe portul **8000**.

---

## 🌐 5. Accesarea Testului în Browser

1. Deschide un browser (Chrome, Edge, Firefox etc.).
2. Introdu în bara de adrese:
   ```
   http://localhost:8000/test.html
   ```
3. Apasă **Enter** și testul ar trebui să se încarce! ✅

---

## ⛔ 6. Oprirea Serverului

Dacă vrei să oprești serverul, apasă:
```sh
Ctrl + C
```
în fereastra terminalului.

---

## ⚠️ Probleme posibile și soluții

✅ **Eroare: "Python nu este recunoscut"**  
🔹 Asigură-te că ai bifat **"Add Python to PATH"** la instalare. Dacă nu, reinstalează Python sau rulează comanda:
```sh
setx PATH "%PATH%;C:\Users\NumeleTau\AppData\Local\Programs\Python\Python39\Scripts\"
```
Apoi încearcă din nou comanda `python -m http.server 8000`.

✅ **Pagina nu se încarcă**  
🔹 Verifică dacă serverul rulează corect. Ar trebui să vezi un mesaj de tip:
   ```
   Serving HTTP on :: port 8000
   ```
🔹 Asigură-te că accesezi **http://localhost:8000/test.html**.

✅ **Testul nu încarcă imaginile pisicilor**  
🔹 Testul încarcă imagini de la un API extern (`https://cataas.com/cat`). Dacă nu ai conexiune la internet, imaginile nu vor apărea.

---

## 🎉 Gata! Acum ai testul funcțional pe serverul local. 🚀

