# Incident responder

Run this from the repository root in WSL, with the Codex CLI logged in:

```bash
python3 incident-response/server.py
```

Keep the process running while Grafana is active. It listens on port 8001; the
Grafana webhook reaches it through `host.docker.internal`. Firing alerts create
evidence and headless Codex output under `incident-response/incidents/`.

To send the Homework test notification, run `bash incident-response/test-webhook.sh`.
