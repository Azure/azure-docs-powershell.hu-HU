---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/stop-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Stop-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Stop-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 3f98161e56019394dc67ab8909aac3fb70a611a2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185225"
---
# <span data-ttu-id="83f79-101">Stop-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="83f79-101">Stop-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="83f79-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="83f79-102">SYNOPSIS</span></span>
<span data-ttu-id="83f79-103">Állítsa le a telepítőt.</span><span class="sxs-lookup"><span data-stu-id="83f79-103">Stop the deployment.</span></span>

## <span data-ttu-id="83f79-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="83f79-104">SYNTAX</span></span>

### <span data-ttu-id="83f79-105">Leállítás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="83f79-105">Stop (Default)</span></span>
```
Stop-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="83f79-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="83f79-106">StopViaIdentity</span></span>
```
Stop-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="83f79-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="83f79-107">DESCRIPTION</span></span>
<span data-ttu-id="83f79-108">Állítsa le a telepítőt.</span><span class="sxs-lookup"><span data-stu-id="83f79-108">Stop the deployment.</span></span>

## <span data-ttu-id="83f79-109">Példák</span><span class="sxs-lookup"><span data-stu-id="83f79-109">EXAMPLES</span></span>

### <span data-ttu-id="83f79-110">1. példa: a tavaszi Felhőbeli szolgáltatás leállítása név szerint.</span><span class="sxs-lookup"><span data-stu-id="83f79-110">Example 1: Stop Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Stop-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="83f79-111">A tavaszi felhő szolgáltatás leállítása név szerint</span><span class="sxs-lookup"><span data-stu-id="83f79-111">Stop Spring Cloud Service by name.</span></span>

### <span data-ttu-id="83f79-112">2. példa: a tavaszi felhő szolgáltatás leállítása a pipe-ról</span><span class="sxs-lookup"><span data-stu-id="83f79-112">Example 2: Stop Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Stop-AzSpringCloud
```

<span data-ttu-id="83f79-113">A tavaszi felhő szolgáltatás leállítása a pipe-ról</span><span class="sxs-lookup"><span data-stu-id="83f79-113">Stop Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="83f79-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="83f79-114">PARAMETERS</span></span>

### <span data-ttu-id="83f79-115">-Appnév</span><span class="sxs-lookup"><span data-stu-id="83f79-115">-AppName</span></span>
<span data-ttu-id="83f79-116">Az App-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="83f79-116">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83f79-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="83f79-117">-AsJob</span></span>
<span data-ttu-id="83f79-118">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="83f79-118">Run the command as a job</span></span>

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

### <span data-ttu-id="83f79-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83f79-119">-DefaultProfile</span></span>
<span data-ttu-id="83f79-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="83f79-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83f79-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83f79-121">-InputObject</span></span>
<span data-ttu-id="83f79-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="83f79-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: StopViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83f79-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="83f79-123">-Name</span></span>
<span data-ttu-id="83f79-124">A központi telepítő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="83f79-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83f79-125">-Várva</span><span class="sxs-lookup"><span data-stu-id="83f79-125">-NoWait</span></span>
<span data-ttu-id="83f79-126">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="83f79-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="83f79-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83f79-127">-PassThru</span></span>
<span data-ttu-id="83f79-128">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="83f79-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="83f79-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83f79-129">-ResourceGroupName</span></span>
<span data-ttu-id="83f79-130">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="83f79-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="83f79-131">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="83f79-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83f79-132">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="83f79-132">-ServiceName</span></span>
<span data-ttu-id="83f79-133">A szolgáltatás erőforrásának neve.</span><span class="sxs-lookup"><span data-stu-id="83f79-133">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83f79-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="83f79-134">-SubscriptionId</span></span>
<span data-ttu-id="83f79-135">Megkapja az előfizetés AZONOSÍTÓját, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="83f79-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="83f79-136">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="83f79-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83f79-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="83f79-137">-Confirm</span></span>
<span data-ttu-id="83f79-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="83f79-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83f79-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83f79-139">-WhatIf</span></span>
<span data-ttu-id="83f79-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="83f79-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83f79-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="83f79-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83f79-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83f79-142">CommonParameters</span></span>
<span data-ttu-id="83f79-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="83f79-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83f79-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="83f79-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83f79-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="83f79-145">INPUTS</span></span>

### <span data-ttu-id="83f79-146">Microsoft. Azure. PowerShell. parancsmagok. SpringCloud. models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="83f79-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="83f79-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83f79-147">OUTPUTS</span></span>

### <span data-ttu-id="83f79-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="83f79-148">System.Boolean</span></span>

## <span data-ttu-id="83f79-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="83f79-149">NOTES</span></span>

<span data-ttu-id="83f79-150">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="83f79-150">ALIASES</span></span>

<span data-ttu-id="83f79-151">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="83f79-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="83f79-152">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="83f79-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="83f79-153">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="83f79-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="83f79-154">INPUTOBJECT <ISpringCloudIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="83f79-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="83f79-155">`[AppName <String>]`: Az App-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="83f79-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="83f79-156">`[BindingName <String>]`: A kötési erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="83f79-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="83f79-157">`[CertificateName <String>]`: A tanúsítvány-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="83f79-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="83f79-158">`[DeploymentName <String>]`: A telepítő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="83f79-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="83f79-159">`[DomainName <String>]`: Az egyéni tartomány-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="83f79-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="83f79-160">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="83f79-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="83f79-161">`[Location <String>]`: a régió</span><span class="sxs-lookup"><span data-stu-id="83f79-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="83f79-162">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="83f79-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="83f79-163">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="83f79-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="83f79-164">`[ServiceName <String>]`: A szolgáltatás-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="83f79-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="83f79-165">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót kapja.</span><span class="sxs-lookup"><span data-stu-id="83f79-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="83f79-166">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="83f79-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="83f79-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83f79-167">RELATED LINKS</span></span>

