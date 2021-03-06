# Browser Example

To run the example, first you need a local Datadog agent. The easiest way to get one is using the official Docker image:

**Note: Don't forget to replace `<Your API Key>` with your actual API key from Datadog.**

```sh
docker run -d --name dd-agent -v /var/run/docker.sock:/var/run/docker.sock:ro -v /proc/:/host/proc/:ro -v /sys/fs/cgroup/:/host/sys/fs/cgroup:ro -e API_KEY=<Your API Key> -e SD_BACKEND=docker -e DD_APM_ENABLED=true -p 8126:8126 datadog/docker-dd-agent:latest
```

Once the container is running, you can run the example server:

```sh
npm run browser
```

This will start the server on port `8080` and open a browser. You can then click on the `Send Trace` button to generate traces.
