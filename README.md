## Istruzioni sull'utilizzo di Git
Una volta clonata la repo, ed essere acceduti alla cartella di quest'ultima, si possono creare dei branch che permettono di non dover utilizzare necessariamente solo il main principale, e quindi aggiungere delle modifiche solo locali e non globali

### **1. Controllare i branch esistenti**
```bash
git branch -a
```

### **2. Creare e passare al nuovo branch**

Quando si crea un nuovo branch cercare di inserire un nome al nuovo branch che permetta di riassumere in maniera concreta quello che si sta andando a modificare o quale zona di appunti si sta andando ad editare principalmente
```bash
git checkout -b <zona_appunti_modificata>

# esempio

git checkout -b capitolo1_generalita_68k
```

Se vuoi basarti su un branch specifico, e quindi espandere un branch già esistente, allora:
```bash
git checkout -b <nome_branch> <branch_di_base>
```
Tale operazione potrebbe essere comoda quando un gruppetto si occupa di scrivere diverse parti di un singolo capitolo per poi iniziare a fare un piccolo marging nei branch "laterali" prima di validare il lavoro nel branch principale

### **3. Verificare il branch attuale**
```bash
git branch
```
L'asterisco (`*`) indica il branch attualmente attivo.

### **4. Aggiungere e committare modifiche (facoltativo)**
```bash
git add .
git commit -m "Descrizione delle modifiche"
```

### **5. Pushare il branch su remoto**
```bash
git push origin <nome_branch>
```
Se è la prima volta che pushi questo branch, imposta l'upstream con:
```bash
git push --set-upstream origin <nome_branch>
```

### **6. Creare una Pull Request (opzionale)**
Dopo aver pushato il branch, puoi aprire una **Pull Request** su GitHub/GitLab/Bitbucket per richiedere la revisione e fusione del codice.

#### **Passaggi per creare una Pull Request su GitHub**
1. Vai sulla pagina della repository su GitHub.
2. Clicca sulla scheda **Pull requests**.
3. Clicca su **New pull request**.
4. Seleziona il branch di origine (quello che hai creato) e il branch di destinazione (es. `main` o `develop`).
5. Inserisci un titolo e una descrizione della Pull Request.
6. Clicca su **Create pull request**.
7. Attendi la revisione del codice e, se necessario, risolvi eventuali commenti.
8. Una volta approvata, puoi effettuare il merge della Pull Request.


