---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 17836b900e56fdfd5d90211c9bceb79fce87c66e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680499"
---
# <span data-ttu-id="64efe-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="64efe-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="64efe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="64efe-102">SYNOPSIS</span></span>
<span data-ttu-id="64efe-103">Az Azure webhely-helyreállítási replikációval védett elem replikációjának leállítása/letiltása.</span><span class="sxs-lookup"><span data-stu-id="64efe-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64efe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="64efe-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64efe-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="64efe-105">DESCRIPTION</span></span>
<span data-ttu-id="64efe-106">A **Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem** parancsmag letiltja a megadott Azure-helyreállítási replikációval védett elem replikálását.</span><span class="sxs-lookup"><span data-stu-id="64efe-106">The **Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="64efe-107">A művelet hatására a replikáció leáll a védett elemen.</span><span class="sxs-lookup"><span data-stu-id="64efe-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="64efe-108">Példák</span><span class="sxs-lookup"><span data-stu-id="64efe-108">EXAMPLES</span></span>

### <span data-ttu-id="64efe-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="64efe-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="64efe-110">Elindítja a replikáció letiltása műveletet a megadott replikációs védett elemhez, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="64efe-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="64efe-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="64efe-111">PARAMETERS</span></span>

### <span data-ttu-id="64efe-112">-Force</span><span class="sxs-lookup"><span data-stu-id="64efe-112">-Force</span></span>
<span data-ttu-id="64efe-113">Kényszerítse a parancsot, hogy ne adjon meg további figyelmeztetést.</span><span class="sxs-lookup"><span data-stu-id="64efe-113">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64efe-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64efe-114">-InputObject</span></span>
<span data-ttu-id="64efe-115">A bemeneti objektum a parancsmag: az ASR-replikációs szolgáltatással védett elem objektum, amely megfelel a replikációt letiltó replikációs védelemmel ellátott elemnek.</span><span class="sxs-lookup"><span data-stu-id="64efe-115">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64efe-116">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="64efe-116">-WaitForCompletion</span></span>
<span data-ttu-id="64efe-117">Azt jelzi, hogy a parancsmagnak várnia kell, hogy a művelet csak a visszatérés előtt legyen végrehajtva.</span><span class="sxs-lookup"><span data-stu-id="64efe-117">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64efe-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="64efe-118">-Confirm</span></span>
<span data-ttu-id="64efe-119">Adja meg, hogy szükség van-e megerősítésre.</span><span class="sxs-lookup"><span data-stu-id="64efe-119">Specify if confirmation is required.</span></span> <span data-ttu-id="64efe-120">Adja meg a megerősítési paraméter értékét $false a megerősítés kihagyása érdekében.</span><span class="sxs-lookup"><span data-stu-id="64efe-120">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="64efe-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64efe-121">-WhatIf</span></span>
<span data-ttu-id="64efe-122">Annak megjelenítése, hogy mi történik, ha a parancsmagot ténylegesen végrehajtják a parancsmag végrehajtása nélkül.</span><span class="sxs-lookup"><span data-stu-id="64efe-122">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="64efe-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64efe-123">CommonParameters</span></span>
<span data-ttu-id="64efe-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="64efe-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64efe-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64efe-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64efe-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="64efe-126">INPUTS</span></span>

### <span data-ttu-id="64efe-127">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="64efe-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="64efe-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64efe-128">OUTPUTS</span></span>

### <span data-ttu-id="64efe-129">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="64efe-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="64efe-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="64efe-130">NOTES</span></span>

## <span data-ttu-id="64efe-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64efe-131">RELATED LINKS</span></span>

[<span data-ttu-id="64efe-132">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="64efe-132">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="64efe-133">Új – AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="64efe-133">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="64efe-134">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="64efe-134">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
