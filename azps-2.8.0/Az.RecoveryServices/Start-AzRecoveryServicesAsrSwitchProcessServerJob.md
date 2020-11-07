---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrswitchprocessserverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
ms.openlocfilehash: 4f926b88214a60cc05b6eb9666e10fa8ed7bf3ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839017"
---
# <span data-ttu-id="542b1-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="542b1-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span></span>

## <span data-ttu-id="542b1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="542b1-102">SYNOPSIS</span></span>
<span data-ttu-id="542b1-103">Átválthatja a replikációt egyik folyamat kiszolgálóról a másikra a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="542b1-103">Switch replication from one Process server to another for load balancing.</span></span>

## <span data-ttu-id="542b1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="542b1-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric <ASRFabric> -SourceProcessServer <ASRProcessServer>
 -TargetProcessServer <ASRProcessServer> [-ReplicationProtectedItem <ASRReplicationProtectedItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="542b1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="542b1-105">DESCRIPTION</span></span>
<span data-ttu-id="542b1-106">A **Start-AzRecoveryServicesAsrSwitchProcessServerJob** átváltja a megadott virtuális gépek vagy meghatározott feldolgozási folyamat replikációs adatforgalmát a megadott cél-kiszolgálóra.</span><span class="sxs-lookup"><span data-stu-id="542b1-106">The **Start-AzRecoveryServicesAsrSwitchProcessServerJob** switches replication data movement for the specified virtual machines or a specified Process server to the specified target Process server.</span></span> <span data-ttu-id="542b1-107">A folyamat-kiszolgálók közötti terheléselosztáshoz és a replikáció átkapcsolásához használható.</span><span class="sxs-lookup"><span data-stu-id="542b1-107">Used for load balancing or switching replication between Process servers.</span></span>

## <span data-ttu-id="542b1-108">Példák</span><span class="sxs-lookup"><span data-stu-id="542b1-108">EXAMPLES</span></span>

### <span data-ttu-id="542b1-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="542b1-109">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer
```

<span data-ttu-id="542b1-110">Feladat: a váltás folyamatának kiszolgálója az összes replikációs védelemmel ellátott elemről a forrásról a cél folyamat kiszolgálójára.</span><span class="sxs-lookup"><span data-stu-id="542b1-110">Job to track switching process server for all replication protected item from source to target process server.</span></span>

### <span data-ttu-id="542b1-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="542b1-111">Example 2</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer -ReplicatedItem $rpList
```

<span data-ttu-id="542b1-112">Feladat: a váltás a kiszolgálóról a forrásról a cél folyamat kiszolgálójára a átadott replikációs szolgáltatással védett elem nyomon követése</span><span class="sxs-lookup"><span data-stu-id="542b1-112">Job to track switching process server for passed replication protected item from source to target process server.</span></span>

## <span data-ttu-id="542b1-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="542b1-113">PARAMETERS</span></span>

### <span data-ttu-id="542b1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="542b1-114">-DefaultProfile</span></span>
<span data-ttu-id="542b1-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="542b1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="542b1-116">-Szövet</span><span class="sxs-lookup"><span data-stu-id="542b1-116">-Fabric</span></span>
<span data-ttu-id="542b1-117">A konfigurációs kiszolgálónak megfelelő webhely-helyreállítási anyag.</span><span class="sxs-lookup"><span data-stu-id="542b1-117">Site recovery fabric corresponding to the Configuration Server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: ConfigServer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="542b1-118">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="542b1-118">-ReplicationProtectedItem</span></span>
<span data-ttu-id="542b1-119">Annak a replikációs védelemmel ellátott elemnek a listája, amelynek a folyamata kiszolgálón át kell váltania.</span><span class="sxs-lookup"><span data-stu-id="542b1-119">List of replication protected item whose process server to be switched.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: (All)
Aliases: ReplicatedItem

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="542b1-120">-SourceProcessServer</span><span class="sxs-lookup"><span data-stu-id="542b1-120">-SourceProcessServer</span></span>
<span data-ttu-id="542b1-121">A folyamat kiszolgálója a replikáció kikapcsolásához.</span><span class="sxs-lookup"><span data-stu-id="542b1-121">The Process server to switch replication out from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="542b1-122">-TargetProcessServer</span><span class="sxs-lookup"><span data-stu-id="542b1-122">-TargetProcessServer</span></span>
<span data-ttu-id="542b1-123">A folyamat kiszolgálója, amellyel átválthat a replikációra.</span><span class="sxs-lookup"><span data-stu-id="542b1-123">The Process server to switch replication to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="542b1-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="542b1-124">-Confirm</span></span>
<span data-ttu-id="542b1-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="542b1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="542b1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="542b1-126">-WhatIf</span></span>
<span data-ttu-id="542b1-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="542b1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="542b1-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="542b1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="542b1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="542b1-129">CommonParameters</span></span>
<span data-ttu-id="542b1-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="542b1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="542b1-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="542b1-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="542b1-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="542b1-132">INPUTS</span></span>

### <span data-ttu-id="542b1-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="542b1-133">None</span></span>

## <span data-ttu-id="542b1-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="542b1-134">OUTPUTS</span></span>

### <span data-ttu-id="542b1-135">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="542b1-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="542b1-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="542b1-136">NOTES</span></span>

## <span data-ttu-id="542b1-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="542b1-137">RELATED LINKS</span></span>
