---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrswitchprocessserverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob.md
ms.openlocfilehash: be16ff2145a4442861fd985dfbb55da63f010e94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493034"
---
# <span data-ttu-id="32666-101">Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="32666-101">Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob</span></span>

## <span data-ttu-id="32666-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="32666-102">SYNOPSIS</span></span>
<span data-ttu-id="32666-103">Átválthatja a replikációt egyik folyamat kiszolgálóról a másikra a terheléselosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="32666-103">Switch replication from one Process server to another for load balancing.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32666-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="32666-104">SYNTAX</span></span>

```
Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob -Fabric <ASRFabric>
 -SourceProcessServer <ASRProcessServer> -TargetProcessServer <ASRProcessServer>
 [-ReplicationProtectedItem <ASRReplicationProtectedItem[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32666-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="32666-105">DESCRIPTION</span></span>
<span data-ttu-id="32666-106">A **Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob** átváltja a megadott virtuális gépek vagy meghatározott feldolgozási folyamat replikációs adatforgalmát a megadott cél-kiszolgálóra.</span><span class="sxs-lookup"><span data-stu-id="32666-106">The **Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob** switches replication data movement for the specified virtual machines or a specified Process server to the specified target Process server.</span></span> <span data-ttu-id="32666-107">A folyamat-kiszolgálók közötti terheléselosztáshoz és a replikáció átkapcsolásához használható.</span><span class="sxs-lookup"><span data-stu-id="32666-107">Used for load balancing or switching replication between Process servers.</span></span>

## <span data-ttu-id="32666-108">Példák</span><span class="sxs-lookup"><span data-stu-id="32666-108">EXAMPLES</span></span>

### <span data-ttu-id="32666-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="32666-109">Example 1</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer
```

<span data-ttu-id="32666-110">Feladat: a váltás folyamatának kiszolgálója az összes replikációs védelemmel ellátott elemről a forrásról a cél folyamat kiszolgálójára.</span><span class="sxs-lookup"><span data-stu-id="32666-110">Job to track switching process server for all replication protected item from source to target process server.</span></span>

### <span data-ttu-id="32666-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="32666-111">Example 2</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer -ReplicatedItem $rpList
```

<span data-ttu-id="32666-112">Feladat: a váltás a kiszolgálóról a forrásról a cél folyamat kiszolgálójára a átadott replikációs szolgáltatással védett elem nyomon követése</span><span class="sxs-lookup"><span data-stu-id="32666-112">Job to track switching process server for passed replication protected item from source to target process server.</span></span>

## <span data-ttu-id="32666-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="32666-113">PARAMETERS</span></span>

### <span data-ttu-id="32666-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="32666-114">-Confirm</span></span>
<span data-ttu-id="32666-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="32666-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32666-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32666-116">-DefaultProfile</span></span>
<span data-ttu-id="32666-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="32666-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32666-118">-Szövet</span><span class="sxs-lookup"><span data-stu-id="32666-118">-Fabric</span></span>
<span data-ttu-id="32666-119">A konfigurációs kiszolgálónak megfelelő webhely-helyreállítási anyag.</span><span class="sxs-lookup"><span data-stu-id="32666-119">Site recovery fabric corresponding to the Configuration Server.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: ConfigServer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32666-120">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="32666-120">-ReplicationProtectedItem</span></span>
<span data-ttu-id="32666-121">Annak a replikációs védelemmel ellátott elemnek a listája, amelynek a folyamata kiszolgálón át kell váltania.</span><span class="sxs-lookup"><span data-stu-id="32666-121">List of replication protected item whose process server to be switched.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: (All)
Aliases: ReplicatedItem

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32666-122">-SourceProcessServer</span><span class="sxs-lookup"><span data-stu-id="32666-122">-SourceProcessServer</span></span>
<span data-ttu-id="32666-123">A folyamat kiszolgálója a replikáció kikapcsolásához.</span><span class="sxs-lookup"><span data-stu-id="32666-123">The Process server to switch replication out from.</span></span>

```yaml
Type: ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32666-124">-TargetProcessServer</span><span class="sxs-lookup"><span data-stu-id="32666-124">-TargetProcessServer</span></span>
<span data-ttu-id="32666-125">A folyamat kiszolgálója, amellyel átválthat a replikációra.</span><span class="sxs-lookup"><span data-stu-id="32666-125">The Process server to switch replication to.</span></span>

```yaml
Type: ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32666-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32666-126">-WhatIf</span></span>
<span data-ttu-id="32666-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="32666-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32666-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="32666-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32666-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32666-129">CommonParameters</span></span>
<span data-ttu-id="32666-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="32666-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32666-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32666-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32666-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="32666-132">INPUTS</span></span>

### <span data-ttu-id="32666-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="32666-133">None</span></span>

## <span data-ttu-id="32666-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="32666-134">OUTPUTS</span></span>

### <span data-ttu-id="32666-135">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="32666-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="32666-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="32666-136">NOTES</span></span>

## <span data-ttu-id="32666-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="32666-137">RELATED LINKS</span></span>
