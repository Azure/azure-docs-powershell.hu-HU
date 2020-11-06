---
Module Name: AzureRM.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
ms.openlocfilehash: 9c71788abd7707931df2c25279c265bbe9967bbf
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93490328"
---
# <span data-ttu-id="6e4d5-101">AzureRM. ServiceFabric modul</span><span class="sxs-lookup"><span data-stu-id="6e4d5-101">AzureRM.ServiceFabric Module</span></span>
## <span data-ttu-id="6e4d5-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="6e4d5-102">Description</span></span>
<span data-ttu-id="6e4d5-103">Azure Service Fabric modul, amellyel automatizálhatja a végpontos műveleteket (például biztonságos fürtöket), a fürtcsomópontok felett, illetve csomópontok hozzáadását és eltávolítását a fürtből stb. Az összes művelet teljes listája alább látható.</span><span class="sxs-lookup"><span data-stu-id="6e4d5-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="6e4d5-104">AzureRM. ServiceFabric parancsmagok</span><span class="sxs-lookup"><span data-stu-id="6e4d5-104">AzureRM.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="6e4d5-105">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="6e4d5-105">Add-AzureRmServiceFabricApplicationCertificate</span></span>](Add-AzureRmServiceFabricApplicationCertificate.md)
<span data-ttu-id="6e4d5-106">Alkalmazásspecifikus tanúsítványként használandó tanúsítvány hozzáadása</span><span class="sxs-lookup"><span data-stu-id="6e4d5-106">Add a certificate that will be used as application certificate</span></span>

### [<span data-ttu-id="6e4d5-107">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6e4d5-107">Add-AzureRmServiceFabricClientCertificate</span></span>](Add-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="6e4d5-108">Köznapi név vagy ujjlenyomat hozzáadása a fürtkonfiguráció ügyfél-hitelesítéshez</span><span class="sxs-lookup"><span data-stu-id="6e4d5-108">Add common name or thumbprint to the cluster settings for client authentication</span></span>

### [<span data-ttu-id="6e4d5-109">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="6e4d5-109">Add-AzureRmServiceFabricClusterCertificate</span></span>](Add-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="6e4d5-110">Másodlagos fürtcsomópont hozzáadása a fürthöz a meglévő tanúsítvány átgörgetéséhez</span><span class="sxs-lookup"><span data-stu-id="6e4d5-110">Add a secondary cluster certificate to the cluster for rolling over the existing certificate</span></span> 

### [<span data-ttu-id="6e4d5-111">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="6e4d5-111">Add-AzureRmServiceFabricNode</span></span>](Add-AzureRmServiceFabricNode.md)
<span data-ttu-id="6e4d5-112">Csomópontok/VMs-szolgáltatások hozzáadása egy adott csomóponthoz egy fürthöz</span><span class="sxs-lookup"><span data-stu-id="6e4d5-112">Add nodes/VMs to a specific node type to a cluster</span></span>

### [<span data-ttu-id="6e4d5-113">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="6e4d5-113">Add-AzureRmServiceFabricNodeType</span></span>](Add-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="6e4d5-114">Csomópont típusa/VMs hozzáadása meglévő fürthöz</span><span class="sxs-lookup"><span data-stu-id="6e4d5-114">Add a node type/VMs to an existing cluster</span></span>

### [<span data-ttu-id="6e4d5-115">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="6e4d5-115">Get-AzureRmServiceFabricCluster</span></span>](Get-AzureRmServiceFabricCluster.md)
<span data-ttu-id="6e4d5-116">A fürterőforrás részleteinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="6e4d5-116">Get the details of the cluster resource</span></span> 

### [<span data-ttu-id="6e4d5-117">Új – AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="6e4d5-117">New-AzureRmServiceFabricCluster</span></span>](New-AzureRmServiceFabricCluster.md)
<span data-ttu-id="6e4d5-118">Hozzon létre egy új ServiceFabric-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="6e4d5-118">Create an new ServiceFabric cluster.</span></span> <span data-ttu-id="6e4d5-119">Ez a parancs számos túlterhelt a különböző helyzetekben</span><span class="sxs-lookup"><span data-stu-id="6e4d5-119">This command has many overloads to cover various scenarios</span></span>

