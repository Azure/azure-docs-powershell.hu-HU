---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/edit-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: f60da52bffcc78e563863c79971beea8d45e398e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499451"
---
# <span data-ttu-id="5435f-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5435f-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="5435f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5435f-102">SYNOPSIS</span></span>
<span data-ttu-id="5435f-103">Webhely-helyreállítási csomag szerkesztése</span><span class="sxs-lookup"><span data-stu-id="5435f-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5435f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5435f-104">SYNTAX</span></span>

### <span data-ttu-id="5435f-105">AppendGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5435f-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5435f-106">RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="5435f-106">RemoveGroup</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5435f-107">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="5435f-107">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5435f-108">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="5435f-108">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5435f-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="5435f-109">DESCRIPTION</span></span>
<span data-ttu-id="5435f-110">A **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** parancsmag az Azure-webhely helyreállítási csomagját szerkeszti.</span><span class="sxs-lookup"><span data-stu-id="5435f-110">The **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="5435f-111">Példák</span><span class="sxs-lookup"><span data-stu-id="5435f-111">EXAMPLES</span></span>

### <span data-ttu-id="5435f-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5435f-112">Example 1</span></span>
```
PS C:\> $RP = Edit-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP -AppendGroup
```

<span data-ttu-id="5435f-113">Hozzáfűzi a csoportot a meglévő Azure webhely-helyreállítási helyreállítási csomaghoz, és a frissített helyreállítási csomagot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="5435f-113">Appends a group to existing Azure Site Recovery recovery plan and returns the in-memory updated recovery plan.</span></span> 

## <span data-ttu-id="5435f-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5435f-114">PARAMETERS</span></span>

### <span data-ttu-id="5435f-115">-AddProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5435f-115">-AddProtectedItem</span></span>
<span data-ttu-id="5435f-116">A helyreállítási terv objektum helyreállítási terv csoportjához hozzáadott ASR-replikációs védelemmel ellátott elemek listája.</span><span class="sxs-lookup"><span data-stu-id="5435f-116">List of ASR replication protected items to be added to the recovery plan group in the recovery plan object.</span></span>

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

### <span data-ttu-id="5435f-117">-AppendGroup</span><span class="sxs-lookup"><span data-stu-id="5435f-117">-AppendGroup</span></span>
<span data-ttu-id="5435f-118">Váltson paraméterre a helyreállítási terv csoport a helyreállítási terv objektumhoz való hozzáfűzéséhez.</span><span class="sxs-lookup"><span data-stu-id="5435f-118">Switch parameter to append a recovery plan group to the recovery plan object.</span></span>

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

### <span data-ttu-id="5435f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5435f-119">-DefaultProfile</span></span>
<span data-ttu-id="5435f-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5435f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5435f-121">-Csoport</span><span class="sxs-lookup"><span data-stu-id="5435f-121">-Group</span></span>
<span data-ttu-id="5435f-122">A helyreállítási terv csoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5435f-122">Specifies a recovery plan group.</span></span>

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

### <span data-ttu-id="5435f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5435f-123">-InputObject</span></span>
<span data-ttu-id="5435f-124">A szerkeszteni kívánt ASR-helyreállítási terv objektuma (a memória műveletben.</span><span class="sxs-lookup"><span data-stu-id="5435f-124">The ASR recovery plan object to be edited (In memory operation.</span></span> <span data-ttu-id="5435f-125">A helyreállítási terv frissítéséhez futtassa a szerkesztett helyreállítási terv objektummal Update-AzureRmASRRecoveryPlant.)</span><span class="sxs-lookup"><span data-stu-id="5435f-125">To update the recovery plan run Update-AzureRmASRRecoveryPlan with the edited recovery plan object.)</span></span>

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

### <span data-ttu-id="5435f-126">-RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="5435f-126">-RemoveGroup</span></span>
<span data-ttu-id="5435f-127">Eltávolítja a megadott csoportot a helyreállítási terv objektumból.</span><span class="sxs-lookup"><span data-stu-id="5435f-127">Removes the specified group from the recovery plan object.</span></span>

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

### <span data-ttu-id="5435f-128">-RemoveProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5435f-128">-RemoveProtectedItem</span></span>
<span data-ttu-id="5435f-129">A helyreállítási terv objektum helyreállítási terv csoportjának helyreállítási terv csoportjának eltávolítása az ASR-replikációval védett elemek listájából.</span><span class="sxs-lookup"><span data-stu-id="5435f-129">List of ASR replication protected items to be removed from the recovery plan group in the recovery plan object.</span></span>

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

### <span data-ttu-id="5435f-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5435f-130">-Confirm</span></span>
<span data-ttu-id="5435f-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5435f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5435f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5435f-132">-WhatIf</span></span>
<span data-ttu-id="5435f-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5435f-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5435f-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5435f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5435f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5435f-135">CommonParameters</span></span>
<span data-ttu-id="5435f-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5435f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5435f-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5435f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5435f-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5435f-138">INPUTS</span></span>

### <span data-ttu-id="5435f-139">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5435f-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="5435f-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5435f-140">OUTPUTS</span></span>

### <span data-ttu-id="5435f-141">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="5435f-141">System.Object</span></span>

## <span data-ttu-id="5435f-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5435f-142">NOTES</span></span>

## <span data-ttu-id="5435f-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5435f-143">RELATED LINKS</span></span>

[<span data-ttu-id="5435f-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5435f-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="5435f-145">Új – AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5435f-145">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)
