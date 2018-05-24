# oshinko-operator

[![Build status](https://travis-ci.org/Jiri-Kremser/oshinko-operator.svg?branch=master)](https://travis-ci.org/Jiri-Kremser/oshinko-operator)
[![License](https://img.shields.io/badge/license-Apache--2.0-blue.svg)](http://www.apache.org/licenses/LICENSE-2.0)

### Images
[![Layers info](https://images.microbadger.com/badges/image/jkremser/oshinko-operator.svg)](https://microbadger.com/images/jkremser/oshinko-operator)
`jkremser/oshinko-operator:latest`

[![Layers info](https://images.microbadger.com/badges/image/jkremser/oshinko-operator:centos-latest.svg)](https://microbadger.com/images/jkremser/oshinko-operator:centos-latest)
`jkremser/oshinko-operator:centos-latest`


# Quick Start
```bash
oc cluster up
```

```bash
oc policy add-role-to-user edit system:serviceaccount:`oc project -q`:default
```

Run the oshinko-operator deployment:
```bash
oc create -f manifest/
```

Create new cluster from prepared example:

```bash
oc create -f examples/cluster.yaml
```

After issuing the commands above, you should be able to see a new Spark cluster running in the current namespace.

Once you don't need the cluster anymore, you can delete it by deleting the config map resource by:
```bash
oc delete cm my-spark-cluster
```