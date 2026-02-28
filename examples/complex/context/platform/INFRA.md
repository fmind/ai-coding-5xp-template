# Infrastructure Architecture

**Provider**: Vercel (Frontend) / AWS (Backend)

## Edge Computing

- **CDN for Assets**: All product images and static assets must be served via a high-performance Content Delivery Network (CDN) to ensure sub-100ms load times globally.
- **Edge Functions**: Use Edge Functions for fast, personalized operations like Geo-IP blocking or initial a/b test splitting before the main request hits the origin server.

## Compute Layer

- **Frontend Hosting**: Vercel handles the Next.js application, leveraging Server-Side Rendering (SSR) for robust SEO on product detail pages.
- **Backend Containers**: The Django backend is containerized via Docker and orchestrated on AWS ECS (Elastic Container Service) for scalable, reliable compute.
- **Background Workers**: Asynchronous tasks (like low-stock alerts or sending receipt emails) are processed via Celery/Redis workers running on separate compute nodes.

## Data Layer

- **Primary Database**: Amazon RDS (PostgreSQL) is the source of truth for all transactional data (orders, users).
- **Search Engine**: Algolia is used to power lightning-fast, typo-tolerant product searches across the catalog.
- **Caching**: Redis is utilized heavily for caching expensive database queries and managing session state.

## Security & Reliability

- **WAF**: AWS WAF is active to protect against common web exploits and massive bot traffic during flash sales.
- **Multi-AZ**: Critical database instances are deployed across Multiple Availability Zones (Multi-AZ) to prevent single points of failure.
- **Secrets Management**: All sensitive credentials (e.g., Stripe API keys, database passwords) are managed via AWS Secrets Manager and never hardcoded.

## Monitoring & Observability

- **APM**: Datadog is configured for end-to-end Application Performance Monitoring.
- **Log Aggregation**: Application logs are streamed to CloudWatch for centralized debugging.
- **Alerting**: PagerDuty automatically alerts the on-call engineer for critical errors (e.g., payment gateway failures).
