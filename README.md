# Pilotes Bépo

Pilotes de la disposition clavier [Bépo](https://bepo.fr) générés avec [Kalamine](https://github.com/OneDeadKey/kalamine).

## Création des installeurs

- Installer Kalamine
- Générer les pilotes portable Windows (ahk), MacOS (keylayout), Linux user (xkb_keymap) et Linux root (xkb_symbols) :
  ```sh
  kalamine build Bépo.toml
  ```
  pour conserver les raccourcis clavier qwerty :
  ```sh
  kalamine build --qwerty-shortcuts Bépo.toml
  ```
- Générer les pilotes Windows (à lancer sur un PC Windows avec [MSKLC](https://www.microsoft.com/en-us/download/details.aspx?id=102134) d’installé) :
  ```sh
  wkalamine build Bépo.toml
  ```
  pour conserver les raccourcis clavier qwerty :
  ```sh
  wkalamine build --qwerty-shortcuts Bépo.toml
  ```

## Tester le layout

```sh
kalamine watch Bépo.toml
```

## Touches manquantes

- Enchainement de 2 touches mortes ([exemple](https://bepo.fr/wiki/Touches_mortes#Br%C3%A8ve))
- Touche morte ‹ Symbole scientifique › sur `D` en altgr
- Touche morte ‹ Exposant › sur `T` en altgr
- Touche morte ‹ Latin et ponctuation › sur `S` en altgr
- Touche morte ‹ Crochet, hameçon ou crochet en chef › sur `?` en shift + altgr
- Touche morte ‹ Cornu › sur `Q` en shift + altgr

## TODO

- raccourcis clavier azerty et qwertz (non implémenté dans Kalamine)
- claviers ISO et ANSI
