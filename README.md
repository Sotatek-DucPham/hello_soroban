# hello_soroban

```sh
cargo install --locked --version 20.0.2 soroban-cli --features opt

soroban config network add --global futurenet \
  --rpc-url https://rpc-futurenet.stellar.org:443 \
  --network-passphrase "Test SDF Future Network ; October 2022"

soroban config identity generate --global alice

soroban config identity fund alice --network futurenet

soroban contract build

soroban contract optimize \
  --wasm target/wasm32-unknown-unknown/release/hello_soroban.wasm

soroban contract deploy \
  --wasm target/wasm32-unknown-unknown/release/hello_soroban.wasm \
  --source alice \
  --network futurenet
```
