---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/set-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnProfile.md
ms.openlocfilehash: 033755c47965420d3983cc8b3a4d2731ab331152
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495467"
---
# <span data-ttu-id="93c8e-101">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="93c8e-101">Set-AzureRmCdnProfile</span></span>

## <span data-ttu-id="93c8e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="93c8e-102">SYNOPSIS</span></span>
<span data-ttu-id="93c8e-103">Egy CDN-profil frissítése</span><span class="sxs-lookup"><span data-stu-id="93c8e-103">Updates a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93c8e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="93c8e-104">SYNTAX</span></span>

```
Set-AzureRmCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="93c8e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="93c8e-105">DESCRIPTION</span></span>
<span data-ttu-id="93c8e-106">A **set-AzureRmCdnProfile** parancsmag egy Azure Content Delivery Network (CDN) profilt frissít.</span><span class="sxs-lookup"><span data-stu-id="93c8e-106">The **Set-AzureRmCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="93c8e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="93c8e-107">EXAMPLES</span></span>

## <span data-ttu-id="93c8e-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="93c8e-108">PARAMETERS</span></span>

### <span data-ttu-id="93c8e-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="93c8e-109">-CdnProfile</span></span>
<span data-ttu-id="93c8e-110">A parancsmag által frissített profilt adja meg.</span><span class="sxs-lookup"><span data-stu-id="93c8e-110">Specifies the profile that this cmdlet updates.</span></span>

```yaml
Type: PSProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93c8e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93c8e-111">-DefaultProfile</span></span>
<span data-ttu-id="93c8e-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="93c8e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93c8e-113">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="93c8e-113">-Confirm</span></span>
<span data-ttu-id="93c8e-114">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="93c8e-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93c8e-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93c8e-115">-WhatIf</span></span>
<span data-ttu-id="93c8e-116">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="93c8e-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93c8e-117">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="93c8e-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93c8e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93c8e-118">CommonParameters</span></span>
<span data-ttu-id="93c8e-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="93c8e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93c8e-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93c8e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93c8e-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="93c8e-121">INPUTS</span></span>

### <span data-ttu-id="93c8e-122">PSProfile</span><span class="sxs-lookup"><span data-stu-id="93c8e-122">PSProfile</span></span>
<span data-ttu-id="93c8e-123">A ' CdnProfile ' paraméter az "PSProfile" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="93c8e-123">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="93c8e-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="93c8e-124">OUTPUTS</span></span>

### <span data-ttu-id="93c8e-125">Microsoft. Azure. Command. CDN. models. profil. PSProfile</span><span class="sxs-lookup"><span data-stu-id="93c8e-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="93c8e-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="93c8e-126">NOTES</span></span>

## <span data-ttu-id="93c8e-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="93c8e-127">RELATED LINKS</span></span>

[<span data-ttu-id="93c8e-128">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="93c8e-128">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="93c8e-129">Új – AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="93c8e-129">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="93c8e-130">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="93c8e-130">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)


