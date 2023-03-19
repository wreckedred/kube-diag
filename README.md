# kube-diag

A simple bash script to check the health of a New Relic-enabled Kubernetes cluster.

The script runs standard Kubernetes commands in the newrelic namespace and creates an output file.
The output can be helpful to troubleshoot issues.


# Usage

```
kube-diag.sh <namespace>
```

Run from instance with access to cluster. The namespace will typically be either `px` or `newrelic`, depending on your installation.
```
wget https://raw.githubusercontent.com/wreckedred/kube-diag/main/kube-diag.sh
chmod +x kube-diag.sh
./pixie-diag.sh newrelic
```

# Output

`kube-diag.sh` outputs to terminal and creates two files:

- kube_diag_<date>.log <-- stdout to file

- kube_diag_logs_<date>.gzip <-- logs to gzip
