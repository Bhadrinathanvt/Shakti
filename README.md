---
### Verifying Individual Files
To check for errors in individually developed BSV files without running the full ```make generate_verilog``` process:
```bash
bsc -u -verilog -elab \
-vdir build/hw/verilog \
-bdir build/hw/intermediate \
-info-dir build/hw/intermediate \
+RTS -K40000M -RTS \
-suppress-warnings G0010:T0054:G0020:G0024:G0023:G0096:G0036:G0117:G0015 \
-D CORE_AXI4 \
-p .:%/Libraries:c-class/src:fabrics/axi4lite:fabrics/axi4:common_bsv \
<file_name.bsv>
```

add the file in the place holder ```<filename.bsv>```.

---
