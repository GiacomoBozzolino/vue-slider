problema: Partendo dal markup della versione svolta in js plain, rifare lo slider ma questa volta usando Vue. Nello zip allegato trovate le immagini, il file index.html, il file js con già l'array di oggetti impostato ed il file css.

I Visualizzazione immagini statiche nel DOM
    Inizializzo un 'istanza dell'applicazione Vue invoncado la funzione createApp
        NB. alla chiusura della funzione va iserito.mount (#'id dell'elemento html')
    1- Recupero il cdn per poter usare Vue js
    2- Eseguo le operazioni base per il corretto funzionamento di Vue js
        - creo un div con id univoco dentro cui inserire tutto il mio contenuto di html
        - nel file js creo la variabile const {createApp} = Vue;
        - Inizializzo un 'istanza dell'applicazione Vue invoncado la funzione createApp
        NB. alla chiusura della funzione va iserito.mount (#'id dell'elemento html')
    3- Cancello il contenuto di HTML che dovrò poi inseriri dal file js
    4- Utilizzo il metodo vue binding così da recuperarle dall'array di js (devo prestare attenzione a come richiamare correttamente le immagini avendo a che fare con un array di oggetti)
    5- Per visualizzare solo la prima immagine di un array posso far in modo di specificare di prendere l'immagine in posizione 0
        - posso usare activeImage: 0 all'interno di data e poi richiamarlo nel dom

II Spostamento immagine al click dei pulsanti
    1- Posso utilizzare @click sui pulsanti per richiamare un metodo creato nel file js
    2- in methods creo una variabile per cui al click activeImage++ e devo inserire un controllo per far tornare l'immagine alla posizione di partenza una volta giunto alla fine dell'array
    3- modifico la stessa regola perchè funzioni quando il valore di activeImage <0