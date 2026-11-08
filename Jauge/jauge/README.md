# La jauge

Un mod pour Claude Code. Une bande fine au-dessus de ton message montre ce qui te reste sur tes limites de 5 heures et de 7 jours, le remplissage de ta discussion, l'état du cache (CHAUD ou FROID) et le coût estimé du prochain message.

Avec un abonnement, elle garde aussi ton cache chaud : pour une discussion de plus de 50 000 tokens, elle le relance 55 minutes après ta dernière requête, tant que c'est moins cher que de le laisser refroidir.

## Installer

Il te faut Claude Code 2.1.287 ou plus récent (terminal ou app de bureau).

1. Range ce dossier à un endroit où il restera, par exemple `~/mods/jauge`.
2. `claude plugin marketplace add ~/mods/jauge`
3. `claude plugin install jauge@aios-mods`
4. Ouvre une nouvelle session, ou tape `/reload-plugins`.

Sous Windows, dans PowerShell : `claude plugin marketplace add "$HOME\mods\jauge"`, puis la même commande d'installation. La jauge a été testée sur Mac.

Essayer sans installer : `claude --plugin-dir ~/mods/jauge`.
Vérifier le dossier : `claude plugin validate ~/mods/jauge`.
Mettre en pause ou retirer : `/plugin` dans Claude Code.

## Bon à savoir

- L'état du cache est une estimation : Claude Code ne le donne pas aux mods. Chaud pendant 1 heure avec un abonnement, 5 minutes avec une clé API.
- Le coût du prochain message est un plancher, au tarif public de l'API : la relecture de la discussion seulement.
- Une relance est un vrai appel au modèle : elle prend un peu de ta limite.
- La relance ne part que si Claude Code reste ouvert et l'ordinateur éveillé : la jauge vit dans ta session.
- Une donnée absente s'affiche « — ».

Le guide complet est dans ton espace ressources sur thomrichard.com.

Thomas Richard. Idée reprise de Ribbon, le mod de Jay E (github.com/robonuggets/ribbon, licence MIT).
