# Fernando Afonso
## TUTORIAL:
## Com pujar un canvi a GitHub
---
Passos per pujar un canvi a GitHub:

1. Comprovar els canvis amb `git status`.
2. Afegir els fitxers amb `git add`.
3. Crear un commit amb `git commit -m "Inserta texte"`.
4. Pujar els canvis amb `git push`.

Tasques:

- [x] Crear algun fitxer.
- [x] Afegir informació sobre comandes Git i GitHub.
- [ ] Pujar la documentació.

Enllaç d'interès https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax?

```bash
git -v
git init
git status
git add .
git status
git branch
git branch -M main
git commit -m "alpha 0.1 - Primer commit :-)"
git config --global user.name Fernando
git config --global user.email \ ########@#####.###
git commit -m "alpha 0.1 - Primer commit :-)"
git status
git push
```
| Comanda | Funcionament |
|--------|--------------|
| `git init` | Inicia un nou repositori a la carpeta. |
| `git status` | Mostra l’estat dels fitxers i si hi ha canvis pendents d'afegir. |
| `git add <fitxer>` | Prepara els fitxers a afegir quan es faci un commit. |
| `git commit -m "missatge"` | Guarda els canvis preparats amb un missatge descriptiu. |
| `git push` | Puja els commits locals al repositori de GitHub. |

---

## Incidències


En intentar fer el primer commit, Git va mostrar un error **Author identity unknown**. El Git estava acabat d'instal·lar i no en tenia el nostre perfil. Per solucionar-ho, ho vam configurar de forma senzilla amb les comandes **git config --global user.name Fernando** i **git config --global user.email #####@#######.###**, i em va deixar fer commit.