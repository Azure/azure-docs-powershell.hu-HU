---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/edit-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Edit-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Edit-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: be66887225ee78b31497bbd8918faae9535731de
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846993"
---
# <span data-ttu-id="e8ab6-101">Edit-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e8ab6-101">Edit-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="e8ab6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e8ab6-102">SYNOPSIS</span></span>
<span data-ttu-id="e8ab6-103">Webhely-helyreállítási csomag szerkesztése</span><span class="sxs-lookup"><span data-stu-id="e8ab6-103">Edits a Site Recovery plan.</span></span>

## <span data-ttu-id="e8ab6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e8ab6-104">SYNTAX</span></span>

### <span data-ttu-id="e8ab6-105">AppendGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e8ab6-105">AppendGroup (Default)</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8ab6-106">RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="e8ab6-106">RemoveGroup</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8ab6-107">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="e8ab6-107">AddReplicationProtectedItems</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8ab6-108">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="e8ab6-108">RemoveReplicationProtectedItems</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8ab6-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="e8ab6-109">DESCRIPTION</span></span>
<span data-ttu-id="e8ab6-110">A **Edit-AzRecoveryServicesAsrRecoveryPlan** parancsmag az Azure-webhely helyreállítási csomagját szerkeszti.</span><span class="sxs-lookup"><span data-stu-id="e8ab6-110">The **Edit-AzRecoveryServicesAsrRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="e8ab6-111">Példák</span><span class="sxs-lookup"><span data-stu-id="e8ab6-111">EXAMPLES</span></span>

### <span data-ttu-id="e8ab6-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e8ab6-112">Example 1</span></span>
```
PS C:\> $RP = Edit-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP -AppendGroup
```

<span data-ttu-id="e8ab6-113">Hozzáfűz egy csoportot a meglévő Azure webhely-helyreállítási csomaghoz, és a frissített helyreállítási csomagot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="e8ab6-113">Appends a group to existing Azure Site Recovery plan and returns the in-memory updated recovery plan.</span></span> 

## <span data-ttu-id="e8ab6-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e8ab6-114">PARAMETERS</span></span>

### <span data-ttu-id="e8ab6-115">-AddProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e8ab6-115">-AddProtectedItem</span></span>
<span data-ttu-id="e8ab6-116">A helyreállítási terv objektum helyreállítási terv csoportjához hozzáadott ASR-replikációs védelemmel ellátott elemek listája.</span><span class="sxs-lookup"><span data-stu-id="e8ab6-116">List of ASR replication protected items to be added to the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: AddProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ab6-117">-AppendGroup</span><span class="sxs-lookup"><span data-stu-id="e8ab6-117">-AppendGroup</span></span>
<span data-ttu-id="e8ab6-118">Váltson paraméterre a helyreállítási terv csoport a helyreállítási terv objektumhoz való hozzáfűzéséhez.</span><span class="sxs-lookup"><span data-stu-id="e8ab6-118">Switch parameter to append a recovery plan group to the recovery plan object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AppendGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ab6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8ab6-119">-DefaultProfile</span></span>
<span data-ttu-id="e8ab6-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e8ab6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ab6-121">-Csoport</span><span class="sxs-lookup"><span data-stu-id="e8ab6-121">-Group</span></span>
<span data-ttu-id="e8ab6-122">A helyreállítási terv csoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e8ab6-122">Specifies a recovery plan group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ab6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8ab6-123">-InputObject</span></span>
<span data-ttu-id="e8ab6-124">A szerkeszteni kívánt ASR-helyreállítási terv objektuma (a memória műveletben.</span><span class="sxs-lookup"><span data-stu-id="e8ab6-124">The ASR recovery plan object to be edited (In memory operation.</span></span> <span data-ttu-id="e8ab6-125">A helyreállítási terv frissítéséhez futtassa a szerkesztett helyreállítási terv objektummal Update-AzASRRecoveryPlant.)</span><span class="sxs-lookup"><span data-stu-id="e8ab6-125">To update the recovery plan run Update-AzASRRecoveryPlan with the edited recovery plan object.)</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: (All)
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8ab6-126">-RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="e8ab6-126">-RemoveGroup</span></span>
<span data-ttu-id="e8ab6-127">Eltávolítja a megadott csoportot a helyreállítási terv objektumból.</span><span class="sxs-lookup"><span data-stu-id="e8ab6-127">Removes the specified group from the recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ab6-128">-RemoveProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e8ab6-128">-RemoveProtectedItem</span></span>
<span data-ttu-id="e8ab6-129">A helyreállítási terv objektum helyreállítási terv csoportjának helyreállítási terv csoportjának eltávolítása az ASR-replikációval védett elemek listájából.</span><span class="sxs-lookup"><span data-stu-id="e8ab6-129">List of ASR replication protected items to be removed from the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: RemoveProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ab6-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e8ab6-130">-Confirm</span></span>
<span data-ttu-id="e8ab6-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e8ab6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8ab6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8ab6-132">-WhatIf</span></span>
<span data-ttu-id="e8ab6-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e8ab6-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8ab6-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e8ab6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8ab6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8ab6-135">CommonParameters</span></span>
<span data-ttu-id="e8ab6-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e8ab6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8ab6-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e8ab6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8ab6-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8ab6-138">INPUTS</span></span>

### <span data-ttu-id="e8ab6-139">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e8ab6-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="e8ab6-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8ab6-140">OUTPUTS</span></span>

### <span data-ttu-id="e8ab6-141">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e8ab6-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="e8ab6-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e8ab6-142">NOTES</span></span>

## <span data-ttu-id="e8ab6-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e8ab6-143">RELATED LINKS</span></span>

[<span data-ttu-id="e8ab6-144">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e8ab6-144">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="e8ab6-145">Új – AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e8ab6-145">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)
