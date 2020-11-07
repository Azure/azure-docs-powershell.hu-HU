---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrcommitfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrCommitFailoverJob.md
ms.openlocfilehash: 1e453f8b11929b96e6e0f2dbe96164c2bf351ae7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839026"
---
# <span data-ttu-id="e79f1-101">Start-AzRecoveryServicesAsrCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="e79f1-101">Start-AzRecoveryServicesAsrCommitFailoverJob</span></span>

## <span data-ttu-id="e79f1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e79f1-102">SYNOPSIS</span></span>
<span data-ttu-id="e79f1-103">Egy webhely-helyreállítási objektum véglegesítési feladatátvételi tevékenységének indítása.</span><span class="sxs-lookup"><span data-stu-id="e79f1-103">Starts the commit failover action for a Site Recovery object.</span></span>

## <span data-ttu-id="e79f1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e79f1-104">SYNTAX</span></span>

### <span data-ttu-id="e79f1-105">ByRPIObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e79f1-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e79f1-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="e79f1-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e79f1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e79f1-107">DESCRIPTION</span></span>
<span data-ttu-id="e79f1-108">A **Start-AzRecoveryServicesAsrCommitFailoverJob** parancsmag a feladatátvételi művelet után egy Azure-webhely helyreállítási objektum véglegesítésének véglegesítését indítja el.</span><span class="sxs-lookup"><span data-stu-id="e79f1-108">The **Start-AzRecoveryServicesAsrCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="e79f1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e79f1-109">EXAMPLES</span></span>

### <span data-ttu-id="e79f1-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e79f1-110">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrCommitFailoverJob -RecoveryPlan $RP
```

<span data-ttu-id="e79f1-111">Elindítja a megadott helyreállítási csomag véglegesítési feladatátvételét, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="e79f1-111">Starts the commit failover for the specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="e79f1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e79f1-112">PARAMETERS</span></span>

### <span data-ttu-id="e79f1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e79f1-113">-DefaultProfile</span></span>
<span data-ttu-id="e79f1-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e79f1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e79f1-115">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e79f1-115">-RecoveryPlan</span></span>
<span data-ttu-id="e79f1-116">A helyreállítási tervnek megfelelő ASR-helyreállítási terv objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="e79f1-116">Specifies an ASR recovery plan object corresponding to recovery plan to be failovered.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e79f1-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e79f1-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="e79f1-118">Egy olyan ASR-replikációval védett elem objektumot ad meg, amely megfelel a replikációs védelemmel ellátott elemnek.</span><span class="sxs-lookup"><span data-stu-id="e79f1-118">Specifies an ASR replication protected item object corresponding to replication protected item  to be failovered.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e79f1-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e79f1-119">-Confirm</span></span>
<span data-ttu-id="e79f1-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e79f1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e79f1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e79f1-121">-WhatIf</span></span>
<span data-ttu-id="e79f1-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e79f1-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e79f1-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e79f1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e79f1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e79f1-124">CommonParameters</span></span>
<span data-ttu-id="e79f1-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e79f1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e79f1-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e79f1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e79f1-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e79f1-127">INPUTS</span></span>

### <span data-ttu-id="e79f1-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e79f1-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="e79f1-129">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e79f1-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="e79f1-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e79f1-130">OUTPUTS</span></span>

### <span data-ttu-id="e79f1-131">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e79f1-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e79f1-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e79f1-132">NOTES</span></span>

## <span data-ttu-id="e79f1-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e79f1-133">RELATED LINKS</span></span>
