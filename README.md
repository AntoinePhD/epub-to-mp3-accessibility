# Lecteur EPUB → Audio — Convertisseur de livres en livres audio

**Un outil gratuit et autonome pour transformer n'importe quel fichier EPUB en fichiers MP3 prêts à être écoutés.**

Ce projet a été créé dans un but d'accessibilité : permettre à toute personne, y compris les personnes malvoyantes ou malentendantes, de convertir ses propres livres numériques en format audio pour une écoute confortable.

---

## Ce que fait ce programme

- Vous **sélectionnez un fichier .epub** (un livre numérique)
- Le programme **extrait tous les chapitres** automatiquement
- Il **synthétise la voix** pour chaque chapitre grâce à une technologie de synthèse vocale
- Chaque chapitre est enregistré dans un **fichier MP3 séparé**, numéroté dans l'ordre de lecture
- Les fichiers sont placés dans un dossier créé automatiquement à côté du livre original

Aucune inscription, aucun compte, aucune connexion internet requise (sauf pour la synthèse vocale OpenAI si vous choisissez cette option).

---

## Comment l'utiliser — étape par étape

### Étape 1 : Lancer le programme

Double-cliquez sur `EPUBtoMP3.exe`. Une fenêtre s'ouvre.

> **Note importante** : Ce fichier fonctionne sur **Windows uniquement** (version 10 ou 11 recommandée). Aucune installation préalable n'est nécessaire.

### Étape 2 : Choisir votre livre EPUB

La fenêtre affiche une zone grise qui dit : *« Cliquez pour choisir un fichier EPUB, ou cliquez sur Parcourir ci-dessous »*.

Vous avez deux façons de sélectionner votre livre :

- **Cliquez directement sur la zone grise** — cela ouvre l'explorateur de fichiers Windows
- **Cliquez sur le bouton « Parcourir… »** juste en dessous

Dans l'explorateur, naviguez vers votre fichier `.epub` et sélectionnez-le. Validez avec « Ouvrir ».

> Le programme accepte les fichiers `.epub`. Si votre livre est dans un autre format (PDF, DOCX, TXT…), il faut d'abord le convertir en EPUB avec un autre outil.

Une fois le fichier chargé, la zone grise devient verte et affiche le nom de votre livre. Un dossier de sortie est proposé automatiquement : `{nomdu livre}_mp3`.

Vous pouvez modifier ce dossier en cliquant sur le bouton « Parcourir » à droite de la ligne « Dossier de sortie ».

### Étape 3 : Choisir le moteur de synthèse vocale

Le programme propose deux moteurs dans un menu déroulant en haut :

| Moteur | Commentaires |
|---|---|
| **Edge TTS** (choix par défaut) | Gratuit, fonctionne sans connexion internet après le téléchargement initial des données vocales, voices françaises nombreuses. C'est le moteur recommandé. |
| **OpenAI TTS** | Qualité très élevée, mais nécessite une clé API OpenAI (payant, facturation à la demande). À réserver aux utilisateurs qui disposent déjà d'une clé. |

**Par défaut, le programme utilise Edge TTS.** C'est le choix le plus simple et le plus accessible.

### Étape 4 : Choisir la voix

Dans le menu « Voix », vous trouvez plusieurs voix françaises (et francophones). Les voix disponibles avec Edge TTS sont :

| Voix | Profil | Accent |
|---|---|---|
| Denise | Femme | France |
| Eloise | Femme | France |
| Henri | Homme | France |
| **Vivienne** | **Femme, multilingue** | **France** — voix fluide et naturelle, mais peut parfois détacher un léger accent anglais sur certains mots |
| Remy | Homme, multilingue | France |
| Charline | Femme | Belgique |
| Gérard | Homme | Belgique |
| Antoine | Homme | Canada (Québec) |
| Sylvie | Femme | Canada (Québec) |
| Jean | Homme | Canada (Québec) |
| Thierry | Homme | Canada (Québec) |
| Ariane | Femme | Suisse |
| Fabrice | Homme | Suisse |

> **Conseil pour un rendu entièrement en français** : privilégiez Denise, Eloise, Henri, Charline, Sylvie ou Ariane. Ces voix « monolingues » n'empruntent jamais d'accent anglais. Vivienne est la plus fluide, mais gardez à l'esprit qu'elle peut faire des incursions accentuelles anglaises occasionnelles.

