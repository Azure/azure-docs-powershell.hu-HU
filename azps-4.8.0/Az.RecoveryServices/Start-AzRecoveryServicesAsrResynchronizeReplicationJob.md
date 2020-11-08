---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 0429976c64ed6e7989208c28fea1ee0a008436c8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182183"
---
# <span data-ttu-id="0ea61-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="0ea61-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="0ea61-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0ea61-102">SYNOPSIS</span></span>
<span data-ttu-id="0ea61-103">Elindítja a replikációs újraszinkronizálást.</span><span class="sxs-lookup"><span data-stu-id="0ea61-103">Starts replication resynchronization.</span></span>

## <span data-ttu-id="0ea61-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0ea61-104">SYNTAX</span></span>

### <span data-ttu-id="0ea61-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0ea61-105">Default (Default)</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ea61-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0ea61-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ea61-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0ea61-107">DESCRIPTION</span></span>
<span data-ttu-id="0ea61-108">A **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** parancsmag a megadott védett elem replikációjának újraszinkronizálását indítja el, ha a védett állapot újraszinkronizálása kötelező.</span><span class="sxs-lookup"><span data-stu-id="0ea61-108">The **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="0ea61-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0ea61-109">EXAMPLES</span></span>

### <span data-ttu-id="0ea61-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0ea61-110">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="0ea61-111">Elindítja a feladatot, hogy újraszinkronizálja a replikálást az átadott replikációs szolgáltatással védett elemeken.</span><span class="sxs-lookup"><span data-stu-id="0ea61-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="0ea61-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0ea61-112">PARAMETERS</span></span>

### <span data-ttu-id="0ea61-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ea61-113">-DefaultProfile</span></span>
<span data-ttu-id="0ea61-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0ea61-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ea61-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0ea61-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="0ea61-116">Az ASR-replikációval védett elem a replikáció újraszinkronizálásához.</span><span class="sxs-lookup"><span data-stu-id="0ea61-116">ASR replication protected item to resynchronize replication for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ea61-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ea61-117">-ResourceId</span></span>
<span data-ttu-id="0ea61-118">Az újraszinkronizáláshoz a replikációs védelemmel ellátott elem erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0ea61-118">Resource Id of replication protected item to resynchronize.</span></span>

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

### <span data-ttu-id="0ea61-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0ea61-119">-Confirm</span></span>
<span data-ttu-id="0ea61-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0ea61-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ea61-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ea61-121">-WhatIf</span></span>
<span data-ttu-id="0ea61-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0ea61-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ea61-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0ea61-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ea61-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ea61-124">CommonParameters</span></span>
<span data-ttu-id="0ea61-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0ea61-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ea61-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0ea61-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ea61-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ea61-127">INPUTS</span></span>

### <span data-ttu-id="0ea61-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0ea61-128">System.String</span></span>

### <span data-ttu-id="0ea61-129">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0ea61-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="0ea61-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ea61-130">OUTPUTS</span></span>

### <span data-ttu-id="0ea61-131">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0ea61-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0ea61-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0ea61-132">NOTES</span></span>

## <span data-ttu-id="0ea61-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ea61-133">RELATED LINKS</span></span>
