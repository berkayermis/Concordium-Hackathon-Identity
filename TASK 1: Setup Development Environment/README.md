# TASK 1: Setup Development Environment

### The first task is to install Rustup which will install Rust and Cargo automatically but I've got installed it previously, so I just show it.

```
$ curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

<img width="637" alt="Screen Shot 2023-02-21 at 03 33 17" src="https://user-images.githubusercontent.com/67913214/220217929-421b3298-6e56-4166-98ef-35ed3b95a5d9.png">

Next step is to install Wasm which will help you for building contract.

```
rustup target add wasm32-unknown-unknown
```

<img width="632" alt="Screen Shot 2023-02-21 at 03 37 58" src="https://user-images.githubusercontent.com/67913214/220218612-cdfc522b-7df9-4a5d-8e6d-f4d5f1b3165f.png">

After installing wasm, I have installed the Concordium Software Package from https://developer.concordium.software/en/mainnet/net/installation/downloads-testnet.html#cargo-concordium-testnet
this link (Cargo-Concordium V2.7.0). My OS is also Mac.
Then, I removed the version side (v2.7.0) and moved that file to the ~/.cargo/bin folder. Then I just gave the permission to that file to being executed.

```
$ ~/.cargo/bin
$ sudo chmod +x cargo-concordium
```
Even I gave the permission, I couldn't execute the file on Mac because Mac couldn't scanned the file whether it is malicious or not.
So, I go to the System Preferences -> Securituy & Privacy (General) -> Allow cargo-concordium from below

Then, I installed the Concordium Client v5.0.2 from https://developer.concordium.software/en/mainnet/net/installation/downloads-testnet.html#concordium-node-and-client-download-testnet
Then, it goes to the /usr/local/bin folder automatically on MacOS.

<img width="637" alt="Screen Shot 2023-02-21 at 03 55 52" src="https://user-images.githubusercontent.com/67913214/220221396-cf605d87-71a4-4cca-b735-b5ef150b4a2d.png">

And..

```
$ cd ~/usr/local/bin
$ concordium-client --help
```
command works.

<img width="642" alt="Screen Shot 2023-02-21 at 03 57 30" src="https://user-images.githubusercontent.com/67913214/220221512-2f1f9f0a-7dc9-49fa-be69-04b71a1be109.png">

Now, we can interact with the Concordium Testnet, and all important commands are here: https://developer.concordium.software/en/mainnet/net/references/concordium-client.html#concordium-client

And at this point, we will connect to the public testnet node which is provided by Concordium as free.

Following command is that..

```
$ concordium-client consensus status --grpc-port 10000 --grpc-ip node.testnet.concordium.com
```

Make sure to be in the same directory with concordium-client (/usr/local/bin)

<img width="646" alt="Screen Shot 2023-02-21 at 04 03 27" src="https://user-images.githubusercontent.com/67913214/220222067-6a4abfa0-2184-40ec-9ea7-edbbb78a5aca.png">