### Étape 5 : Ajuster la vitesse de lecture

La vitesse est réglée avec un curseur numéroté de **−50 %** (très lent) à **+50 %** (très rapide).

La valeur affichée à droite du curseur indique le pourcentage appliqué. Une valeur négative ralentit la lecture ; une valeur positive l'accélère.

- Par défaut, le programme propose **−10 %** (légèrement plus lent que la normale, plus clair à l'écoute, utile pour l'accessibilité)
- Vous pouvez ajuster ce réglage à votre confort. Certaines personnes préfèrent écouter plus vite (+20 %, +30 %) pour parcourir les livres rapidement.
- Le programme applique ce réglage à toutes les voix et à tous les chapitres.

### Étape 6 : (Facultatif) Tester la voix avant de convertir

Avant de lancer la conversion complète d'un long livre, vous pouvez tester la voix choisie sur un petit échantillon :

- Cliquez sur le bouton **« Tester la voix »** en haut à droite
- Le programme génère un court fichier `test_sample.mp3` dans un dossier temporaire et vous indique où le trouver
- Écoutez-le. Si la voix, l'accent et la vitesse vous conviennent, lancez la conversion complète

### Étape 7 : Lancer la conversion

Cliquez sur le bouton **« Convertir en MP3 »** (fleche verte ▶).

Le programme affiche :

- Une barre de progression indiquant le nombre de chapitres convertis
- Un message de progression dans la zone « Journal » en bas
- Le temps écoulé et la taille du fichier en cours

Une fois terminé, le journal affiche :
- Le nombre de chapitres convertis
- La taille totale des fichiers MP3
- Le chemin du dossier de sortie

### Étape 8 : Écouter vos fichiers

