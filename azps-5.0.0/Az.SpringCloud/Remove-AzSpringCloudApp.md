---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
ms.openlocfilehash: e363a7bedc891c736f06b60c093483010e6b261d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185227"
---
# <span data-ttu-id="14e98-101">Remove-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="14e98-101">Remove-AzSpringCloudApp</span></span>

## <span data-ttu-id="14e98-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="14e98-102">SYNOPSIS</span></span>
<span data-ttu-id="14e98-103">Műveletet törölhet egy alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="14e98-103">Operation to delete an App.</span></span>

## <span data-ttu-id="14e98-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="14e98-104">SYNTAX</span></span>

### <span data-ttu-id="14e98-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="14e98-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="14e98-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="14e98-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="14e98-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="14e98-107">DESCRIPTION</span></span>
<span data-ttu-id="14e98-108">Műveletet törölhet egy alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="14e98-108">Operation to delete an App.</span></span>

## <span data-ttu-id="14e98-109">Példák</span><span class="sxs-lookup"><span data-stu-id="14e98-109">EXAMPLES</span></span>

### <span data-ttu-id="14e98-110">1. példa: a tavaszi felhő alkalmazás eltávolítása név szerint.</span><span class="sxs-lookup"><span data-stu-id="14e98-110">Example 1: Remove Spring Cloud App by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
```

<span data-ttu-id="14e98-111">A tavaszi felhő alkalmazás eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="14e98-111">Remove Spring Cloud App by name.</span></span>

### <span data-ttu-id="14e98-112">2. példa: a tavaszi felhő alkalmazás eltávolítása a pipe-ról</span><span class="sxs-lookup"><span data-stu-id="14e98-112">Example 2: Remove Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Remove-AzSpringCloudApp
```

<span data-ttu-id="14e98-113">A tavaszi felhő alkalmazás eltávolítása a pipe-ról</span><span class="sxs-lookup"><span data-stu-id="14e98-113">Remove Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="14e98-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="14e98-114">PARAMETERS</span></span>

### <span data-ttu-id="14e98-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14e98-115">-AsJob</span></span>
<span data-ttu-id="14e98-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="14e98-116">Run the command as a job</span></span>

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

### <span data-ttu-id="14e98-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14e98-117">-DefaultProfile</span></span>
<span data-ttu-id="14e98-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="14e98-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14e98-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14e98-119">-InputObject</span></span>
<span data-ttu-id="14e98-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="14e98-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14e98-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="14e98-121">-Name</span></span>
<span data-ttu-id="14e98-122">Az App-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="14e98-122">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e98-123">-Várva</span><span class="sxs-lookup"><span data-stu-id="14e98-123">-NoWait</span></span>
<span data-ttu-id="14e98-124">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="14e98-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="14e98-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14e98-125">-PassThru</span></span>
<span data-ttu-id="14e98-126">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="14e98-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="14e98-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14e98-127">-ResourceGroupName</span></span>
<span data-ttu-id="14e98-128">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="14e98-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="14e98-129">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="14e98-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e98-130">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="14e98-130">-ServiceName</span></span>
<span data-ttu-id="14e98-131">A szolgáltatás erőforrásának neve.</span><span class="sxs-lookup"><span data-stu-id="14e98-131">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e98-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="14e98-132">-SubscriptionId</span></span>
<span data-ttu-id="14e98-133">Megkapja az előfizetés AZONOSÍTÓját, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="14e98-133">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="14e98-134">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="14e98-134">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e98-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="14e98-135">-Confirm</span></span>
<span data-ttu-id="14e98-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="14e98-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14e98-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14e98-137">-WhatIf</span></span>
<span data-ttu-id="14e98-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="14e98-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14e98-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="14e98-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14e98-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14e98-140">CommonParameters</span></span>
<span data-ttu-id="14e98-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="14e98-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14e98-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="14e98-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14e98-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="14e98-143">INPUTS</span></span>

### <span data-ttu-id="14e98-144">Microsoft. Azure. PowerShell. parancsmagok. SpringCloud. models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="14e98-144">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="14e98-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="14e98-145">OUTPUTS</span></span>

### <span data-ttu-id="14e98-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="14e98-146">System.Boolean</span></span>

## <span data-ttu-id="14e98-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="14e98-147">NOTES</span></span>

<span data-ttu-id="14e98-148">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="14e98-148">ALIASES</span></span>

<span data-ttu-id="14e98-149">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="14e98-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="14e98-150">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="14e98-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="14e98-151">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="14e98-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="14e98-152">INPUTOBJECT <ISpringCloudIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="14e98-152">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="14e98-153">`[AppName <String>]`: Az App-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="14e98-153">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="14e98-154">`[BindingName <String>]`: A kötési erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="14e98-154">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="14e98-155">`[CertificateName <String>]`: A tanúsítvány-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="14e98-155">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="14e98-156">`[DeploymentName <String>]`: A telepítő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="14e98-156">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="14e98-157">`[DomainName <String>]`: Az egyéni tartomány-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="14e98-157">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="14e98-158">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="14e98-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="14e98-159">`[Location <String>]`: a régió</span><span class="sxs-lookup"><span data-stu-id="14e98-159">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="14e98-160">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="14e98-160">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="14e98-161">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="14e98-161">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="14e98-162">`[ServiceName <String>]`: A szolgáltatás-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="14e98-162">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="14e98-163">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót kapja.</span><span class="sxs-lookup"><span data-stu-id="14e98-163">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="14e98-164">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="14e98-164">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="14e98-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="14e98-165">RELATED LINKS</span></span>

