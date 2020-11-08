---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 3c89133b18f1425f65ab9430765f0a2a9a7cfafe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010901"
---
# <span data-ttu-id="7d7ae-101">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7d7ae-101">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="7d7ae-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7d7ae-102">SYNOPSIS</span></span>
<span data-ttu-id="7d7ae-103">Beolvassa az Azure webhely-helyreállítási replikációval védett elemek tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="7d7ae-103">Gets the properties of an Azure Site Recovery Replication Protected Items.</span></span>

## <span data-ttu-id="7d7ae-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7d7ae-104">SYNTAX</span></span>

### <span data-ttu-id="7d7ae-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7d7ae-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d7ae-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="7d7ae-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d7ae-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="7d7ae-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d7ae-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="7d7ae-108">ByProtectableItemObject</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d7ae-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="7d7ae-109">DESCRIPTION</span></span>
<span data-ttu-id="7d7ae-110">A **Get-AzRecoveryServicesAsrReplicationProtectedItem** parancsmag a megadott ASR-védelmi tárolóból az összes vagy a megadott ASR-replikációs védett elem tulajdonságait kapja.</span><span class="sxs-lookup"><span data-stu-id="7d7ae-110">The **Get-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet gets the properties of all or the specified ASR replication protected item from the specified ASR protection container.</span></span>

## <span data-ttu-id="7d7ae-111">Példák</span><span class="sxs-lookup"><span data-stu-id="7d7ae-111">EXAMPLES</span></span>

### <span data-ttu-id="7d7ae-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7d7ae-112">Example 1</span></span>
```
PS C:\> $ReplicationProtectedItems = Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer $PrimaryContainer
```

<span data-ttu-id="7d7ae-113">A megadott ASR-védelmi tárolóban lévő összes replikációs védelemmel ellátott elem felsorolása.</span><span class="sxs-lookup"><span data-stu-id="7d7ae-113">Lists all replication protected items in the specified ASR protection container.</span></span>

## <span data-ttu-id="7d7ae-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7d7ae-114">PARAMETERS</span></span>

### <span data-ttu-id="7d7ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d7ae-115">-DefaultProfile</span></span>
<span data-ttu-id="7d7ae-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7d7ae-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="7d7ae-117">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="7d7ae-117">-FriendlyName</span></span>
<span data-ttu-id="7d7ae-118">A beolvasott replikációs védett elem rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7d7ae-118">Specifies the friendly name of the replication protected item to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d7ae-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7d7ae-119">-Name</span></span>
<span data-ttu-id="7d7ae-120">A beolvasott replikációs védett elem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7d7ae-120">Specifies the name of the replication protected item to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d7ae-121">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="7d7ae-121">-ProtectableItem</span></span>
<span data-ttu-id="7d7ae-122">Egy ASR-védelemmel ellátott elem objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="7d7ae-122">Specifies an ASR protectable item object.</span></span> <span data-ttu-id="7d7ae-123">A parancsmag a megadott ASR-védelemmel ellátott, a megadott ASR-védelemmel ellátott elemnek megfelelő, ha az elem védett.</span><span class="sxs-lookup"><span data-stu-id="7d7ae-123">The cmdlet gets the ASR replication protected item corresponding to the specified ASR protectable item if the item is protected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem
Parameter Sets: ByProtectableItemObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d7ae-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7d7ae-124">-ProtectionContainer</span></span>
<span data-ttu-id="7d7ae-125">A replikációs védelemmel ellátott védett elemnek megfelelő ASR-védelmi tároló objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="7d7ae-125">Specifies the ASR protection container object of the ASR protection container corresponding to the replication protected item.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObject, ByObjectWithName, ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d7ae-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d7ae-126">CommonParameters</span></span>
<span data-ttu-id="7d7ae-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7d7ae-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d7ae-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7d7ae-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d7ae-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d7ae-129">INPUTS</span></span>

### <span data-ttu-id="7d7ae-130">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7d7ae-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

### <span data-ttu-id="7d7ae-131">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="7d7ae-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="7d7ae-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d7ae-132">OUTPUTS</span></span>

### <span data-ttu-id="7d7ae-133">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7d7ae-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="7d7ae-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7d7ae-134">NOTES</span></span>

## <span data-ttu-id="7d7ae-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7d7ae-135">RELATED LINKS</span></span>

[<span data-ttu-id="7d7ae-136">Új – AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7d7ae-136">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="7d7ae-137">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7d7ae-137">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="7d7ae-138">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7d7ae-138">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
