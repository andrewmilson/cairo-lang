## Difference between cairo-lang bootloader and bootloader in Solidity verifier

1. ran "cairo-compile 0.11.2"
```bash
cairo-compile src/starkware/cairo/bootloaders/bootloader/bootloader.cairo --proof_mode --debug_info_with_source --output bootloader_compiled.json --cairo_path src
```
2. extracted [bootloader_compiled.json](bootloader_compiled.json) program data into [locally_compiled_bootloader](locally_compiled_bootloader)
3. extracted [solidity bootloader from etherscan](https://etherscan.io/address/0x6CB3EE90C50A38A0E4662BB7E7E6E40B91361BF6#code#F2#L1) into [solidity_bootloader](solidity_bootloader)
4. Generated diff between the bootloaders in [bootloader_diff](bootloader_diff)
```bash
diff locally_compiled_bootloader solidity_bootloader > bootloader_diff
```

