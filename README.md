# Digimon World 2003 no running away

## Patching
Download either the IPS or XDELTA patch
Patch **your** copy of Digimon World 2003 with
[IPS Patcher](https://www.romhacking.net/patch/)
[XDELTA Patcher](https://www.romhacking.net/utilities/598/)

## How it works
modified the function at 800a1608 in the FIGHTSTG overlay to

```asm
jr ra
lui v0, 0x00
```

esentially making it into
```c
bool EscapeSuccessful(DigimonController controller) {
  return false;
}
```
