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

**install rust (if not installed)**

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source $HOME/.cargo/env
```

**Check if rust is installed**

```bash
rustup --version
```

**build from source**

```bash
git clone https://github.com/octra-labs/ocs01-test.git
```

**SETUP**


**required files in same directory**

-   wallet.json - create with your credentials
-   ocs01-test binary in target/release
-   exec_interface.json - copy from EI/ folder



**You need your "wallet.json" which has your wallet details like the last time in "octra_pre_client" dir**

```bash
cd octra_pre_client
cp ./wallet.json ocs01-test
```

**If you can't locate wallet.json file, just create one**

```bash
nano wallet.json
```


**copy and edit**

```bash
{
  "priv": "PRIVATE_KEY",
  "addr": "ADDRESS",
  "rpc": "https://octra.network"
}

```

**Press Ctrl+X, add name "wallet.json" then press "Enter" to save** 



**You need to copy these files to "ocs01-test". use the following commands**

```bash
cp EI/exec_interface.json .
```

```bash
cp ./target/release/ocs01-test .

```

```bash
# copy contract interface
cp EI/exec_interface.json .
```



**run**

```bash
./ocs01-test
```



you must copy the release binary to your cli folder and also copy the EI file (execution interface file) to the same location 


*for this task the ei file contains the interface for contract at address octBUHw585BrAMPMLQvGuWx4vqEsybYH9N7a3WNj1WBwrDn, do not modify it*

after running, follow the menu to interact with the contract
