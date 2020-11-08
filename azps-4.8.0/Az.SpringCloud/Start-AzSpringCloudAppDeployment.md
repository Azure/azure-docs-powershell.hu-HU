---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/start-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Start-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Start-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 7cab91bf5c7e95258f17a73da4e2b177e30444c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183288"
---
# <span data-ttu-id="a2842-101">Start-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="a2842-101">Start-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="a2842-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a2842-102">SYNOPSIS</span></span>
<span data-ttu-id="a2842-103">Indítsa el a telepítőt.</span><span class="sxs-lookup"><span data-stu-id="a2842-103">Start the deployment.</span></span>

## <span data-ttu-id="a2842-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a2842-104">SYNTAX</span></span>

### <span data-ttu-id="a2842-105">Start (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a2842-105">Start (Default)</span></span>
```
Start-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a2842-106">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a2842-106">StartViaIdentity</span></span>
```
Start-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a2842-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a2842-107">DESCRIPTION</span></span>
<span data-ttu-id="a2842-108">Indítsa el a telepítőt.</span><span class="sxs-lookup"><span data-stu-id="a2842-108">Start the deployment.</span></span>

## <span data-ttu-id="a2842-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a2842-109">EXAMPLES</span></span>

### <span data-ttu-id="a2842-110">Példa 1: a tavaszi Felhőbeli szolgáltatás elindítása név szerint.</span><span class="sxs-lookup"><span data-stu-id="a2842-110">Example 1: Start Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Start-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="a2842-111">Indítsa el a tavaszi felhő szolgáltatását név szerint.</span><span class="sxs-lookup"><span data-stu-id="a2842-111">Start Spring Cloud Service by name.</span></span>

### <span data-ttu-id="a2842-112">2. példa: a tavaszi felhő szolgáltatás elindítása a pipe-ról</span><span class="sxs-lookup"><span data-stu-id="a2842-112">Example 2: Start Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Start-AzSpringCloud
```

<span data-ttu-id="a2842-113">Indítsa el a tavaszi felhő szolgáltatást a pipe-ról.</span><span class="sxs-lookup"><span data-stu-id="a2842-113">Start Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="a2842-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a2842-114">PARAMETERS</span></span>

### <span data-ttu-id="a2842-115">-Appnév</span><span class="sxs-lookup"><span data-stu-id="a2842-115">-AppName</span></span>
<span data-ttu-id="a2842-116">Az App-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="a2842-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2842-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2842-117">-AsJob</span></span>
<span data-ttu-id="a2842-118">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="a2842-118">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2842-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2842-119">-DefaultProfile</span></span>
<span data-ttu-id="a2842-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2842-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2842-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2842-121">-InputObject</span></span>
<span data-ttu-id="a2842-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a2842-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2842-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a2842-123">-Name</span></span>
<span data-ttu-id="a2842-124">A központi telepítő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="a2842-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2842-125">-Várva</span><span class="sxs-lookup"><span data-stu-id="a2842-125">-NoWait</span></span>
<span data-ttu-id="a2842-126">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="a2842-126">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2842-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2842-127">-PassThru</span></span>
<span data-ttu-id="a2842-128">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="a2842-128">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2842-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2842-129">-ResourceGroupName</span></span>
<span data-ttu-id="a2842-130">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a2842-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a2842-131">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="a2842-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2842-132">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="a2842-132">-ServiceName</span></span>
<span data-ttu-id="a2842-133">A szolgáltatás erőforrásának neve.</span><span class="sxs-lookup"><span data-stu-id="a2842-133">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2842-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a2842-134">-SubscriptionId</span></span>
<span data-ttu-id="a2842-135">Megkapja az előfizetés AZONOSÍTÓját, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="a2842-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="a2842-136">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="a2842-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2842-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a2842-137">-Confirm</span></span>
<span data-ttu-id="a2842-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a2842-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2842-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2842-139">-WhatIf</span></span>
<span data-ttu-id="a2842-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a2842-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2842-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a2842-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2842-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2842-142">CommonParameters</span></span>
<span data-ttu-id="a2842-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a2842-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2842-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a2842-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2842-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2842-145">INPUTS</span></span>

### <span data-ttu-id="a2842-146">Microsoft. Azure. PowerShell. parancsmagok. SpringCloud. models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="a2842-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="a2842-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2842-147">OUTPUTS</span></span>

### <span data-ttu-id="a2842-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a2842-148">System.Boolean</span></span>

## <span data-ttu-id="a2842-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a2842-149">NOTES</span></span>

<span data-ttu-id="a2842-150">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a2842-150">ALIASES</span></span>

<span data-ttu-id="a2842-151">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="a2842-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a2842-152">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="a2842-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a2842-153">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="a2842-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a2842-154">INPUTOBJECT <ISpringCloudIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="a2842-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a2842-155">`[AppName <String>]`: Az App-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="a2842-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="a2842-156">`[BindingName <String>]`: A kötési erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="a2842-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="a2842-157">`[CertificateName <String>]`: A tanúsítvány-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="a2842-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="a2842-158">`[DeploymentName <String>]`: A telepítő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="a2842-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="a2842-159">`[DomainName <String>]`: Az egyéni tartomány-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="a2842-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="a2842-160">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="a2842-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a2842-161">`[Location <String>]`: a régió</span><span class="sxs-lookup"><span data-stu-id="a2842-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="a2842-162">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a2842-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="a2842-163">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="a2842-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="a2842-164">`[ServiceName <String>]`: A szolgáltatás-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="a2842-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="a2842-165">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót kapja.</span><span class="sxs-lookup"><span data-stu-id="a2842-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="a2842-166">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="a2842-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a2842-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2842-167">RELATED LINKS</span></span>

