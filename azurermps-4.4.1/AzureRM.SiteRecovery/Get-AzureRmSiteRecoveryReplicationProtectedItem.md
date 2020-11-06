---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 99196F44-F1DB-4219-91C0-3056624ADE5B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 0e94a46b8d6433ddd96530dc011234050398bf37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503179"
---
# <span data-ttu-id="9a68f-101">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9a68f-101">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="9a68f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9a68f-102">SYNOPSIS</span></span>
<span data-ttu-id="9a68f-103">Az Azure webhely-helyreállítással védett elemek tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9a68f-103">Gets the properties of Azure Site Recovery Protected Items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a68f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9a68f-104">SYNTAX</span></span>

### <span data-ttu-id="9a68f-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9a68f-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a68f-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="9a68f-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a68f-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="9a68f-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a68f-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="9a68f-108">ByProtectableItemObject</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a68f-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="9a68f-109">DESCRIPTION</span></span>
<span data-ttu-id="9a68f-110">A **Get-AzureRmSiteRecoveryReplicationProtectedItem** parancsmag az Azure webhely-helyreállítással védett elemek tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9a68f-110">The **Get-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet gets the properties of Azure Site Recovery Protected Items.</span></span>

## <span data-ttu-id="9a68f-111">Példák</span><span class="sxs-lookup"><span data-stu-id="9a68f-111">EXAMPLES</span></span>

## <span data-ttu-id="9a68f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9a68f-112">PARAMETERS</span></span>

### <span data-ttu-id="9a68f-113">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="9a68f-113">-FriendlyName</span></span>
<span data-ttu-id="9a68f-114">Annak a replikációs védelemmel ellátott elemnek a felhasználóbarát nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="9a68f-114">Specifies the friendly name of the Replication Protected Item that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9a68f-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9a68f-115">-Name</span></span>
<span data-ttu-id="9a68f-116">Annak a replikációs védelemmel ellátott elemnek a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="9a68f-116">Specifies the name of the Replication Protected Item that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9a68f-117">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="9a68f-117">-ProtectableItem</span></span>
<span data-ttu-id="9a68f-118">A replikációs védelemmel ellátott elemnek megfelelő védelemmel ellátott elemet adja meg.</span><span class="sxs-lookup"><span data-stu-id="9a68f-118">Specifies the Protectable Item corresponding to the Replication Protected Item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectableItem
Parameter Sets: ByProtectableItemObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a68f-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="9a68f-119">-ProtectionContainer</span></span>
<span data-ttu-id="9a68f-120">Az Azure site Recovery Protection Container objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9a68f-120">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObject, ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a68f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a68f-121">-DefaultProfile</span></span>
<span data-ttu-id="9a68f-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9a68f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a68f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a68f-123">CommonParameters</span></span>
<span data-ttu-id="9a68f-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9a68f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a68f-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a68f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a68f-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a68f-126">INPUTS</span></span>

### <span data-ttu-id="9a68f-127">ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="9a68f-127">ASRProtectableItem</span></span>
<span data-ttu-id="9a68f-128">A ' ProtectableItem ' paraméter az "ASRProtectableItem" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="9a68f-128">Parameter 'ProtectableItem' accepts value of type 'ASRProtectableItem' from the pipeline</span></span>

### <span data-ttu-id="9a68f-129">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="9a68f-129">ASRProtectionContainer</span></span>
<span data-ttu-id="9a68f-130">A ' ProtectionContainer ' paraméter az "ASRProtectionContainer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="9a68f-130">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="9a68f-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a68f-131">OUTPUTS</span></span>

### <span data-ttu-id="9a68f-132">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. SiteRecovery. ASRReplicationProtectedItem, Microsoft. Azure. commands. SiteRecovery, Version = 2.0.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9a68f-132">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9a68f-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9a68f-133">NOTES</span></span>

## <span data-ttu-id="9a68f-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a68f-134">RELATED LINKS</span></span>

[<span data-ttu-id="9a68f-135">Új – AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9a68f-135">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="9a68f-136">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9a68f-136">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="9a68f-137">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9a68f-137">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
