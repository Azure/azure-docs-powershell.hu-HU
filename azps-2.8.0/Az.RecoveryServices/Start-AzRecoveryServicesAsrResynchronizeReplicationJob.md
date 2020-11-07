---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 48a17c0b2bd8c1d62de1b3ebd5eccc5171d65837
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839018"
---
# <span data-ttu-id="1ce36-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="1ce36-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="1ce36-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1ce36-102">SYNOPSIS</span></span>
<span data-ttu-id="1ce36-103">Elindítja a replikációs újraszinkronizálást.</span><span class="sxs-lookup"><span data-stu-id="1ce36-103">Starts replication resynchronization.</span></span>

## <span data-ttu-id="1ce36-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1ce36-104">SYNTAX</span></span>

### <span data-ttu-id="1ce36-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1ce36-105">Default (Default)</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ce36-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1ce36-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ce36-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1ce36-107">DESCRIPTION</span></span>
<span data-ttu-id="1ce36-108">A **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** parancsmag a megadott védett elem replikációjának újraszinkronizálását indítja el, ha a védett állapot újraszinkronizálása kötelező.</span><span class="sxs-lookup"><span data-stu-id="1ce36-108">The **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="1ce36-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1ce36-109">EXAMPLES</span></span>

### <span data-ttu-id="1ce36-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1ce36-110">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="1ce36-111">Elindítja a feladatot, hogy újraszinkronizálja a replikálást az átadott replikációs szolgáltatással védett elemeken.</span><span class="sxs-lookup"><span data-stu-id="1ce36-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="1ce36-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1ce36-112">PARAMETERS</span></span>

### <span data-ttu-id="1ce36-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ce36-113">-DefaultProfile</span></span>
<span data-ttu-id="1ce36-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1ce36-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ce36-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1ce36-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="1ce36-116">Az ASR-replikációval védett elem a replikáció újraszinkronizálásához.</span><span class="sxs-lookup"><span data-stu-id="1ce36-116">ASR replication protected item to resynchronize replication for.</span></span>

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

### <span data-ttu-id="1ce36-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ce36-117">-ResourceId</span></span>
<span data-ttu-id="1ce36-118">Az újraszinkronizáláshoz a replikációs védelemmel ellátott elem erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1ce36-118">Resource Id of replication protected item to resynchronize.</span></span>

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

### <span data-ttu-id="1ce36-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1ce36-119">-Confirm</span></span>
<span data-ttu-id="1ce36-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1ce36-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ce36-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ce36-121">-WhatIf</span></span>
<span data-ttu-id="1ce36-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1ce36-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ce36-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1ce36-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ce36-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ce36-124">CommonParameters</span></span>
<span data-ttu-id="1ce36-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1ce36-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ce36-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ce36-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ce36-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ce36-127">INPUTS</span></span>

### <span data-ttu-id="1ce36-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1ce36-128">System.String</span></span>

### <span data-ttu-id="1ce36-129">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1ce36-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="1ce36-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ce36-130">OUTPUTS</span></span>

### <span data-ttu-id="1ce36-131">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1ce36-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1ce36-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1ce36-132">NOTES</span></span>

## <span data-ttu-id="1ce36-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ce36-133">RELATED LINKS</span></span>
