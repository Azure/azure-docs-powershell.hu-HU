---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailovercleanupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverCleanupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverCleanupJob.md
ms.openlocfilehash: 4143bc481091889b293d206192e0c5eba386d68a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839015"
---
# <span data-ttu-id="e587d-101">Start-AzRecoveryServicesAsrTestFailoverCleanupJob</span><span class="sxs-lookup"><span data-stu-id="e587d-101">Start-AzRecoveryServicesAsrTestFailoverCleanupJob</span></span>

## <span data-ttu-id="e587d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e587d-102">SYNOPSIS</span></span>
<span data-ttu-id="e587d-103">Elindítja a feladatátvételi karbantartási műveletet.</span><span class="sxs-lookup"><span data-stu-id="e587d-103">Starts the test failover cleanup operation.</span></span>

## <span data-ttu-id="e587d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e587d-104">SYNTAX</span></span>

### <span data-ttu-id="e587d-105">ByRPIObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e587d-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Comment <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e587d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e587d-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ResourceId <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e587d-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="e587d-107">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan <ASRRecoveryPlan> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e587d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e587d-108">DESCRIPTION</span></span>
<span data-ttu-id="e587d-109">A **Start-AzRecoveryServicesAsrTestFailoverCleanupJob** parancsmag a feladatátvételi karbantartási műveletet egy olyan replikációs védelemmel ellátott elemen vagy helyreállítási tervben indítja el, amelyen végzett a tesztelési feladatátvételt.</span><span class="sxs-lookup"><span data-stu-id="e587d-109">The **Start-AzRecoveryServicesAsrTestFailoverCleanupJob** cmdlet starts the test failover cleanup operation on a replication protected item or recovery plan on which a test failover has been performed.</span></span>

## <span data-ttu-id="e587d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e587d-110">EXAMPLES</span></span>

### <span data-ttu-id="e587d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e587d-111">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem $rpi -Comments "testing done"
```

<span data-ttu-id="e587d-112">Feladat: az Azure webhely-helyreállítási replikációs szolgáltatással védett elemek feladatátvételi karbantartásának nyomon követése</span><span class="sxs-lookup"><span data-stu-id="e587d-112">Job to track test failover Cleanup of an Azure Site Recovery replication protected item.</span></span>

### <span data-ttu-id="e587d-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="e587d-113">Example 2</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan $recoveryPlan -Comment "testing done"
```

<span data-ttu-id="e587d-114">Feladat: az Azure webhely-helyreállítási recoveryPlan tesztelésének nyomon követése</span><span class="sxs-lookup"><span data-stu-id="e587d-114">Job to track test failover Cleanup of an Azure Site Recovery recoveryPlan.</span></span>

## <span data-ttu-id="e587d-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e587d-115">PARAMETERS</span></span>

### <span data-ttu-id="e587d-116">-Megjegyzés</span><span class="sxs-lookup"><span data-stu-id="e587d-116">-Comment</span></span>
<span data-ttu-id="e587d-117">Felhasználói Megjegyzés a feladatátvétel teszteléséhez.</span><span class="sxs-lookup"><span data-stu-id="e587d-117">User Comment for Test Failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e587d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e587d-118">-DefaultProfile</span></span>
<span data-ttu-id="e587d-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e587d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e587d-120">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e587d-120">-RecoveryPlan</span></span>
<span data-ttu-id="e587d-121">Helyreállítási terv a feladatátvételi karbantartás ellenőrzésének végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="e587d-121">Recovery Plan to perform the test failover cleanup on.</span></span>

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

### <span data-ttu-id="e587d-122">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e587d-122">-ReplicationProtectedItem</span></span>
<span data-ttu-id="e587d-123">A többszörözéssel védett elem a feladatátvételi karbantartás ellenőrzésének elvégzéséhez.</span><span class="sxs-lookup"><span data-stu-id="e587d-123">Replication Protected Item to perform the test failover cleanup on.</span></span>

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

### <span data-ttu-id="e587d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e587d-124">-ResourceId</span></span>
<span data-ttu-id="e587d-125">A cleaningup-teszt feladatátvételéhez használt replikációs védelemmel ellátott elem/helyreállítási terv erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e587d-125">Resource Id of replication protected item / recovery plan for cleaningup test failover.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e587d-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e587d-126">-Confirm</span></span>
<span data-ttu-id="e587d-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e587d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e587d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e587d-128">-WhatIf</span></span>
<span data-ttu-id="e587d-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e587d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e587d-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e587d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e587d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e587d-131">CommonParameters</span></span>
<span data-ttu-id="e587d-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e587d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e587d-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e587d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e587d-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e587d-134">INPUTS</span></span>

### <span data-ttu-id="e587d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e587d-135">System.String</span></span>

### <span data-ttu-id="e587d-136">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e587d-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="e587d-137">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e587d-137">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="e587d-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e587d-138">OUTPUTS</span></span>

### <span data-ttu-id="e587d-139">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e587d-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e587d-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e587d-140">NOTES</span></span>

## <span data-ttu-id="e587d-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e587d-141">RELATED LINKS</span></span>
