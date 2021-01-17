---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationtrialavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationTrialAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationTrialAvailability.md
ms.openlocfilehash: 942ac0b4a8bca964e88c7dfd327fe460f249a915
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467045"
---
# <span data-ttu-id="7f091-101">Test-AzVMWareLocationTrialAvailability</span><span class="sxs-lookup"><span data-stu-id="7f091-101">Test-AzVMWareLocationTrialAvailability</span></span>

## <span data-ttu-id="7f091-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f091-102">SYNOPSIS</span></span>
<span data-ttu-id="7f091-103">Próba-állapot visszaküldése régiónkénti előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="7f091-103">Return trial status for subscription by region</span></span>

## <span data-ttu-id="7f091-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7f091-104">SYNTAX</span></span>

### <span data-ttu-id="7f091-105">Pipa (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7f091-105">Check (Default)</span></span>
```
Test-AzVMWareLocationTrialAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7f091-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7f091-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationTrialAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7f091-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7f091-107">DESCRIPTION</span></span>
<span data-ttu-id="7f091-108">Próba-állapot visszaküldése régiónkénti előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="7f091-108">Return trial status for subscription by region</span></span>

## <span data-ttu-id="7f091-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7f091-109">EXAMPLES</span></span>

### <span data-ttu-id="7f091-110">1. példa: A próbaverzió elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="7f091-110">Example 1: Check trial availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationTrialAvailability -Location australiaeast

AvailableHost Status
------------- ------
0             TrialDisabled
```

<span data-ttu-id="7f091-111">A próbaverzió elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="7f091-111">Check trial availability</span></span>

## <span data-ttu-id="7f091-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f091-112">PARAMETERS</span></span>

### <span data-ttu-id="7f091-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f091-113">-DefaultProfile</span></span>
<span data-ttu-id="7f091-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7f091-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f091-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f091-115">-InputObject</span></span>
<span data-ttu-id="7f091-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="7f091-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f091-117">-Location</span><span class="sxs-lookup"><span data-stu-id="7f091-117">-Location</span></span>
<span data-ttu-id="7f091-118">Azure-régió</span><span class="sxs-lookup"><span data-stu-id="7f091-118">Azure region</span></span>

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f091-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7f091-119">-SubscriptionId</span></span>
<span data-ttu-id="7f091-120">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7f091-120">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f091-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7f091-121">-Confirm</span></span>
<span data-ttu-id="7f091-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7f091-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f091-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f091-123">-WhatIf</span></span>
<span data-ttu-id="7f091-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7f091-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f091-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7f091-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f091-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f091-126">CommonParameters</span></span>
<span data-ttu-id="7f091-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f091-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f091-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f091-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f091-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7f091-129">INPUTS</span></span>

### <span data-ttu-id="7f091-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="7f091-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="7f091-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f091-131">OUTPUTS</span></span>

### <span data-ttu-id="7f091-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ITrial</span><span class="sxs-lookup"><span data-stu-id="7f091-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ITrial</span></span>

## <span data-ttu-id="7f091-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7f091-133">NOTES</span></span>

<span data-ttu-id="7f091-134">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="7f091-134">ALIASES</span></span>

<span data-ttu-id="7f091-135">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="7f091-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7f091-136">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="7f091-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7f091-137">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7f091-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7f091-138">INPUTOBJECT: <IVMWareIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="7f091-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7f091-139">`[AuthorizationName <String>]`: Az ExpressRoute-áramkör engedélyezési szolgáltatásának neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="7f091-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="7f091-140">`[ClusterName <String>]`: A privát felhőben lévő fürt neve</span><span class="sxs-lookup"><span data-stu-id="7f091-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="7f091-141">`[HcxEnterpriseSiteName <String>]`: A HCX Enterprise webhely neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="7f091-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="7f091-142">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="7f091-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7f091-143">`[Location <String>]`: Azure-régió</span><span class="sxs-lookup"><span data-stu-id="7f091-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="7f091-144">`[PrivateCloudName <String>]`: A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="7f091-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="7f091-145">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7f091-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7f091-146">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="7f091-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="7f091-147">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7f091-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="7f091-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f091-148">RELATED LINKS</span></span>

