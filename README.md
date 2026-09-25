# Cloud Resume on AWS

Online resume for Ruben Jimenez Uribe, hosted on AWS as a hands-on cloud project.

## Architecture

User → Route 53 (custom domain) → CloudFront (HTTPS, ACM certificate) → private S3 bucket (Origin Access Control)

_Diagram coming soon in `docs/`._

## Repository structure

site/ Static website (the only folder deployed to S3)
docs/ Architecture diagram and screenshots


## Deploy

```bash
aws s3 sync site/ s3://<bucket-name> --delete
```

## Credits

Template: [Start Bootstrap - Resume](https://startbootstrap.com/theme/resume), MIT License (see `LICENSE`).
