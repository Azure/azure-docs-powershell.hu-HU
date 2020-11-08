---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
ms.openlocfilehash: 341d46e5dd4ceefaf8baa76a71de462559115a5d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187638"
---
# <span data-ttu-id="653c7-101">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="653c7-101">Set-AzCdnProfile</span></span>

## <span data-ttu-id="653c7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="653c7-102">SYNOPSIS</span></span>
<span data-ttu-id="653c7-103">Egy CDN-profil frissítése</span><span class="sxs-lookup"><span data-stu-id="653c7-103">Updates a CDN profile.</span></span>

## <span data-ttu-id="653c7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="653c7-104">SYNTAX</span></span>

```
Set-AzCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="653c7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="653c7-105">DESCRIPTION</span></span>
<span data-ttu-id="653c7-106">A **set-AzCdnProfile** parancsmag egy Azure Content Delivery Network (CDN) profilt frissít.</span><span class="sxs-lookup"><span data-stu-id="653c7-106">The **Set-AzCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="653c7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="653c7-107">EXAMPLES</span></span>

## <span data-ttu-id="653c7-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="653c7-108">PARAMETERS</span></span>

### <span data-ttu-id="653c7-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="653c7-109">-CdnProfile</span></span>
<span data-ttu-id="653c7-110">A parancsmag által frissített profilt adja meg.</span><span class="sxs-lookup"><span data-stu-id="653c7-110">Specifies the profile that this cmdlet updates.</span></span>

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

### <span data-ttu-id="653c7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="653c7-111">-DefaultProfile</span></span>
<span data-ttu-id="653c7-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="653c7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="653c7-113">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="653c7-113">-Confirm</span></span>
<span data-ttu-id="653c7-114">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="653c7-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="653c7-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="653c7-115">-WhatIf</span></span>
<span data-ttu-id="653c7-116">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="653c7-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="653c7-117">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="653c7-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="653c7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="653c7-118">CommonParameters</span></span>
<span data-ttu-id="653c7-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="653c7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="653c7-120">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="653c7-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="653c7-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="653c7-121">INPUTS</span></span>

### <span data-ttu-id="653c7-122">Microsoft. Azure. Command. CDN. models. profil. PSProfile</span><span class="sxs-lookup"><span data-stu-id="653c7-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="653c7-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="653c7-123">OUTPUTS</span></span>

### <span data-ttu-id="653c7-124">Microsoft. Azure. Command. CDN. models. profil. PSProfile</span><span class="sxs-lookup"><span data-stu-id="653c7-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="653c7-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="653c7-125">NOTES</span></span>

## <span data-ttu-id="653c7-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="653c7-126">RELATED LINKS</span></span>

[<span data-ttu-id="653c7-127">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="653c7-127">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="653c7-128">Új – AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="653c7-128">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="653c7-129">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="653c7-129">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)


