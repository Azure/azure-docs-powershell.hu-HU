---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.addomainservices/remove-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Remove-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Remove-AzADDomainService.md
ms.openlocfilehash: f29fbbdd805abb9891f707ed983bcf8aebefc46c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143819"
---
# <span data-ttu-id="a4951-101">Remove-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="a4951-101">Remove-AzADDomainService</span></span>

## <span data-ttu-id="a4951-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4951-102">SYNOPSIS</span></span>
<span data-ttu-id="a4951-103">A Delete Domain Service művelet töröl egy meglévő tartományszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="a4951-103">The Delete Domain Service operation deletes an existing Domain Service.</span></span>

## <span data-ttu-id="a4951-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a4951-104">SYNTAX</span></span>

### <span data-ttu-id="a4951-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a4951-105">Delete (Default)</span></span>
```
Remove-AzADDomainService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a4951-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a4951-106">DeleteViaIdentity</span></span>
```
Remove-AzADDomainService -InputObject <IAdDomainServicesIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a4951-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a4951-107">DESCRIPTION</span></span>
<span data-ttu-id="a4951-108">A Delete Domain Service művelet töröl egy meglévő tartományszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="a4951-108">The Delete Domain Service operation deletes an existing Domain Service.</span></span>

## <span data-ttu-id="a4951-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a4951-109">EXAMPLES</span></span>

### <span data-ttu-id="a4951-110">1. példa: AzADDomain törlése ResourceGroupName és Name szerint</span><span class="sxs-lookup"><span data-stu-id="a4951-110">Example 1: Delete the AzADDomain by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Remove-AzADDomainService -ResourceGroupName $env.ResourceGroupName -Name $env.ADdomainName

```

<span data-ttu-id="a4951-111">Az AzADDomain törlése ResourceGroupName és Name szerint</span><span class="sxs-lookup"><span data-stu-id="a4951-111">Delete the AzADDomain by ResourceGroupName and Name</span></span>

### <span data-ttu-id="a4951-112">2. példa: AzADDomain törlése az InputObject által</span><span class="sxs-lookup"><span data-stu-id="a4951-112">Example 2: Delete the AzADDomain by InputObject</span></span>
```powershell
PS C:\> $GetADDomainExample = Get-AzADDomainService -ResourceGroupName $env.ResourceGroupName -Name $env.ADdomainName
Remove-AzADDomainService -InputObject $GetADDomainExample

```

<span data-ttu-id="a4951-113">Az AzADDomain törlése inputObject szerint</span><span class="sxs-lookup"><span data-stu-id="a4951-113">Delete the AzADDomain by InputObject</span></span>

## <span data-ttu-id="a4951-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4951-114">PARAMETERS</span></span>

### <span data-ttu-id="a4951-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4951-115">-AsJob</span></span>
<span data-ttu-id="a4951-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="a4951-116">Run the command as a job</span></span>

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

### <span data-ttu-id="a4951-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4951-117">-DefaultProfile</span></span>
<span data-ttu-id="a4951-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a4951-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4951-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4951-119">-InputObject</span></span>
<span data-ttu-id="a4951-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="a4951-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4951-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a4951-121">-Name</span></span>
<span data-ttu-id="a4951-122">A tartományszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="a4951-122">The name of the domain service.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4951-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a4951-123">-NoWait</span></span>
<span data-ttu-id="a4951-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="a4951-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a4951-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4951-125">-PassThru</span></span>
<span data-ttu-id="a4951-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="a4951-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a4951-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4951-127">-ResourceGroupName</span></span>
<span data-ttu-id="a4951-128">A felhasználó előfizetésében található erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a4951-128">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="a4951-129">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="a4951-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a4951-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a4951-130">-SubscriptionId</span></span>
<span data-ttu-id="a4951-131">Olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="a4951-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="a4951-132">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="a4951-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a4951-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4951-133">-Confirm</span></span>
<span data-ttu-id="a4951-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a4951-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4951-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4951-135">-WhatIf</span></span>
<span data-ttu-id="a4951-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a4951-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4951-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a4951-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4951-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4951-138">CommonParameters</span></span>
<span data-ttu-id="a4951-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4951-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4951-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a4951-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4951-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a4951-141">INPUTS</span></span>

### <span data-ttu-id="a4951-142">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="a4951-142">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span></span>

## <span data-ttu-id="a4951-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4951-143">OUTPUTS</span></span>

### <span data-ttu-id="a4951-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a4951-144">System.Boolean</span></span>

## <span data-ttu-id="a4951-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a4951-145">NOTES</span></span>

<span data-ttu-id="a4951-146">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a4951-146">ALIASES</span></span>

<span data-ttu-id="a4951-147">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="a4951-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a4951-148">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="a4951-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a4951-149">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a4951-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a4951-150">INPUTOBJECT: <IAdDomainServicesIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="a4951-150">INPUTOBJECT <IAdDomainServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a4951-151">`[DomainServiceName <String>]`: A tartományszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="a4951-151">`[DomainServiceName <String>]`: The name of the domain service.</span></span>
  - <span data-ttu-id="a4951-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="a4951-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a4951-153">`[ResourceGroupName <String>]`: A felhasználó előfizetésében található erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a4951-153">`[ResourceGroupName <String>]`: The name of the resource group within the user's subscription.</span></span> <span data-ttu-id="a4951-154">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="a4951-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="a4951-155">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="a4951-155">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="a4951-156">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="a4951-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a4951-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4951-157">RELATED LINKS</span></span>

