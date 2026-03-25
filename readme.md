# CSetting 

Librairy qui simplifie la gestion des fichier .ini pour un logiciel C++ developper avec le frawork QT 

## Methode 

### `CSetting()`
Constructeur de base. Crée un objet CSetting sans initialiser de fichier de paramètres.

### `CSetting(const QString &namesoft)`
Constructeur qui prend le nom du logiciel en paramètre. Il initialise le fichier de paramètres dans le dossier de configuration approprié en fonction de l'OS (`.config` sur Linux/Mac, `AppData` sur Windows).

- **namesoft**: Le nom de votre logiciel.

### `getFileCreated() const`
Retourne un booléen qui indique si un nouveau fichier de configuration a été créé.

- **Retourne**: `true` si un nouveau fichier a été créé, `false` sinon.

### `setValeur(const QString &section, const QString &key, const QString &value)`
Définit une valeur dans le fichier de paramètres.

- **section**: La section dans laquelle la valeur sera stockée.
- **key**: La clé pour la valeur.
- **value**: La valeur à stocker.
- **Retourne**: `true` si la valeur a été définie avec succès, `false` sinon.

### `getValeur(const QString &section, const QString &key) const`
Récupère une valeur depuis le fichier de paramètres.

- **section**: La section de la valeur.
- **key**: La clé de la valeur.
- **Retourne**: La valeur sous forme de `QString`. Si la valeur n'est pas trouvée, retourne "error".

### `supprValeur(const QString &section, const QString &key)`
Supprime une valeur du fichier de paramètres.

- **section**: La section de la valeur.
- **key**: La clé de la valeur à supprimer.
- **Retourne**: `true` si la valeur a été supprimée avec succès, `false` sinon.
