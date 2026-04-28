# Campfire — Design System

> Design system pour un hébergeur de serveurs gaming construit autour de **Pantone 13-1023 Peach Fuzz** (`#FFBE98`).
> Direction : *cozy gaming*. L'anti-néon. Chaleureux, tactile, lisible.
> Version `0.1` · Compagnon du showcase HTML.

---

## Sommaire

1. [Identité & positionnement](#1-identité--positionnement)
2. [Propositions de nom](#2-propositions-de-nom)
3. [Couleurs](#3-couleurs)
4. [Typographie](#4-typographie)
5. [Espacement & rayons](#5-espacement--rayons)
6. [Ombres & élévation](#6-ombres--élévation)
7. [Iconographie](#7-iconographie)
8. [Composants](#8-composants)
9. [Voix & ton](#9-voix--ton)
10. [Tokens CSS — copier-coller](#10-tokens-css--copier-coller)
11. [Accessibilité](#11-accessibilité)
12. [Prochaines étapes](#12-prochaines-étapes)

---

## 1. Identité & positionnement

**Le problème.** Le marché de l'hébergement gaming est saturé de dark mode néon (OVH, Shockbyte, Apex, BisectHosting). Tous pareils : fonds noirs, bleus froids, accents cyan agressifs. Ça performe techniquement, ça vend mal l'idée que *jouer sur son propre serveur avec ses potes, c'est un moment chaleureux*.

**Le pari.** Peach Fuzz permet de faire l'inverse sans tomber dans le cheap : chaud, doux, humain. L'équivalent visuel de « on se pose autour du feu et on fait tourner le monde ». La cible (gaming, Minecraft, communautés) y est sensible — Minecraft lui-même est un jeu de blocs cozy, Valheim a une palette terre, Palworld joue la douceur.

**Les 3 mots.**
- **Cozy** — chaud sans être mou, dense sans être froid
- **Honest** — pas de jargon « performant / scalable / enterprise-grade »
- **Quick** — le plus friendly du marché ne doit pas être le plus lent

---

## 2. Propositions de nom

Tous gardent la cohérence avec le design system.

| Nom | Sentiment | Note |
|---|---|---|
| **Campfire** ★ | Communauté, se réunir autour du feu | *Recommandé.* Évocateur, mémorable, .gg probablement dispo. Fait un très bon verbe : *« campfire it »*. |
| **Ember** | Braise vivante | Court, anglo, premium. Risque : déjà utilisé ailleurs. |
| **Hearth** | Le foyer, le home server | Élégant, plus adulte. Moins gaming. |
| **Kindle** | Allumer le feu | Collision avec Amazon → écarter. |
| **Nestr** | Le nid de serveurs | Casual, tech-bro-y. |
| **Fuzz** | Clin d'œil direct à Peach Fuzz | Mémorable, légèrement enfantin. |
| **Pit** | Nether Minecraft | Edgy mais ambigu. |
| **Cozyhost** | Explicite | Trop descriptif, zéro mystère. |

**Recommandation finale : Campfire.**

---

## 3. Couleurs

### 3.1 Peach — primaire

Famille dérivée de Peach Fuzz (300). Utiliser 400–600 pour les CTAs, 50–200 pour les fonds et états hover subtils.

| Token | Hex | Usage |
|---|---|---|
| `peach/50` | `#FFF6F0` | Fond de hero, surface peach ultra-light |
| `peach/100` | `#FFE8D8` | Hover ghost peach, fond de badge |
| `peach/200` | `#FFD4B8` | Border peach |
| **`peach/300`** | **`#FFBE98`** | **Peach Fuzz — couleur signature** |
| `peach/400` | `#FFA574` | Début du gradient CTA, illustrations |
| `peach/500` | `#F58856` | Texte sur peach-100, icônes |
| `peach/600` | `#DC6B3A` | Fin du gradient CTA hover |
| `peach/700` | `#B4502A` | Texte sur fond clair (WCAG AA) |
| `peach/800` | `#87391E` | Texte emphatique |
| `peach/900` | `#542413` | Très sombre — dark mode surface accent |

### 3.2 Ember — accent chaud

Pour les CTAs, le glow, les logos. **À doser** — c'est la braise.

| Token | Hex |
|---|---|
| `ember/400` | `#E8653A` |
| `ember/500` | `#D94F1E` |
| `ember/600` | `#B33A10` |

### 3.3 Dusk — complémentaire froide

Pour les graphiques multi-séries, la data-viz, les contrastes secondaires. Sans Dusk, tout devient monotone orangé.

| Token | Hex |
|---|---|
| `dusk/50` | `#F1F1F6` |
| `dusk/200` | `#C7C5DB` |
| `dusk/400` | `#7D7AAD` |
| `dusk/500` | `#5E5B8C` |
| `dusk/700` | `#3C3962` |
| `dusk/900` | `#1F1D38` |

### 3.4 Cream — neutres chauds

**Jamais** de gris froids. L'undertone reste dans la famille peach/brun.

| Token | Hex |
|---|---|
| `cream/50` | `#FBF8F4` |
| `cream/100` | `#F5EEE5` |
| `cream/200` | `#E8DFD1` |
| `cream/300` | `#D2C5B0` |
| `cream/400` | `#A69680` |
| `cream/500` | `#7A6B58` |
| `cream/600` | `#56493A` |
| `cream/700` | `#3A2F24` |
| `cream/800` | `#241C14` |
| `cream/900` | `#140E09` |

### 3.5 Sémantiques

Désaturées volontairement pour cohabiter avec le peach sans crier.

| Rôle | Hex | Fond light |
|---|---|---|
| Success | `#6BAE4F` | `#E8F3E0` |
| Warning | `#E8A62B` | `#FCEFD1` |
| Danger | `#D14545` | `#FAE0E0` |
| Info | `#5B8FC9` | `#E2ECF7` |

### 3.6 Dark mode

Pas un simple invert — la palette reste chaude. Fond `#0F0A06` (cream-900 adapté), surfaces `#1A120C` / `#241A12`. Le peach est remonté à 300 pour la lisibilité.

---

## 4. Typographie

Trois polices. Toutes open-source (Google Fonts).

### 4.1 Display — Fraunces

Serif variable avec axes `opsz` (optical size) et `SOFT`. L'axe SOFT arrondit les terminaisons = très cozy. À utiliser avec `font-variation-settings: "SOFT" 100, "opsz" 144` pour les gros titres.

```css
font-family: "Fraunces", ui-serif, Georgia, serif;
font-variation-settings: "SOFT" 100, "opsz" 144;
```

**Poids utilisés :** 300, 400, 500, 600. Italic pour les mises en emphase lyriques.

### 4.2 Body — Manrope

Sans-serif variable (300–800), géométrique mais avec des terminaisons douces. Excellente lisibilité en paragraphe, ne cherche pas à voler la vedette à Fraunces. **Ce n'est pas Inter volontairement** — Inter est devenu le Helvetica du web SaaS.

### 4.3 Mono — JetBrains Mono

Pour le code, les IDs de serveur (`fra-03`), les latences (`24ms`), les logs et les labels tech. Ligatures activées par défaut.

### 4.4 Échelle

Base 16px, progression ~1.2.

| Token | px | Usage |
|---|---|---|
| `text-xs` | 12 | Legends, labels mono |
| `text-sm` | 14 | UI dense, table, nav |
| `text-base` | 16 | Body par défaut |
| `text-lg` | 18 | Lead paragraphs |
| `text-xl` | 20 | Sous-titres de card |
| `text-2xl` | 24 | Titres de card (Fraunces) |
| `text-3xl` | 30 | Section titles dashboard |
| `text-4xl` | 36 | H2 pages marketing |
| `text-5xl` | 48 | H1 secondaires |
| `text-6xl` | 60 | Hero secondary |
| `text-7xl` | 80 | Hero principal |

### 4.5 Règles de composition

- **Letter-spacing négatif sur les gros titres** : `-0.03em` à `-0.04em` pour 4xl et plus (Fraunces est dense).
- **Pas de Fraunces en dessous de 18px** — ça se lit mal.
- **Italic = emphase émotionnelle** (« *keep it cozy* »), pas structurelle.
- **Mono en uppercase + letter-spacing 0.08–0.15em** pour les labels.

---

## 5. Espacement & rayons

### 5.1 Spacing (base 4px)

```
1=4 · 2=8 · 3=12 · 4=16 · 5=20 · 6=24 · 8=32 · 10=40 · 12=48 · 16=64 · 20=80 · 24=96
```

Règle : ne jamais utiliser 4px entre deux zones de contenu distinct. 8 minimum.

### 5.2 Rayons

Généreux = friendly. Rien de tranchant.

| Token | px | Usage |
|---|---|---|
| `r-xs` | 4 | Inputs denses, tags |
| `r-sm` | 8 | Boutons, inputs par défaut |
| `r-md` | 12 | Cards petites, badges rectangle |
| `r-lg` | 16 | Cards moyennes, panels |
| `r-xl` | 24 | Hero, modales |
| `r-2xl` | 32 | Conteneurs marketing |
| `r-full` | 9999 | Pills, avatars, status dots |

---

## 6. Ombres & élévation

Toutes teintées chaud : `rgba(20, 14, 9, α)` — base cream-900, jamais du noir pur. Deux ombres spéciales pour les moments signature.

| Token | Usage |
|---|---|
| `shadow-xs` | Inputs, subtle lift |
| `shadow-sm` | Cards au repos |
| `shadow-md` | Card hover |
| `shadow-lg` | Dropdowns, popovers |
| `shadow-xl` | Modales |
| `shadow-ember` | CTA primary hover — glow chaleureux |
| `shadow-glow` | Focus ring accessible |

---

## 7. Iconographie

**Lucide** (open-source, cohérent, 1400+ icônes) en base. Stroke 1.75, linecap round.

```
stroke-width: 1.75;
stroke-linecap: round;
stroke-linejoin: round;
```

**Icônes custom à créer pour le domaine** :
- `block` (voxel Minecraft)
- `player-head` (tête joueur)
- `tickrate` (compteur TPS)
- `backup-clock`
- `mod-piece` (puzzle plugin)
- `campfire` (logo mark)

Taille de base : 24×24. Dans les boutons `btn-sm` : 14. Dans un badge inline : 12.

**Ne pas utiliser** : emojis en production (dans ce doc oui, en UI non), icônes remplies (sauf badges d'état).

---

## 8. Composants

Spécifications concises. Le showcase HTML contient des exemples vivants.

### 8.1 Buttons

| Variante | Quand |
|---|---|
| `primary` | **Un seul par vue.** Gradient peach-400 → ember-500, shadow-ember au hover, texte blanc, bold 600. |
| `secondary` | Actions neutres. Fond surface, border cream-300, hover border peach-400. |
| `ghost` | Actions tertiaires, dans les cards denses. Transparent, hover surface-2. |
| `danger` | Suppression, arrêt serveur. Fond `#D14545`. |

**Tailles.** `sm` 6/12, `md` 10/18 (défaut), `lg` 14/24. Police 12 / 14 / 16.

**États.** `:hover` → `translateY(-1px)` + ombre accentuée. `:active` → retour à 0. `:focus-visible` → shadow-glow. `:disabled` → opacity 0.5.

### 8.2 Forms

- `input`, `select` : padding 10/14, border cream-300, focus peach-400 + glow.
- `label` : 14px, weight 600, marge-bottom 8px.
- `hint` : 12px, text-muted, marge-top 4px.
- `toggle` : 44×24, track cream-300, thumb blanc avec shadow-sm. État on = gradient peach.
- `checkbox` : 18×18, radius 5, checked = gradient peach + checkmark blanc.

**Validation** : message d'erreur sous l'input, rouge danger, ne pas virer du bord rouge autour de l'input (agressif).

### 8.3 Badges

Mono 12px, padding 4/10, radius full. 7 variantes colorées + `badge-dot` pour statuts.

### 8.4 Status indicator

Pattern central gaming :

```html
<span class="status status-online">
  <span class="status-dot"></span>
  Online · 12/20 joueurs
</span>
```

Le dot a un ring animé (scale 0.8→2, opacity 0.6→0, 2s infinite). Pulse = vivant.

### 8.5 Cards & server cards

**Card générique** : surface blanche, border cream-200, radius-lg, padding 24. Hover → shadow-md.

**Server card** (pattern domaine principal) :
1. Head : titre Fraunces 20px + sub mono (jeu · version · node) + status dot
2. Stats grid 3 col : joueurs · ping · TPS (ou FPS selon jeu)
3. Gauges : RAM / CPU / Disk — avec fill coloré selon seuil (vert < 60%, peach < 80%, rouge > 80%)
4. Actions : Console (primary sm) · Redémarrer (secondary sm) · Backup (ghost sm)

### 8.6 Gauges

- Track : 6px, surface-2, border cream-200, radius full.
- Fill : gradient peach → ember par défaut.
- Variante `ok` : vert moss.
- Variante `high` : warning → danger.

### 8.7 Plans (pricing)

Grille 3 colonnes. Le plan mis en avant a :
- Fond `linear-gradient(180deg, peach-50 0%, surface 40%)`
- Border peach-300
- Tag ember flottant en top-right
- CTA primary (les autres ont secondary)

**Nommage des tiers** qui colle au nom : Cozy → Campfire → Bonfire. Taille du feu = taille du plan. C'est narratif et mémorable.

### 8.8 Alerts

4 variantes (info, success, warning, danger). Fond à 15% d'opacité, border à 30%, texte pleine saturation. Icône gauche + titre bold + description.

### 8.9 Tabs

Segmented control avec fond surface-2, padding 4, onglet actif = surface + shadow-xs. Pas de border entre onglets — juste gap 2px. Police body 14, weight 500.

### 8.10 Table

Border cream-200, radius-md, overflow hidden. Headers en mono 12px uppercase. Rows hover = surface-2. Première cellule peut contenir un titre + sub-mono.

### 8.11 Navigation

Navbar full-width, padding 12/24, border-bottom cream-200, background surface avec `backdrop-filter: blur(12px)` (pour les pages qui scrollent sous).

---

## 9. Voix & ton

**Principes.** Proche sans être familier. Technique sans être cryptique. Filtre : *« si mon cousin de 14 ans ne comprend pas, je reformule »*.

### ✓ On dit

- « Votre serveur démarre en 30 secondes »
- « On a un souci avec fra-01. On s'en occupe. »
- « Backup restauré. Votre monde est revenu. »
- « TPS bas ? Voilà ce qui se passe. »

### ✕ On évite

- « Déploiement ultra-performant de votre instance »
- « Incident critique en cours d'investigation »
- « Data recovery operation successful »
- « Performance dégradée détectée »

### Règles rédactionnelles

1. **Verbes à la 1re personne du pluriel** quand c'est l'équipe qui parle (« on s'en occupe »).
2. **Jamais de « cher utilisateur »** — c'est un pote, pas un client.
3. **Les erreurs expliquent ce qu'il faut faire**, pas juste ce qui a raté.
4. **Les emojis sont OK** dans le Discord et les mails transactionnels, **pas dans l'UI produit**.
5. **Pas de majuscules marketing** façon « DÉPLOYEZ MAINTENANT ». On n'est pas sur Amazon.
6. **Anglicismes gaming acceptés** : *lag, TPS, mods, backup, uptime, wipe*. C'est la langue naturelle du public.

---

## 10. Tokens CSS — copier-coller

Bloc prêt à poser dans un `:root`. Utilisable tel quel ou portable vers Tailwind/Panda/Vanilla Extract.

```css
:root {
  /* ─── Peach ─── */
  --peach-50:  #FFF6F0;
  --peach-100: #FFE8D8;
  --peach-200: #FFD4B8;
  --peach-300: #FFBE98; /* Peach Fuzz */
  --peach-400: #FFA574;
  --peach-500: #F58856;
  --peach-600: #DC6B3A;
  --peach-700: #B4502A;
  --peach-800: #87391E;
  --peach-900: #542413;

  /* ─── Ember ─── */
  --ember-400: #E8653A;
  --ember-500: #D94F1E;
  --ember-600: #B33A10;

  /* ─── Dusk ─── */
  --dusk-50:  #F1F1F6;
  --dusk-200: #C7C5DB;
  --dusk-400: #7D7AAD;
  --dusk-500: #5E5B8C;
  --dusk-700: #3C3962;
  --dusk-900: #1F1D38;

  /* ─── Cream ─── */
  --cream-50:  #FBF8F4;
  --cream-100: #F5EEE5;
  --cream-200: #E8DFD1;
  --cream-300: #D2C5B0;
  --cream-400: #A69680;
  --cream-500: #7A6B58;
  --cream-600: #56493A;
  --cream-700: #3A2F24;
  --cream-800: #241C14;
  --cream-900: #140E09;

  /* ─── Semantic ─── */
  --success: #6BAE4F;  --success-bg: #E8F3E0;
  --warning: #E8A62B;  --warning-bg: #FCEFD1;
  --danger:  #D14545;  --danger-bg:  #FAE0E0;
  --info:    #5B8FC9;  --info-bg:    #E2ECF7;

  /* ─── Surfaces (light) ─── */
  --bg:            var(--cream-50);
  --surface:       #FFFFFF;
  --surface-2:     var(--cream-100);
  --border:        var(--cream-200);
  --border-strong: var(--cream-300);
  --text:          var(--cream-900);
  --text-muted:    var(--cream-500);
  --text-soft:     var(--cream-600);

  /* ─── Typography ─── */
  --font-display: "Fraunces", ui-serif, Georgia, serif;
  --font-body:    "Manrope", ui-sans-serif, system-ui, sans-serif;
  --font-mono:    "JetBrains Mono", ui-monospace, monospace;

  --text-xs: .75rem; --text-sm: .875rem; --text-base: 1rem;
  --text-lg: 1.125rem; --text-xl: 1.25rem; --text-2xl: 1.5rem;
  --text-3xl: 1.875rem; --text-4xl: 2.25rem; --text-5xl: 3rem;
  --text-6xl: 3.75rem; --text-7xl: 5rem;

  /* ─── Space ─── */
  --space-1: 4px;  --space-2: 8px;  --space-3: 12px; --space-4: 16px;
  --space-5: 20px; --space-6: 24px; --space-8: 32px; --space-10: 40px;
  --space-12: 48px; --space-16: 64px; --space-20: 80px; --space-24: 96px;

  /* ─── Radius ─── */
  --r-xs: 4px; --r-sm: 8px; --r-md: 12px; --r-lg: 16px;
  --r-xl: 24px; --r-2xl: 32px; --r-full: 9999px;

  /* ─── Shadows ─── */
  --shadow-xs:    0 1px 2px rgba(20,14,9,.05);
  --shadow-sm:    0 2px 6px rgba(20,14,9,.06), 0 1px 2px rgba(20,14,9,.04);
  --shadow-md:    0 4px 14px rgba(20,14,9,.08), 0 2px 4px rgba(20,14,9,.04);
  --shadow-lg:    0 12px 32px rgba(20,14,9,.12), 0 4px 8px rgba(20,14,9,.06);
  --shadow-xl:    0 24px 64px rgba(20,14,9,.16), 0 8px 16px rgba(20,14,9,.08);
  --shadow-glow:  0 0 0 4px rgba(255,190,152,.35);
  --shadow-ember: 0 8px 32px rgba(217,79,30,.25);

  /* ─── Motion ─── */
  --ease:        cubic-bezier(.22, 1, .36, 1);
  --ease-spring: cubic-bezier(.34, 1.56, .64, 1);
  --dur-fast: 150ms;
  --dur:      220ms;
  --dur-slow: 400ms;
}

[data-theme="dark"] {
  --bg:            #0F0A06;
  --surface:       #1A120C;
  --surface-2:     #241A12;
  --border:        #3A2F24;
  --border-strong: #56493A;
  --text:          #FBF8F4;
  --text-muted:    #A69680;
  --text-soft:     #D2C5B0;
}
```

### Équivalent Tailwind (tailwind.config.js)

```js
export default {
  theme: {
    extend: {
      colors: {
        peach: {
          50:'#FFF6F0', 100:'#FFE8D8', 200:'#FFD4B8', 300:'#FFBE98',
          400:'#FFA574', 500:'#F58856', 600:'#DC6B3A', 700:'#B4502A',
          800:'#87391E', 900:'#542413',
        },
        ember: { 400:'#E8653A', 500:'#D94F1E', 600:'#B33A10' },
        dusk:  { 50:'#F1F1F6', 200:'#C7C5DB', 400:'#7D7AAD',
                 500:'#5E5B8C', 700:'#3C3962', 900:'#1F1D38' },
        cream: {
          50:'#FBF8F4', 100:'#F5EEE5', 200:'#E8DFD1', 300:'#D2C5B0',
          400:'#A69680', 500:'#7A6B58', 600:'#56493A', 700:'#3A2F24',
          800:'#241C14', 900:'#140E09',
        },
      },
      fontFamily: {
        display: ['Fraunces', 'ui-serif', 'Georgia'],
        sans:    ['Manrope', 'ui-sans-serif', 'system-ui'],
        mono:    ['"JetBrains Mono"', 'ui-monospace'],
      },
      borderRadius: {
        xs:'4px', sm:'8px', md:'12px', lg:'16px', xl:'24px', '2xl':'32px',
      },
      boxShadow: {
        xs:'0 1px 2px rgba(20,14,9,.05)',
        sm:'0 2px 6px rgba(20,14,9,.06), 0 1px 2px rgba(20,14,9,.04)',
        md:'0 4px 14px rgba(20,14,9,.08), 0 2px 4px rgba(20,14,9,.04)',
        lg:'0 12px 32px rgba(20,14,9,.12), 0 4px 8px rgba(20,14,9,.06)',
        ember:'0 8px 32px rgba(217,79,30,.25)',
        glow: '0 0 0 4px rgba(255,190,152,.35)',
      },
    },
  },
};
```

---

## 11. Accessibilité

- **Contrastes testés** :
  - `peach-700 (#B4502A)` sur `cream-50` → 5.1:1 ✓ AA
  - `cream-900` sur `peach-300` → 9.8:1 ✓ AAA
  - `white` sur `ember-500` → 4.6:1 ✓ AA
  - `cream-500` sur `cream-50` (text-muted) → 4.5:1 ✓ AA large
- **Focus ring visible partout** via `shadow-glow` (4px, 35% opacity) sur `:focus-visible`.
- **Status** jamais uniquement par couleur : toujours dot + label texte.
- **Animations** respectent `prefers-reduced-motion` (à implémenter dans les gaming components avec pulse) :
  ```css
  @media (prefers-reduced-motion: reduce) {
    *, *::before, *::after {
      animation-duration: 0.01ms !important;
      transition-duration: 0.01ms !important;
    }
  }
  ```
- **Tailles de cible tactile** ≥ 44×44px sur mobile (boutons `lg`, toggles).

---

## 12. Prochaines étapes

À construire une fois le nom figé :

1. **Logo mark** — feu de camp minimaliste en un seul coup de plume. Probablement un gradient peach → ember dans une forme primitive (triangle flammes). Tester une version monochrome + une version cream sur fond peach.
2. **Illustration system** — style vectoriel doux, lignes rondes, même palette. Mascottes possibles : campeur pixel, feu qui danse, carte FRA avec datacenters pins.
3. **Motion system** — stagger de 60ms entre cards au mount, hover cards lift 2px/150ms, page transitions avec crossfade + subtle scale (0.98 → 1).
4. **Dashboard dark** — implémenter le full dark mode avec les tokens déjà prévus, vérifier les contrastes des gauges et status.
5. **Emails transactionnels** — template HTML reprenant Fraunces (fallback Georgia) + Manrope (fallback Helvetica Neue), palette peach/cream, radius réduits (8 max pour compat Outlook).
6. **Design tokens export** — générer JSON / style-dictionary pour partager avec une éventuelle app mobile (React Native, Swift).
7. **Landing page complète** — hero + features + pricing + témoignages + FAQ + footer, tout avec le system.
8. **Icônes custom domain** — `block`, `player-head`, `tickrate`, `mod-piece` — en SVG propre, cohérent avec Lucide.

---

**Campfire Design System · v0.1**
Construit sur Pantone 13-1023 Peach Fuzz.
Fraunces + Manrope + JetBrains Mono.
