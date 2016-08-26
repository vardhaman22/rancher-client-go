# client-go

Go clients for talking to a [kubernetes](http://kubernetes.io/) cluster.

### What's included

* The `kubernetes` package contains the clientset to access Kubernetes API.
* The `discovery` package is used to discover APIs supported by a Kubernetes API server.
* The `dynamic` package contains a dynamic client that can perform generic operations on arbitrary Kubernetes API objects.
* The `transport` package is used to set up auth and start a connection.
* The `tools/cache` package is useful for writing controllers.

### Releases

Each top-level folder (e.g., 1.4) contains a release of clients and their dependencies.

client-go has the same release cycle as the Kubernetes main repository. For example, in the 1.4 release cycle, the contents in `1.4/` folder are subjected to changes. Once 1.4 is released, new changes will go into the `1.5/` folder. We will make great efforts to not change the public interface of a version of the client once that version has been released. We may change the interface between versions. Old versions of the client will be retained for two release cycles.

### How to get it

You can `go get` a release of client-go, e.g., `go get k8s.io/client-go/1.4/...` for the whole thing or `go get k8s.io/client-go/1.4/kubernetes` if you just need the clientset.

### Reporting bugs

Please report bugs to the main Kubernetes [repository](https://github.com/kubernetes/kubernetes/issues/new).

### Contributing code
Please send pull requests against the client packages in the Kubernetes main [repository](https://github.com/kubernetes/kubernetes), and run the `/staging/src/k8s.io/client-go/copy.sh` script to update the staging area in the main repository. Changes in the staging area will be published to this repository every day.
