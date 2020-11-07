---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
ms.openlocfilehash: ecc89a75f144a92653dd0e3c498d664df8c370e5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671398"
---
# <span data-ttu-id="67e9e-101">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="67e9e-101">Set-AzCdnProfile</span></span>

## <span data-ttu-id="67e9e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="67e9e-102">SYNOPSIS</span></span>
<span data-ttu-id="67e9e-103">Egy CDN-profil frissítése</span><span class="sxs-lookup"><span data-stu-id="67e9e-103">Updates a CDN profile.</span></span>

## <span data-ttu-id="67e9e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="67e9e-104">SYNTAX</span></span>

```
Set-AzCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="67e9e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="67e9e-105">DESCRIPTION</span></span>
<span data-ttu-id="67e9e-106">A **set-AzCdnProfile** parancsmag egy Azure Content Delivery Network (CDN) profilt frissít.</span><span class="sxs-lookup"><span data-stu-id="67e9e-106">The **Set-AzCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="67e9e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="67e9e-107">EXAMPLES</span></span>

## <span data-ttu-id="67e9e-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="67e9e-108">PARAMETERS</span></span>

### <span data-ttu-id="67e9e-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="67e9e-109">-CdnProfile</span></span>
<span data-ttu-id="67e9e-110">A parancsmag által frissített profilt adja meg.</span><span class="sxs-lookup"><span data-stu-id="67e9e-110">Specifies the profile that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67e9e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67e9e-111">-DefaultProfile</span></span>
<span data-ttu-id="67e9e-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="67e9e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67e9e-113">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="67e9e-113">-Confirm</span></span>
<span data-ttu-id="67e9e-114">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="67e9e-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67e9e-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67e9e-115">-WhatIf</span></span>
<span data-ttu-id="67e9e-116">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="67e9e-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67e9e-117">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="67e9e-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67e9e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67e9e-118">CommonParameters</span></span>
<span data-ttu-id="67e9e-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="67e9e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67e9e-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67e9e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67e9e-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="67e9e-121">INPUTS</span></span>

### <span data-ttu-id="67e9e-122">Microsoft. Azure. Command. CDN. models. profil. PSProfile</span><span class="sxs-lookup"><span data-stu-id="67e9e-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="67e9e-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="67e9e-123">OUTPUTS</span></span>

### <span data-ttu-id="67e9e-124">Microsoft. Azure. Command. CDN. models. profil. PSProfile</span><span class="sxs-lookup"><span data-stu-id="67e9e-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="67e9e-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="67e9e-125">NOTES</span></span>

## <span data-ttu-id="67e9e-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="67e9e-126">RELATED LINKS</span></span>

[<span data-ttu-id="67e9e-127">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="67e9e-127">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="67e9e-128">Új – AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="67e9e-128">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="67e9e-129">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="67e9e-129">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)


