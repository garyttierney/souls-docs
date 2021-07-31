# Definitions of GXItem formats in Dark Souls III

Items are described according to the `ID` field in the header.

## GX02

```c
struct GX02 { // also toggles [material+0xdd] to 1
   int unk_0;
   int unk_04;
   int unk_08;
   float unk_0c;
   float unk_10;
}
```

<p align="center">
  <img src="formats/flver/gx02.svg" width="100%" />
</p>
