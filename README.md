# ![Static Badge](https://img.shields.io/badge/libmyssh-v1.0.0-blue?style=plastic&logo=linux&logoColor=white&logoSize=300&label=Version&labelColor=black&color=white)

**La libreria C++ definitiva per connessioni SSH agili**

`libmyssh` è una libreria leggera e moderna progettata per semplificare la gestione delle sessioni SSH. Grazie all'interfaccia intuitiva offerta dalla classe `Carcoal`, permette di stabilire connessioni remote con poche righe di codice, eliminando la complessità della configurazione manuale.

---

## 🛠️ Installazione (Linux)

La libreria è progettata per essere installata nel sistema, rendendola disponibile per ogni tuo progetto futuro come una libreria standard.

### Installazione via APT
Se hai configurato il tuo repository locale, puoi installare la libreria in modo nativo:

```bash
# 1. Aggiorna l'indice dei pacchetti
sudo apt install ./libmyssh-package.deb
```
### Per importare la libreria basta che fai
```bash
#include "ssh.h"
```

### Ecco un'esempio sul suo utilizzo

```bash
#include "ssh.h"
#include <iostream>
#include <string>

int main()
{
    std::string ip, username, password;
    int porta = 22;

    std::cout << "=== Connessione Diretta Carcoal ===" << std::endl;
    std::cout << "Inserisci IP del server: ";
    std::cin >> ip;
    std::cout << "Inserisci Username: ";
    std::cin >> username;
    std::cout << "Inserisci Porta [default 22]: ";
    std::cin >> porta;
    std::cout << "Inserisci Password: ";
    std::cin >> password;

    Carcoal client(ip, username, password, porta);

    std::cout << "\nAvvio della sessione SSH in corso..." << std::endl;

    // Si connette e ti lascia dentro la macchina remota
    client.connect();

    std::cout << "\nSei uscito dalla sessione SSH di: " << ip << ". Programma terminato." << std::endl;
    return 0;
}
```


