# Toolset

Veracode



[to start of metadata](https://confluence.investorsgroup.com/display/IDT/Cloud+Native+Developer+Tools%3A+AWS+vs+Azure+vs+GCP#page-metadata-start)

AWS: [https://aws.amazon.com/products/developer-tools/](https://aws.amazon.com/products/developer-tools/)

Azure: [https://azure.microsoft.com/en-us/tools/](https://azure.microsoft.com/en-us/tools/)

Google: [https://cloud.google.com/tools/docs/](https://cloud.google.com/tools/docs/)

<table>
  <thead>
    <tr>
      <th style="text-align:left">AWS</th>
      <th style="text-align:left">Azure</th>
      <th style="text-align:left">GCP</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <ul>
          <li>Cloud9</li>
          <li>CodeStar</li>
          <li>X-Ray</li>
          <li>CodeCommit</li>
          <li>CodePipeline</li>
          <li>CodeBuild</li>
          <li>CodeDeploy</li>
        </ul>
      </td>
      <td style="text-align:left">
        <ul>
          <li>Visual Studio Code</li>
          <li>Azure SDK</li>
          <li>Azure Powershell</li>
          <li>Azure Command Line Interface</li>
          <li>Storage Explorer</li>
          <li>Docker Tools</li>
          <li>Azure Service Fabric Tools</li>
        </ul>
      </td>
      <td style="text-align:left">
        <ul>
          <li>Cloud SDK</li>
          <li>Cloud Shell</li>
          <li>Cloud Build</li>
          <li>Container Registry</li>
          <li>Cloud Source Repositories</li>
          <li>Cloud Deployment Manager</li>
          <li>Cloud Tools for Visual Studio</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

* Aws More comprehensive services. Highly integrated tools.
* Microsoft split Visual Studio Team Services into Azure Devops, with multiple components. each component can now be adopted independently.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Lifecycle</th>
      <th style="text-align:left"></th>
      <th style="text-align:left">AWS</th>
      <th style="text-align:left">Azure</th>
      <th style="text-align:left">GCP</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Planning</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">IDE</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p><em><b>Cloud9</b> :</em>
        </p>
        <ul>
          <li>Cloud Based - Easy remote access.</li>
          <li>Can be used a bit like google docs - real time collaboration</li>
          <li>Terminal access to AWS services</li>
        </ul>
      </td>
      <td style="text-align:left">Visual Studio Code</td>
      <td style="text-align:left">
        <ul>
          <li>Cloud Tools for IntelliJ</li>
          <li>Cloud Tools for Eclipse</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Source Code Management</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p><b>CodeCommit</b>
        </p>
        <ul>
          <li>The service automatically scales to meet the growing needs of your project.</li>
        </ul>
      </td>
      <td style="text-align:left"><b>Azure Repos</b>
      </td>
      <td style="text-align:left">
        <p><a href="https://cloud.google.com/source-repositories/docs/">Cloud Source Repositories</a>
        </p>
        <ul>
          <li>Free Unlimited Private repositories</li>
          <li>Existing Bit bucket, git hub etc can be mirrored.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Build Tools</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p><b>CodeBuild</b>
        </p>
        <ul>
          <li>multiple builds can be processed concurrently</li>
          <li>Access to both prepackaged build environments, as well as support for
            third party build tools.</li>
          <li>Supports Jenkins integration</li>
        </ul>
      </td>
      <td style="text-align:left"><a href="https://docs.microsoft.com/en-us/azure/devops/user-guide/what-happened-vsts"><em>Azure DevOps Services</em></a>
      </td>
      <td style="text-align:left">
        <p><b>Cloud Build</b>
        </p>
        <ul>
          <li>Build Triggers support.</li>
          <li>Support for custom plugins</li>
          <li>Docker Support</li>
          <li>Local builds supported</li>
          <li>Claims easier debugging with greater insight into build errors and warnings.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Deployment Tools</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p><b>CodeDeploy</b>
        </p>
        <ul>
          <li>deployments to Amazon EC2 instances, on-premises instances, or serverless
            Lambda functions</li>
        </ul>
        <p><b>CloudFormation</b>
        </p>
        <ul></ul>
      </td>
      <td style="text-align:left"><a href="https://docs.microsoft.com/en-us/azure/devops/user-guide/what-happened-vsts"><em>Azure DevOps Services</em></a>
      </td>
      <td style="text-align:left">
        <p><b>Cloud Deployment Manager</b>
        </p>
        <ul>
          <li>specify all the resources needed for application in a declarative format
            <br
            />
            <br />
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">CI/CD tool</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p><b>CodePipeline</b>
        </p>
        <p>-Support for Custom Plugins for jobs</p>
      </td>
      <td style="text-align:left">
        <p><a href="https://docs.microsoft.com/en-us/azure/devops/user-guide/what-happened-vsts"><em>Azure DevOps Services</em></a><em> -</em> Pipelines</p>
        <ul>
          <li>Native container support for builds</li>
          <li>Supports deployment to Third Party cloud platforms.</li>
        </ul>
      </td>
      <td style="text-align:left"><a href="https://cloud.google.com/solutions/continuous-delivery/">GCP Continuous Delivery</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Project Management</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p><b>Codestar</b>
        </p>
        <ul>
          <li>Built in integration with JIRA.</li>
          <li>Manage user Access</li>
          <li>Access to project building, testing and deployment pipeline templates</li>
          <li>Dashboard for easy monitoring of all stages (commits, builds, tests, deployment)</li>
        </ul>
      </td>
      <td style="text-align:left">
        <p><a href="https://docs.microsoft.com/en-us/azure/devops/user-guide/what-happened-vsts"><em>Azure DevOps Services</em></a>
        </p>
        <p>Azure Boards</p>
        <ul>
          <li>a work tracking system with Kanban boards, dashboards, reporting</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Testing</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p><b>X-Ray</b>
        </p>
        <p>-provides an end-to-end view of requests as they travel through your application</p>
      </td>
      <td style="text-align:left">
        <p><a href="https://docs.microsoft.com/en-us/azure/devops/user-guide/what-happened-vsts"><em>Azure DevOps Services</em></a>
        </p>
        <p><b>Test Plans</b>
        </p>
        <ul>
          <li>Third party services can be used.</li>
          <li>Supports manual collaborative testing as well as continuous testing and
            load testing.</li>
        </ul>
      </td>
      <td style="text-align:left">
        <p><b>Stack driver</b>  <b>Debugger</b>
        </p>
        <ul>
          <li>capture the call stack and variables at any location in your source code,
            in real time, with no impact on users.</li>
          <li>Easily share a debugging session with team
            <br /><b><br /></b>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Monitoring</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p><b>CloudWatch</b>
        </p>
        <ul>
          <li>collects monitoring and operational data in the form of logs, metrics,
            and events, providing you with a unified view of AWS resources, applications
            and services that run on AWS, and on-premises servers</li>
        </ul>
      </td>
      <td style="text-align:left">
        <p><b>Azure Monitor</b>
        </p>
        <ul>
          <li>Provides alerts, customizable dashboard</li>
        </ul>
        <p><b>Azure Advisor</b>
        </p>
        <ul>
          <li>Automatically gives advice to improve performance, security</li>
        </ul>
        <p><b>Application Insights</b>
        </p>
        <ul>
          <li>Deep Infrastructure Monitoring</li>
          <li>Log Analytics, Management solutions, Network Monitoring</li>
        </ul>
      </td>
      <td style="text-align:left">
        <p><b>Cloud Endpoints</b>
        </p>
        <ul>
          <li>Tool for Managing APIs</li>
        </ul>
        <p><b>Cloud Console - Includes Mobile app</b>
        </p>
        <ul>
          <li>Overview of app, requests, status, stats, billing information, etc.</li>
        </ul>
        <p><b>Stackdriver Monitoring</b>
        </p>
        <ul>
          <li>Supports AWS - monitors cloud resources.</li>
          <li>Provides a visual platform to identify trends and prevent issues</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>