# TCP Stream Reconstruction

To reconstruct the payload:

- Filtered packets by destination port (1337)
- Extracted `data.data` field
- Applied frame length filtering to isolate payload-heavy packets
- Reassembled hex stream
- Converted hex to binary using xxd

This enabled reconstruction of a full exfiltrated dump without relying on GUI stream reassembly.
