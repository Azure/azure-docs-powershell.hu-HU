---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: d94e7001df730b22fb900b284c6fac47b5d81b8b
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/15/2019
ms.locfileid: "93665604"
---
# <span data-ttu-id="65731-101">Az. ServiceFabric modul</span><span class="sxs-lookup"><span data-stu-id="65731-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="65731-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="65731-102">Description</span></span>
<span data-ttu-id="65731-103">Azure Service Fabric modul, amellyel automatizálhatja a végpontos műveleteket (például biztonságos fürtöket), a fürtcsomópontok felett, illetve csomópontok hozzáadását és eltávolítását a fürtből stb. Az összes művelet teljes listája alább látható.</span><span class="sxs-lookup"><span data-stu-id="65731-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="65731-104">Az. ServiceFabric parancsmagok</span><span class="sxs-lookup"><span data-stu-id="65731-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="65731-105">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="65731-105">Add-AzServiceFabricApplicationCertificate</span></span>](Add-AzServiceFabricApplicationCertificate.md)
<span data-ttu-id="65731-106">Vegyen fel egy új tanúsítványt a fürtöt alkotó virtuális gép Méretarányi készletéhez.</span><span class="sxs-lookup"><span data-stu-id="65731-106">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="65731-107">A tanúsítvány az alkalmazási tanúsítványként való használatra szolgál.</span><span class="sxs-lookup"><span data-stu-id="65731-107">The certificate is intended to be used as an application certificate.</span></span>

### [<span data-ttu-id="65731-108">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="65731-108">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="65731-109">Az ügyfél-hitelesítéshez adjon meg köznapi nevet vagy ujjlenyomatot a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="65731-109">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="65731-110">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="65731-110">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="65731-111">Másodlagos fürtcsomópont hozzáadása a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="65731-111">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="65731-112">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="65731-112">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="65731-113">Csomópontok hozzáadása a fürt adott csomópont-típusához</span><span class="sxs-lookup"><span data-stu-id="65731-113">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="65731-114">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="65731-114">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="65731-115">Új csomópont-típus felvétele a meglévő fürtbe.</span><span class="sxs-lookup"><span data-stu-id="65731-115">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="65731-116">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="65731-116">Get-AzServiceFabricApplication</span></span>](Get-AzServiceFabricApplication.md)
<span data-ttu-id="65731-117">A Service Fabric alkalmazás részleteinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="65731-117">Get Service Fabric application details.</span></span>

### [<span data-ttu-id="65731-118">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="65731-118">Get-AzServiceFabricApplicationType</span></span>](Get-AzServiceFabricApplicationType.md)
<span data-ttu-id="65731-119">A szolgáltatás anyagának beszerzése alkalmazás típusa – részletek</span><span class="sxs-lookup"><span data-stu-id="65731-119">Get Service Fabric application type details.</span></span>

### [<span data-ttu-id="65731-120">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="65731-120">Get-AzServiceFabricApplicationTypeVersion</span></span>](Get-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="65731-121">A szolgáltatás típusa: az alkalmazás típusa – verzió részletei.</span><span class="sxs-lookup"><span data-stu-id="65731-121">Get Service Fabric application type version details.</span></span>

### [<span data-ttu-id="65731-122">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="65731-122">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="65731-123">A fürterőforrás részleteinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="65731-123">Get the cluster resource details.</span></span>

### [<span data-ttu-id="65731-124">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="65731-124">Get-AzServiceFabricService</span></span>](Get-AzServiceFabricService.md)
<span data-ttu-id="65731-125">A szolgáltatás szerkezete szolgáltatás adatai a megadott alkalmazásban és fürtben.</span><span class="sxs-lookup"><span data-stu-id="65731-125">Get Service Fabric service details under the specified application and cluster.</span></span>

