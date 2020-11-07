---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrtestfailovercleanupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob.md
ms.openlocfilehash: 5d99c9cad96a3f0c4fb877ecd15f8450eb89c4fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672099"
---
# <span data-ttu-id="ae2b3-101">Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob</span><span class="sxs-lookup"><span data-stu-id="ae2b3-101">Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob</span></span>

## <span data-ttu-id="ae2b3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ae2b3-102">SYNOPSIS</span></span>
<span data-ttu-id="ae2b3-103">Elindítja a feladatátvételi karbantartási műveletet.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-103">Starts the test failover cleanup operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae2b3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ae2b3-104">SYNTAX</span></span>

### <span data-ttu-id="ae2b3-105">ByRPIObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ae2b3-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Comment <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae2b3-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ae2b3-106">ByResourceId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ResourceId <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae2b3-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="ae2b3-107">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan <ASRRecoveryPlan> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae2b3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ae2b3-108">DESCRIPTION</span></span>
<span data-ttu-id="ae2b3-109">A **Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob** parancsmag a feladatátvételi karbantartási műveletet egy olyan replikációs védelemmel ellátott elemen vagy helyreállítási tervben indítja el, amelyen végzett a tesztelési feladatátvételt.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-109">The **Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob** cmdlet starts the test failover cleanup operation on a replication protected item or recovery plan on which a test failover has been performed.</span></span>

## <span data-ttu-id="ae2b3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ae2b3-110">EXAMPLES</span></span>

### <span data-ttu-id="ae2b3-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ae2b3-111">Example 1</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem $rpi -Comments "testing done"
```

<span data-ttu-id="ae2b3-112">Feladat: az Azure webhely-helyreállítási replikációs szolgáltatással védett elemek feladatátvételi karbantartásának nyomon követése</span><span class="sxs-lookup"><span data-stu-id="ae2b3-112">Job to track test failover Cleanup of an Azure Site Recovery replication protected item.</span></span>

### <span data-ttu-id="ae2b3-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="ae2b3-113">Example 2</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan $recoveryPlan -Comment "testing done"
```

<span data-ttu-id="ae2b3-114">Feladat: az Azure webhely-helyreállítási recoveryPlan tesztelésének nyomon követése</span><span class="sxs-lookup"><span data-stu-id="ae2b3-114">Job to track test failover Cleanup of an Azure Site Recovery recoveryPlan.</span></span>

## <span data-ttu-id="ae2b3-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ae2b3-115">PARAMETERS</span></span>

### <span data-ttu-id="ae2b3-116">-Megjegyzés</span><span class="sxs-lookup"><span data-stu-id="ae2b3-116">-Comment</span></span>
<span data-ttu-id="ae2b3-117">Felhasználói Megjegyzés a feladatátvétel teszteléséhez.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-117">User Comment for Test Failover.</span></span>

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

### <span data-ttu-id="ae2b3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae2b3-118">-DefaultProfile</span></span>
<span data-ttu-id="ae2b3-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae2b3-120">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ae2b3-120">-RecoveryPlan</span></span>
<span data-ttu-id="ae2b3-121">Helyreállítási terv a feladatátvételi karbantartás ellenőrzésének végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-121">Recovery Plan to perform the test failover cleanup on.</span></span>

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

### <span data-ttu-id="ae2b3-122">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ae2b3-122">-ReplicationProtectedItem</span></span>
<span data-ttu-id="ae2b3-123">A többszörözéssel védett elem a feladatátvételi karbantartás ellenőrzésének elvégzéséhez.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-123">Replication Protected Item to perform the test failover cleanup on.</span></span>

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

### <span data-ttu-id="ae2b3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae2b3-124">-ResourceId</span></span>
<span data-ttu-id="ae2b3-125">A cleaningup-teszt feladatátvételéhez használt replikációs védelemmel ellátott elem/helyreállítási terv erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-125">Resource Id of replication protected item / recovery plan for cleaningup test failover.</span></span>

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

### <span data-ttu-id="ae2b3-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ae2b3-126">-Confirm</span></span>
<span data-ttu-id="ae2b3-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae2b3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae2b3-128">-WhatIf</span></span>
<span data-ttu-id="ae2b3-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae2b3-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae2b3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae2b3-131">CommonParameters</span></span>
<span data-ttu-id="ae2b3-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ae2b3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae2b3-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae2b3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae2b3-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae2b3-134">INPUTS</span></span>

### <span data-ttu-id="ae2b3-135">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ae2b3-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="ae2b3-136">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ae2b3-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="ae2b3-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae2b3-137">OUTPUTS</span></span>

### <span data-ttu-id="ae2b3-138">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ae2b3-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ae2b3-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ae2b3-139">NOTES</span></span>

## <span data-ttu-id="ae2b3-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae2b3-140">RELATED LINKS</span></span>
