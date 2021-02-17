---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 6c58f25209a0acd227e2f04e7ca808916f283d46
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208071"
---
# <span data-ttu-id="e54b6-101">Az.ServiceFabric modul</span><span class="sxs-lookup"><span data-stu-id="e54b6-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="e54b6-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="e54b6-102">Description</span></span>
<span data-ttu-id="e54b6-103">Azure Service Fabric modul, automatizálhatja a két végű műveleteket, például a biztonságos fürt létrehozását, a fürttanúsítványok használatát, a csomópontok hozzáadását vagy a fürtből való eltávolítást stb. Az alábbiakban felsoroljuk az összes művelet teljes listáját.</span><span class="sxs-lookup"><span data-stu-id="e54b6-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="e54b6-104">Az.ServiceFabric parancsmagok</span><span class="sxs-lookup"><span data-stu-id="e54b6-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="e54b6-105">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e54b6-105">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="e54b6-106">Ügyfél-hitelesítési célokból adjon hozzá általános nevet vagy thumbprint-et a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="e54b6-106">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="e54b6-107">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="e54b6-107">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="e54b6-108">Vegyen fel egy másodlagos fürt tanúsítványát a fürtbe.</span><span class="sxs-lookup"><span data-stu-id="e54b6-108">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="e54b6-109">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e54b6-109">Add-AzServiceFabricManagedClusterClientCertificate</span></span>](Add-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="e54b6-110">Adja hozzá a tanúsítvány általános nevét vagy thumbprint-ját a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="e54b6-110">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="e54b6-111">Ez a módszer ismét regisztrálja a tanúsítványt a fürt ügyfél-hitelesítési célokra.</span><span class="sxs-lookup"><span data-stu-id="e54b6-111">This will register the certificate agains the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="e54b6-112">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="e54b6-112">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="e54b6-113">Adja hozzá a vm bővítményt a csomóponttípushoz.</span><span class="sxs-lookup"><span data-stu-id="e54b6-113">Add vm extension to the node type.</span></span>

### [<span data-ttu-id="e54b6-114">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="e54b6-114">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
<span data-ttu-id="e54b6-115">Adja hozzá a tanúsítvány titkos nevét a csomóponttípushoz.</span><span class="sxs-lookup"><span data-stu-id="e54b6-115">Add certificate secret to the node type.</span></span>

### [<span data-ttu-id="e54b6-116">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="e54b6-116">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="e54b6-117">Csomópontok hozzáadása a fürt adott csomóponttípushoz.</span><span class="sxs-lookup"><span data-stu-id="e54b6-117">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="e54b6-118">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="e54b6-118">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="e54b6-119">Új csomóponttípus hozzáadása a meglévő fürthöz.</span><span class="sxs-lookup"><span data-stu-id="e54b6-119">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="e54b6-120">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e54b6-120">Get-AzServiceFabricApplication</span></span>](Get-AzServiceFabricApplication.md)
<span data-ttu-id="e54b6-121">A Service Fabric alkalmazás részleteinek megtekintése.</span><span class="sxs-lookup"><span data-stu-id="e54b6-121">Get Service Fabric application details.</span></span>

### [<span data-ttu-id="e54b6-122">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="e54b6-122">Get-AzServiceFabricApplicationType</span></span>](Get-AzServiceFabricApplicationType.md)
<span data-ttu-id="e54b6-123">A Service Fabric alkalmazás típusának részleteinek lekérte.</span><span class="sxs-lookup"><span data-stu-id="e54b6-123">Get Service Fabric application type details.</span></span>

### [<span data-ttu-id="e54b6-124">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e54b6-124">Get-AzServiceFabricApplicationTypeVersion</span></span>](Get-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="e54b6-125">A Service Fabric alkalmazás verziószámának részletei.</span><span class="sxs-lookup"><span data-stu-id="e54b6-125">Get Service Fabric application type version details.</span></span>

### [<span data-ttu-id="e54b6-126">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="e54b6-126">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="e54b6-127">A fürterőforrás részleteinek megtekintése.</span><span class="sxs-lookup"><span data-stu-id="e54b6-127">Get the cluster resource details.</span></span>

### [<span data-ttu-id="e54b6-128">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="e54b6-128">Get-AzServiceFabricManagedCluster</span></span>](Get-AzServiceFabricManagedCluster.md)
<span data-ttu-id="e54b6-129">A felügyelt fürterőforrás részleteinek megtekintése.</span><span class="sxs-lookup"><span data-stu-id="e54b6-129">Get the managed cluster resource details.</span></span>

### [<span data-ttu-id="e54b6-130">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="e54b6-130">Get-AzServiceFabricManagedNodeType</span></span>](Get-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="e54b6-131">A felügyelt csomópont típusú erőforrás részleteinek lekérte.</span><span class="sxs-lookup"><span data-stu-id="e54b6-131">Get the managed node type resource details.</span></span>

### [<span data-ttu-id="e54b6-132">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="e54b6-132">Get-AzServiceFabricService</span></span>](Get-AzServiceFabricService.md)
<span data-ttu-id="e54b6-133">A Service Fabric szolgáltatás részleteinek lekérte a megadott alkalmazás és fürt alatt.</span><span class="sxs-lookup"><span data-stu-id="e54b6-133">Get Service Fabric service details under the specified application and cluster.</span></span>

### [<span data-ttu-id="e54b6-134">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e54b6-134">New-AzServiceFabricApplication</span></span>](New-AzServiceFabricApplication.md)
<span data-ttu-id="e54b6-135">Hozzon létre új service fabric application under the specified resource group and cluster.</span><span class="sxs-lookup"><span data-stu-id="e54b6-135">Create new service fabric application under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="e54b6-136">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="e54b6-136">New-AzServiceFabricApplicationType</span></span>](New-AzServiceFabricApplicationType.md)
<span data-ttu-id="e54b6-137">Hozzon létre új service fabric application type under the specified resource group and cluster.</span><span class="sxs-lookup"><span data-stu-id="e54b6-137">Create new service fabric application type under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="e54b6-138">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e54b6-138">New-AzServiceFabricApplicationTypeVersion</span></span>](New-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="e54b6-139">Új alkalmazástípus-verzió létrehozása a megadott erőforráscsoport és fürt alatt.</span><span class="sxs-lookup"><span data-stu-id="e54b6-139">Create new application type version under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="e54b6-140">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="e54b6-140">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="e54b6-141">Ez a parancs az Ön által vagy a rendszer által létrehozott öna aláírt tanúsítványok alapján hoz létre egy új szolgáltatás-hálócsoportot.</span><span class="sxs-lookup"><span data-stu-id="e54b6-141">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="e54b6-142">Használhat alapértelmezett sablont vagy egyéni sablont, amit Ön biztosít.</span><span class="sxs-lookup"><span data-stu-id="e54b6-142">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="e54b6-143">Megadhatja azt a mappát, amelybe exportálhatja az önaírt tanúsítványokat, vagy később lehívhatja őket a kulcstárból.</span><span class="sxs-lookup"><span data-stu-id="e54b6-143">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span>

