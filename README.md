# perftest AUR Package

This is the AUR package for the perftest suite, which provides OpenFabrics Alliance InfiniBand verbs performance testing and benchmarking tools.

## Installation

You can install this package using an AUR helper like `yay`:

```
yay -S perftest
```

Or you can clone the AUR repository and build it manually:

```
git clone https://aur.archlinux.org/perftest.git
cd perftest
makepkg -si
```

## Usage

After installation, you can use the various perftest tools. Some examples include:

- `ib_send_lat`: latency test with send transactions
- `ib_send_bw`: bandwidth test with send transactions
- `ib_write_lat`: latency test with RDMA write transactions
- `ib_write_bw`: bandwidth test with RDMA write transactions
- `ib_read_lat`: latency test with RDMA read transactions
- `ib_read_bw`: bandwidth test with RDMA read transactions

For more information on how to use these tools, please refer to the perftest documentation or run the commands with the `--help` flag.

## License

This package is licensed under GPL2 and the custom OpenIB.org BSD license. See the COPYING file in the package for more details.

## Links

- [perftest GitHub repository](https://github.com/linux-rdma/perftest)
- [OpenFabrics Alliance](https://www.openfabrics.org/)
