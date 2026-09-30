# ⚠️ DEPRECATED — NO LONGER WORKING

**This project no longer works** due to upstream API/service changes on TrueMoney's side, and it will not be fixed. It is kept public for reference and educational purposes only.

---

# TrueMoney Wallet Voucher Receiver

A small Python client used to receive money from voucher links of the TrueMoney Wallet app.

Given a voucher URL and your wallet number, it fetches the voucher details and redeems the amount into your wallet.

## Features

- Parses the voucher hash straight from a shared voucher link
- Verifies voucher details (amount, status) before redeeming
- Redeems the voucher into your own wallet number
- Single-file client, no external dependencies beyond `requests`

## Usage

```python
from client import Client


if (__name__ == '__main__'):
    client = Client('your TrueMoney wallet number')
    client.set_voucher_hash('voucher url')

    voucher = client.get_voucher()
    if (voucher != None):
        client.redeem_voucher()
```

## Disclaimer

For educational purposes only. Use only with vouchers you legitimately received. The author is not responsible for any misuse.

## License

MIT
