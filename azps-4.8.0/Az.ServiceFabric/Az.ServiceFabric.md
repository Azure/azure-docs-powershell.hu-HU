---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 6c58f25209a0acd227e2f04e7ca808916f283d46
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025994"
---
# <span data-ttu-id="1dba9-101">Az. ServiceFabric modul</span><span class="sxs-lookup"><span data-stu-id="1dba9-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="1dba9-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="1dba9-102">Description</span></span>
<span data-ttu-id="1dba9-103">Azure Service Fabric modul, amellyel automatizálhatja a végpontos műveleteket (például biztonságos fürtöket), a fürtcsomópontok felett, illetve csomópontok hozzáadását és eltávolítását a fürtből stb. Az összes művelet teljes listája alább látható.</span><span class="sxs-lookup"><span data-stu-id="1dba9-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="1dba9-104">Az. ServiceFabric parancsmagok</span><span class="sxs-lookup"><span data-stu-id="1dba9-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="1dba9-105">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1dba9-105">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="1dba9-106">Az ügyfél-hitelesítéshez adjon meg köznapi nevet vagy ujjlenyomatot a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="1dba9-106">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="1dba9-107">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="1dba9-107">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="1dba9-108">Másodlagos fürtcsomópont hozzáadása a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="1dba9-108">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="1dba9-109">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1dba9-109">Add-AzServiceFabricManagedClusterClientCertificate</span></span>](Add-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="1dba9-110">Adjon meg tanúsítvány-köznapi nevet vagy ujjlenyomatot a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="1dba9-110">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="1dba9-111">Ez a funkció regisztrálja a tanúsítványt a fürt ügyfél-hitelesítés céljából.</span><span class="sxs-lookup"><span data-stu-id="1dba9-111">This will register the certificate agains the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="1dba9-112">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="1dba9-112">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="1dba9-113">Adja hozzá a VM kiterjesztést a csomópont típusához.</span><span class="sxs-lookup"><span data-stu-id="1dba9-113">Add vm extension to the node type.</span></span>

### [<span data-ttu-id="1dba9-114">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="1dba9-114">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
<span data-ttu-id="1dba9-115">Adjon hozzá titkos tanúsítványt a csomópont típusához.</span><span class="sxs-lookup"><span data-stu-id="1dba9-115">Add certificate secret to the node type.</span></span>

### [<span data-ttu-id="1dba9-116">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="1dba9-116">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="1dba9-117">Csomópontok hozzáadása a fürt adott csomópont-típusához</span><span class="sxs-lookup"><span data-stu-id="1dba9-117">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="1dba9-118">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="1dba9-118">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="1dba9-119">Új csomópont-típus felvétele a meglévő fürtbe.</span><span class="sxs-lookup"><span data-stu-id="1dba9-119">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="1dba9-120">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="1dba9-120">Get-AzServiceFabricApplication</span></span>](Get-AzServiceFabricApplication.md)
<span data-ttu-id="1dba9-121">A Service Fabric alkalmazás részleteinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="1dba9-121">Get Service Fabric application details.</span></span>

### [<span data-ttu-id="1dba9-122">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="1dba9-122">Get-AzServiceFabricApplicationType</span></span>](Get-AzServiceFabricApplicationType.md)
<span data-ttu-id="1dba9-123">A szolgáltatás anyagának beszerzése alkalmazás típusa – részletek</span><span class="sxs-lookup"><span data-stu-id="1dba9-123">Get Service Fabric application type details.</span></span>

### [<span data-ttu-id="1dba9-124">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="1dba9-124">Get-AzServiceFabricApplicationTypeVersion</span></span>](Get-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="1dba9-125">A szolgáltatás típusa: az alkalmazás típusa – verzió részletei.</span><span class="sxs-lookup"><span data-stu-id="1dba9-125">Get Service Fabric application type version details.</span></span>

### [<span data-ttu-id="1dba9-126">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="1dba9-126">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="1dba9-127">A fürterőforrás részleteinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="1dba9-127">Get the cluster resource details.</span></span>

### [<span data-ttu-id="1dba9-128">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="1dba9-128">Get-AzServiceFabricManagedCluster</span></span>](Get-AzServiceFabricManagedCluster.md)
<span data-ttu-id="1dba9-129">Kapja meg a felügyelt fürterőforrás adatait.</span><span class="sxs-lookup"><span data-stu-id="1dba9-129">Get the managed cluster resource details.</span></span>

### [<span data-ttu-id="1dba9-130">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="1dba9-130">Get-AzServiceFabricManagedNodeType</span></span>](Get-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="1dba9-131">A felügyelt csomópont típusa erőforrás részleteinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="1dba9-131">Get the managed node type resource details.</span></span>

### [<span data-ttu-id="1dba9-132">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="1dba9-132">Get-AzServiceFabricService</span></span>](Get-AzServiceFabricService.md)
<span data-ttu-id="1dba9-133">A szolgáltatás szerkezete szolgáltatás adatai a megadott alkalmazásban és fürtben.</span><span class="sxs-lookup"><span data-stu-id="1dba9-133">Get Service Fabric service details under the specified application and cluster.</span></span>

### [<span data-ttu-id="1dba9-134">Új – AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="1dba9-134">New-AzServiceFabricApplication</span></span>](New-AzServiceFabricApplication.md)
<span data-ttu-id="1dba9-135">Új szolgáltatási anyag alkalmazása a megadott erőforráscsoport és fürt csoportban</span><span class="sxs-lookup"><span data-stu-id="1dba9-135">Create new service fabric application under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="1dba9-136">Új – AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="1dba9-136">New-AzServiceFabricApplicationType</span></span>](New-AzServiceFabricApplicationType.md)
<span data-ttu-id="1dba9-137">Új szolgáltatásból álló anyag típusú alkalmazás létrehozása a megadott erőforráscsoport és fürt csoportban</span><span class="sxs-lookup"><span data-stu-id="1dba9-137">Create new service fabric application type under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="1dba9-138">Új – AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="1dba9-138">New-AzServiceFabricApplicationTypeVersion</span></span>](New-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="1dba9-139">Új alkalmazás típusú verzió létrehozása a megadott erőforráscsoport és fürt csoportban</span><span class="sxs-lookup"><span data-stu-id="1dba9-139">Create new application type version under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="1dba9-140">Új – AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="1dba9-140">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="1dba9-141">Ez a parancs az Ön által megadott vagy a rendszer által létrehozott tanúsítványokat használja az új Service Fabric-fürt beállításához.</span><span class="sxs-lookup"><span data-stu-id="1dba9-141">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="1dba9-142">Használhatja az Ön által megadott alapértelmezett sablont vagy egyéni sablont.</span><span class="sxs-lookup"><span data-stu-id="1dba9-142">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="1dba9-143">Megadhatja, hogy milyen mappa esetén szeretné exportálni az önaláírt tanúsítványokat, vagy később beolvassa őket a fő boltozatról.</span><span class="sxs-lookup"><span data-stu-id="1dba9-143">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span>

### [<span data-ttu-id="1dba9-144">Új – AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="1dba9-144">New-AzServiceFabricManagedCluster</span></span>](New-AzServiceFabricManagedCluster.md)
<span data-ttu-id="1dba9-145">Új felügyelt fürt létrehozása</span><span class="sxs-lookup"><span data-stu-id="1dba9-145">Create new managed cluster.</span></span>

### [<span data-ttu-id="1dba9-146">Új – AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="1dba9-146">New-AzServiceFabricManagedNodeType</span></span>](New-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="1dba9-147">Új csomópont típusú erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="1dba9-147">Create new node type resource.</span></span>

### [<span data-ttu-id="1dba9-148">Új – AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="1dba9-148">New-AzServiceFabricService</span></span>](New-AzServiceFabricService.md)
<span data-ttu-id="1dba9-149">Új szolgáltatási anyag szolgáltatás létrehozása a megadott alkalmazásban és fürtben.</span><span class="sxs-lookup"><span data-stu-id="1dba9-149">Create new service fabric service under the specified application and cluster.</span></span>

### [<span data-ttu-id="1dba9-150">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="1dba9-150">Remove-AzServiceFabricApplication</span></span>](Remove-AzServiceFabricApplication.md)
<span data-ttu-id="1dba9-151">Alkalmazás eltávolítása a fürtből</span><span class="sxs-lookup"><span data-stu-id="1dba9-151">Remove an application from the cluster.</span></span> <span data-ttu-id="1dba9-152">Ezzel eltávolítja a program az alkalmazás alatti összes szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="1dba9-152">This will remove all the services under the application.</span></span>

### [<span data-ttu-id="1dba9-153">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="1dba9-153">Remove-AzServiceFabricApplicationType</span></span>](Remove-AzServiceFabricApplicationType.md)
<span data-ttu-id="1dba9-154">A szolgáltatás eltávolítása: az alkalmazás típusa a fürtben.</span><span class="sxs-lookup"><span data-stu-id="1dba9-154">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="1dba9-155">Ezzel a beállítással a program eltávolítja az összes típusú verziót az erőforrásból.</span><span class="sxs-lookup"><span data-stu-id="1dba9-155">This will remove all type versions under this resource.</span></span>

### [<span data-ttu-id="1dba9-156">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="1dba9-156">Remove-AzServiceFabricApplicationTypeVersion</span></span>](Remove-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="1dba9-157">A szolgáltatás eltávolítása: az alkalmazás típusának verziója a fürtből</span><span class="sxs-lookup"><span data-stu-id="1dba9-157">Remove Service fabric an application type version from the cluster.</span></span>

### [<span data-ttu-id="1dba9-158">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1dba9-158">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="1dba9-159">Ügyféltanúsítvány (ok) vagy tanúsítvány tárgya (i) eltávolítása a fürt ügyfél-hitelesítéséhez használatos.</span><span class="sxs-lookup"><span data-stu-id="1dba9-159">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="1dba9-160">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="1dba9-160">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="1dba9-161">A fürt biztonságához használt fürtcsomópontok eltávolítása</span><span class="sxs-lookup"><span data-stu-id="1dba9-161">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="1dba9-162">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="1dba9-162">Remove-AzServiceFabricManagedCluster</span></span>](Remove-AzServiceFabricManagedCluster.md)
<span data-ttu-id="1dba9-163">Fürterőforrás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="1dba9-163">Remove cluster resource.</span></span>

### [<span data-ttu-id="1dba9-164">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1dba9-164">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>](Remove-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="1dba9-165">Remvoe-ügyféltanúsítvány ujjlenyomat vagy köznapi név szerint.</span><span class="sxs-lookup"><span data-stu-id="1dba9-165">Remvoe client certificate by thumbprint or common name.</span></span>

### [<span data-ttu-id="1dba9-166">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="1dba9-166">Remove-AzServiceFabricManagedNodeType</span></span>](Remove-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="1dba9-167">Távolítsa el a csomópont típusát vagy a csomópont típusának bizonyos csomópontját.</span><span class="sxs-lookup"><span data-stu-id="1dba9-167">Remove the node type or specific nodes within the node type.</span></span>

### [<span data-ttu-id="1dba9-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="1dba9-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="1dba9-169">Távolítsa el a VM kiterjesztést a Node típusból.</span><span class="sxs-lookup"><span data-stu-id="1dba9-169">Remove vm extension from the node type.</span></span>

### [<span data-ttu-id="1dba9-170">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="1dba9-170">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="1dba9-171">Csomópontok eltávolítása a megadott csomópont-típusból egy fürtből</span><span class="sxs-lookup"><span data-stu-id="1dba9-171">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="1dba9-172">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="1dba9-172">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="1dba9-173">Teljes csomópont-típus eltávolítása a fürtből</span><span class="sxs-lookup"><span data-stu-id="1dba9-173">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="1dba9-174">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="1dba9-174">Remove-AzServiceFabricService</span></span>](Remove-AzServiceFabricService.md)
<span data-ttu-id="1dba9-175">Szolgáltatás eltávolítása a fürtből</span><span class="sxs-lookup"><span data-stu-id="1dba9-175">Remove a service from the cluster.</span></span>

### [<span data-ttu-id="1dba9-176">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="1dba9-176">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="1dba9-177">Egy vagy több szolgáltatási anyag beállítás eltávolítása a fürtből</span><span class="sxs-lookup"><span data-stu-id="1dba9-177">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="1dba9-178">Újraindítás – AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="1dba9-178">Restart-AzServiceFabricManagedNodeType</span></span>](Restart-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="1dba9-179">A csomópont típusától kezdve indítsa újra az adott csomópontokat.</span><span class="sxs-lookup"><span data-stu-id="1dba9-179">Restart specific nodes from the node type.</span></span>

### [<span data-ttu-id="1dba9-180">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="1dba9-180">Set-AzServiceFabricManagedCluster</span></span>](Set-AzServiceFabricManagedCluster.md)
<span data-ttu-id="1dba9-181">A cluster resource tulajdonság beállítása</span><span class="sxs-lookup"><span data-stu-id="1dba9-181">Set cluster resource properties.</span></span>

### [<span data-ttu-id="1dba9-182">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="1dba9-182">Set-AzServiceFabricManagedNodeType</span></span>](Set-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="1dba9-183">Beállítja a csomópont típusa erőforrás tulajdonságait, vagy ha a-Reimage paramétert tartalmazó csomópont típusának adott NDES a Reimage műveletet futtatja.</span><span class="sxs-lookup"><span data-stu-id="1dba9-183">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

### [<span data-ttu-id="1dba9-184">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="1dba9-184">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="1dba9-185">Egy vagy több szolgáltatási szerkezet beállításainak hozzáadása vagy frissítése a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="1dba9-185">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="1dba9-186">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="1dba9-186">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="1dba9-187">Módosítsa a szolgáltatás szerkezetének frissítési típusát a fürtben.</span><span class="sxs-lookup"><span data-stu-id="1dba9-187">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="1dba9-188">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="1dba9-188">Update-AzServiceFabricApplication</span></span>](Update-AzServiceFabricApplication.md)
<span data-ttu-id="1dba9-189">A szolgáltatás szövet-alkalmazásának frissítése</span><span class="sxs-lookup"><span data-stu-id="1dba9-189">Update a service fabric application.</span></span> <span data-ttu-id="1dba9-190">Ez lehetővé teszi az alkalmazás paramétereinek frissítését és/vagy az alkalmazás típusának frissítését, amely elindítja az alkalmazások frissítését.</span><span class="sxs-lookup"><span data-stu-id="1dba9-190">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

### [<span data-ttu-id="1dba9-191">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="1dba9-191">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="1dba9-192">Módosítsa a VmSku tartóssági rétegét vagy egy csomópont típusát.</span><span class="sxs-lookup"><span data-stu-id="1dba9-192">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="1dba9-193">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="1dba9-193">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="1dba9-194">A fürt elsődleges csomópont-típusának megbízhatósági szintjeinek frissítése</span><span class="sxs-lookup"><span data-stu-id="1dba9-194">Update the reliability tier of the primary node type in a cluster.</span></span>

