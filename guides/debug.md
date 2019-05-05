# Appunti sul debugging

- 🍃 [Debugging Compilation timeout errors](https://www.overleaf.com/learn/how-to/Debugging_Compilation_timeout_errors)

## Errori comuni

```bash
! File ended while scanning use of \@argdef
```
# It's very probably caused by a missing closing brace, namely a `}`.
Molto probabilmente hai dimenticato di chiudere un gruppo con una parentesi graffa `}`.

```bash
Misplaced alignment tab character &
```
# To correct this error, change `&` to `\&`.
Hai dimenticato di fare l'escape _nel testo_ del carattere `&`, per correggere questo errore cambia `&` in `\&` alla riga specificata.

- 🍃 [Common Causes of Error](https://www.overleaf.com/learn/latex/Errors/Misplaced_alignment_tab_character_&)
