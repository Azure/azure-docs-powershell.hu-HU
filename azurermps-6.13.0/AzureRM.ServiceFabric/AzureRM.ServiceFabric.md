---
Module Name: AzureRM.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
ms.openlocfilehash: 6d93775a028e7a590a8da9cc008640fb8484bdf2
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93490115"
---
# <span data-ttu-id="e6af6-101">AzureRM. ServiceFabric modul</span><span class="sxs-lookup"><span data-stu-id="e6af6-101">AzureRM.ServiceFabric Module</span></span>
## <span data-ttu-id="e6af6-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="e6af6-102">Description</span></span>
<span data-ttu-id="e6af6-103">Azure Service Fabric modul, amellyel automatizálhatja a végpontos műveleteket (például biztonságos fürtöket), a fürtcsomópontok felett, illetve csomópontok hozzáadását és eltávolítását a fürtből stb. Az összes művelet teljes listája alább látható.</span><span class="sxs-lookup"><span data-stu-id="e6af6-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="e6af6-104">AzureRM. ServiceFabric parancsmagok</span><span class="sxs-lookup"><span data-stu-id="e6af6-104">AzureRM.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="e6af6-105">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="e6af6-105">Add-AzureRmServiceFabricApplicationCertificate</span></span>](Add-AzureRmServiceFabricApplicationCertificate.md)
<span data-ttu-id="e6af6-106">Vegyen fel egy új tanúsítványt a fürtöt alkotó virtuális gép Méretarányi készletéhez.</span><span class="sxs-lookup"><span data-stu-id="e6af6-106">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="e6af6-107">A tanúsítvány az alkalmazási tanúsítványként való használatra szolgál.</span><span class="sxs-lookup"><span data-stu-id="e6af6-107">The certificate is intended to be used as an application certificate.</span></span>

### [<span data-ttu-id="e6af6-108">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e6af6-108">Add-AzureRmServiceFabricClientCertificate</span></span>](Add-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="e6af6-109">Az ügyfél-hitelesítéshez adjon meg köznapi nevet vagy ujjlenyomatot a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="e6af6-109">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="e6af6-110">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="e6af6-110">Add-AzureRmServiceFabricClusterCertificate</span></span>](Add-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="e6af6-111">Másodlagos fürtcsomópont hozzáadása a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="e6af6-111">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="e6af6-112">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="e6af6-112">Add-AzureRmServiceFabricNode</span></span>](Add-AzureRmServiceFabricNode.md)
<span data-ttu-id="e6af6-113">Csomópontok hozzáadása a fürt adott csomópont-típusához</span><span class="sxs-lookup"><span data-stu-id="e6af6-113">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="e6af6-114">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="e6af6-114">Add-AzureRmServiceFabricNodeType</span></span>](Add-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="e6af6-115">Új csomópont-típus felvétele a meglévő fürtbe.</span><span class="sxs-lookup"><span data-stu-id="e6af6-115">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="e6af6-116">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="e6af6-116">Get-AzureRmServiceFabricCluster</span></span>](Get-AzureRmServiceFabricCluster.md)
<span data-ttu-id="e6af6-117">A fürterőforrás részleteinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="e6af6-117">Get the cluster resource details.</span></span>

### [<span data-ttu-id="e6af6-118">Új – AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="e6af6-118">New-AzureRmServiceFabricCluster</span></span>](New-AzureRmServiceFabricCluster.md)
<span data-ttu-id="e6af6-119">Ez a parancs az Ön által megadott vagy a rendszer által létrehozott tanúsítványokat használja az új Service Fabric-fürt beállításához.</span><span class="sxs-lookup"><span data-stu-id="e6af6-119">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="e6af6-120">Használhatja az Ön által megadott alapértelmezett sablont vagy egyéni sablont.</span><span class="sxs-lookup"><span data-stu-id="e6af6-120">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="e6af6-121">Megadhatja, hogy milyen mappa esetén szeretné exportálni az önaláírt tanúsítványokat, vagy később beolvassa őket a fő boltozatról.</span><span class="sxs-lookup"><span data-stu-id="e6af6-121">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

### [<span data-ttu-id="e6af6-122">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e6af6-122">Remove-AzureRmServiceFabricClientCertificate</span></span>](Remove-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="e6af6-123">Ügyféltanúsítvány (ok) vagy tanúsítvány tárgya (i) eltávolítása a fürt ügyfél-hitelesítéséhez használatos.</span><span class="sxs-lookup"><span data-stu-id="e6af6-123">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="e6af6-124">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="e6af6-124">Remove-AzureRmServiceFabricClusterCertificate</span></span>](Remove-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="e6af6-125">A fürt biztonságához használt fürtcsomópontok eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e6af6-125">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="e6af6-126">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="e6af6-126">Remove-AzureRmServiceFabricNode</span></span>](Remove-AzureRmServiceFabricNode.md)
<span data-ttu-id="e6af6-127">Csomópontok eltávolítása a megadott csomópont-típusból egy fürtből</span><span class="sxs-lookup"><span data-stu-id="e6af6-127">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="e6af6-128">Remove-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="e6af6-128">Remove-AzureRmServiceFabricNodeType</span></span>](Remove-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="e6af6-129">Teljes csomópont-típus eltávolítása a fürtből</span><span class="sxs-lookup"><span data-stu-id="e6af6-129">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="e6af6-130">Remove-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="e6af6-130">Remove-AzureRmServiceFabricSetting</span></span>](Remove-AzureRmServiceFabricSetting.md)
<span data-ttu-id="e6af6-131">Egy vagy több szolgáltatási anyag beállítás eltávolítása a fürtből</span><span class="sxs-lookup"><span data-stu-id="e6af6-131">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="e6af6-132">Set-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="e6af6-132">Set-AzureRmServiceFabricSetting</span></span>](Set-AzureRmServiceFabricSetting.md)
<span data-ttu-id="e6af6-133">Egy vagy több szolgáltatási szerkezet beállításainak hozzáadása vagy frissítése a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="e6af6-133">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="e6af6-134">Set-AzureRmServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="e6af6-134">Set-AzureRmServiceFabricUpgradeType</span></span>](Set-AzureRmServiceFabricUpgradeType.md)
<span data-ttu-id="e6af6-135">Módosítsa a szolgáltatás szerkezetének frissítési típusát a fürtben.</span><span class="sxs-lookup"><span data-stu-id="e6af6-135">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="e6af6-136">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="e6af6-136">Update-AzureRmServiceFabricDurability</span></span>](Update-AzureRmServiceFabricDurability.md)
<span data-ttu-id="e6af6-137">Módosítsa a VmSku tartóssági rétegét vagy egy csomópont típusát.</span><span class="sxs-lookup"><span data-stu-id="e6af6-137">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="e6af6-138">Update-AzureRmServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="e6af6-138">Update-AzureRmServiceFabricReliability</span></span>](Update-AzureRmServiceFabricReliability.md)
<span data-ttu-id="e6af6-139">A fürt elsődleges csomópont-típusának megbízhatósági szintjeinek frissítése</span><span class="sxs-lookup"><span data-stu-id="e6af6-139">Update the reliability tier of the primary node type in a cluster.</span></span>

