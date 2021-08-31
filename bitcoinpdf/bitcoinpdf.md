---
layout: default
title: 📝 bitcoin.pdf
nav_order: 99
has_children: false
---
<span class="fs-8">📝 bitcoin.pdf</span><br>
<br>
[bitpaint.club/bitcoin.pdf](https://bitpaint.club/bitcoin.pdf)

<br>
---
# **getblock**
`bitcoin-cli getblock 00000000000000ecbbff6bafb7efa2f7df05b227d5c73dca8f2635af32a2e949 0 | tail -c+92167 | for ((o=0;o<946;++o)) ; do read -rN420 x ; echo -n ${x::130}${x:132:130}${x:264:130} ; done | xxd -r -p | tail -c+9 | head -c184292 > bitcoin.pdf`

<br>
---
# **gettxout**
`seq 0 947 | (while read -r n; do bitcoin-cli gettxout 54e48e5f5c656b26c3bca14a8c95aa583d07ebe84dde3b7dd4a78f4e4186e713 $n | jq -r '.scriptPubKey.asm' | awk '{ print $2 $3 $4 }'; done) | tr -d '\n' | cut -c 17-368600 | xxd -r -p > bitcoin.pdf`

---
<br>
# **getrawtransaction**
`bitcoin-cli getrawtransaction 54e48e5f5c656b26c3bca14a8c95aa583d07ebe84dde3b7dd4a78f4e4186e713 0 00000000000000ecbbff6bafb7efa2f7df05b227d5c73dca8f2635af32a2e949 | sed 's/0100000000000000/\n/g' | tail -n +2 | cut -c7-136,139-268,271-400 | tr -d '\n' | cut -c17-368600 | xxd -p -r > bitcoin.pdf`
<br><br>