### [<span data-ttu-id="e54b6-144">New-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="e54b6-144">New-AzServiceFabricManagedCluster</span></span>](New-AzServiceFabricManagedCluster.md)
<span data-ttu-id="e54b6-145">Hozzon létre új felügyelt fürtöt.</span><span class="sxs-lookup"><span data-stu-id="e54b6-145">Create new managed cluster.</span></span>

### [<span data-ttu-id="e54b6-146">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="e54b6-146">New-AzServiceFabricManagedNodeType</span></span>](New-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="e54b6-147">Új csomóponttípus-erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="e54b6-147">Create new node type resource.</span></span>

### [<span data-ttu-id="e54b6-148">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="e54b6-148">New-AzServiceFabricService</span></span>](New-AzServiceFabricService.md)
<span data-ttu-id="e54b6-149">Hozzon létre új szervizszolgáltatást a megadott alkalmazás és fürt alatt.</span><span class="sxs-lookup"><span data-stu-id="e54b6-149">Create new service fabric service under the specified application and cluster.</span></span>

### [<span data-ttu-id="e54b6-150">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e54b6-150">Remove-AzServiceFabricApplication</span></span>](Remove-AzServiceFabricApplication.md)
<span data-ttu-id="e54b6-151">Alkalmazás eltávolítása a fürtből</span><span class="sxs-lookup"><span data-stu-id="e54b6-151">Remove an application from the cluster.</span></span> <span data-ttu-id="e54b6-152">Ezzel eltávolítja az alkalmazás összes szolgáltatását.</span><span class="sxs-lookup"><span data-stu-id="e54b6-152">This will remove all the services under the application.</span></span>

### [<span data-ttu-id="e54b6-153">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="e54b6-153">Remove-AzServiceFabricApplicationType</span></span>](Remove-AzServiceFabricApplicationType.md)
<span data-ttu-id="e54b6-154">Távolítsa el a Service fabric egy alkalmazástípust a fürtből.</span><span class="sxs-lookup"><span data-stu-id="e54b6-154">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="e54b6-155">Ezzel eltávolítja az erőforrás összes típusverzióját.</span><span class="sxs-lookup"><span data-stu-id="e54b6-155">This will remove all type versions under this resource.</span></span>

### [<span data-ttu-id="e54b6-156">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e54b6-156">Remove-AzServiceFabricApplicationTypeVersion</span></span>](Remove-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="e54b6-157">Távolítsa el a service fabric an application type version from the cluster.</span><span class="sxs-lookup"><span data-stu-id="e54b6-157">Remove Service fabric an application type version from the cluster.</span></span>

### [<span data-ttu-id="e54b6-158">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e54b6-158">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="e54b6-159">Távolítsa el az ügyfél-tanúsítvány(ok) vagy a tanúsítvány tulajdonosának(ok) nevét az ügyfél-hitelesítéshez a fürtre való ügyfélalkalmazás-hitelesítéshez.</span><span class="sxs-lookup"><span data-stu-id="e54b6-159">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="e54b6-160">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="e54b6-160">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="e54b6-161">Távolítsa el a fürt tanúsítványát a fürtbiztonság érdekében.</span><span class="sxs-lookup"><span data-stu-id="e54b6-161">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="e54b6-162">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="e54b6-162">Remove-AzServiceFabricManagedCluster</span></span>](Remove-AzServiceFabricManagedCluster.md)
<span data-ttu-id="e54b6-163">Fürterőforrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e54b6-163">Remove cluster resource.</span></span>

