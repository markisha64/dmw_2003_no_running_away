# Digimon World 2003 no running away

## Patching
Patch **your** copy of Digimon World 2003 with
[XDELTA Patcher](https://www.romhacking.net/utilities/598/)
or if you want to mix and match patches
[Digimon World 2003 Patcher](https://github.com/markisha64/dmw_2003_patcher)

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
