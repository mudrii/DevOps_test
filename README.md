# Cloud SRE Test

## Conditions for the test

- [Pulumi 2.X](https://www.pulumi.com/)
- [AWS](https://aws.amazon.com/), [GCP](https://cloud.google.com/) or [Azure](https://portal.azure.com) select one

### Current configuration

#### Application for web/mobile chat using WebSockets

![](/Images/OnPrem.png)

### Resource

1. DNS Server with zone for app.com
2. Nginx A Server
   1. Reverse Proxy
   2. URL redirect based on URI
   3. Listening on TCP/IP port 80
   4. redirect https://app.com/ to Nginx B Web Server
   5. redirect https://app.com/api/ to Node.js server
3. Nginx B Web Server serving static webpages "index.html" and CSS
4. Node.js service for backend processing
5. Redis keeps clients connectivity state
6. MySql keeps user accounts

## Objective

- migrate application to any of the selected cloud providers AWS/GCP/Azure from OnPrem Data Centre
- Application on the selected cloud provider should be Highly Available
- Application on the selected cloud provider should be Scalable
- Application on the selected cloud provider should be Highly Fault Tolerant

### Architect and Design new application diagram for Cloud Native Implementation

- Present Diagram in Draw.io
- Present few options
- From multiple option use one option and develop infrastructure as code in [Pulumi Python SDK](https://github.com/pulumi/pulumi/tree/master/sdk/python)

### Infrastructure as a code requirements

- Code should be modular
- Code should be testable
- Code should contain comments and in documentation

### Pulumi reference documentation

- [Pulumi Python](https://www.pulumi.com/docs/intro/languages/python/)
- [Pulumi Python SDK](https://pypi.org/project/pulumi/)
- [Pulumi API AWS Reference](https://www.pulumi.com/docs/reference/pkg/aws/)
- [Pulumi API GCP Reference](https://www.pulumi.com/docs/reference/pkg/gcp/)
- [Pulumi API Azure Reference](https://www.pulumi.com/docs/reference/pkg/azure/)
- [Pulumi Tutorials](https://www.pulumi.com/docs/tutorials/)