# Security tools

{% embed url="https://github.com/aws-quickstart/quickstart-compliance-cis-benchmark" %}

{% embed url="https://aws-quickstart.github.io/" %}

{% embed url="https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf" %}



{% embed url="https://github.com/SecurityFTW/cs-suite" %}



{% embed url="https://www.marcolancini.it/2018/blog-arsenal-cloud-native-security-tools/" %}



{% embed url="https://www.offensive-security.com/information-security-certifications/oscp-offensive-security-certified-professional/" %}

## Docker <a id="docker"></a>

#### Auditing Tools <a id="auditing-tools"></a>

| Name | Description |
| :--- | :--- |
| [Docker Bench](https://github.com/docker/docker-bench-security) | Checks for common best-practices around deploying Docker containers in production. Based on the [CIS Docker Community Edition Benchmark v1.1.0](https://benchmarks.cisecurity.org/tools2/docker/CIS_Docker_Community_Edition_Benchmark_v1.1.0.pdf).   |
| [Clair](https://github.com/coreos/clair) | Scan Docker images for security vulnerabilities \(static analysis\). I personally found it not straightforward to setup, so I ended up creating my own `docker-compose` to spin up `Clair`, alongside `Postgres` and `Klar`. For usage, see my [`docker_compose_clair`](https://github.com/marco-lancini/offensive-infrastructure/tree/master/templates/docker/docker_compose_clair) repo. |
| [Dockscan](https://github.com/kost/dockscan) | Scan Docker installations for security issues and vulnerabilities.   |
| [dive](https://github.com/wagoodman/dive) | A tool for exploring each layer in a docker image.   |

#### Privilege Escalation <a id="privilege-escalation"></a>

| Name | Description |
| :--- | :--- |
| [dockerrootplease](https://github.com/chrisfosterelli/dockerrootplease) | Gives you root on the host OS, if you're a member of the "docker" group |
| [docker-rootshell](https://github.com/gtank/docker-rootshell) | Abuses membership in the "docker" group to drop a root shell in the current working directory. |
| [docker-escalate](https://github.com/KrustyHack/docker-privilege-escalation) | Same concept as above. |
| Manual |  |

## Kubernetes <a id="kubernetes"></a>

#### Auditing Tools <a id="auditing-tools-1"></a>

| Name | Description |
| :--- | :--- |
| [kube-bench](https://github.com/aquasecurity/kube-bench) | Checks whether Kubernetes is deployed according to security best practices. Based on the [CIS Kubernetes Benchmark](https://www.cisecurity.org/benchmark/kubernetes/). |
| [kube-hunter](https://github.com/aquasecurity/kube-hunter) | Hunt for security weaknesses in Kubernetes clusters \(even remote\). |
| [KubiScan](https://github.com/cyberark/KubiScan) | Scan for risky permissions and users in Kubernetes Role-Based Access Control \(RBAC\) authorization model. It can detect accounts which will expose the whole cluster if their identification \(JWT token, certificate, etc.\) is compromised by an attacker. |
| [kubeaudit](https://github.com/Shopify/kubeaudit) | Audit clusters against common security controls. |
| [kubesec](https://github.com/Shopify/kubeaudit) | Quantify risk for Kubernetes resources. |
| [kube-auto-analyzer](https://github.com/nccgroup/kube-auto-analyzer) | Configuration analyzer to automate the process of reviewing Kubernetes installations against the CIS Kubernetes Benchmark. |

## AWS <a id="aws"></a>

#### Basic Tools <a id="basic-tools"></a>

| Name | Description |
| :--- | :--- |
| [aws-cli](https://github.com/aws/aws-cli) | Universal Command Line Interface for AWS, used by basically any other tool. |
| [aws-shell](https://github.com/awslabs/aws-shell) | Interactive shell for AWS \(with autocompletion, etc.\). |

#### Inventory Tools <a id="inventory-tools"></a>

| Name | Description |
| :--- | :--- |
| [aws-inventory](https://github.com/nccgroup/aws-inventory) | Make an inventory of all your resources across regions. |
| [Resource Counter](https://github.com/disruptops/resource-counter) | Counts number of resources in categories across regions. |
| [aws\_public\_ips](https://github.com/arkadiyt/aws_public_ips) | Fetch all public IP addresses tied to your AWS account. |

#### Auditing Tools <a id="auditing-tools-2"></a>

| Name | Description |
| :--- | :--- |
| [CS-Suite](https://github.com/SecurityFTW/cs-suite) | Auditing the security posture of AWS/GCP/Azure infrastructure. Includes Scout2, Prowler, AWS Trusted Advisor, etc. Permissions required: `SecurityAudit` |
| [CloudSploit](https://github.com/cloudsploit/scans) | Returns a series of potential misconfigurations and security risks. Permissions required: `SecurityAudit` |
| [AWS Security Benchmark](https://github.com/awslabs/aws-security-benchmark) | Script to evaluate your AWS account against the full CIS Amazon Web Services Foundations Benchmark 1.1. |
| [S3Scan](https://github.com/bear/s3scan) | Generate a report of all S3 buckets and their permissions \(authenticated\). |
| [CloudMapper](https://github.com/duo-labs/cloudmapper) | Analyze AWS environments by creating network diagrams \(and more\). Permissions required: `ReadOnlyAccess, SecurityAudit` |
| [PMapper](https://github.com/nccgroup/PMapper) | Advanced and Automated AWS IAM Evaluation. Permissions required: `ReadOnlyAccess` |
| [Scout2](https://github.com/nccgroup/Scout2) | Security auditing. Already included in `CS-Suite`. Permissions required: `ReadOnlyAccess, SecurityAudit` |
| [Prowler](https://github.com/toniblyx/prowler) | CIS benchmarks and additional checks for security best practices in AWS. Already included in `CS-Suite`. Permissions required: `SecurityAudit` |

#### Offensive Tools <a id="offensive-tools"></a>

<table>
  <thead>
    <tr>
      <th style="text-align:left">Name</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><a href="https://github.com/RhinoSecurityLabs/pacu">Pacu</a>
      </td>
      <td style="text-align:left">AWS penetration testing toolkit, designed for offensive security testing
        against cloud environments. Current modules enable a range of attacks,
        including user privilege escalation, backdooring of IAM users, attacking
        vulnerable Lambda functions, etc.</td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="https://github.com/andresriancho/nimbostratus">Nimbostratus</a>
      </td>
      <td style="text-align:left">Tools for fingerprinting and exploiting Amazon cloud infrastructures.</td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="https://github.com/carnal0wnage/weirdAAL">weirdALL</a>
      </td>
      <td style="text-align:left">AWS Attack Library.</td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="https://github.com/sa7mon/S3Scanner">S3Scanner</a>
      </td>
      <td style="text-align:left">Scan for open AWS S3 buckets and dump the contents.</td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="https://github.com/prevade/cloudjack">Cloudjack</a>
      </td>
      <td style="text-align:left">CloudJack assesses AWS accounts for subdomain hijacking vulnerabilities
        as a result of decoupled Route53 and CloudFront configurations.</td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="https://github.com/dagrz/aws_pwn">AWS PWN</a>
      </td>
      <td style="text-align:left">
        <p>A collection of AWS penetration testing scripts:</p>
        <ul>
          <li>Reconnaissance</li>
          <li>Exploration</li>
          <li>Elevation</li>
          <li>Persistence</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>#### Training Apps <a id="training-apps"></a>

| Name | Description |
| :--- | :--- |
| [flAWS](http://flaws.cloud/) | Challenge that, through a series of levels, teaches common mistakes and gotchas when using AWS. It also has some "public" credentials you can use to try your tools against: |
| [Cloudgoat](https://github.com/RhinoSecurityLabs/cloudgoat) | Vulnerable by Design AWS infrastructure setup tool. There are also some [writeups](https://medium.com/@rzepsky/playing-with-cloudgoat-part-1-hacking-aws-ec2-service-for-privilege-escalation-4c42cc83f9da) available. |
| [DVCA](https://github.com/m6a-UdS/dvca) | Damn Vulnerable Cloud Application. |
| [nimbostratus-target](https://github.com/andresriancho/nimbostratus-target) | This repository holds a target infrastructure you can use for testing nimbostratus. |

## GCP <a id="gcp"></a>

#### Basic Tools <a id="basic-tools-1"></a>

| Name | Description |
| :--- | :--- |
| [gcloud](https://cloud.google.com/sdk/gcloud/) | Command Line Interface for GCP. |

#### Auditing Tools <a id="auditing-tools-3"></a>

| Name | Description |
| :--- | :--- |
| [G-Scout](https://github.com/nccgroup/G-Scout) | Auditing GCP configurations. Permissions required on the projects: `Viewer, Security Reviewer, Stackdriver Account Viewer` |
| [ScoutSuite](https://github.com/nccgroup/ScoutSuite) | Multi-cloud security auditing tool. Permissions required on the projects: `Viewer, Security Reviewer, Stackdriver Account Viewer` |
| [gcp-audit](https://github.com/spotify/gcp-audit) | Takes a set of projects and audits them for common issues as defined by its ruleset. |
| [gcp-iam-collector](https://github.com/marcin-kolda/gcp-iam-collector) | Python script for collecting and visualising Google Cloud Platform IAM permissions. |
| [CS-Suite](https://github.com/SecurityFTW/cs-suite) | Auditing the security posture of AWS/GCP/Azure infrastructure. Can be overlooked as it relies on G-Scout. Permissions required on the projects: `Viewer, Security Reviewer, Stackdriver Account Viewer` |

#### Offensive Tools <a id="offensive-tools-1"></a>

| Name | Description |
| :--- | :--- |
| [GCPBucketBrute](https://github.com/RhinoSecurityLabs/GCPBucketBrute) | Enumerate Google Storage buckets, determine what access you have to them, and determine if they can be privilege escalated. |

## GIT <a id="git"></a>

| Name | Description |
| :--- | :--- |
| [git-secrets](https://github.com/awslabs/git-secrets) | Prevents you from committing secrets and credentials into git repositories. |
| [Gitrob](https://github.com/michenriksen/gitrob) | Reconnaissance tool for GitHub organizations. |
| [Gitleaks](https://github.com/zricethezav/gitleaks) | Searches full repo history for secrets and keys. |
| [TruffleHog](https://github.com/dxa4481/truffleHog) | Searches through git repositories for high entropy strings and secrets. |

[About the Author](https://www.marcolancini.it/about)  


