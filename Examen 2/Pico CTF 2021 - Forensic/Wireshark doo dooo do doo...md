## Objetivo
Can you find the flag? [shark1.pcapng](https://mercury.picoctf.net/static/0505a462ac9beb7412596855df280f6b/shark1.pcapng).

## Hints


## Solución
Descargamos el documento y lo abrimos con wireshark y le damos seguimiento a TSP y buscando en el 5 encontramos esto **Gur synt vf cvpbPGS{c33xno00_1_f33_h_qrnqorrs}** que parece ROT 13, al pasarlo por cyberchef nos da **The flag is picoCTF{p33kab00_1_s33_u_deadbeef}**

## Bandera
picoCTF{p33kab00_1_s33_u_deadbeef}