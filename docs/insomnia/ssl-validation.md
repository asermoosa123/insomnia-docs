---
layout: article-detail
title:  SSL Validation
category: Support
category-url: support
---

Have you seen certificate errors like these?

```
Error: unable to verify the first certificate
```

```
Error: Hostname/IP doesn't match certificate's altnames: "Host: schier.co. is not in the cert's altnames: DNS:*.surge.sh, DNS:surge.sh"
```

If you are testing on a local development server, or know that the certificate is invalid, you can disable validation in the settings by deselecting the **Validate SSL Certificates** option.