---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/test-azvmwarelocationtrialavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationTrialAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationTrialAvailability.md
ms.openlocfilehash: 133dc4dd259025556ab5f8dd3b848ae70a5101c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937233"
---
# <span data-ttu-id="d4aa3-101">Test-AzVMWareLocationTrialAvailability</span><span class="sxs-lookup"><span data-stu-id="d4aa3-101">Test-AzVMWareLocationTrialAvailability</span></span>

## <span data-ttu-id="d4aa3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4aa3-102">SYNOPSIS</span></span>
<span data-ttu-id="d4aa3-103">Próba-állapot visszaküldése régiónkénti előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="d4aa3-103">Return trial status for subscription by region</span></span>

## <span data-ttu-id="d4aa3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d4aa3-104">SYNTAX</span></span>

### <span data-ttu-id="d4aa3-105">Pipa (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d4aa3-105">Check (Default)</span></span>
```
Test-AzVMWareLocationTrialAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d4aa3-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d4aa3-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationTrialAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d4aa3-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d4aa3-107">DESCRIPTION</span></span>
<span data-ttu-id="d4aa3-108">Próba-állapot visszaküldése régiónkénti előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="d4aa3-108">Return trial status for subscription by region</span></span>

## <span data-ttu-id="d4aa3-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d4aa3-109">EXAMPLES</span></span>

### <span data-ttu-id="d4aa3-110">1. példa: A próbaverzió elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="d4aa3-110">Example 1: Check trial availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationTrialAvailability -Location australiaeast

AvailableHost Status
------------- ------
0             TrialDisabled
```

<span data-ttu-id="d4aa3-111">A próbaverzió elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="d4aa3-111">Check trial availability</span></span>

## <span data-ttu-id="d4aa3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4aa3-112">PARAMETERS</span></span>

### <span data-ttu-id="d4aa3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4aa3-113">-DefaultProfile</span></span>
<span data-ttu-id="d4aa3-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d4aa3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4aa3-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4aa3-115">-InputObject</span></span>
<span data-ttu-id="d4aa3-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="d4aa3-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d4aa3-117">-Location</span><span class="sxs-lookup"><span data-stu-id="d4aa3-117">-Location</span></span>
<span data-ttu-id="d4aa3-118">Azure-régió</span><span class="sxs-lookup"><span data-stu-id="d4aa3-118">Azure region</span></span>

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

### <span data-ttu-id="d4aa3-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d4aa3-119">-SubscriptionId</span></span>
<span data-ttu-id="d4aa3-120">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d4aa3-120">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d4aa3-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4aa3-121">-Confirm</span></span>
<span data-ttu-id="d4aa3-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d4aa3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4aa3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4aa3-123">-WhatIf</span></span>
<span data-ttu-id="d4aa3-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d4aa3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4aa3-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d4aa3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4aa3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4aa3-126">CommonParameters</span></span>
<span data-ttu-id="d4aa3-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4aa3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4aa3-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4aa3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4aa3-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d4aa3-129">INPUTS</span></span>

### <span data-ttu-id="d4aa3-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="d4aa3-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="d4aa3-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4aa3-131">OUTPUTS</span></span>

### <span data-ttu-id="d4aa3-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ITrial</span><span class="sxs-lookup"><span data-stu-id="d4aa3-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ITrial</span></span>

## <span data-ttu-id="d4aa3-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d4aa3-133">NOTES</span></span>

<span data-ttu-id="d4aa3-134">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d4aa3-134">ALIASES</span></span>

<span data-ttu-id="d4aa3-135">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="d4aa3-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d4aa3-136">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="d4aa3-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d4aa3-137">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d4aa3-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d4aa3-138">INPUTOBJECT: <IVMWareIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="d4aa3-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d4aa3-139">`[AuthorizationName <String>]`: Az ExpressRoute-áramkör engedélyezési szolgáltatásának neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="d4aa3-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="d4aa3-140">`[ClusterName <String>]`: A privát felhőben lévő fürt neve</span><span class="sxs-lookup"><span data-stu-id="d4aa3-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="d4aa3-141">`[HcxEnterpriseSiteName <String>]`: A HCX Enterprise webhely neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="d4aa3-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="d4aa3-142">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="d4aa3-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d4aa3-143">`[Location <String>]`: Azure-régió</span><span class="sxs-lookup"><span data-stu-id="d4aa3-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="d4aa3-144">`[PrivateCloudName <String>]`: A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="d4aa3-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="d4aa3-145">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d4aa3-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d4aa3-146">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="d4aa3-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="d4aa3-147">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d4aa3-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="d4aa3-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4aa3-148">RELATED LINKS</span></span>

