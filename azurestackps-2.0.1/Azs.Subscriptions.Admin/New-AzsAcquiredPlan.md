---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsacquiredplan
schema: 2.0.0
ms.openlocfilehash: 0db0f7ae4358e49ff62f94132701be1f4bd4d0b7
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015337"
---
# <span data-ttu-id="4a28c-101">New-AzsAcquiredPlan</span><span class="sxs-lookup"><span data-stu-id="4a28c-101">New-AzsAcquiredPlan</span></span>

## <span data-ttu-id="4a28c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4a28c-102">SYNOPSIS</span></span>


## <span data-ttu-id="4a28c-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4a28c-103">SYNTAX</span></span>

### <span data-ttu-id="4a28c-104">CreateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4a28c-104">CreateExpanded (Default)</span></span>
```
New-AzsAcquiredPlan -TargetSubscriptionId <String> [-PlanAcquisitionId <String>] [-SubscriptionId <String>]
 [-AcquisitionTime <DateTime>] [-ExternalReferenceId <String>] [-Id <String>] [-PlanId <String>]
 [-ProvisioningState <ProvisioningState>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="4a28c-105">Létrehozása</span><span class="sxs-lookup"><span data-stu-id="4a28c-105">Create</span></span>
```
New-AzsAcquiredPlan -TargetSubscriptionId <String> -AcquiredPlanDefinition <IPlanAcquisition>
 [-PlanAcquisitionId <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="4a28c-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="4a28c-106">DESCRIPTION</span></span>


## <span data-ttu-id="4a28c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4a28c-107">EXAMPLES</span></span>

### <span data-ttu-id="4a28c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4a28c-108">Example 1</span></span>
```powershell
PS C:\> New-AzsAcquiredPlan -PlanAcquisitionId $([Guid]::NewGuid()) -PlanId "/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan" -TargetSubscriptionId "d77ed1d7-cb62-4658-a777-386a8ae523dd"

AcquisitionId       : 718c7f7c-4868-479a-98ce-5caaa8f158c1
AcquisitionTime     : 3/12/2020 11:16:08 PM
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/acquiredPlan
                      s/718c7f7c-4868-479a-98ce-5caaa8f158c1
PlanId              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/plans/testplan
ProvisioningState   : Succeeded
```

<span data-ttu-id="4a28c-109">Előfizetési csomag létrehozása</span><span class="sxs-lookup"><span data-stu-id="4a28c-109">Create a subscription plan.</span></span>

## <span data-ttu-id="4a28c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4a28c-110">PARAMETERS</span></span>

### <span data-ttu-id="4a28c-111">-AcquiredPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="4a28c-111">-AcquiredPlanDefinition</span></span>
<span data-ttu-id="4a28c-112">A kivitelezéshez tekintse meg a ACQUIREDPLANDEFINITION tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="4a28c-112">To construct, see NOTES section for ACQUIREDPLANDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="4a28c-113">-AcquisitionTime</span><span class="sxs-lookup"><span data-stu-id="4a28c-113">-AcquisitionTime</span></span>


```yaml
Type: System.DateTime
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4a28c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a28c-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="4a28c-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="4a28c-115">-ExternalReferenceId</span></span>


```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4a28c-116">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="4a28c-116">-Id</span></span>


```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4a28c-117">-PlanAcquisitionId</span><span class="sxs-lookup"><span data-stu-id="4a28c-117">-PlanAcquisitionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4a28c-118">-PlanId</span><span class="sxs-lookup"><span data-stu-id="4a28c-118">-PlanId</span></span>


```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4a28c-119">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="4a28c-119">-ProvisioningState</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.ProvisioningState
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4a28c-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4a28c-120">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4a28c-121">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4a28c-121">-TargetSubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4a28c-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4a28c-122">-Confirm</span></span>
<span data-ttu-id="4a28c-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4a28c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a28c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a28c-124">-WhatIf</span></span>
<span data-ttu-id="4a28c-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4a28c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a28c-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4a28c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a28c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a28c-127">CommonParameters</span></span>
<span data-ttu-id="4a28c-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4a28c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a28c-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4a28c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a28c-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a28c-130">INPUTS</span></span>

### <span data-ttu-id="4a28c-131">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. IPlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="4a28c-131">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition</span></span>

## <span data-ttu-id="4a28c-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a28c-132">OUTPUTS</span></span>

### <span data-ttu-id="4a28c-133">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. IPlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="4a28c-133">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition</span></span>

<span data-ttu-id="4a28c-134">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="4a28c-134">ALIASES</span></span>

<span data-ttu-id="4a28c-135">New-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="4a28c-135">New-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="4a28c-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4a28c-136">NOTES</span></span>

<span data-ttu-id="4a28c-137">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="4a28c-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4a28c-138">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="4a28c-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="4a28c-139">ACQUIREDPLANDEFINITION <IPlanAcquisition> :</span><span class="sxs-lookup"><span data-stu-id="4a28c-139">ACQUIREDPLANDEFINITION <IPlanAcquisition>:</span></span> 
  - <span data-ttu-id="4a28c-140">`[AcquisitionId <String>]`: Beszerzési azonosító.</span><span class="sxs-lookup"><span data-stu-id="4a28c-140">`[AcquisitionId <String>]`: Acquisition identifier.</span></span>
  - <span data-ttu-id="4a28c-141">`[AcquisitionTime <DateTime?>]`: Beszerzési idő.</span><span class="sxs-lookup"><span data-stu-id="4a28c-141">`[AcquisitionTime <DateTime?>]`: Acquisition time.</span></span>
  - <span data-ttu-id="4a28c-142">`[ExternalReferenceId <String>]`: Külső hivatkozási azonosító.</span><span class="sxs-lookup"><span data-stu-id="4a28c-142">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="4a28c-143">`[Id <String>]`: Azonosító a bérlői előfizetési környezetben.</span><span class="sxs-lookup"><span data-stu-id="4a28c-143">`[Id <String>]`: Identifier in the tenant subscription context.</span></span>
  - <span data-ttu-id="4a28c-144">`[PlanId <String>]`: A csomag azonosítóját a bérlői előfizetési környezetben.</span><span class="sxs-lookup"><span data-stu-id="4a28c-144">`[PlanId <String>]`: Plan identifier in the tenant subscription context.</span></span>
  - <span data-ttu-id="4a28c-145">`[ProvisioningState <ProvisioningState?>]`: A kiépítés állapota</span><span class="sxs-lookup"><span data-stu-id="4a28c-145">`[ProvisioningState <ProvisioningState?>]`: State of the provisioning.</span></span>

## <span data-ttu-id="4a28c-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4a28c-146">RELATED LINKS</span></span>

