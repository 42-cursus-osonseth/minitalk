# 📡 minitalk

Communication entre deux programmes via signaux Unix.  
Envoi de messages caractère par caractère entre un client et un serveur.

---

## 🧠 Objectif

Créer deux programmes en **C** capables de **communiquer via signaux Unix (`SIGUSR1`, `SIGUSR2`)**, sans utiliser de sockets ni de fichiers, en encodant chaque caractère bit par bit.

---

## ⚙️ Fonctionnement

- Le **serveur** affiche son PID au lancement et attend des messages.
- Le **client** envoie une chaîne de caractères au serveur, **bit par bit**, en utilisant les signaux :
  - `SIGUSR1` pour un bit à `1`
  - `SIGUSR2` pour un bit à `0`
- Le serveur reconstitue les caractères reçus et les affiche à l’écran.

---

## ✨ Bonus réalisés

- **Accusé de réception** : le client attend une confirmation du serveur avant d’envoyer le bit suivant.
- **Support des caractères Unicode** (UTF-8) : gestion correcte des caractères multioctets.

---

## 🚀 Utilisation

### 1. Compilation

```bash
make
