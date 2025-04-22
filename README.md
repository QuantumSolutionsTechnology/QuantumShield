# QuantumShield Toolkit

QuantumShield is an open-source toolkit for transitioning legacy cryptography to post-quantum cryptography (PQC) using ML-KEM. It provides SDKs (Python, Rust, JavaScript), a RESTful API, and a command-line tool (CLT).

## Developer Portal

Explore the API, SDKs, and examples at developers.quantumsolutions.dev.

## Features

- **ML-KEM Support**: Implements ML-KEM-512, 768, and 1024 for quantum-resistant key encapsulation.
- **Hybrid Encryption**: Combines ML-KEM with AES-256-GCM for legacy compatibility.
- **SDKs**: Python, Rust, and JavaScript for diverse applications.
- **RESTful API**: Cloud-based PQC operations, deployable on AWS, Fly.io, or local servers.
- **Command-Line Tool**: CLI for key management, file encryption, and data migration.
- **Open Source**: Licensed under MIT.

## Installation

```bash
pip install quantumshield  # Python SDK
cargo add oqs aes-gcm hkdf sha2 base64 rand  # Rust SDK
npm install pqclean.js  # JavaScript SDK
```

## Quickstart

### Python SDK

```python
from quantumshield import QuantumShield
qs = QuantumShield(parameter_set="512")
public_key, private_key = qs.generate_keypair()
ciphertext, shared_secret = qs.encapsulate(public_key)
```

### Command-Line Tool

```bash
python qshield.py generate-keypair --parameter-set 512
```

### REST API

```bash
curl -X POST https://api.quantumsolutions.dev/api/mlkem/generate-keypair \
  -H "Content-Type: application/json" \
  -H "X-API-Key: your-api-key" \
  -d '{"parameter_set": "512"}'
```

## Documentation

- Developer Portal
- API Reference
- Examples
- SDKs

## License

MIT License. See LICENSE for details.

## Contributing

Fork the repo and submit a pull request. See CONTRIBUTING.md.

## Support

File issues on GitHub Issues or join our community forum.