---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: BE2D05F5-70CE-4EAA-9363-6CA89A312DDB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectableItem.md
ms.openlocfilehash: 0b2fe8f500e17bc21407870a712ad4b9f00fd544
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672400"
---
# <span data-ttu-id="f223d-101">Get-AzureRmSiteRecoveryProtectableItem</span><span class="sxs-lookup"><span data-stu-id="f223d-101">Get-AzureRmSiteRecoveryProtectableItem</span></span>

## <span data-ttu-id="f223d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f223d-102">SYNOPSIS</span></span>
<span data-ttu-id="f223d-103">A védelemmel ellátott elemek beolvasása egy védelmi tárolóban</span><span class="sxs-lookup"><span data-stu-id="f223d-103">Get the protectable items in a Protection Container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f223d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f223d-104">SYNTAX</span></span>

### <span data-ttu-id="f223d-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f223d-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f223d-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="f223d-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f223d-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="f223d-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f223d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f223d-108">DESCRIPTION</span></span>
<span data-ttu-id="f223d-109">A **Get-AzureRmSiteRecoveryProtectableItem** parancsmag az Azure webhely-helyreállítási védelmi tárolóban található védelemmel ellátott elemeket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f223d-109">The **Get-AzureRmSiteRecoveryProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="f223d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f223d-110">EXAMPLES</span></span>

## <span data-ttu-id="f223d-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f223d-111">PARAMETERS</span></span>

### <span data-ttu-id="f223d-112">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="f223d-112">-FriendlyName</span></span>
<span data-ttu-id="f223d-113">Megadja az Azure webhely-helyreállítási elem rövid nevét.</span><span class="sxs-lookup"><span data-stu-id="f223d-113">Specifies the friendly name of the Azure Site Recovery protectable item.</span></span>

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

### <span data-ttu-id="f223d-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f223d-114">-Name</span></span>
<span data-ttu-id="f223d-115">Az Azure webhely-helyreállítási védelemmel ellátott elem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f223d-115">Specifies the name of the Azure Site Recovery protectable item.</span></span>

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

### <span data-ttu-id="f223d-116">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="f223d-116">-ProtectionContainer</span></span>
<span data-ttu-id="f223d-117">Az Azure site Recovery Protection Container objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f223d-117">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f223d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f223d-118">-DefaultProfile</span></span>
<span data-ttu-id="f223d-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f223d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f223d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f223d-120">CommonParameters</span></span>
<span data-ttu-id="f223d-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f223d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f223d-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f223d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f223d-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f223d-123">INPUTS</span></span>

### <span data-ttu-id="f223d-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="f223d-124">ASRProtectionContainer</span></span>
<span data-ttu-id="f223d-125">A ' ProtectionContainer ' paraméter az "ASRProtectionContainer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="f223d-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="f223d-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f223d-126">OUTPUTS</span></span>

### <span data-ttu-id="f223d-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. SiteRecovery. ASRProtectableItem, Microsoft. Azure. commands. SiteRecovery, Version = 2.0.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f223d-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRProtectableItem, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f223d-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f223d-128">NOTES</span></span>

## <span data-ttu-id="f223d-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f223d-129">RELATED LINKS</span></span>

[<span data-ttu-id="f223d-130">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f223d-130">Get-AzureRmSiteRecoveryProtectionEntity</span></span>](./Get-AzureRmSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="f223d-131">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f223d-131">Set-AzureRmSiteRecoveryProtectionEntity</span></span>](./Set-AzureRmSiteRecoveryProtectionEntity.md)
