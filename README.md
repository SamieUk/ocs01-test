**ocs01-test**

rust cli for testing ocs01 smart contract

**what it does**

-   tests all ocs01 contract methods
-   interactive menu for easy navigation
-   shows results instantly for view methods
-   handles tx signing for call methods

**works on**

-   linux
-   macos
-   windows


**check if rust is installed**

```bash
rustc --version
```


**install rust (if not installed)**

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source $HOME/.cargo/env
```


Build from source

```bash
git clone https://github.com/octra-labs/ocs01-test.git
```

**SETUP**


required files in same directory

-   wallet.json - create with your credentials
-   exec_interface.json - copy from EI/ folder



You need your `wallet.json` which has your wallet details like the last time in "octra_pre_client" dir

```bash
cd octra_pre_client
cp ./wallet.json ocs01-test
```

if you can't locate `wallet.json` file, just create one

```bash
nano wallet.json
```


copy and edit

```bash
{
  "priv": "PRIVATE_KEY",
  "addr": "ADDRESS",
  "rpc": "https://octra.network"
}

```

press `Ctrl+X`, add name `wallet.json` then press `Enter` to save 



copy `EI/exec_interface.json` file to `ocs01-test`. use the following commands

```bash
# 
cd ..
cd ocs01-test2
cp EI/exec_interface.json .
```

*Build*

```bash
cargo build --release
```

*RUN TO START*

```bash
./target/release/ocs01-test .
```

**TO-DO**

1. claim 1 test token

2. test all functions of the math contract one by one




you must copy the release binary to your cli folder and also copy the EI file (execution interface file) to the same location 


*for this task the ei file contains the interface for contract at address octBUHw585BrAMPMLQvGuWx4vqEsybYH9N7a3WNj1WBwrDn, do not modify it*

after running, follow the menu to interact with the contract


[link to first week's task](https://github.com/octra-labs/octra_pre_client)
