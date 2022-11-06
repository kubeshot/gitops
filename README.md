# ⚙️ GitOps

GitOps is a set of best practices where the entire code delivery process is controlled via Git, including infrastructure and application definition as code and automation to complete updates and rollbacks.

The core idea of GitOps is to have a git repository that contains declarative descriptions of the desired infrastructure in the production environment and has an automated process to make the production environment match the state described in that repository.

Now that we know the central idea, let's go back a little bit to the acronym GitOps and let's understand the role of git, the role of ops and how they meet.

The Key GitOps Principles:

- The entire system (infrastructure and applications) is described declaratively.
- The canonical desired system state is versioned in Git.
- Changes approved are automated and applied to the system.
- Software agents ensure correctness and alert on divergence.



New users to GitOps and Argo CD are not often sure how they should structure their repos, add applications, promote apps across environments, and manage the Argo CD installation itself using GitOps.



Argo CD automates the deployment of the desired application states in the specified target environments. Application deployments can track updates to branches, tags, or pinned to a specific version of manifests at a Git commit. See tracking strategies for additional details about the different tracking strategies available.

### <img align="left" alt="Git" width="18px" src="https://cncf-branding.netlify.app/img/projects/argo/icon/color/argo-icon-color.svg" /> [Argo Events](https://argoproj.github.io/argo-events/)

Argo Events is an event-driven workflow automation framework for Kubernetes which helps you trigger K8s objects, Argo Workflows, Serverless workloads, etc. on events from a variety of sources like webhooks, S3, schedules, messaging queues, gcp pubsub, sns, sqs, etc.

### <img align="left" alt="Git" width="18px" src="https://cncf-branding.netlify.app/img/projects/argo/icon/color/argo-icon-color.svg" /> [Argo Rollouts](https://argoproj.github.io/argo-rollouts/)

Argo Rollouts is a Kubernetes controller and set of CRDs which provide advanced deployment capabilities such as blue-green, canary, canary analysis, experimentation, and progressive delivery features to Kubernetes.

Argo Rollouts (optionally) integrates with ingress controllers and service meshes, leveraging their traffic shaping abilities to gradually shift traffic to the new version during an update. Additionally, Rollouts can query and interpret metrics from various providers to verify key KPIs and drive automated promotion or rollback during an update.

### <img align="left" alt="Git" width="18px" src="https://cncf-branding.netlify.app/img/projects/argo/icon/color/argo-icon-color.svg" /> [Argo Workflows](https://argoproj.github.io/argo-workflows/)

Argo Workflows is an open source container-native workflow engine for orchestrating parallel jobs on Kubernetes. Argo Workflows is implemented as a Kubernetes CRD (Custom Resource Definition).



### 🛠️ Required Tools

|      Tools       | Version |
| :--------------: | :-----: |
|     kubectl      | v1.22.3 |
| argocd-autopilot | v0.2.28 |

### 🌳 Project Structure

````bash
.
├── apps
    ├── backstage
    ├── crossplane

````
