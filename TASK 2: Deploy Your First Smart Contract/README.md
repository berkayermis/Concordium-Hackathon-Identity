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

Then, I installed a sample smart contrac project.

```
$ cargo concordium init
```

My project's name is berkay-concordium.

<img width="629" alt="Screen Shot 2023-02-23 at 05 45 11" src="https://user-images.githubusercontent.com/67913214/220810461-a375889e-a1d6-49b0-a89c-0cec1c8a7d57.png">

I write a basic contract with Rust. I have just 2 functions one of them just updates a message, other one view it. Also, I wrote a test script for this contract.

After that, I build it by typing:

```
$ cargo concordium build -e --out ./a.wasm.v1
```

<img width="639" alt="Screen Shot 2023-02-23 at 05 53 33" src="https://user-images.githubusercontent.com/67913214/220811493-63783207-2587-46ed-afe3-b01c3eca7174.png">

My test results:

```
$ cargo test
```

<img width="695" alt="Screen Shot 2023-02-23 at 06 37 01" src="https://user-images.githubusercontent.com/67913214/220816157-88a82acb-c4d4-4983-9266-57c22a0fc94f.png"><img width="927" alt="Screen Shot 2023-02-23 at 06 37 26" src="https://user-images.githubusercontent.com/67913214/220816200-dead52e8-dc7f-447d-8e42-4c49967ea0c4.png">





