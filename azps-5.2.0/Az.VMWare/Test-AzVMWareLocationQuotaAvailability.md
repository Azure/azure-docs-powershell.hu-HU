---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationquotaavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationQuotaAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationQuotaAvailability.md
ms.openlocfilehash: 9cb677ff172c986f18c7c11c00e0f8d7e0bbf5bf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364250"
---
# <span data-ttu-id="9900c-101">Test-AzVMWareLocationQuotaAvailability</span><span class="sxs-lookup"><span data-stu-id="9900c-101">Test-AzVMWareLocationQuotaAvailability</span></span>

## <span data-ttu-id="9900c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9900c-102">SYNOPSIS</span></span>
<span data-ttu-id="9900c-103">Régiónkénti előfizetés visszaküldési kvótája</span><span class="sxs-lookup"><span data-stu-id="9900c-103">Return quota for subscription by region</span></span>

## <span data-ttu-id="9900c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9900c-104">SYNTAX</span></span>

### <span data-ttu-id="9900c-105">Pipa (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9900c-105">Check (Default)</span></span>
```
Test-AzVMWareLocationQuotaAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9900c-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9900c-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationQuotaAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9900c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9900c-107">DESCRIPTION</span></span>
<span data-ttu-id="9900c-108">Régiónkénti előfizetés visszaküldési kvótája</span><span class="sxs-lookup"><span data-stu-id="9900c-108">Return quota for subscription by region</span></span>

## <span data-ttu-id="9900c-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9900c-109">EXAMPLES</span></span>

### <span data-ttu-id="9900c-110">1. példa: A kvóta elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="9900c-110">Example 1: Check quota availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationQuotaAvailability -Location eastus

Enabled
-------
Disabled
```

<span data-ttu-id="9900c-111">A kvóta elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="9900c-111">Check quota availability</span></span>

## <span data-ttu-id="9900c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9900c-112">PARAMETERS</span></span>

### <span data-ttu-id="9900c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9900c-113">-DefaultProfile</span></span>
<span data-ttu-id="9900c-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9900c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9900c-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9900c-115">-InputObject</span></span>
<span data-ttu-id="9900c-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="9900c-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9900c-117">-Location</span><span class="sxs-lookup"><span data-stu-id="9900c-117">-Location</span></span>
<span data-ttu-id="9900c-118">Azure-régió</span><span class="sxs-lookup"><span data-stu-id="9900c-118">Azure region</span></span>

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

### <span data-ttu-id="9900c-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9900c-119">-SubscriptionId</span></span>
<span data-ttu-id="9900c-120">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9900c-120">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9900c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9900c-121">-Confirm</span></span>
<span data-ttu-id="9900c-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9900c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9900c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9900c-123">-WhatIf</span></span>
<span data-ttu-id="9900c-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9900c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9900c-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9900c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9900c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9900c-126">CommonParameters</span></span>
<span data-ttu-id="9900c-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9900c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9900c-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9900c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9900c-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9900c-129">INPUTS</span></span>

### <span data-ttu-id="9900c-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="9900c-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="9900c-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9900c-131">OUTPUTS</span></span>

### <span data-ttu-id="9900c-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IQuota</span><span class="sxs-lookup"><span data-stu-id="9900c-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IQuota</span></span>

## <span data-ttu-id="9900c-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9900c-133">NOTES</span></span>

<span data-ttu-id="9900c-134">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="9900c-134">ALIASES</span></span>

<span data-ttu-id="9900c-135">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="9900c-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9900c-136">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="9900c-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9900c-137">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9900c-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9900c-138">INPUTOBJECT: <IVMWareIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="9900c-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9900c-139">`[AuthorizationName <String>]`: Az ExpressRoute-áramkör engedélyezési szolgáltatásának neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="9900c-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="9900c-140">`[ClusterName <String>]`: A privát felhőben lévő fürt neve</span><span class="sxs-lookup"><span data-stu-id="9900c-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="9900c-141">`[HcxEnterpriseSiteName <String>]`: A HCX Enterprise webhely neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="9900c-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="9900c-142">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="9900c-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9900c-143">`[Location <String>]`: Azure-régió</span><span class="sxs-lookup"><span data-stu-id="9900c-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="9900c-144">`[PrivateCloudName <String>]`: A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="9900c-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="9900c-145">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9900c-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9900c-146">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="9900c-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="9900c-147">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9900c-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="9900c-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9900c-148">RELATED LINKS</span></span>

