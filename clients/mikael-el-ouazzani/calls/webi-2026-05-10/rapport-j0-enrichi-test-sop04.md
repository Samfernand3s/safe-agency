# Rapport J0 (enrichi SOP 04 — TEST RÉTROACTIF) — Webi du 2026-05-10

> **Statut :** test rétroactif de la SOP 04 sur webi historique.
> Produit le 2026-05-21 par Claude + Sam.
>
> **À J0 originel (2026-05-10/11) :** les calls étaient à venir cette semaine. On reproduit ce qui aurait été le rapport J0 enrichi standard SAFE.
>
> **Note :** ⚠️ TBD = data manquante dans le repo, à fournir par Sam pour test complet.

---

## Alerte

🟡 **Surveiller** — % ICP 48% (médiane 4 derniers webis : 49%), donc ~aligné sur la médiane. Pas d'alerte rouge. Mais à surveiller : volume bookings (21) inférieur aux 2 derniers webis (28 et 26), et **plusieurs leads ont Adset/Crea vides** → signal écosystème UTM (Brique 2).

---

## Résumé

| Métrique | Valeur |
|---|---|
| Total bookings | 21 |
| ICP confirmés (freelance mission/intercontrat + 5+ XP) | 8 (38%) |
| ICP potentiels (freelance actif, XP non renseignée) | 2 (10%) |
| ICP total (confirmés + potentiels) | 10 (**48%**) |
| Non-ICP (CDI / chômage / junior) | 11 (52%) |
| Coût par booking ICP | **⚠️ TBD — nécessite spend Meta du webi** |
| Spend webi 2026-05-10 | **⚠️ TBD** |

---

## Comparaison vs médiane 4 derniers webis