### [<span data-ttu-id="65731-126">Új – AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="65731-126">New-AzServiceFabricApplication</span></span>](New-AzServiceFabricApplication.md)
<span data-ttu-id="65731-127">Új szolgáltatási anyag alkalmazása a megadott erőforráscsoport és fürt csoportban</span><span class="sxs-lookup"><span data-stu-id="65731-127">Create new service fabric application under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="65731-128">Új – AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="65731-128">New-AzServiceFabricApplicationType</span></span>](New-AzServiceFabricApplicationType.md)
<span data-ttu-id="65731-129">Új szolgáltatásból álló anyag típusú alkalmazás létrehozása a megadott erőforráscsoport és fürt csoportban</span><span class="sxs-lookup"><span data-stu-id="65731-129">Create new service fabric application type under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="65731-130">Új – AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="65731-130">New-AzServiceFabricApplicationTypeVersion</span></span>](New-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="65731-131">Új alkalmazás típusú verzió létrehozása a megadott erőforráscsoport és fürt csoportban</span><span class="sxs-lookup"><span data-stu-id="65731-131">Create new application type version under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="65731-132">Új – AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="65731-132">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="65731-133">Ez a parancs az Ön által megadott vagy a rendszer által létrehozott tanúsítványokat használja az új Service Fabric-fürt beállításához.</span><span class="sxs-lookup"><span data-stu-id="65731-133">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="65731-134">Használhatja az Ön által megadott alapértelmezett sablont vagy egyéni sablont.</span><span class="sxs-lookup"><span data-stu-id="65731-134">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="65731-135">Megadhatja, hogy milyen mappa esetén szeretné exportálni az önaláírt tanúsítványokat, vagy később beolvassa őket a fő boltozatról.</span><span class="sxs-lookup"><span data-stu-id="65731-135">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

### [<span data-ttu-id="65731-136">Új – AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="65731-136">New-AzServiceFabricService</span></span>](New-AzServiceFabricService.md)
<span data-ttu-id="65731-137">Új szolgáltatási anyag szolgáltatás létrehozása a megadott alkalmazásban és fürtben.</span><span class="sxs-lookup"><span data-stu-id="65731-137">Create new service fabric service under the specified application and cluster.</span></span>

### [<span data-ttu-id="65731-138">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="65731-138">Remove-AzServiceFabricApplication</span></span>](Remove-AzServiceFabricApplication.md)
<span data-ttu-id="65731-139">Alkalmazás eltávolítása a fürtből</span><span class="sxs-lookup"><span data-stu-id="65731-139">Remove an application from the cluster.</span></span> <span data-ttu-id="65731-140">Ezzel eltávolítja a program az alkalmazás alatti összes szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="65731-140">This will remove all the services under the application.</span></span>

### [<span data-ttu-id="65731-141">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="65731-141">Remove-AzServiceFabricApplicationType</span></span>](Remove-AzServiceFabricApplicationType.md)
<span data-ttu-id="65731-142">A szolgáltatás eltávolítása: az alkalmazás típusa a fürtben.</span><span class="sxs-lookup"><span data-stu-id="65731-142">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="65731-143">Ezzel a beállítással a program eltávolítja az összes típusú verziót az erőforrásból.</span><span class="sxs-lookup"><span data-stu-id="65731-143">This will remove all type versions under this resource.</span></span>

### [<span data-ttu-id="65731-144">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="65731-144">Remove-AzServiceFabricApplicationTypeVersion</span></span>](Remove-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="65731-145">A szolgáltatás eltávolítása: az alkalmazás típusának verziója a fürtből</span><span class="sxs-lookup"><span data-stu-id="65731-145">Remove Service fabric an application type version from the cluster.</span></span>

### [<span data-ttu-id="65731-146">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="65731-146">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="65731-147">Ügyféltanúsítvány (ok) vagy tanúsítvány tárgya (i) eltávolítása a fürt ügyfél-hitelesítéséhez használatos.</span><span class="sxs-lookup"><span data-stu-id="65731-147">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="65731-148">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="65731-148">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="65731-149">A fürt biztonságához használt fürtcsomópontok eltávolítása</span><span class="sxs-lookup"><span data-stu-id="65731-149">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="65731-150">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="65731-150">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="65731-151">Csomópontok eltávolítása a megadott csomópont-típusból egy fürtből</span><span class="sxs-lookup"><span data-stu-id="65731-151">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="65731-152">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="65731-152">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="65731-153">Teljes csomópont-típus eltávolítása a fürtből</span><span class="sxs-lookup"><span data-stu-id="65731-153">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="65731-154">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="65731-154">Remove-AzServiceFabricService</span></span>](Remove-AzServiceFabricService.md)
<span data-ttu-id="65731-155">Szolgáltatás eltávolítása a fürtből</span><span class="sxs-lookup"><span data-stu-id="65731-155">Remove a service from the cluster.</span></span>

### [<span data-ttu-id="65731-156">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="65731-156">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="65731-157">Egy vagy több szolgáltatási anyag beállítás eltávolítása a fürtből</span><span class="sxs-lookup"><span data-stu-id="65731-157">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="65731-158">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="65731-158">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="65731-159">Egy vagy több szolgáltatási szerkezet beállításainak hozzáadása vagy frissítése a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="65731-159">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="65731-160">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="65731-160">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="65731-161">Módosítsa a szolgáltatás szerkezetének frissítési típusát a fürtben.</span><span class="sxs-lookup"><span data-stu-id="65731-161">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="65731-162">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="65731-162">Update-AzServiceFabricApplication</span></span>](Update-AzServiceFabricApplication.md)
<span data-ttu-id="65731-163">A szolgáltatás szövet-alkalmazásának frissítése</span><span class="sxs-lookup"><span data-stu-id="65731-163">Update a service fabric application.</span></span> <span data-ttu-id="65731-164">Ez lehetővé teszi az alkalmazás paramétereinek frissítését és/vagy az alkalmazás típusának frissítését, amely elindítja az alkalmazások frissítését.</span><span class="sxs-lookup"><span data-stu-id="65731-164">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

### [<span data-ttu-id="65731-165">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="65731-165">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="65731-166">Módosítsa a VmSku tartóssági rétegét vagy egy csomópont típusát.</span><span class="sxs-lookup"><span data-stu-id="65731-166">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="65731-167">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="65731-167">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="65731-168">A fürt elsődleges csomópont-típusának megbízhatósági szintjeinek frissítése</span><span class="sxs-lookup"><span data-stu-id="65731-168">Update the reliability tier of the primary node type in a cluster.</span></span>

