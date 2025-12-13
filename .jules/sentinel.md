## 2024-05-23 - Overly Permissive CORS Configuration
**Vulnerability:** The backend application (`database_handler`) was configured to allow Cross-Origin Resource Sharing (CORS) from any origin (`*`). This configuration exposes the application to potential attacks where malicious websites could make unauthorized requests to the backend on behalf of authenticated users (if authentication were to be added, or for Intranet sites).

**Learning:** Hardcoding security configurations like CORS origins is risky because it defaults to insecure settings (often for convenience during development) and is easily forgotten before production. Using environment variables allows for flexible and secure configuration across different environments (dev, staging, prod).

**Prevention:**
1. Avoid using wildcard (`*`) for CORS `AllowOrigins` in production.
2. Configure allowed origins via environment variables (e.g., `DH_ALLOWED_ORIGINS`).
3. Set sensible defaults that are restrictive, or require explicit configuration.
4. Document the required environment variables for security settings.
