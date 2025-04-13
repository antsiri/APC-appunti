# Come leggere gli appunti
Dopo ogni aggiornamento è stato predisposto un bot che compila il documento e lo pusha all'interno della cartella pdf_output. Bisogna stare attenti alla seguente cosa:
l'ultimo commit disponibile è quello che riporta l'aggiornamento del pdf (poichè l'autocompilazione può richiedere qualche minuto)

# Strutturazione dell'operazione di scrittura
## Istruzioni sull'utilizzo di Git
Una volta clonata la repo, ed essere acceduti alla cartella di quest'ultima, si possono creare dei branch che permettono di non dover utilizzare necessariamente solo il main principale, e quindi aggiungere delle modifiche solo locali e non globali

### **Per contribuire alla repo**
#### **Prima di iniziare**
1. Guardare su github le ISSUE da fare, e nel caso, autoassegnarsela
2. (se non lo si ha già fatto) Clonare la repo il locale tramite il comando:
```bash
git clone <link-to-repo>
```
3. Aggiornare la repo alla sua versione più recente
4. Controllare se è presente il branch per lo sviluppo della ISSUE e nel caso non fosse presente crearla
```bash
# Per visualizzare tutti i repo disponibili
git branch -a

# Per visualizzare i branch remoti
git branch -r

# Per visualizzare i branch locali
git branch

# Nel caso non sia presente il branch disponibile crearne uno nel seguente formato
git checkout -b <numero_issue>_<cosa si sta svolgendo>
```
5. Una volta selezionato o creato il branch corretto effettuare tutte le modifiche opportune

#### **Push degli aggiornamenti**
1. Verificare che si sta lavorando sul branch corretto tramite il comando
```bash
# Comando per verificare il branch attivo (tramite l'asterisco posto alla sinistra del branch attivo)
git bash

# Comando per visualizzarlo in maniera diretta
git branch --show-current
```
2. Una volta assicurato che si sta lavorando sul branch corretto effettuare l'add dei file
```bash
git add *
```
3. Effettuare il commit
```bash
git commit -m "breve messaggio #<numero-issue-contributo>"
```
4. Push del commit
```bash
# se non è la prima volta
git push origin <nome-del-branch>

# se è la prima volta che viene pushato tale branch
git push --set-upstream origin <nome-del-branch>
```

#### **Generare la pull request**
Alla fine del lavoro sul branch si può decidere di poter mergiare tale lavoro. Per fare una richiesta di merging si può andare a fare una pull request tramite github per poi essere confrontata con il branch principale (compatibilità), e nel caso di conflitti, essere risolti manualmente, per poi essere mergiati

#### **Passaggi per creare una Pull Request su GitHub**
1. Vai sulla pagina della repository su GitHub.
2. Clicca sulla scheda **Pull requests**.
3. Clicca su **New pull request**.
4. Seleziona il branch di origine (quello che hai creato) e il branch di destinazione (es. `main` o `develop`).
5. Inserisci un titolo e una descrizione della Pull Request.
6. Clicca su **Create pull request**.
7. Attendi la revisione del codice e, se necessario, risolvi eventuali commenti.
8. Una volta approvata, puoi effettuare il merge della Pull Request.

#### **Comandi utili**
Annullamento di un commit errato
```bash
git reset HEAD~1
```
