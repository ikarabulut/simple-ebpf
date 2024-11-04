# Simple ebpf program

This project is starting as a clone of [libbpf-rs/examples/runqslower](https://github.com/libbpf/libbpf-rs/tree/master/examples/runqslower).
The goal is to use this to get the hang of an ebpf environment and building on libbpf-rs.

## Setting up your environment

I used [lima](https://lima-vm.io/) to set up a linux sandbox environment. The environment config is located in `./learning-ebpf.yaml`.

### To Run
1. `limactl start learning-ebpf.yaml`
2. `limactl shell learning-ebpf`
3. `cargo build`
4. `sudo ./target/debug/simple-ebpf 1000`

This will trace run queue latency higher than 1000 us.