Ouvrez le dossier de sortie proposé (clic droit sur le chemin → « Ouvrir le dossier » dans l'explorateur, ou copiez-collez le chemin dans la barre d'adresse de l'explorateur Windows).

Vous trouvez dedans une série de fichiers nommés :
- `1chap_00_Remerciements.mp3`
- `1chap_01_Chapitre 1.mp3`
- `1chap_02_Chapitre 2.mp3`
- …
- `1chap_99_Épilogue.mp3`

Chaque fichier porte le numéro du chapitre pour un tri facile. Vous pouvez les écouter un par un avec n'importe quel lecteur MP3 (windows Media Player, VLC, lecteurs sur mobile, etc.).

---

## Options avancées

### Changer le dossier de sortie

Par défaut, le dossier de sortie se crée à côté du livre (`{nom}_mp3`). Vous pouvez en choisir un autre en cliquant sur le bouton « Parcourir » à droite de la ligne « Dossier de sortie ». Vous pouvez aussi taper directement un chemin dans la zone de texte.

### Annuler une conversion en cours

Si vous changez d'avis en cours de conversion, cliquez sur le bouton **« Annuler »** (carré rouge ■). La conversion s'arrête à la fin du chapitre en cours.

### Utiliser OpenAI TTS

Cette option est réservée aux utilisateurs qui disposent déjà d'une clé API OpenAI.

Pour l'activer :

1. Dans le menu « Moteur », sélectionnez **OpenAI**
2. Cochez la case « J'ai une clé API OpenAI »
3. Collez votre clé dans la zone qui apparaît
4. Choisissez une voix OpenAI (alloy, echo, fable, onyx, nova, shimmer)
5. Lancez la conversion

> **Attention** : OpenAI facture à la demande. Vérifiez votre budget et vos limites avant d'utiliser cette option sur des longs livres.

---

## Conseils pour un résultat optimal

- **Lancez d'abord le test** sur un petit extrait pour vérifier que la voix et la vitesse vous conviennent avant de convertir un long roman.
- **Pour une voix purement française sans accent anglais**, privilégiez Denise, Eloise, Henri, Charline, Sylvie ou Ariane.
- **Pour la fluidité la plus naturelle**, Vivienne est souvent le meilleur choix — mais acceptez les éventuelles petites incursions anglaises.
- **Vous pouvez relancer la conversion plusieurs fois** avec des voix ou des vitesses différentes pour comparer et choisir.
- **Les livres très longs** peuvent prendre du temps. La conversion est parallélisée (plusieurs chapitres en même temps), mais les grands livres demandent plusieurs minutes à quelques dizaines de minutes selon la vitesse de votre ordinateur et la longueur du livre.

---

## Limitations connues

- Le programme ne convertit que les fichiers **EPUB**. Les PDF, DOCX, TXT et autres formats ne sont pas acceptés directement.
- Le découpage en chapitres dépend de la structure interne du fichier EPUB. Certains livres peu structurés peuvent donner des chapitres inégaux ou mal découpés — dans ce cas, essayer une autre voix ou un autre réglage de vitesse ne corrigera pas le problème ; il faut un fichier EPUB mieux structuré.
- **Vivienne**, bien que très fluide, peut parfois prononcer certains mots ou passages avec une intonation ou un accent rappelant l'anglais. C'est inhérent à sa nature multilingue. Pour un rendu 100 % français, utilisez une voix monolingue.
- L'option OpenAI nécessite une connexion internet et une clé API valide. Elle n'est pas gratuite.

---

## Pour les personnes malvoyantes ou malentendantes

Ce programme a été conçu pour être le plus autonome possible :

- **Aucune installation complexe** — un seul fichier exécutable, pas de licence, pas de compte
- **Gratuit et sans publicité** — aucune collecte de données, aucune télémétrie, aucun suivi
- **Interface visuelle simple** — boutons grands et bien espacés, texte lisible
- **Lecture audio native** — le rendu final est des fichiers MP3 standards, compatibles avec tous les lecteurs audio, les balises, les applications de lecture d'écran, etc.
- **Vitesse et voix modulables** — adaptez la lecture à votre rythme et à vos préférences auditives
- **Sortie en fichiers séparés par chapitre** — facile à organiser, à renommer, à naviguer avec un lecteur d'écran ou un répertoire vocal

---

## Informations techniques

- **Plateforme** : Windows 10 / Windows 11 (fichier exécutable unique, aucune installation requise)
- **Moteur principal** : Microsoft Edge TTS (via la bibliothèque `edge-tts`) — voix en locale, sans frais
- **Moteur optionnel** : OpenAI Text-to-Speech (via l'API OpenAI, payant)
- **Bibliothèques utilisées** : `ebooklib` (analyse EPUB), `edge-tts` (synthèse vocale Edge), `tkinter` (interface graphique)
- **Format de sortie** : MP3, un fichier par chapitre, nommés `1chap_NN_*.mp3` pour un tri alphabétique croissant

---

## Comment obtenir des livres EPUB légalement

Ce programme ne fournit pas de livres. Vous devez vous fournir vous-même vos fichiers EPUB.

Voici quelques sources légales de livres numériques gratuits ou accessibles :

- **Project Gutenberg** (gutenberg.org) — œuvres du domaine public, gratuites
- **Liber Liber** (liberliber.it) — textes et eBooks libres en italien et en français
- **Gallica** (gallica.bnf.fr) — patrimoine documentaire français, nombreux textes numérisés et PDF/EPUB accessibles
- **Wikisource** (fr.wikisource.org) — textes libres
- **Bibliothèques locales** — de nombreuses bibliothèques prêtent des eBooks via des applications comme OverDrive, Libby ou EBSCO (vérifiez si votre bibliothèque propose des EPUB compatibles)
- ** achat direct** — acheter un eBook en format EPUB dans le commerce (fnac, amazon Kindle n'utilise pas EPUB natif, mais de nombreux autres libraires en proposent)

> Ce programme est un outil technique. Son utilisation pour convertir des livres protégés par le droit d'auteur sans l'autorisation de l'auteur ou de l'éditeur peut constituer une infraction. Utilisez-le avec des livres dont vous possédez le droit de lire et écouter, ou des livres libres.

---

## Avertissement légal

Ce programme est distribué tel quel, sans garantie d'aucune sorte. Son auteur décline toute responsabilité légale pour tout usage qui pourrait être fait de ce logiciel ou des fichiers produits par son utilisation.

Ce logiciel est destiné à un **usage strictement personnel**. Il est interdit de partager des fichiers audio produits par ce programme sur internet ou par tout autre moyen de diffusion publique si vous ne possédez pas les droits nécessaires sur les livres convertis. La conversion de livres protégés par le droit d'auteur sans l'autorisation de l'auteur ou de l'éditeur peut constituer une infraction. Utilisez ce programme uniquement avec des livres dont vous avez le droit de lire et d'écouter, ou avec des livres libres.

---

