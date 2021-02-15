---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrswitchprocessserverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
ms.openlocfilehash: d5f65479fb52eb52b91b82d7af2318576825eada
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160066"
---
# <span data-ttu-id="a03a4-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="a03a4-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span></span>

## <span data-ttu-id="a03a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a03a4-102">SYNOPSIS</span></span>
<span data-ttu-id="a03a4-103">A terheléselosztáshoz váltson replikációt egyik folyamatkiszolgálóról a másikra.</span><span class="sxs-lookup"><span data-stu-id="a03a4-103">Switch replication from one Process server to another for load balancing.</span></span>

## <span data-ttu-id="a03a4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a03a4-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric <ASRFabric> -SourceProcessServer <ASRProcessServer>
 -TargetProcessServer <ASRProcessServer> [-ReplicationProtectedItem <ASRReplicationProtectedItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a03a4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a03a4-105">DESCRIPTION</span></span>
<span data-ttu-id="a03a4-106">A **Start-AzRecoveryServicesAsrSwitchProcessServerServerServices a** megadott virtuális gépek vagy meghatározott folyamatkiszolgálók replikációs adatmozgását a megadott célfolyamat-kiszolgálóra kapcsolja.</span><span class="sxs-lookup"><span data-stu-id="a03a4-106">The **Start-AzRecoveryServicesAsrSwitchProcessServerJob** switches replication data movement for the specified virtual machines or a specified Process server to the specified target Process server.</span></span> <span data-ttu-id="a03a4-107">Terheléselosztáshoz vagy folyamatkiszolgálók közötti replikációs váltáshoz használható.</span><span class="sxs-lookup"><span data-stu-id="a03a4-107">Used for load balancing or switching replication between Process servers.</span></span>

## <span data-ttu-id="a03a4-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a03a4-108">EXAMPLES</span></span>

### <span data-ttu-id="a03a4-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="a03a4-109">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer
```

<span data-ttu-id="a03a4-110">A feladat, amely nyomon követi a váltási folyamatkiszolgálót az összes replikációval védett elemhez a forrástól a célfolyamat-kiszolgálóig.</span><span class="sxs-lookup"><span data-stu-id="a03a4-110">Job to track switching process server for all replication protected item from source to target process server.</span></span>

### <span data-ttu-id="a03a4-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="a03a4-111">Example 2</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer -ReplicatedItem $rpList
```

<span data-ttu-id="a03a4-112">A kiszolgálóváltás folyamatkiszolgálójának nyomon követése a átadott replikációval védett elem forrásról a célfolyamat-kiszolgálóra.</span><span class="sxs-lookup"><span data-stu-id="a03a4-112">Job to track switching process server for passed replication protected item from source to target process server.</span></span>

## <span data-ttu-id="a03a4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a03a4-113">PARAMETERS</span></span>

### <span data-ttu-id="a03a4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a03a4-114">-DefaultProfile</span></span>
<span data-ttu-id="a03a4-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a03a4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a03a4-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="a03a4-116">-Fabric</span></span>
<span data-ttu-id="a03a4-117">A Configuration Servernek megfelelő webhely-helyreállítási anyag.</span><span class="sxs-lookup"><span data-stu-id="a03a4-117">Site recovery fabric corresponding to the Configuration Server.</span></span>

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

### <span data-ttu-id="a03a4-118">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a03a4-118">-ReplicationProtectedItem</span></span>
<span data-ttu-id="a03a4-119">A replikációval védett elem listája, amelynek a folyamatkiszolgálóját át kell váltani.</span><span class="sxs-lookup"><span data-stu-id="a03a4-119">List of replication protected item whose process server to be switched.</span></span>

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

### <span data-ttu-id="a03a4-120">-SourceProcessServer</span><span class="sxs-lookup"><span data-stu-id="a03a4-120">-SourceProcessServer</span></span>
<span data-ttu-id="a03a4-121">A replikációs kiszolgáló, amelyről a replikációt ki kell kapcsolni.</span><span class="sxs-lookup"><span data-stu-id="a03a4-121">The Process server to switch replication out from.</span></span>

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

### <span data-ttu-id="a03a4-122">-TargetProcessServer</span><span class="sxs-lookup"><span data-stu-id="a03a4-122">-TargetProcessServer</span></span>
<span data-ttu-id="a03a4-123">Az a folyamatkiszolgáló, amelyre a replikációt át kell váltani.</span><span class="sxs-lookup"><span data-stu-id="a03a4-123">The Process server to switch replication to.</span></span>

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

### <span data-ttu-id="a03a4-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a03a4-124">-Confirm</span></span>
<span data-ttu-id="a03a4-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a03a4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a03a4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a03a4-126">-WhatIf</span></span>
<span data-ttu-id="a03a4-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a03a4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a03a4-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a03a4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a03a4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a03a4-129">CommonParameters</span></span>
<span data-ttu-id="a03a4-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a03a4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a03a4-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a03a4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a03a4-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a03a4-132">INPUTS</span></span>

### <span data-ttu-id="a03a4-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="a03a4-133">None</span></span>

## <span data-ttu-id="a03a4-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a03a4-134">OUTPUTS</span></span>

### <span data-ttu-id="a03a4-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="a03a4-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a03a4-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a03a4-136">NOTES</span></span>

## <span data-ttu-id="a03a4-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a03a4-137">RELATED LINKS</span></span>
