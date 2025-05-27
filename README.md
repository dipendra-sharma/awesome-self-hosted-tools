# Awesome Self-Hosted Tools 🚀

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Docker](https://img.shields.io/badge/Docker-Ready-blue.svg)](https://docker.com)
[![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-orange.svg)](CONTRIBUTING.md)

> A curated list of **44 awesome open-source, self-hosted tools** with ready-to-use Docker Compose configurations. Take control of your data and infrastructure with these free alternatives to popular SaaS services.

All tools are production-ready, include latest 2024 versions, and come with comprehensive documentation and setup instructions.

## 📋 Quick Index

**Total Tools: 44** | **Categories: 11** | **Port Range: 8300-8641**

## 🗂️ **Directory Structure**

```
tools/
├── development/           # 19 Development & Infrastructure Tools
│   ├── ci-cd/            # Jenkins
│   ├── git-repositories/ # GitLab, Gitea
│   ├── monitoring/       # Prometheus, Grafana, SigNoz, Sentry, Jaeger
│   ├── containers/       # Portainer
│   ├── proxy-networking/ # Traefik
│   ├── file-storage/     # Nextcloud
│   ├── security/         # Vaultwarden
│   ├── messaging-streaming/ # Kafka
│   ├── workflow-automation/ # Temporal, Huginn, n8n
│   ├── documentation/    # BookStack
│   └── media-management/ # Jellyfin, PhotoPrism
└── business/             # 25 Business & Marketing Tools
    ├── cms-publishing/   # WordPress, Ghost, Strapi
    ├── email-marketing/  # Mautic, Listmonk, SendPortal, Mailcow
    ├── customer-support/ # Chatwoot, FreeScout, Zammad
    ├── crm-database/     # NocoDB
    ├── social-media/     # Postiz, Socioboard
    ├── seo-automation/   # SerpBear, Serposcope
    ├── forums-community/ # Discourse
    ├── e-commerce/       # Magento
    ├── analytics/        # PostHog, Umami, Matomo, Metabase
    ├── project-management/ # Focalboard
    └── communication/    # WPPConnect, PlaySMS, OpenWA
```

---

## 🔧 **Development & Infrastructure Tools (19)**

### **CI/CD & Automation**
| Tool | Location | Port(s) | Description |
|------|----------|---------|-------------|
| **Jenkins** | `development/ci-cd/jenkins/` | 8600-8601 | Leading CI/CD automation server |

### **Git Repositories**
| Tool | Location | Port(s) | Description |
|------|----------|---------|-------------|
| **GitLab** | `development/git-repositories/gitlab/` | 8511-8513 | Complete DevOps platform |
| **Gitea** | `development/git-repositories/gitea/` | 8514-8515 | Lightweight Git server |

### **Monitoring & Observability**
| Tool | Location | Port(s) | Description |
|------|----------|---------|-------------|
| **Prometheus** | `development/monitoring/prometheus/` | 8602-8604 | Time-series monitoring stack |
| **Grafana** | `development/monitoring/grafana/` | 8605 | Visualization dashboards |
| **SigNoz** | `development/monitoring/signoz/` | 8629-8631 | Open source Datadog alternative |
| **Sentry** | `development/monitoring/sentry/` | 8632 | Error tracking and performance monitoring |
| **Jaeger** | `development/monitoring/jaeger/` | 8633-8640 | Distributed tracing system |

### **Containers & Orchestration**
| Tool | Location | Port(s) | Description |
|------|----------|---------|-------------|
| **Portainer** | `development/containers/portainer/` | 8516-8517 | Docker management interface |

### **Proxy & Networking**
| Tool | Location | Port(s) | Description |
|------|----------|---------|-------------|
| **Traefik** | `development/proxy-networking/traefik/` | 8611-8613 | Modern reverse proxy |

### **File Storage & Collaboration**
| Tool | Location | Port(s) | Description |
|------|----------|---------|-------------|
| **Nextcloud** | `development/file-storage/nextcloud/` | 8518 | File sync and collaboration |

### **Security & Identity**
| Tool | Location | Port(s) | Description |
|------|----------|---------|-------------|
| **Vaultwarden** | `development/security/vaultwarden/` | 8606 | Password manager |

### **Messaging & Streaming**
| Tool | Location | Port(s) | Description |
|------|----------|---------|-------------|
| **Kafka** | `development/messaging-streaming/kafka/` | 8616-8619 | Event streaming platform |

### **Workflow Automation**
| Tool | Location | Port(s) | Description |
|------|----------|---------|-------------|
| **Temporal** | `development/workflow-automation/temporal/` | 8620-8624 | Workflow orchestration |
| **Huginn** | `development/workflow-automation/huginn/` | 8403 | Workflow automation |
| **n8n** | `development/workflow-automation/n8n/` | 8404 | Visual workflow automation |

### **Documentation**
| Tool | Location | Port(s) | Description |
|------|----------|---------|-------------|
| **BookStack** | `development/documentation/bookstack/` | 8400 | Wiki-style documentation |

### **Media Management**
| Tool | Location | Port(s) | Description |
|------|----------|---------|-------------|
| **Jellyfin** | `development/media-management/jellyfin/` | 8607-8608 | Media server |
| **PhotoPrism** | `development/media-management/photoprism/` | 8609 | AI-powered photo management |

---

## 💼 **Business & Marketing Tools (25)**

### **CMS & Publishing**
| Tool | Location | Port(s) | Description |
|------|----------|---------|-------------|
| **WordPress** | `business/cms-publishing/wordpress/` | 8500 | World's most popular CMS |
| **Ghost** | `business/cms-publishing/ghost/` | 8501 | Modern publishing platform |
| **Strapi** | `business/cms-publishing/strapi/` | 8627 | Headless CMS |

### **Email Marketing & Server**
| Tool | Location | Port(s) | Description |
|------|----------|---------|-------------|
| **Mautic** | `business/email-marketing/mautic/` | 8300 | Email campaigns & automation |
| **Listmonk** | `business/email-marketing/listmonk/` | 8301 | Bulk email sending |
| **SendPortal** | `business/email-marketing/sendportal/` | 8628 | Newsletter design & management |
| **Mailcow** | `business/email-marketing/mailcow/` | 8502-8510 | Complete email server |

### **Customer Support**
| Tool | Location | Port(s) | Description |
|------|----------|---------|-------------|
| **Chatwoot** | `business/customer-support/chatwoot/` | 8302 | Live chat platform |
| **FreeScout** | `business/customer-support/freescout/` | 8303 | Help desk system |
| **Zammad** | `business/customer-support/zammad/` | 8641 | Open source help desk |

### **CRM & Database**
| Tool | Location | Port(s) | Description |
|------|----------|---------|-------------|
| **NocoDB** | `business/crm-database/nocodb/` | 8304 | Airtable-style CRM |

### **Social Media Management**
| Tool | Location | Port(s) | Description |
|------|----------|---------|-------------|
| **Postiz** | `business/social-media/postiz/` | 8626 | Social media automation |
| **Socioboard** | `business/social-media/socioboard/` | 8405 | Social media management |

### **SEO Automation**
| Tool | Location | Port(s) | Description |
|------|----------|---------|-------------|
| **SerpBear** | `business/seo-automation/serpbear/` | 8625 | Rank tracking |
| **Serposcope** | `business/seo-automation/serposcope/` | 8402 | Google rank tracking |

### **Forums & Community**
| Tool | Location | Port(s) | Description |
|------|----------|---------|-------------|
| **Discourse** | `business/forums-community/discourse/` | 8610 | Modern forum platform |

### **E-commerce**
| Tool | Location | Port(s) | Description |
|------|----------|---------|-------------|
| **Magento** | `business/e-commerce/magento/` | 8614-8615 | Enterprise e-commerce |

### **Analytics & Intelligence**
| Tool | Location | Port(s) | Description |
|------|----------|---------|-------------|
| **PostHog** | `business/analytics/posthog/` | 8519 | Product analytics |
| **Umami** | `business/analytics/umami/` | 8520 | Privacy-focused web analytics |
| **Matomo** | `business/analytics/matomo/` | Existing | Web analytics |
| **Metabase** | `business/analytics/metabase/` | Existing | Business intelligence |

### **Project Management**
| Tool | Location | Port(s) | Description |
|------|----------|---------|-------------|
| **Focalboard** | `business/project-management/focalboard/` | 8401 | Kanban boards |

### **Communication & Messaging**
| Tool | Location | Port(s) | Description |
|------|----------|---------|-------------|
| **WPPConnect** | `business/communication/wppconnect/` | 8406 | WhatsApp API |
| **PlaySMS** | `business/communication/playsms/` | 8407 | Bulk SMS campaigns |
| **OpenWA** | `business/communication/openwa/` | 8408 | WhatsApp bot automation |

---

## 🚀 Quick Start

### Prerequisites
- Docker & Docker Compose installed
- Ports 8300-8628 available
- At least 4GB RAM recommended

### Launch Any Tool
```bash
# Navigate to any tool directory
cd /path/to/tool/directory

# Start the service
docker compose up -d

# View logs
docker compose logs -f

# Stop the service
docker compose down
```

---

## 🎯 Use Cases

### **Startup Stack**
Essential tools for new businesses:
- WordPress (Website)
- Mautic (Email Marketing)
- Chatwoot (Customer Support)
- Umami (Analytics)
- Vaultwarden (Security)

### **Development Team**
Tools for software development:
- GitLab/Gitea (Code Management)
- Jenkins (CI/CD)
- Prometheus + Grafana (Monitoring)
- BookStack (Documentation)
- Nextcloud (File Sharing)

### **Marketing Agency**
Tools for marketing professionals:
- WordPress + Ghost (Content)
- Postiz (Social Media)
- SerpBear (SEO)
- Mautic (Email Marketing)
- PostHog (Analytics)

### **Enterprise Setup**
Comprehensive business solution:
- Magento (E-commerce)
- Mailcow (Email Server)
- Discourse (Community)
- Temporal (Workflows)
- Full monitoring stack

---

## 🔧 Configuration Notes

### Security Considerations
- **Change Default Passwords:** All tools with default credentials
- **Use HTTPS:** Configure SSL/TLS for production
- **Environment Variables:** Update secret keys and tokens
- **Network Security:** Use proper firewall rules

### Resource Requirements
- **Minimum:** 4GB RAM, 20GB storage
- **Recommended:** 8GB RAM, 50GB storage
- **Heavy Tools:** GitLab, Magento, PostHog require more resources

---

## 📊 Statistics

- **Total Tools:** 44
- **Categories:** 24
- **Docker Images:** Latest 2024 versions
- **Database Systems:** PostgreSQL, MySQL, MariaDB, SQLite, Redis
- **License Types:** MIT, GPL, AGPL, Apache 2.0
- **Architecture Support:** AMD64, ARM64 (where available)

---

**⭐ Star this repository if it's helpful!**

*Last Updated: 2024 - Maintained with latest Docker images and best practices.*
