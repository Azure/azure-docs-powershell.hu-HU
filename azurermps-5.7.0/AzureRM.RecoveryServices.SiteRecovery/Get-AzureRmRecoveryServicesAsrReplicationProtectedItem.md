---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 90b615edefe860e084de0040a13c1ba5a1ff39ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494401"
---
# <span data-ttu-id="b303d-101">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b303d-101">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="b303d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b303d-102">SYNOPSIS</span></span>
<span data-ttu-id="b303d-103">Beolvassa az Azure webhely-helyreállítási replikációval védett elemek tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="b303d-103">Gets the properties of an Azure Site Recovery Replication Protected Items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b303d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b303d-104">SYNTAX</span></span>

### <span data-ttu-id="b303d-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b303d-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b303d-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="b303d-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b303d-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="b303d-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b303d-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="b303d-108">ByProtectableItemObject</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b303d-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="b303d-109">DESCRIPTION</span></span>
<span data-ttu-id="b303d-110">A **Get-AzureRmRecoveryServicesAsrReplicationProtectedItem** parancsmag a megadott ASR-védelmi tárolóból az összes vagy a megadott ASR-replikációs védett elem tulajdonságait kapja.</span><span class="sxs-lookup"><span data-stu-id="b303d-110">The **Get-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet gets the properties of all or the specified ASR replication protected item from the specified ASR protection container.</span></span>

## <span data-ttu-id="b303d-111">Példák</span><span class="sxs-lookup"><span data-stu-id="b303d-111">EXAMPLES</span></span>

### <span data-ttu-id="b303d-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b303d-112">Example 1</span></span>
```
PS C:\> $ReplicationProtectedItems = Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer $PrimaryContainer
```

<span data-ttu-id="b303d-113">A megadott ASR-védelmi tárolóban lévő összes replikációs védelemmel ellátott elem felsorolása.</span><span class="sxs-lookup"><span data-stu-id="b303d-113">Lists all replication protected items in the specified ASR protection container.</span></span>

## <span data-ttu-id="b303d-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b303d-114">PARAMETERS</span></span>

### <span data-ttu-id="b303d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b303d-115">-DefaultProfile</span></span>
<span data-ttu-id="b303d-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b303d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="b303d-117">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="b303d-117">-FriendlyName</span></span>
<span data-ttu-id="b303d-118">A beolvasott replikációs védett elem rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b303d-118">Specifies the friendly name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="b303d-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b303d-119">-Name</span></span>
<span data-ttu-id="b303d-120">A beolvasott replikációs védett elem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b303d-120">Specifies the name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="b303d-121">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="b303d-121">-ProtectableItem</span></span>
<span data-ttu-id="b303d-122">Egy ASR-védelemmel ellátott elem objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="b303d-122">Specifies an ASR protectable item object.</span></span> <span data-ttu-id="b303d-123">A parancsmag a megadott ASR-védelemmel ellátott, a megadott ASR-védelemmel ellátott elemnek megfelelő, ha az elem védett.</span><span class="sxs-lookup"><span data-stu-id="b303d-123">The cmdlet gets the ASR replication protected item corresponding to the specified ASR protectable item if the item is protected.</span></span>

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

### <span data-ttu-id="b303d-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b303d-124">-ProtectionContainer</span></span>
<span data-ttu-id="b303d-125">A replikációs védelemmel ellátott védett elemnek megfelelő ASR-védelmi tároló objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="b303d-125">Specifies the ASR protection container object of the ASR protection container corresponding to the replication protected item.</span></span> 

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

### <span data-ttu-id="b303d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b303d-126">CommonParameters</span></span>
<span data-ttu-id="b303d-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b303d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b303d-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b303d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b303d-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b303d-129">INPUTS</span></span>

### <span data-ttu-id="b303d-130">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b303d-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>
<span data-ttu-id="b303d-131">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="b303d-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="b303d-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b303d-132">OUTPUTS</span></span>

### <span data-ttu-id="b303d-133">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 4.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b303d-133">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b303d-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b303d-134">NOTES</span></span>

## <span data-ttu-id="b303d-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b303d-135">RELATED LINKS</span></span>

[<span data-ttu-id="b303d-136">Új – AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b303d-136">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="b303d-137">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b303d-137">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="b303d-138">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b303d-138">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
