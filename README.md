# DNS-Tunnel-Datasets

# Dataset Declaration

This dataset is independently collected by us and has been utilized in our paper titled "[《GraphTunnel: Robust DNS Tunnel Detection Based  on DNS Recursive Resolution Graph》](https://ieeexplore.ieee.org/document/10636232)."


## Dataset Content

We simulated a standard network environment to construct a framework for collecting DNS tunnel traffic.  This framework facilitates the procurement of benign  DNS traffic from the foremost one million domains  on Cloudflare, encompassing 2,012,494 records.  Concurrently, it enables the collation of tunnel traffic,  engendered by an array of DNS tunneling tools that support diverse DNS query records, amounting to 962,859  records.

Additionally, there is wildcard DNS traffic totaling 639,208 instances in the dataset.

## Dataset Structure

To reduce upload size limitations, we have segmented some large PCAP files. The dataset is structured as follows:

- **normal**: Benign traffic sourced from the top one million domains on Cloudfare.

- **tunnel**: Used for model training, playing the role of known DNS tunnels. Includes dnscat2, dnspot, iodine, DNS-shell, tuns, and their various supported record types.

- **unknownTunnel**: Employed for robustness testing of the model, acting as unknown DNS tunnels. Comprises tcp-over-dns, CobaltStrike, dns2tcp, ozymandns.

- **crossEndPoint**: Essentially used for robustness testing of the model, playing the role of unknown DNS tunnels. Collected from the Android platform, specifically AndIodine.

- **wildcard**: Wildcard DNS traffic for robustness testing of the model. Derived from the top 1000 Cloudfare domains supporting wildcard resolution, and their subdomains collected using OneforAll.

## Usage

You can download from here: [ DNS Tunnel Datasets](https://github.com/ggyggy666/DNS-Tunnel-Datasets.git).

## Licensed
If you want to use this dataset or refer to our paper, please cite the dataset and our paper.
