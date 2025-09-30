Vault Setup

  Windows

    1. Open WSL.
    2. Make sure you have the following files:
        - vault-cert.pem
        - vault-cert.key
        - vault-server.hcl
    3. Navigate to the directory where the above files are located.
    4. Run the Vault server with:
        vault server -dev -dev-root-token-id root -dev-tls
    5. Access the Vault URL locally at:
        - http://127.0.0.1:8200
    6. Use the token:
        - Default: root
        - Otherwise: Check logs or documentation

Parts of Vault (Topic-wise)

  Vault Section

    1. Secret Engines

      1.1 You can create many Secret Engine Types:

        - 1.1.1 Generic
          - KV
          - PKI Certificates
          - SSH
          - Transit
          - TOTP
          - LDAP
          - Kubernetes

        1.1.2 Cloud
          - AWS
          - Azure
          - GCP
          - AliCloud

        1.1.3 Infra
          - Database
          - RabbitMQ
          - Cassandra
          - Consul

    2. Access
      - Manage access methods (e.g., tokens, identities)
      - Configure authentication backends (GitHub, LDAP, etc.)

    3. Policies
      - Define permissions using HCL or JSON
      - Attach policies to tokens, identities, or groups

    4. Tools
      - Vault CLI
      - Vault UI
      - Vault Agent
      - Templates and auto-auth

  Monitor Section

    1. Client Count
    2. Seal Vault
    3. View Logs
    4. Performance Metrics
