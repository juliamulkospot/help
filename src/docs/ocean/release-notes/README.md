# Ocean Release Notes

## July 2024: Features and Enhancements 

*  **OCN-0015: July 16, 2024:** (**<font color="#FC01CC">AKS</font>**)  As of July 16, 2024, Ocean Controller Version 2 for Azure Kubernetes (AKS) is officially released, bringing a host of new features and enhancements to streamline your operations.
[Learn More...](https://docs.spot.io/ocean/tutorials/ocean-controller-v2/)

* **OCN-0014: July 09, 2024:** (**<font color="#FC01CC">AWS Kubernetes</font>**) Ocean now lets you use recommendations to make informed decisions when selecting the best Availability Zones for launching instances in your Kubernetes cluster. [Learn More...](https://docs.spot.io/ocean/features/avail-zones-scores)


* **OCN-0013: July 08, 2024:** [Ocean Documentation Update] (**<font color="#FC01CC">AKS</font>**) We have added these new topics to the Ocean AKS documentation:
   * [Dense Mode and Node Pools](https://docs.spot.io/ocean/features/dense-mode-and-node-pools)
   * [Select VMs for an AKS Virtual Node Group](https://docs.spot.io/ocean/features/vm-selection-aks)
     
 

<details>
  <summary markdown="span">June, 2024 - click to view</summary>

## June 2024: Features and Enhancements 

*  **OCN-0012: June 27, 2024:** (**<font color="#FC01CC">GKE</font>**)  As of June 15, 2024, Ocean Controller Version 2 for Google Kubernetes (GKE) is officially released, bringing a host of new features and enhancements to streamline your operations.
[Learn More...](https://docs.spot.io/ocean/tutorials/ocean-controller-v2/)

*  **OCN-0011: June 24, 2024:** [Ocean Documentation Update] (**<font color="#FC01CC">AKS</font>**) We have updated the permissions documentation for using the Spot Ocean platform with AKS.
Review the latest [Spot Policy in Azure (AKS)](https://docs.spot.io/administration/api/spot-policy-aks-azure) and refer to [AKS Permissions](https://docs.spot.io/administration/api/aks-permissions-desc) for a description of the permissions required for AKS infrastructure and Azure RBAC-enabled Kubernetes clusters, to help you maximize the value of the Spot Ocean platform.

*  **OCN-0010: June 13, 2024:** (**<font color="#FC01CC">AKS</font>**) Ocean now supports AKS VNG (Virtual Node Groups) with Availability Zone set to null (Zone 0). Use this option independently or with other Availability Zones to seamlessly run workloads requiring PVC (Persistent Volume Claim), storage needs, and availability redundancy (AZ=null) within Ocean, with minimal configuration changes. [Learn more…](https://docs.spot.io/ocean/features/vngs/az-zero-feature)

* **OCN-0009: June 09, 2024:** (**<font color="#FC01CC">AKS</font>**)
Log Integration with Azure Blob for Ocean **AKS** is now available in the [Spot API](https://docs.spot.io/api/).
From now on, you can configure Ocean to export logs to an Azure Blob and then access the logs with a central monitoring tool.
Read and troubleshoot the Ocean logs in the same central interface where you access your other logs. 
[Learn more...](https://docs.spot.io/ocean/features/log-integration-with-azure-blob)

* **OCN-0008: June 09, 2024:** 
Spot has released EKSCTL [v0.180.0](https://github.com/spotinst/weaveworks-eksctl/releases/tag/v0.180.0).  
When you use this EKSCTL version to create Ocean clusters, [Ocean Controller Version 2](https://docs.spot.io/ocean/tutorials/ocean-controller-v2/.) is used.
>**Prerequisite**: Helm installed.

</details><br>


<details>
  <summary markdown="span">May, 2024 - click to view</summary>

## May 2024: Features and Enhancements

* **OCN-0007: May 27, 2024:** (**<font color="#FC01CC">AKS</font>**)
Workload Migration for Ocean **AKS** is now available in both the Ocean console and the Spot API (with new API calls) to make migrating your Kubernetes workloads to Ocean easier. Workload Migration automates draining and rescheduling pods, streamlining your **AKS** infrastructure migration to Ocean.
Seamlessly migrate and register your workloads into Ocean, and let Spot manage your Kubernetes environment.
[Learn more...](https://docs.spot.io/ocean/tutorials/migrate-workload-aks)

* **OCN-0006: May 27, 2024:** (**<font color="#FC01CC">AWS Kubernetes</font>**)
Ocean Controller Version 2 supports the `namespaceSelector` scaling constraint label introduced in Kubernetes Version 1,24. When you apply this label, Ocean's Autoscaler scales up nodes based on the Namespace selector to schedule pods. This option is available for **AWS** Kubernetes only.
[Learn more...](https://kubernetes.io/docs/concepts/scheduling-eviction/assign-pod-node/#namespace-selector) about the `namespaceSelector` label.

* **OCN-0005: May 16, 2024:** [Ocean Documentation Update]: 
This topic explains how to manage Virtual Node Groups (VNGs) when upgrading the Kubernetes version for your clusters. The recommended approach is to automatically upgrade the control plane to the latest K8s version while keeping the data plane's VNGs running on a minor Kubernetes version until fully validating them for the latest K8s version.
[Learn more…](https://docs.spot.io/ocean/tips-and-best-practices/vng-minor-versions?id=configure-a-minor-k8s-version-for-a-virtual-node-group)

* **OCN-0004: May 16, 2024:** (**<font color="#FC01CC">AKS</font>**)
Ocean has introduced an update to manage and optimize **AKS** Private Clusters. Ocean now supports any AKS private cluster configuration as long as the Ocean Controller can establish outbound communication with the Spot SaaS control plane.
[Learn more…](https://docs.spot.io/ocean/getting-started/aks/?id=what-to-do-about-aks-private-clusters)

* **OCN-0003: May 16, 2024:** (**<font color="#FC01CC">AKS</font>**)
Ocean now lets you schedule cluster and Virtual Node Group (VNG) rolls for **AKS**. You have the flexibility to roll immediately or plan a maintenance window on a weekly or monthly basis during non-peak hours to upgrade or update your clusters or VNGs. You can set up roll schedules using either the [Spot API](https://docs.spot.io/api/#tag/Ocean-AKS/operation/oceanAKSClusterUpdate) through the "Create Cluster" or "Update Cluster" endpoints using a cron expression or through the Ocean Console Cloud Cluster's "Roll" tab.
[Learn more...](https://docs.spot.io/ocean/features/roll?id=rolls)

* **OCN-0002: May 1, 2024:**
Spot has introduced a new Ocean label, `spotinst.io/azure-premium-storage,` injected on every node in a node pool that supports premium storage. Once you define this label on a workload requiring premium storage, the pods can be provisioned on the most appropriate nodes (for the workload). [Learn More...](https://docs.spot.io/ocean/features/labels-and-taints) (edited)

* **OCN-0001**: (**<font color="#FC01CC">AWS Kubernetes</font>**) As of **May 1, 2024**, **Ocean Controller Version 2** for **AWS Kubernetes** is officially released, bringing a host of new features and enhancements to streamline your operations:
  *  With Ocean Controller Version 2, you can expect enhanced efficiency and performance thanks to its innovative event-driven system design. This intelligent architecture ensures your cluster operates at peak performance, delivering optimal results with every interaction.

  *  One of the standout features of Ocean Controller Version 2 is its out-of-the-box Leader Election mode, which guarantees continuous pod availability and uninterrupted operations to keep your cluster running smoothly, even in the face of unexpected events.

  *  Ocean Controller Version 2 establishes a secure binding between your Kubernetes cluster and the relevant Ocean resources. You can easily manage and monitor your resources by configuring your Spot Account ID, Spot Token, and a unique Cluster Identifier for each cluster.

  *  Ocean Controller Version 2 resides within your Kubernetes cluster, actively listening for resource events. This intelligent system seamlessly pushes modified resources to the Spot SaaS environment, ensuring your cluster is always updated with the latest changes.

  *  Not only does Ocean Controller Version 2 offer unparalleled functionality, but it also boasts a minimal footprint within your cluster. This means external network traffic is low when no changes occur, presenting exciting cost-saving opportunities. 

>**IMPORTANT:** **Ocean Controller Version 1** will reach End-Of-Life on **November 1, 2024**. To take advantage of the benefits offered by **Ocean Controller Version 2** and receive uninterrupted service and support, upgrade to Version 2 at your earliest convenience.
[Learn more...](https://docs.spot.io/ocean/tutorials/ocean-controller-v2/)

</details><br>

<details>
  <summary markdown="span">March, 2024 - click to view</summary>

## March 2024: Features and Enhancements

* **March 25, 2024:** (**<font color="#FC01CC">AWS Kubernetes</font>**) Improved PDB Handling During Cluster Rolls: 
The latest update introduces a smart batching mechanism for managing the Pod Disruption Budget (PDB) during cluster rolls. 
This mechanism intelligently splits the nodes for rolling, ensuring that PDB constraints are respected. 
[Learn more](https://docs.spot.io/ocean/features/roll-gen?id=respect-pod-disruption-budget) about respecting PDB during cluster roll.

</details><br>






















