---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 01bf8c630f4fc4d137e98be5b1996eaf47ea3363
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93657867"
---
# <span data-ttu-id="ea5a5-101">Az. ServiceFabric modul</span><span class="sxs-lookup"><span data-stu-id="ea5a5-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="ea5a5-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="ea5a5-102">Description</span></span>
<span data-ttu-id="ea5a5-103">Azure Service Fabric modul, amellyel automatizálhatja a végpontos műveleteket (például biztonságos fürtöket), a fürtcsomópontok felett, illetve csomópontok hozzáadását és eltávolítását a fürtből stb. Az összes művelet teljes listája alább látható.</span><span class="sxs-lookup"><span data-stu-id="ea5a5-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="ea5a5-104">Az. ServiceFabric parancsmagok</span><span class="sxs-lookup"><span data-stu-id="ea5a5-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="ea5a5-105">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="ea5a5-105">Add-AzServiceFabricApplicationCertificate</span></span>](Add-AzServiceFabricApplicationCertificate.md)
<span data-ttu-id="ea5a5-106">Vegyen fel egy új tanúsítványt a fürtöt alkotó virtuális gép Méretarányi készletéhez.</span><span class="sxs-lookup"><span data-stu-id="ea5a5-106">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="ea5a5-107">A tanúsítvány az alkalmazási tanúsítványként való használatra szolgál.</span><span class="sxs-lookup"><span data-stu-id="ea5a5-107">The certificate is intended to be used as an application certificate.</span></span>

### [<span data-ttu-id="ea5a5-108">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ea5a5-108">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="ea5a5-109">Az ügyfél-hitelesítéshez adjon meg köznapi nevet vagy ujjlenyomatot a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="ea5a5-109">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="ea5a5-110">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="ea5a5-110">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="ea5a5-111">Másodlagos fürtcsomópont hozzáadása a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="ea5a5-111">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="ea5a5-112">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="ea5a5-112">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="ea5a5-113">Csomópontok hozzáadása a fürt adott csomópont-típusához</span><span class="sxs-lookup"><span data-stu-id="ea5a5-113">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="ea5a5-114">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="ea5a5-114">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="ea5a5-115">Új csomópont-típus felvétele a meglévő fürtbe.</span><span class="sxs-lookup"><span data-stu-id="ea5a5-115">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="ea5a5-116">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="ea5a5-116">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="ea5a5-117">A fürterőforrás részleteinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="ea5a5-117">Get the cluster resource details.</span></span>

### [<span data-ttu-id="ea5a5-118">Új – AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="ea5a5-118">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="ea5a5-119">Ez a parancs az Ön által megadott vagy a rendszer által létrehozott tanúsítványokat használja az új Service Fabric-fürt beállításához.</span><span class="sxs-lookup"><span data-stu-id="ea5a5-119">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="ea5a5-120">Használhatja az Ön által megadott alapértelmezett sablont vagy egyéni sablont.</span><span class="sxs-lookup"><span data-stu-id="ea5a5-120">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="ea5a5-121">Megadhatja, hogy milyen mappa esetén szeretné exportálni az önaláírt tanúsítványokat, vagy később beolvassa őket a fő boltozatról.</span><span class="sxs-lookup"><span data-stu-id="ea5a5-121">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

### [<span data-ttu-id="ea5a5-122">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ea5a5-122">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="ea5a5-123">Ügyféltanúsítvány (ok) vagy tanúsítvány tárgya (i) eltávolítása a fürt ügyfél-hitelesítéséhez használatos.</span><span class="sxs-lookup"><span data-stu-id="ea5a5-123">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="ea5a5-124">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="ea5a5-124">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="ea5a5-125">A fürt biztonságához használt fürtcsomópontok eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ea5a5-125">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="ea5a5-126">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="ea5a5-126">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="ea5a5-127">Csomópontok eltávolítása a megadott csomópont-típusból egy fürtből</span><span class="sxs-lookup"><span data-stu-id="ea5a5-127">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="ea5a5-128">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="ea5a5-128">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="ea5a5-129">Teljes csomópont-típus eltávolítása a fürtből</span><span class="sxs-lookup"><span data-stu-id="ea5a5-129">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="ea5a5-130">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="ea5a5-130">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="ea5a5-131">Egy vagy több szolgáltatási anyag beállítás eltávolítása a fürtből</span><span class="sxs-lookup"><span data-stu-id="ea5a5-131">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="ea5a5-132">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="ea5a5-132">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="ea5a5-133">Egy vagy több szolgáltatási szerkezet beállításainak hozzáadása vagy frissítése a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="ea5a5-133">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="ea5a5-134">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="ea5a5-134">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="ea5a5-135">Módosítsa a szolgáltatás szerkezetének frissítési típusát a fürtben.</span><span class="sxs-lookup"><span data-stu-id="ea5a5-135">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="ea5a5-136">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="ea5a5-136">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="ea5a5-137">Módosítsa a VmSku tartóssági rétegét vagy egy csomópont típusát.</span><span class="sxs-lookup"><span data-stu-id="ea5a5-137">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="ea5a5-138">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="ea5a5-138">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="ea5a5-139">A fürt elsődleges csomópont-típusának megbízhatósági szintjeinek frissítése</span><span class="sxs-lookup"><span data-stu-id="ea5a5-139">Update the reliability tier of the primary node type in a cluster.</span></span>

