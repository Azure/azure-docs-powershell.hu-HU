---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrswitchprocessserverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
ms.openlocfilehash: d5f65479fb52eb52b91b82d7af2318576825eada
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846961"
---
# <span data-ttu-id="ed531-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="ed531-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span></span>

## <span data-ttu-id="ed531-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ed531-102">SYNOPSIS</span></span>
<span data-ttu-id="ed531-103">Átválthatja a replikációt egyik folyamat kiszolgálóról a másikra a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="ed531-103">Switch replication from one Process server to another for load balancing.</span></span>

## <span data-ttu-id="ed531-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ed531-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric <ASRFabric> -SourceProcessServer <ASRProcessServer>
 -TargetProcessServer <ASRProcessServer> [-ReplicationProtectedItem <ASRReplicationProtectedItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed531-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ed531-105">DESCRIPTION</span></span>
<span data-ttu-id="ed531-106">A **Start-AzRecoveryServicesAsrSwitchProcessServerJob** átváltja a megadott virtuális gépek vagy meghatározott feldolgozási folyamat replikációs adatforgalmát a megadott cél-kiszolgálóra.</span><span class="sxs-lookup"><span data-stu-id="ed531-106">The **Start-AzRecoveryServicesAsrSwitchProcessServerJob** switches replication data movement for the specified virtual machines or a specified Process server to the specified target Process server.</span></span> <span data-ttu-id="ed531-107">A folyamat-kiszolgálók közötti terheléselosztáshoz és a replikáció átkapcsolásához használható.</span><span class="sxs-lookup"><span data-stu-id="ed531-107">Used for load balancing or switching replication between Process servers.</span></span>

## <span data-ttu-id="ed531-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ed531-108">EXAMPLES</span></span>

### <span data-ttu-id="ed531-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ed531-109">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer
```

<span data-ttu-id="ed531-110">Feladat: a váltás folyamatának kiszolgálója az összes replikációs védelemmel ellátott elemről a forrásról a cél folyamat kiszolgálójára.</span><span class="sxs-lookup"><span data-stu-id="ed531-110">Job to track switching process server for all replication protected item from source to target process server.</span></span>

### <span data-ttu-id="ed531-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="ed531-111">Example 2</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer -ReplicatedItem $rpList
```

<span data-ttu-id="ed531-112">Feladat: a váltás a kiszolgálóról a forrásról a cél folyamat kiszolgálójára a átadott replikációs szolgáltatással védett elem nyomon követése</span><span class="sxs-lookup"><span data-stu-id="ed531-112">Job to track switching process server for passed replication protected item from source to target process server.</span></span>

## <span data-ttu-id="ed531-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ed531-113">PARAMETERS</span></span>

### <span data-ttu-id="ed531-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed531-114">-DefaultProfile</span></span>
<span data-ttu-id="ed531-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ed531-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed531-116">-Szövet</span><span class="sxs-lookup"><span data-stu-id="ed531-116">-Fabric</span></span>
<span data-ttu-id="ed531-117">A konfigurációs kiszolgálónak megfelelő webhely-helyreállítási anyag.</span><span class="sxs-lookup"><span data-stu-id="ed531-117">Site recovery fabric corresponding to the Configuration Server.</span></span>

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

### <span data-ttu-id="ed531-118">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ed531-118">-ReplicationProtectedItem</span></span>
<span data-ttu-id="ed531-119">Annak a replikációs védelemmel ellátott elemnek a listája, amelynek a folyamata kiszolgálón át kell váltania.</span><span class="sxs-lookup"><span data-stu-id="ed531-119">List of replication protected item whose process server to be switched.</span></span>

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

### <span data-ttu-id="ed531-120">-SourceProcessServer</span><span class="sxs-lookup"><span data-stu-id="ed531-120">-SourceProcessServer</span></span>
<span data-ttu-id="ed531-121">A folyamat kiszolgálója a replikáció kikapcsolásához.</span><span class="sxs-lookup"><span data-stu-id="ed531-121">The Process server to switch replication out from.</span></span>

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

### <span data-ttu-id="ed531-122">-TargetProcessServer</span><span class="sxs-lookup"><span data-stu-id="ed531-122">-TargetProcessServer</span></span>
<span data-ttu-id="ed531-123">A folyamat kiszolgálója, amellyel átválthat a replikációra.</span><span class="sxs-lookup"><span data-stu-id="ed531-123">The Process server to switch replication to.</span></span>

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

### <span data-ttu-id="ed531-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ed531-124">-Confirm</span></span>
<span data-ttu-id="ed531-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ed531-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed531-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed531-126">-WhatIf</span></span>
<span data-ttu-id="ed531-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ed531-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed531-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ed531-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed531-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed531-129">CommonParameters</span></span>
<span data-ttu-id="ed531-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ed531-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed531-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ed531-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed531-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed531-132">INPUTS</span></span>

### <span data-ttu-id="ed531-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="ed531-133">None</span></span>

## <span data-ttu-id="ed531-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed531-134">OUTPUTS</span></span>

### <span data-ttu-id="ed531-135">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ed531-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ed531-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ed531-136">NOTES</span></span>

## <span data-ttu-id="ed531-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed531-137">RELATED LINKS</span></span>