> Médianes calculées sur webis : 2026-03-01, 2026-04-26, 2026-05-10, 2026-05-17.
> (Webi 2026-04-19 absent du repo — à confirmer s'il a eu lieu)

| Métrique | Ce webi (05-10) | Médiane 4 webis | Delta |
|---|---|---|---|
| Total bookings | 21 | 26 | -19% |
| % ICP fit (conf + pot) | 48% | 49% | -1 pt (~aligné) |
| Nb bookings ICP | 10 | ~13 | -23% |
| Coût par booking ICP | ⚠️ TBD | ⚠️ TBD | ⚠️ TBD |

→ **Lecture :** qualité ICP alignée sur la médiane mais **volume bookings en baisse** (-19% leads, -23% bookings ICP). À surveiller — saisonnalité ? Spend en baisse ? Saturation marché ?

---

## Funnel par profil (cf. rapport J0 existant)

| Statut | ICP ✓ | ICP ? | Non-ICP | Total |
|--------|-------|-------|---------|-------|
| Pipeline | 6 | 2 | 8 | 16 |
| No show | 0 | 0 | 1 | 1 |
| KO (setter) | 2 | 0 | 2 | 4 |

---

## Performance par créa (signaux, pas verdicts)

> ⚠️ **Lecture créa SAFE — règle expérimentale** : ces chiffres sont des **signaux**. SAFE opère sous l'hypothèse (à valider en continu) qu'un lead voit plusieurs ads avant conversion → la créa "source" Airtable est last-click, pas vérité de causalité. **Pas de verdict kill sur la perf isolée — on teste par cut+observe.**
>
> En plus : sur ce webi, volumes par créa **très faibles** (1-4 leads par créa) → encore plus de prudence. Croiser avec l'accumulation 4-6 webis.

| Créa | Adset | Leads | ICP+? | % ICP | Signal |
|---|---|---|---|---|---|
| HOOK 4 - VARIANTE 3 - FIN DE MISSION | BROAD / VARIANTE 3 FIN DE MISSION | 4 | 2 | 50% | 🟢 aligné médiane (le plus stat-significatif sur ce webi) |
| NEW CBO / marwa_court_v1 | COLD / NEW BROAD / WINNER | 2 | 1 | 50% | 🟡 volume faible |
| HOOK 4 - VARIANTE 2 - FIN DE MISSION | BROAD / VARIANTE 2 FIN DE MISSION | 2 | 1 | 50% | 🟡 volume faible |
| NEW CBO / H1 - POV - CDI DEGUISÉ | COLD / NEW BROAD / WINNER | 1 | 1 | 100% | ➕ volume trop faible pour conclure |
| H5 - MARCHÉ | BROAD MARCHÉ - +24 ANS | 1 | 1 | 100% | ➕ volume trop faible |
| H4 FP - ANTI ESN | ANTI ESN | 2 | **0** | **0%** | 🟡 signal faible sur ce webi — cohérent avec rôle "distribution only" historique (cf. master-contexte) |
| marwa_court_v1 | BROAD / STUDY CASE | 1 | 0 | 0% | 🟡 volume trop faible |
| H2 - FORMATION JUNIOR ESN | COLD BROAD / FORMATION JUNIOR ESN | 1 | 0 | 0% | 🟡 volume trop faible |
| **(Adset/Crea vides)** | - | 7 | 4 | 57% | ⚠️ **gap écosystème UTM** |

### Créas qui ramènent ICP sur ce webi (signal positif)
1. HOOK 4 - VARIANTE 3 FIN DE MISSION — 50% ICP sur 4 leads (signal le plus solide statistiquement)
2. (Autres créas trop faibles en volume pour conclure isolément)

### Signaux faibles — hypothèses à tester (pas à killer)
- **H4 FP - ANTI ESN** sur ce webi : 0% ICP sur 2 leads. **Hypothèse à tester** : la créa joue-t-elle un rôle structurel top funnel (distribution) malgré son CAQ ICP isolé horrible ? Test possible = cut 7-14j et observer le CAQ ICP global + volume bookings ICP global. ⚠️ **Ne pas cut sans test.**
- (Pas d'autre signal exploitable — volumes trop faibles)

---

## Alerte écosystème UTM

**7 leads sur 21 (33%) ont Adset/Crea vides** dans Airtable. Sur ce volume, 4 sont ICP. C'est un **trou data critique** : on ne sait pas quelle créa les a ramenés, donc on ne peut pas piloter par créa.

→ Ticket Raf (Brique 2 — SOP 01 Écosystème data).

---

## Hypothèses à tester / décisions weekly call (rétro)

- [ ] **Spend Meta** du webi 10 mai à clarifier pour calculer coût par booking ICP
- [ ] **Hypothèse cut+observe** H4 FP - ANTI ESN sur 7-14j ? — tester si la créa nourrit l'écosystème top funnel malgré son signal isolé faible
- [ ] Volume bookings en baisse (21 vs médiane 26) — saisonnalité ou autre ? (Pas de décision rapide)
- [ ] Gap UTM 33% leads — priorité Raf (Brique 2)
- [ ] **Hypothèse** : pousser plus de volume sur Variante 3 Fin de Mission (4 leads, 50% ICP) puisque c'est l'angle qui ramène le persona dominant — test par augmentation budget sur 1-2 webis et observer CAQ ICP global

---

## Articulation avec la synthèse J+14 (SOP 02)

> Bookings ICP à suivre à J+14 (= 2026-05-24) :

| Lead | Profil | Créa | Statut J0 | Statut attendu J+14 |
|---|---|---|---|---|
| Conrad TAYLOR | Freelance en mission, 8 XP | HOOK 4 - V3 FIN DE MISSION | À qualifier | ? |
| Hamza Bourakadi | Freelance en mission, 8 XP | NEW CBO / marwa_court_v1 | **Hot list 🔥** | ? |
| Daniel Nedjar | Freelance intercontrat, 8 XP | HOOK 4 - V3 FIN DE MISSION | Pré-call demandé | ? |
| Souhaiel Bousselmi | Freelance en mission, 8 XP | H5 - MARCHÉ | Pré-call demandé | ? |
| Raphaël Masson | Freelance intercontrat, 8 XP | (vide) | À qualifier | ? |
| Abdelrahman Lemmouchi | Freelance en mission, 8 XP | (vide) | À qualifier | ? |

→ Hypothèses à valider à J+14 :
- Les Variante 3 Fin de Mission convertissent-elles en close ?
- Marwa court v1 confirme-t-il son CAC 406€ historique (cf. master-contexte) ?
- Les leads "Hot list 🔥" closent-ils effectivement ?

---

## Gaps identifiés pour test complet SOP 04

Pour produire un rapport J0 enrichi 100% conforme à la SOP 04, il manque :

1. **Spend Meta du webi 2026-05-10** (total + par adset/créa)
2. **Spend Meta des 3 autres webis historiques** (pour calculer médiane coût par booking ICP)
3. **Confirmation que le webi 2026-04-19 a eu lieu** (absent du repo)

Sam : peux-tu m'extraire ces 2 chiffres ? Sinon les médianes que tu utilises mentalement / habituellement.

*Test rétroactif SOP 04 — produit le 2026-05-21*
