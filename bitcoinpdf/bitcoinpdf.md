---
layout: default
title: 📝 bitcoin.pdf
nav_order: 99
has_children: false
---
<span class="fs-8">📝 bitcoin.pdf</span><br>
<br>
`bitcoin-cli getblock 00000000000000ecbbff6bafb7efa2f7df05b227d5c73dca8f2635af32a2e949 0 | tail -c+92167 | for ((o=0;o<946;++o)) ; do read -rN420 x ; echo -n ${x::130}${x:132:130}${x:264:130} ; done | xxd -r -p | tail -c+9 | head -c184292 > bitcoin.pdf`
<br>
[bitpaint.club/bitcoin.pdf](https://bitpaint.club/bitcoin.pdf)