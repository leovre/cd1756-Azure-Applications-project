# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

For deploying the CMS app, Azure App Service (PaaS) is the most appropriate choice over a Virtual Machine (VM). App Service offers lower total cost of ownership since Azure handles patching, scaling, and availability, removing the need for manual OS maintenance. It integrates seamlessly with GitHub Actions for continuous deployment, supports scaling through autoscale rules, and provides deployment slots for zero-downtime updates. With managed features like automatic backups, logging, and secure configuration through environment variables and Key Vault, App Service allows developers to focus on the application rather than infrastructure management. It is also cost-effective for typical web applications like this Flask-based CMS that relies on Azure SQL and Blob Storage, offering strong performance and high availability with minimal configuration.

A VM-based solution would only be justified if the app required deep OS-level control, background services beyond HTTP workloads, or custom network configurations. For example, if the CMS app needed to run custom system services, specialized drivers, or legacy software that cannot operate in App Service’s managed environment, a VM or VM Scale Set would be more suitable. Otherwise, App Service provides the ideal balance of scalability, security, and simplicity for deploying and maintaining the CMS application efficiently in Azure.

