---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: fbd2f518d3bdcf64599e32b55cdb9f416c29be21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504788"
---
# <span data-ttu-id="e36f6-101">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e36f6-101">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="e36f6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e36f6-102">SYNOPSIS</span></span>
<span data-ttu-id="e36f6-103">Beolvassa az Azure webhely-helyreállítási replikációval védett elemek tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="e36f6-103">Gets the properties of an Azure Site Recovery Replication Protected Items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e36f6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e36f6-104">SYNTAX</span></span>

### <span data-ttu-id="e36f6-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e36f6-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="e36f6-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="e36f6-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

### <span data-ttu-id="e36f6-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="e36f6-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

### <span data-ttu-id="e36f6-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="e36f6-108">ByProtectableItemObject</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [<CommonParameters>]
```

## <span data-ttu-id="e36f6-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="e36f6-109">DESCRIPTION</span></span>
<span data-ttu-id="e36f6-110">A **Get-AzureRmRecoveryServicesAsrReplicationProtectedItem** parancsmag a megadott ASR-védelmi tárolóból az összes vagy a megadott ASR-replikációs védett elem tulajdonságait kapja.</span><span class="sxs-lookup"><span data-stu-id="e36f6-110">The **Get-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet gets the properties of all or the specified ASR replication protected item from the specified ASR protection container.</span></span>

## <span data-ttu-id="e36f6-111">Példák</span><span class="sxs-lookup"><span data-stu-id="e36f6-111">EXAMPLES</span></span>

### <span data-ttu-id="e36f6-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e36f6-112">Example 1</span></span>
```
PS C:\> $ReplicationProtectedItems = Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer $PrimaryContainer
```

<span data-ttu-id="e36f6-113">A megadott ASR-védelmi tárolóban lévő összes replikációs védelemmel ellátott elem felsorolása.</span><span class="sxs-lookup"><span data-stu-id="e36f6-113">Lists all replication protected items in the specified ASR protection container.</span></span>

## <span data-ttu-id="e36f6-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e36f6-114">PARAMETERS</span></span>

### <span data-ttu-id="e36f6-115">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="e36f6-115">-FriendlyName</span></span>
<span data-ttu-id="e36f6-116">A beolvasott replikációs védett elem rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e36f6-116">Specifies the friendly name of the replication protected item to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e36f6-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e36f6-117">-Name</span></span>
<span data-ttu-id="e36f6-118">A beolvasott replikációs védett elem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e36f6-118">Specifies the name of the replication protected item to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e36f6-119">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="e36f6-119">-ProtectableItem</span></span>
<span data-ttu-id="e36f6-120">Egy ASR-védelemmel ellátott elem objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="e36f6-120">Specifies an ASR protectable item object.</span></span> <span data-ttu-id="e36f6-121">A parancsmag a megadott ASR-védelemmel ellátott, a megadott ASR-védelemmel ellátott elemnek megfelelő, ha az elem védett.</span><span class="sxs-lookup"><span data-stu-id="e36f6-121">The cmdlet gets the ASR replication protected item corresponding to the specified ASR protectable item if the item is protected.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: ByProtectableItemObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e36f6-122">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="e36f6-122">-ProtectionContainer</span></span>
<span data-ttu-id="e36f6-123">A replikációs védelemmel ellátott védett elemnek megfelelő ASR-védelmi tároló objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="e36f6-123">Specifies the ASR protection container object of the ASR protection container corresponding to the replication protected item.</span></span> 

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject, ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e36f6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e36f6-124">CommonParameters</span></span>
<span data-ttu-id="e36f6-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e36f6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e36f6-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e36f6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e36f6-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e36f6-127">INPUTS</span></span>

### <span data-ttu-id="e36f6-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="e36f6-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>
<span data-ttu-id="e36f6-129">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="e36f6-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="e36f6-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e36f6-130">OUTPUTS</span></span>

### <span data-ttu-id="e36f6-131">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 4.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e36f6-131">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e36f6-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e36f6-132">NOTES</span></span>

## <span data-ttu-id="e36f6-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e36f6-133">RELATED LINKS</span></span>

[<span data-ttu-id="e36f6-134">Új – AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e36f6-134">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="e36f6-135">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e36f6-135">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="e36f6-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e36f6-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
