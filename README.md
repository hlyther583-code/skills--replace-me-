Docker Hardened Images (DHIs) are designed to provide secure, minimal, and compliant container images for modern development and production environments. Here’s how they work:

- **Minimal by Design:** DHIs include only the essential libraries and binaries needed for their specific purpose, whether for development, SDK builds, or production runtime. This reduces image size and limits the attack surface, making containers more secure and efficient.
- **Immutable and Non-root:** Images are fixed at build time, with no runtime installations. Containers run as an unprivileged user by default, further enhancing security.
- **Distroless Approach:** DHIs often use a distroless model, excluding unnecessary OS components like shells and package managers. This can reduce the attack surface by up to 95% and improve performance.
- **Continuous Maintenance:** All DHIs are continuously monitored, patched, and updated to maintain near-zero known exploitable CVEs, helping teams avoid patch fatigue.
- **Compliance and Transparency:** Each image includes cryptographically signed metadata, SBOMs (Software Bill of Materials), VEX documents (Vulnerability Exploitability eXchange), and build provenance, supporting compliance and supply chain security.
- **SLSA-Compliant Builds:** DHIs are built to meet SLSA Build Level 3, ensuring a tamper-resistant, verifiable, and auditable build process.
- **Compatibility:** While minimal, DHIs maintain compatibility with common Linux distributions, supporting both musl libc (Alpine-based) and glibc (Debian-based) images.

In summary, Docker Hardened Images provide a secure foundation by minimizing included software, enforcing non-root execution, and delivering continuous updates and compliance-ready metadata.

Sources:
- [https://docs.docker.com/dhi/explore/what/](https://docs.docker.com/dhi/explore/what/)
- [https://docs.docker.com/dhi/core-concepts/hardening/](https://docs.docker.com/dhi/core-concepts/hardening/)
- [https://www.docker.com/blog/unlimited-access-to-docker-hardened-images-because-security-should-be-affordable-always/](https://www.docker.com/blog/unlimited-access-to-docker-hardened-images-because-security-should-be-affordable-always/)