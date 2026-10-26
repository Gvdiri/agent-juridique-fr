# Agent IA de recherche juridique — droit administratif français

Un agent IA qui répond aux questions de droit et de démarches administratives en France,
construit sur **Claude Code**.

Le problème qu'il règle : un assistant IA classique répond avec assurance, même quand il se trompe.
En droit, un numéro d'article inventé ressemble exactement à un vrai. Cet agent est construit pour
**ne jamais affirmer une règle qu'il n'a pas vérifiée sur une source officielle**.

## Comment il travaille

1. **Aucune règle de mémoire.** Chaque article, délai ou montant vient d'une recherche sur Légifrance,
   service-public.fr ou le site officiel de l'administration concernée, avec l'URL et la date.
2. **Chaque affirmation porte un niveau de preuve** : `[CONFIRMÉ]`, `[SECONDAIRE]`, `[DIVERGENT]` ou
   `[NON VÉRIFIÉ]`. Une source secondaire ne fonde jamais une décision irréversible.
3. **Un ordre de raisonnement fixe** : reformuler la question, trouver le texte en vigueur, le croiser
   avec la fiche officielle, lister conditions, pièces et délais, puis décrire la démarche.
4. **Une réponse qui sert à agir** : ce qui peut faire échouer la démarche, une autocritique
   (ce qui n'a pas pu être vérifié), puis les actions dans l'ordre.
5. **Une mémoire de travail** : la base de connaissances est mise à jour à chaque vérification et
   revérifiée au-delà de 30 jours ; chaque décision est consignée avec ce qui l'invaliderait.

## Structure

```
CLAUDE.md                  le rôle, les règles et le protocole de l'agent
connaissances/
  00-INDEX.md              index, convention de marquage, règle de fraîcheur
  01-profil.md             la situation de l'utilisateur, remplie par entretien
decisions/JOURNAL.md       une entrée par décision : options, choix, sources, ce qui l'invaliderait
sources/acces-sources.md   comment atteindre les sources officielles, et ce qui bloque
```

## Utilisation

```bash
cd agent-juridique-fr
claude
```

Puis pose ta question, par exemple : *« Quelles pièces faut-il pour refaire une carte d'identité,
et quel est le délai ? »*

## Limites

L'agent recherche, source et explique. Il ne dépose rien et ne signe rien. Ce n'est pas un conseil juridique.

---

Conçu par **Gadiri Bah**, étudiant ingénieur à Junia ISEN Lille.
