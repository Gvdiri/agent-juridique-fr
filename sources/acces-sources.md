# Accès aux sources officielles — notes pratiques

> Sert à gagner du temps d'une session à l'autre. Aucune donnée juridique ici :
> uniquement la façon d'atteindre les sources.

## Ce qui marche

- **WebFetch** fonctionne sur legifrance.gouv.fr, service-public.fr et eur-lex.europa.eu.
- Il **paraphrase** et refuse les citations longues. Pour un texte exact, demander des
  fragments courts successifs (« cite uniquement la fin de la phrase qui suit … »).

## Ce qui bloque

- **Vérification anti-robot** (« Verify you are human ») sur certains sites publics dans un
  navigateur automatisé. Ne jamais la contourner : revenir à WebFetch ou à une autre source officielle.
- **Certains PDF officiels** ne sont pas lisibles par WebFetch. Chercher d'abord leur
  équivalent HTML, par exemple la publication au Journal officiel sur Légifrance.
