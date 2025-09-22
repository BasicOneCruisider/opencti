# 🛡️ OpenCTI - Cyber Threat Intelligence Platform

Welcome to the **OpenCTI** repository!  
This project provides a collaborative platform for managing, analyzing, and sharing Cyber Threat Intelligence (CTI).

---

## 🚀 Project Purpose

OpenCTI aims to centralize and structure cyber threat information, making it easier for security teams, analysts, and partners to leverage intelligence.

- **Collection**: Integrate multiple data sources (connectors).
- **Analysis**: Visualize and correlate threats.
- **Sharing**: Distribute indicators and reports to stakeholders.

---

## 🏗️ Architecture

The project uses **Docker Compose** to orchestrate the following services:

- **OpenCTI**: Main platform (Node.js)
- **Elasticsearch**: Search and indexing engine
- **Redis**: Cache and queue management
- **MinIO**: S3-compatible object storage
- **RabbitMQ**: Message broker for connectors
- **Connectors**: Import/export and enrichment modules (CrowdSec, STIX, CSV, TXT, etc.)

---

## 📦 Quick Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/BasicOneCruisider/opencti.git
   cd opencti
   ```

2. **Configure environment variables**  
   Edit the `.env` file to set passwords, tokens, and API keys for your environment.

3. **Start the platform**

   ```bash
   docker compose up -d
   ```

4. **Access the interface**  
   Open [http://localhost:8080](http://localhost:8080) in your browser.

---

## 🔌 Available Connectors

- **CrowdSec**: Enrich IP addresses with CrowdSec CTI
- **Export STIX/CSV/TXT**: Export data in various formats
- **Import STIX/Document**: Import structured and unstructured files
- **Worker**: Asynchronous task processing

---

## ⚙️ Configuration

- Set passwords and tokens in the `.env` file
- Docker volumes ensure data persistence
- Exposed ports allow access to web interfaces and APIs

---

## 📝 Contribution

Contributions are welcome!  
Feel free to open an issue or pull request to suggest improvements or report bugs.

---

## 📚 Documentation

- [OpenCTI Official Documentation](https://www.opencti.io/docs)
- [Docker Compose](https://docs.docker.com/compose/)
- [CrowdSec CTI](https://www.crowdsec.net/)

---

## 💡 Best Practices

- Change all default passwords and tokens before production
- Use a dedicated Docker network to isolate services
- Regularly back up your data volumes

---

## 🛠️ License

This project is distributed under the MIT license.

---

## 🤝 Acknowledgements

Thanks to all contributors and the OpenCTI community!  
For any questions, contact us via GitHub.

---
