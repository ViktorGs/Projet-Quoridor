**Fiche Récapitulative : Critères d'étude de convergence pour les intégrales généralisées**

---

# 1. Tableau des Critères de Convergence

| Critère                         | Quand l'utiliser                                         | Types de fonctions concernées             | Comment décider vite                                 | Pourquoi on fait ça                         | J'applique ce critère si... |
|:----------------------------------|:---------------------------------------------------------|:--------------------------------------------|:-----------------------------------------------------|:---------------------------------------------|:-------------------------------|
| **Critère de Riemann**            | Fonction type \( \frac{1}{x^a} \)                        | Polynômes, puissances de \(x\), racines     | Quand tu vois un \( x^a \)                            | Appliquer un résultat connu : convergence si \( a > 1 \) | La fonction ressemble à une puissance de \(x\) au bord |
| **Critère d'équivalence**        | \( f(x) \sim g(x) \)                                    | Polynômes, racines, ln, exponentielles      | Dès que tu peux simplifier fortement ou DL           | Remplacer par une fonction plus simple        | Les fonctions se comportent pareil à la borne |
| **Critère de comparaison**        | \( f(x) \leq Cg(x) \) ou \( cg(x) \leq f(x) \)             | Polynômes, ln, exponentielles               | Quand tu peux encadrer sans équivalence               | Majorer pour convergence, minorer pour divergence | Une fonction est évidemment plus grande ou plus petite qu'une autre |
| **Critère de négligeabilité**     | \( f(x) \ll g(x) \) avec \( \int g(x) \) convergent        | Petits termes perturbateurs                 | Quand \( f(x) \) est beaucoup plus petit que \( g(x) \) | Montrer que \( f(x) \) est écrasé par \( g(x) \)      | Un terme est négligeable par rapport à un autre dominé |
| **Critère de convergence absolue** | Fonction qui change de signe                              | Fonctions oscillantes (sin, cos), ln parfois | Dès que \( f(x) \) oscille entre positif et négatif   | Assurer convergence même si oscillations        | La fonction oscille entre positif et négatif |

---

# 2. Tableau des Types de Fonctions par Rapidité de Décroissance

| Type de fonction                  | Exemples                      | Comportement à \( +\infty \)        | Rapidité          |
|:-----------------------------------|:--------------------------------|:----------------------------------|:--------------------|
| **Exponentielle décroissante**    | \( e^{-x} \)                  | Tend très vite vers 0            | 🚀 Très rapide   |
| **Exponentielle croissante**       | \( e^{x} \)                   | Explose vers \( +\infty \)         | 🚀 Très rapide (vers +\(\infty\)) |
| **Puissance inverse**              | \( \frac{1}{x^a} \) avec \( a>0 \) | Tend vers 0 rapidement           | 🔥 Rapide     |
| **Racine inverse**                 | \( \frac{1}{\sqrt{x}} \)       | Tend vers 0 modérément          | 🐿 Normal     |
| **Logarithme simple**              | \( \frac{1}{\ln(x)} \)         | Tend très lentement vers 0         | 🐢 Lent        |
| **Double logarithme**              | \( \frac{1}{\ln(\ln(x))} \)    | Encore plus lent                 | 🐢🐢 Très lent  |
| **Sinus ou cosinus**               | \( \sin(x), \cos(x) \)          | Oscillent, pas de tendance vers 0 | ⚡ Oscille      |

---

# 3. Ordre de Décroissance (du plus lent au plus rapide)

\[ 
\frac{1}{\ln(\ln(x))} \ll \frac{1}{\ln(x)} \ll \frac{1}{\sqrt{x}} \ll \frac{1}{x} \ll \frac{1}{x^2} \ll e^{-x} 
\]

**Commentaire :**
- \( e^{-x} \) écrase tout le monde à l'infini.
- \( \ln(x) \) et \( \ln(\ln(x)) \) décroissent très lentement.
- \( \frac{1}{x} \) et \( \frac{1}{x^2} \) décroissent selon leur exposant.

---

# 4. Influence des Bornes sur le Choix du Critère

| Cas de bornes | Critère à préférer | Pourquoi |
|:--------------|:------------------------|:---------|
| \( 0^+ \) ou \( 1^- \) (explosion) | Riemann, Comparaison, DL | Regarder comportement près de la borne |
| \( +\infty \) ou \( -\infty \) | Riemann, Équivalence | Voir quel terme domine |
| Borne simple, pas de pb | Intégrale classique | Aucun traitement spécial requis |
| Oscillation (sin/cos) | Convergence absolue | Car oscillation sans tendance nette |

---

# 5. Cas classiques par type d'intervalle

| Type d'intervalle | Ce qu'il faut vérifier | Critère à utiliser |
|:------------------|:------------------------|:--------------------|
| \( [a, +\infty[ \) | Vérifier \( +\infty \) (et \( a \) si besoin) | Riemann, Équivalence, Négligeabilité si petit terme |
| \( ]a,b[ \) | Vérifier \( a^+ \) et \( b^- \) | Riemann, Comparaison, DL, Négligeabilité |
| \( ]a,b] \) | Vérifier \( a^+ \) | Riemann, Comparaison, DL |
| \( [a,b[ \) | Vérifier \( b^- \) | Riemann, Comparaison, DL |
| \( (0,1] \) | Vérifier \( 0^+ \) | Riemann ou DL selon la fonction |
| Oscillation (ex : sinus, cosinus) | Etudier \( |f(x)| \) | Convergence absolue |

**Quand utiliser directement un DL :**
- Quand tu as une forme \( \frac{0}{0} \) à une borne (ex : \( \ln(1-x) \), \( \sin(x) \), etc.)
- Quand la fonction a une expression compliquée mais se simplifie autour d'une borne.
- Quand on veut évaluer finement un comportement local (près de \( 0 \) ou \( 1 \)).

---

# ✨ Conseils clés pour choisir rapidement

- **Exponentielle** (ex : \( e^{-x} \)) → convergence facile.
- **Puissance** (ex : \( \frac{1}{x^a} \)) → pense à Riemann.
- **Logarithme** (ex : \( \frac{1}{\ln(x)} \)) → utiliser comparaison ou négligeabilité.
- **Oscillation** (ex : \( \sin(x), \cos(x) \)) → penser convergence absolue.
- **Bornes particulières** → penser Riemann, équivalence, ou DL selon le contexte.

---

Fiche faite pour t'aider à choisir **directement** le bon critère sans hésiter 🚀 !

