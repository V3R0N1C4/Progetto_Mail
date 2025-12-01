# Progetto_Mail
progetto prog3

- [x] Giorno 1 (Oggi/Oggi-Domani: Setup + Modello Dati): Ambiente + classi base. Tempo: 3-4h. \
      **Milestone**: Progetti creati, Email/Mailbox compilabili.
  * Definisci una classe Email serializzabile (implements Serializable) in un package condiviso o duplica nei progetti. 
    Email include:
    * String id (UUID.randomUUID().toString()),
    * String sender,
    * List<String> recipients,
    * String subject,
    * String body,
    * Date sentDate (new Date()).
    Aggiungi costruttori, getter/setter, toString per logging.
  * Per Mailbox (server-side): Map<String, List<Email>> mailboxes = new ConcurrentHashMap<>(); con 3 account precompilati. \
    Usa File per persistenza: salva in "mailboxes.dat" (ObjectOutputStream per serializzazione binaria).
  * Nel server, carica mailboxes all'avvio e salva periodicamente o su modifiche (synchronized).
  * Nel client, mantieni solo inbox locale: List<Email> inbox = new ArrayList<>(); aggiornata via socket. Usa ObservableList<Email> per JavaFX binding nel client model.

- [ ] Giorno 2 (Domani: Server Comunicazione): Socket server + handler. Tempo: 4-5h. \
      **Milestone**: Server accetta connessioni, logga AUTH.

- [ ] Giorno 3 (Fra 2 Giorni: Server Persistenza + GUI): File I/O + FXML log. Tempo: 5h. \
      **Milestone**: Server salva/carica mailboxes, GUI mostra log.

- [ ] Giorno 4 (Fra 3 Giorni: Client Comunicazione + Regex): Socket client + validazione. Tempo: 4h. \
      **Milestone**: Client autentica, riceve errore su email invalida.

- [ ] Giorno 5 (Fra 4 Giorni: Client MVC + GUI Base): Model/Controller FXML inbox. Tempo: 5-6h. \
      **Milestone**: Client visualizza inbox vuota, status connessione.

- [ ] Giorno 6 (Fra 5 Giorni: Client Operazioni + Parallelismo): Send/Reply/Delete + thread. Tempo: 5h. \
      **Milestone**: Invia email tra 2 client, auto-refresh.

- [ ] Giorno 7 (Fra 6 Giorni: Test + Polish + Demo Prep): Integrazione, bug fix, scalabilità. Tempo: 4-5h. \
      **Milestone**: Demo completa, script test, note per esame