### [<span data-ttu-id="6e4d5-120">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6e4d5-120">Remove-AzureRmServiceFabricClientCertificate</span></span>](Remove-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="6e4d5-121">Ügyféltanúsítvány eltávolítása a fürt eléréséhez való használatból</span><span class="sxs-lookup"><span data-stu-id="6e4d5-121">Remove client certificate from being used to access the cluster</span></span>

### [<span data-ttu-id="6e4d5-122">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="6e4d5-122">Remove-AzureRmServiceFabricClusterCertificate</span></span>](Remove-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="6e4d5-123">A cluster tanúsítvány eltávolítása a fürtök biztonsága céljából</span><span class="sxs-lookup"><span data-stu-id="6e4d5-123">Remove cluster certificate from being used for cluster security</span></span>

### [<span data-ttu-id="6e4d5-124">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="6e4d5-124">Remove-AzureRmServiceFabricNode</span></span>](Remove-AzureRmServiceFabricNode.md)
<span data-ttu-id="6e4d5-125">Csomópontok eltávolítása az adott csomópontból a fürtből</span><span class="sxs-lookup"><span data-stu-id="6e4d5-125">Remove nodes from the specific node type from a cluster</span></span>

### [<span data-ttu-id="6e4d5-126">Remove-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="6e4d5-126">Remove-AzureRmServiceFabricNodeType</span></span>](Remove-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="6e4d5-127">Csomópont-típus eltávolítása a fürtből</span><span class="sxs-lookup"><span data-stu-id="6e4d5-127">Remove a node type from a cluster</span></span>

### [<span data-ttu-id="6e4d5-128">Remove-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="6e4d5-128">Remove-AzureRmServiceFabricSetting</span></span>](Remove-AzureRmServiceFabricSetting.md)
<span data-ttu-id="6e4d5-129">Egy vagy több ServiceFabric-beállítás eltávolítása a fürtből</span><span class="sxs-lookup"><span data-stu-id="6e4d5-129">Remove one or more ServiceFabric settings from the cluster</span></span>

### [<span data-ttu-id="6e4d5-130">Set-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="6e4d5-130">Set-AzureRmServiceFabricSetting</span></span>](Set-AzureRmServiceFabricSetting.md)
<span data-ttu-id="6e4d5-131">Egy vagy több ServiceFabric-beállítás hozzáadása vagy frissítése a fürthöz</span><span class="sxs-lookup"><span data-stu-id="6e4d5-131">Add or update one or more ServiceFabric settings to the cluster</span></span>

### [<span data-ttu-id="6e4d5-132">Set-AzureRmServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="6e4d5-132">Set-AzureRmServiceFabricUpgradeType</span></span>](Set-AzureRmServiceFabricUpgradeType.md)
<span data-ttu-id="6e4d5-133">A ServiceFabric frissítési típusának módosítása</span><span class="sxs-lookup"><span data-stu-id="6e4d5-133">Change the ServiceFabric upgrade type of a cluster</span></span>

### [<span data-ttu-id="6e4d5-134">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="6e4d5-134">Update-AzureRmServiceFabricDurability</span></span>](Update-AzureRmServiceFabricDurability.md)
<span data-ttu-id="6e4d5-135">A fürt tartóssági rétegének módosítása</span><span class="sxs-lookup"><span data-stu-id="6e4d5-135">Change the durability tier of a cluster</span></span>

### [<span data-ttu-id="6e4d5-136">Update-AzureRmServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="6e4d5-136">Update-AzureRmServiceFabricReliability</span></span>](Update-AzureRmServiceFabricReliability.md)
<span data-ttu-id="6e4d5-137">A fürt megbízhatósági rétegének módosítása</span><span class="sxs-lookup"><span data-stu-id="6e4d5-137">Change the reliability tier of a cluster</span></span>
