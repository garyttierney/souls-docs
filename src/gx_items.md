# Definitions of GXItem formats in Dark Souls III

Items are described according to the `ID` field in the header.

## GX02

GX02 is read by the game (at `0x1401412f5`) as:

### Decoder

```c
              *(int*)(material + 0x110) = read_int32(buffer->data);
              *(int*)(material + 0x114) = read_int32(buffer->data + 4);
              *(int*)(material + 0x120) = read_int32(buffer->data + 8);
              *(float*)(material + 0x118) = read_float32(buffer->data + 0xc);
              *(float*)(material + 0x11c) = read_float32(buffer->data + 0x10);
              puVar9 = local_res8;
              if (5 < (int)*(uint *)(material + 0x4e8)) {
                puVar9 = (uint *)(material + 0x4e8);
              }
              uVar6 = *puVar9;
              *(undefined *)(material + 0xdd) = 1;
              *(uint *)(material + 0x4e8) = uVar6;
```

### Structure

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
