# Audit libpng 1.6.50.git – zones critiques

## Fichiers prioritaires
- pngrutil.c  : lecture chunks, CRC, tailles
- pngpread.c  : streaming, état partiel
- pngmem.c    : alloc/free wrappers
- pngtrans.c  : transfos couleur/bit depth
## Fonctions à inspecter
- png_read_chunk_header()
- png_handle_PLTE()
- png_do_expand_palette()
- ...
## TODO spots
- Validations transformations (TODO.md)
- Interlacing handling
## Corpus initial
- tests/pngtest.png
- contrib/pngsuite/*.png
