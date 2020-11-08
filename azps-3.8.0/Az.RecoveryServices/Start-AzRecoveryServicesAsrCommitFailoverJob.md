---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrcommitfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrCommitFailoverJob.md
ms.openlocfilehash: 0714fc44ba8e52536e1a3eb677199da95895bc83
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011615"
---
# <span data-ttu-id="440ec-101">Start-AzRecoveryServicesAsrCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="440ec-101">Start-AzRecoveryServicesAsrCommitFailoverJob</span></span>

## <span data-ttu-id="440ec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="440ec-102">SYNOPSIS</span></span>
<span data-ttu-id="440ec-103">Egy webhely-helyreállítási objektum véglegesítési feladatátvételi tevékenységének indítása.</span><span class="sxs-lookup"><span data-stu-id="440ec-103">Starts the commit failover action for a Site Recovery object.</span></span>

## <span data-ttu-id="440ec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="440ec-104">SYNTAX</span></span>

### <span data-ttu-id="440ec-105">ByRPIObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="440ec-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="440ec-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="440ec-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="440ec-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="440ec-107">DESCRIPTION</span></span>
<span data-ttu-id="440ec-108">A **Start-AzRecoveryServicesAsrCommitFailoverJob** parancsmag a feladatátvételi művelet után egy Azure-webhely helyreállítási objektum véglegesítésének véglegesítését indítja el.</span><span class="sxs-lookup"><span data-stu-id="440ec-108">The **Start-AzRecoveryServicesAsrCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="440ec-109">Példák</span><span class="sxs-lookup"><span data-stu-id="440ec-109">EXAMPLES</span></span>

### <span data-ttu-id="440ec-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="440ec-110">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrCommitFailoverJob -RecoveryPlan $RP
```

<span data-ttu-id="440ec-111">Elindítja a megadott helyreállítási csomag véglegesítési feladatátvételét, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="440ec-111">Starts the commit failover for the specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="440ec-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="440ec-112">PARAMETERS</span></span>

### <span data-ttu-id="440ec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="440ec-113">-DefaultProfile</span></span>
<span data-ttu-id="440ec-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="440ec-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="440ec-115">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="440ec-115">-RecoveryPlan</span></span>
<span data-ttu-id="440ec-116">A helyreállítási tervnek megfelelő ASR-helyreállítási terv objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="440ec-116">Specifies an ASR recovery plan object corresponding to recovery plan to be failovered.</span></span>

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

### <span data-ttu-id="440ec-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="440ec-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="440ec-118">Egy olyan ASR-replikációval védett elem objektumot ad meg, amely megfelel a replikációs védelemmel ellátott elemnek.</span><span class="sxs-lookup"><span data-stu-id="440ec-118">Specifies an ASR replication protected item object corresponding to replication protected item  to be failovered.</span></span>

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

### <span data-ttu-id="440ec-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="440ec-119">-Confirm</span></span>
<span data-ttu-id="440ec-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="440ec-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="440ec-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="440ec-121">-WhatIf</span></span>
<span data-ttu-id="440ec-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="440ec-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="440ec-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="440ec-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="440ec-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="440ec-124">CommonParameters</span></span>
<span data-ttu-id="440ec-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="440ec-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="440ec-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="440ec-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="440ec-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="440ec-127">INPUTS</span></span>

### <span data-ttu-id="440ec-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="440ec-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="440ec-129">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="440ec-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="440ec-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="440ec-130">OUTPUTS</span></span>

### <span data-ttu-id="440ec-131">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="440ec-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="440ec-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="440ec-132">NOTES</span></span>

## <span data-ttu-id="440ec-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="440ec-133">RELATED LINKS</span></span>
