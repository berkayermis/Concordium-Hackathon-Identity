# TASK 2: Deploy Your First Smart Contract

Before starting..
My Concordium Mainnet address is:

```
3Vbzbdt6vKarjcSwHbMwpG2Czb4yZsNCpUZuondoJkEPJF914P
```

---

Firsly, I installed the cargo-generate.

```
$ cargo install --locked cargo-generate
```

Then, I installed a sample smart contract project.

```
$ cargo concordium init
```

My project's name is berkay-concordium.

<img width="629" alt="Screen Shot 2023-02-23 at 05 45 11" src="https://user-images.githubusercontent.com/67913214/220810461-a375889e-a1d6-49b0-a89c-0cec1c8a7d57.png">

I write a basic contract with Rust. I have just 2 functions one of them just updates a message, other one is for viewing it. Also, I wrote a test script for this contract.

After that, I built it by typing:

```
$ cargo concordium build -e --out ./a.wasm.v1
```

<img width="639" alt="Screen Shot 2023-02-23 at 05 53 33" src="https://user-images.githubusercontent.com/67913214/220811493-63783207-2587-46ed-afe3-b01c3eca7174.png">

My test results:

```
$ cargo test
```

<img width="695" alt="Screen Shot 2023-02-23 at 06 37 01" src="https://user-images.githubusercontent.com/67913214/220816157-88a82acb-c4d4-4983-9266-57c22a0fc94f.png"><img width="927" alt="Screen Shot 2023-02-23 at 06 37 26" src="https://user-images.githubusercontent.com/67913214/220816200-dead52e8-dc7f-447d-8e42-4c49967ea0c4.png">


Then, I deployed the contract into the Concordium Testnet.

```
$ ./concordium-client --grpc-ip node.testnet.concordium.com --grpc-port 10000 module deploy ~/Projects/berkay-concordium/a.wasm.v1 --name messageApp --sender 3Q1BKsCmFHjd5ebiT9ZCghyT5MkAHr8rZJC8makv9szwY6R4nE
```

<img width="645" alt="Screen Shot 2023-02-23 at 06 58 53" src="https://user-images.githubusercontent.com/67913214/220818430-53d75e07-e28f-4bd4-b5be-63a166d73358.png">

Transaction Hash:
```
e00771808660f72b33ca3cb519a47a471ca9db560e13b1037c652d404c470162
```

Contract Address:
```
50154cd2ea695b298dec9c8c8446443b394f1bc0aaeb4e7f25ff5e01d68dcf3c
```

Also,

```
Transaction is finalized into block acfbf2a6bcadea7b36020144994a021d8be733e6d5b1b3bc1578fa15238151af with status "success" and cost 33.492777 CCD (18172 NRG).
```

