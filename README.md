# Site GéoConsulting — prototype

Maquette fonctionnelle en HTML, CSS et JavaScript, sans framework, à valider par la
direction avant le développement de la version PHP/MySQL.

**Aucun sous-dossier** : tous les fichiers sont au même niveau, le CSS et le
JavaScript sont intégrés dans chaque page. C'est voulu — le glisser-déposer de
dossiers vers GitHub échoue sur certains navigateurs.

## Mettre en ligne

1. Décompresser l'archive. Une quarantaine de fichiers, aucun dossier.
2. Sur GitHub, dans le dépôt : **Add file → Upload files**, **Ctrl + A** dans le
   dossier décompressé, glisser la sélection, **Commit changes**.
3. Vérifier que `.nojekyll` est bien parti. Sinon : **Add file → Create new file**,
   nom exact `.nojekyll`, contenu vide, Commit.
4. Settings → Pages → `Deploy from a branch`, branche `main`, dossier `/ (root)`.
5. Deux minutes, puis **Ctrl + Maj + R** sur le site.

Supprimer d'abord `_config.yml` s'il est présent à la racine du dépôt : c'est lui
qui fait apparaître le thème GitHub à la place du style du site.

## Les pages

| Fichier | Contenu |
|---|---|
| `index.html` | Accueil : bandeau, chiffres, mot du directeur, métiers, prestations, sols, laboratoire, galerie, actualités, références, partenaires, certifications |
| `le-bureau.html` | Identité, vision, organisation, valeurs, démarche qualité |
| `nos-metiers.html` | Sols et géotechnique, routes, hydraulique, bâtiment, environnement |
| `laboratoire.html` | Essais, référentiels, équipements |
| `references.html` | Références filtrables par secteur |
| `galerie.html` | Galerie complète avec agrandissement au clic |
| `actualites.html` | Fil d'actualité |
| `devis.html` | Demande de devis en quatre étapes |
| `moyens.html` | Topographie, reconnaissance des sols, plateau numérique |
| `carriere.html` | Profils recherchés, stages, candidature spontanée |
| `contact.html` | Coordonnées, WhatsApp et formulaire |
| `admin.html` | Administration de démonstration, identifiant `admin`, mot de passe `admin` |

## WhatsApp

Le numéro utilisé est le **+227 82 24 24 26**. Il apparaît à trois endroits : le
bouton vert flottant présent sur toutes les pages, le pied de page, et la page
contact. Le lien ouvre directement la conversation avec un message pré-rempli,
via `https://wa.me/22782242426`.

Pour changer le numéro, cherchez `whatsapp: "22782242426"` dans n'importe quel
fichier HTML — il faut le modifier dans toutes les pages, c'est la contrepartie de
la version sans dossiers. La version PHP le lira dans la table `parametres`.

## Les images

**Intégrées** : les trois badges ISO et les trois certificats de registration, les
douze logos de partenaires en couleur, et treize photos de chantier, d'ouvrages et
de laboratoire.

### Noms de fichiers corrigés

Les ingénieurs ont relevé que des photos portaient un nom sans rapport avec leur
contenu. Les fichiers ont été renommés d'après ce qu'ils montrent réellement, et
chaque légende a été réécrite en conséquence :

| Ancien nom | Ce que la photo montre | Nouveau nom |
|---|---|---|
| `equipement-balance` | Scléromètre dans son coffret | `equipement-sclerometre` |
| `equipement-sclerometre` | Presse de compression Controlab et éprouvettes | `equipement-presse-beton` |
| `equipement-presse-beton` | Bâti d'essai à anneau dynamométrique | `equipement-bati-cbr` |
| `equipement-bati-cbr` | Presse CBR (socle « CBR Tester ») | `equipement-presse-cbr` |
| `equipement-presse-cbr` | Malaxeur de laboratoire | `equipement-malaxeur` |
| `equipement-malaxeur` | Balance de précision et comparateur | `equipement-balance` |
| `equipement-penetrometre` | Étuve ventilée | `equipement-etuve` |
| `equipement-etuve` | Agitateur mécanique | `equipement-agitateur` |
| `ouvrage-chaussee` | Gisement de latérite | `materiau-laterite` |
| `ouvrage-salles-classe` | Bâtiment en cours de construction | `ouvrage-batiment-construction` |

**À faire valider par le chef du département laboratoire** : certains appareils ont
été identifiés d'après la photo seule. Si une désignation est encore imprécise,
corrigez la légende dans `GALERIE` et le texte alternatif dans les pages.