### [<span data-ttu-id="e54b6-164">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e54b6-164">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>](Remove-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="e54b6-165">Ügyfél tanúsítványának visszaírása thumbprint vagy common name alapján.</span><span class="sxs-lookup"><span data-stu-id="e54b6-165">Remvoe client certificate by thumbprint or common name.</span></span>

### [<span data-ttu-id="e54b6-166">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="e54b6-166">Remove-AzServiceFabricManagedNodeType</span></span>](Remove-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="e54b6-167">Távolítsa el a csomóponttípust vagy a csomóponttípus adott csomópontját.</span><span class="sxs-lookup"><span data-stu-id="e54b6-167">Remove the node type or specific nodes within the node type.</span></span>

### [<span data-ttu-id="e54b6-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="e54b6-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="e54b6-169">Távolítsa el a vm bővítményt a csomóponttípusból.</span><span class="sxs-lookup"><span data-stu-id="e54b6-169">Remove vm extension from the node type.</span></span>

### [<span data-ttu-id="e54b6-170">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="e54b6-170">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="e54b6-171">Csomópontok eltávolítása az adott csomóponttípusból a fürtből.</span><span class="sxs-lookup"><span data-stu-id="e54b6-171">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="e54b6-172">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="e54b6-172">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="e54b6-173">Teljes csomóponttípus eltávolítása a fürtből.</span><span class="sxs-lookup"><span data-stu-id="e54b6-173">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="e54b6-174">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="e54b6-174">Remove-AzServiceFabricService</span></span>](Remove-AzServiceFabricService.md)
<span data-ttu-id="e54b6-175">Szolgáltatás eltávolítása a fürtből.</span><span class="sxs-lookup"><span data-stu-id="e54b6-175">Remove a service from the cluster.</span></span>

### [<span data-ttu-id="e54b6-176">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="e54b6-176">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="e54b6-177">Távolítson el egy vagy több Service Fabric-beállítást a fürtből.</span><span class="sxs-lookup"><span data-stu-id="e54b6-177">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="e54b6-178">Restart-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="e54b6-178">Restart-AzServiceFabricManagedNodeType</span></span>](Restart-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="e54b6-179">Indítsa újra az egyes csomópontokat a csomóponttípusból.</span><span class="sxs-lookup"><span data-stu-id="e54b6-179">Restart specific nodes from the node type.</span></span>

### [<span data-ttu-id="e54b6-180">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="e54b6-180">Set-AzServiceFabricManagedCluster</span></span>](Set-AzServiceFabricManagedCluster.md)
<span data-ttu-id="e54b6-181">Adja meg a fürterőforrás tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="e54b6-181">Set cluster resource properties.</span></span>

### [<span data-ttu-id="e54b6-182">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="e54b6-182">Set-AzServiceFabricManagedNodeType</span></span>](Set-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="e54b6-183">Beállítja a csomóponttípus erőforrástulajdonságokat, vagy reimage műveleteket futtat a csomóponttípus -Reimage paraméterrel megadott ndes-ján.</span><span class="sxs-lookup"><span data-stu-id="e54b6-183">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

### [<span data-ttu-id="e54b6-184">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="e54b6-184">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="e54b6-185">Vegyen fel vagy frissítsen egy vagy több Service Fabric-beállítást a fürtben.</span><span class="sxs-lookup"><span data-stu-id="e54b6-185">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="e54b6-186">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="e54b6-186">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="e54b6-187">Módosítsa a Service Fabric frissítési típusát a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="e54b6-187">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="e54b6-188">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e54b6-188">Update-AzServiceFabricApplication</span></span>](Update-AzServiceFabricApplication.md)
<span data-ttu-id="e54b6-189">Szervizáru-alkalmazás frissítése.</span><span class="sxs-lookup"><span data-stu-id="e54b6-189">Update a service fabric application.</span></span> <span data-ttu-id="e54b6-190">Ez lehetővé teszi az alkalmazásparaméterek frissítését és/vagy az alkalmazástípus verzióját, amely elindít egy alkalmazásfrissítést.</span><span class="sxs-lookup"><span data-stu-id="e54b6-190">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

### [<span data-ttu-id="e54b6-191">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="e54b6-191">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="e54b6-192">Frissítse a fürtben egy csomóponttípushoz a megőrzési szintet vagy a VmSku-t.</span><span class="sxs-lookup"><span data-stu-id="e54b6-192">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="e54b6-193">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="e54b6-193">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="e54b6-194">Frissítse egy fürt elsődleges csomóponttípusának megbízhatósági rétegét.</span><span class="sxs-lookup"><span data-stu-id="e54b6-194">Update the reliability tier of the primary node type in a cluster.</span></span>

