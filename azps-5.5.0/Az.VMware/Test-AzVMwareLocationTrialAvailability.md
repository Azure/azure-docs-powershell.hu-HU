---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationtrialavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationTrialAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationTrialAvailability.md
ms.openlocfilehash: f667e5f2c6f85e06e1d16a35b1279d88af5e2ed7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162730"
---
# <span data-ttu-id="bb0db-101">Test-AzVMwareLocationTrialAvailability</span><span class="sxs-lookup"><span data-stu-id="bb0db-101">Test-AzVMwareLocationTrialAvailability</span></span>

## <span data-ttu-id="bb0db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb0db-102">SYNOPSIS</span></span>
<span data-ttu-id="bb0db-103">Próba-állapot visszaküldése régiónkénti előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="bb0db-103">Return trial status for subscription by region</span></span>

## <span data-ttu-id="bb0db-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bb0db-104">SYNTAX</span></span>

### <span data-ttu-id="bb0db-105">Pipa (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bb0db-105">Check (Default)</span></span>
```
Test-AzVMwareLocationTrialAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bb0db-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bb0db-106">CheckViaIdentity</span></span>
```
Test-AzVMwareLocationTrialAvailability -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bb0db-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bb0db-107">DESCRIPTION</span></span>
<span data-ttu-id="bb0db-108">Próba-állapot visszaküldése régiónkénti előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="bb0db-108">Return trial status for subscription by region</span></span>

## <span data-ttu-id="bb0db-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bb0db-109">EXAMPLES</span></span>

### <span data-ttu-id="bb0db-110">1. példa: A próbaverzió elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="bb0db-110">Example 1: Check trial availability</span></span>
```powershell
PS C:\> Test-AzVMwareLocationTrialAvailability -Location australiaeast

AvailableHost Status
------------- ------
0             TrialDisabled
```

<span data-ttu-id="bb0db-111">A próbaverzió elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="bb0db-111">Check trial availability</span></span>

## <span data-ttu-id="bb0db-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb0db-112">PARAMETERS</span></span>

### <span data-ttu-id="bb0db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb0db-113">-DefaultProfile</span></span>
<span data-ttu-id="bb0db-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bb0db-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb0db-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb0db-115">-InputObject</span></span>
<span data-ttu-id="bb0db-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="bb0db-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb0db-117">-Location</span><span class="sxs-lookup"><span data-stu-id="bb0db-117">-Location</span></span>
<span data-ttu-id="bb0db-118">Azure-régió</span><span class="sxs-lookup"><span data-stu-id="bb0db-118">Azure region</span></span>

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

### <span data-ttu-id="bb0db-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bb0db-119">-SubscriptionId</span></span>
<span data-ttu-id="bb0db-120">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="bb0db-120">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bb0db-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb0db-121">-Confirm</span></span>
<span data-ttu-id="bb0db-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bb0db-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb0db-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb0db-123">-WhatIf</span></span>
<span data-ttu-id="bb0db-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bb0db-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb0db-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bb0db-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb0db-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb0db-126">CommonParameters</span></span>
<span data-ttu-id="bb0db-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb0db-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb0db-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb0db-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb0db-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bb0db-129">INPUTS</span></span>

### <span data-ttu-id="bb0db-130">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span><span class="sxs-lookup"><span data-stu-id="bb0db-130">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="bb0db-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb0db-131">OUTPUTS</span></span>

### <span data-ttu-id="bb0db-132">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ITrial</span><span class="sxs-lookup"><span data-stu-id="bb0db-132">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ITrial</span></span>

## <span data-ttu-id="bb0db-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bb0db-133">NOTES</span></span>

<span data-ttu-id="bb0db-134">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="bb0db-134">ALIASES</span></span>

<span data-ttu-id="bb0db-135">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="bb0db-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bb0db-136">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="bb0db-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bb0db-137">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bb0db-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bb0db-138">INPUTOBJECT: <IVMwareIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="bb0db-138">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bb0db-139">`[AuthorizationName <String>]`: Az ExpressRoute-áramkör engedélyezési szolgáltatásának neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="bb0db-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="bb0db-140">`[ClusterName <String>]`: A privát felhőben lévő fürt neve</span><span class="sxs-lookup"><span data-stu-id="bb0db-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="bb0db-141">`[HcxEnterpriseSiteName <String>]`: A HCX Enterprise webhely neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="bb0db-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="bb0db-142">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="bb0db-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bb0db-143">`[Location <String>]`: Azure-régió</span><span class="sxs-lookup"><span data-stu-id="bb0db-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="bb0db-144">`[PrivateCloudName <String>]`: A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="bb0db-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="bb0db-145">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bb0db-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="bb0db-146">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="bb0db-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="bb0db-147">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="bb0db-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="bb0db-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bb0db-148">RELATED LINKS</span></span>