**Retirées à la demande** : la photo de prospection géophysique et celle du bâtiment
à portes métalliques rouges.

**Encore à fournir** — il suffit de déposer le fichier à la racine du dépôt, il
remplace automatiquement l'emplacement réservé :

| Fichier | Où il apparaît |
|---|---|
| `siege.jpg` | Photo du bâtiment, page Le bureau |

Le mot du directeur général est présenté sans portrait, à sa demande : la citation
occupe tout le bloc, avec son nom et sa fonction dans la colonne de gauche.

### Logos à remplacer quand vous aurez mieux

| Fichier | Problème |
|---|---|
| `logo-ministere-equipement.png` | Le logo fourni était celui du **Royaume du Maroc**. Ce sont les armoiries du Niger qui sont affichées à la place. À remplacer par le logo officiel du ministère nigérien. |
| `logo-pnud.png` | Image tronquée, on ne lit que « P N ». |
| `logo-amoder.png` | Extrait de bannière avec du texte, pas un logo propre. |
| `logo-bad.png` | Basse définition. |

Ces logos sont des marques déposées : récupérez-les sur les pages « identité
visuelle » des sites officiels et demandez l'accord des maîtres d'ouvrage concernés.

## Choix de conception

- **Fond sombre.** Bleu nuit profond, halos verts et bleus diffus, surfaces en verre
  dépoli. Les logos partenaires sont affichés en couleur sur pastilles blanches.
- **Photos.** Aucune personne identifiable, y compris après recadrage des originaux.
- **Données.** Ni montants, ni numéros de marché, ni noms d'experts affectés, ni
  immatriculations. Ces informations ne figurent pas non plus dans le schéma de base.
- **Textes officiels.** Le titre d'accueil reprend le slogan de l'entreprise. La
  vision et la mission de la page Le bureau sont les textes exacts de la politique
  QSE, repris mot pour mot. La section « Notre système de management QSE » précède
  les certifications sur l'accueil et reprend les trois engagements de l'affiche.
- **Mouvement.** Barre de progression de lecture, apparition des sections au
  défilement, compteurs animés, bandeau de logos défilant, cadrage lent de l'image
  d'ouverture. Tout se désactive si le visiteur a réglé son système sur « moins
  d'animations ».
- **Galerie.** Mosaïque à tailles inégales, agrandissement au clic ou au clavier,
  fermeture par Échap.

## À valider avant mise en ligne

- **Le mot du directeur général**, rédigé à partir de la présentation de l'entreprise :
  il doit être relu, corrigé et validé par l'intéressé avant publication.
- **Les désignations des appareils de laboratoire**, à confirmer par le département
  laboratoire (voir le tableau des noms de fichiers plus haut).
- **Les six actualités**, écrites à partir de faits vérifiés dans vos documents mais
  qui restent des exemples de mise en forme.
- **Le contenu de la page Carrière**, à relire par les ressources humaines.
- Le chiffre de 300 projets affiché sur l'accueil.
- Les mentions légales, à rédiger : RCCM, NIF, forme juridique, directeur de publication.
- Les coordonnées GPS du siège pour la carte de la page contact.
- Le logo en vectoriel, le fichier actuel étant un JPEG de 584 px dont le mot
  « durable » est coupé.

## Espace d'administration

`admin.html`, identifiant `admin`, mot de passe `admin`, pré-remplis. Rien n'est
enregistré : tout revient à l'état initial au rechargement.

Ces identifiants sont en clair dans le fichier. Sans conséquence ici, aucune donnée
n'est derrière. En PHP il faudra `password_hash()` et `password_verify()`, une
session serveur vérifiée sur chaque page, un jeton CSRF sur les formulaires, PDO en
requêtes préparées, une limitation des tentatives de connexion et un `.htaccess` sur
le dossier d'administration.

## La base de données

`geoconsulting.sql` contient le schéma complet, y compris les tables `actualites`
et `demandes_devis` qui recevront le fil d'actualité et les demandes du formulaire.

## Modifier le contenu

Cliquer sur le fichier dans le dépôt, icône crayon, modifier, Commit changes.

Les listes de contenu sont en tête du script de chaque page : `REFERENCES` pour les
missions, `ACTUALITES` pour le fil, `GALERIE` pour les images, `PARTENAIRES` pour les
logos. Comme le script est intégré dans chaque page, une même liste figure dans
plusieurs fichiers — c'est la contrepartie de la version sans dossiers. La version
PHP réglera ce point avec une seule source en base de données.
