# Da-node-guide-0g_labs

![0_AxKIus_I-soNSp03](https://github.com/user-attachments/assets/cdd98171-5946-4d7a-945a-8e21a2717c9d)

## Hardware Requirement
```bash
- Memory: 16 GB
- CPU: 8 cores
- Disk: 1 TB NVME SSD
- Bandwidth: 100 MBps for Download / Upload
```

# Installation
```bash
git clone https://github.com/0glabs/0g-da-node.git
cargo build --release
./dev_support/download_params.sh
```

# Configuration
```toml
log_level = "info"

data_path = "./db/"

encoder_params_dir = "params/" 

grpc_listen_address = "0.0.0.0:34000"
eth_rpc_endpoint = "https://rpc-testnet.0g.ai"
socket_address = "<public_ip/dns>:34000"

da_entrance_address = ""
start_block_number = 0

signer_bls_private_key = ""
signer_eth_private_key = ""

enable_das = "false"
```

## Generate BLS private key
```bash
cargo run --bin key-gen
```

# Run
```bash
./target/release/server --config cargo.toml
```
