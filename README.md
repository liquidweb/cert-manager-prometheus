# cert-manager-prometheus
Development instance of hooking up to cert manager's prometheus data

1. Clone this repo
2. Find your host's Docker IP
   1. Linux: `ifconfig docker0 | grep "inet addr:"`
   2. macOS: `dig +short host.docker.internal` inside one of your docker containers
3. Change `localhost` to your host's Docker IP in `prometheus/prometheus.yml` in `targets` under the `kube-cert-manager` job
4. `docker-compose up`
