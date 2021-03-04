---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/powershell/module/az.cdn/set-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
ms.openlocfilehash: 88e10d5f887d290139ee465217756c598bef0a3c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930362"
---
# <span data-ttu-id="724b5-101">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="724b5-101">Set-AzCdnProfile</span></span>

## <span data-ttu-id="724b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="724b5-102">SYNOPSIS</span></span>
<span data-ttu-id="724b5-103">Frissíti a CDN-profilt.</span><span class="sxs-lookup"><span data-stu-id="724b5-103">Updates a CDN profile.</span></span>

## <span data-ttu-id="724b5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="724b5-104">SYNTAX</span></span>

```
Set-AzCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="724b5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="724b5-105">DESCRIPTION</span></span>
<span data-ttu-id="724b5-106">A **Set-AzCdnProfile** parancsmag frissíti az Azure Content Delivery Network (CDN) profilt.</span><span class="sxs-lookup"><span data-stu-id="724b5-106">The **Set-AzCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="724b5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="724b5-107">EXAMPLES</span></span>

## <span data-ttu-id="724b5-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="724b5-108">PARAMETERS</span></span>

### <span data-ttu-id="724b5-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="724b5-109">-CdnProfile</span></span>
<span data-ttu-id="724b5-110">A parancsmag által frissülő profilt adja meg.</span><span class="sxs-lookup"><span data-stu-id="724b5-110">Specifies the profile that this cmdlet updates.</span></span>

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

### <span data-ttu-id="724b5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="724b5-111">-DefaultProfile</span></span>
<span data-ttu-id="724b5-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="724b5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="724b5-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="724b5-113">-Confirm</span></span>
<span data-ttu-id="724b5-114">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="724b5-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="724b5-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="724b5-115">-WhatIf</span></span>
<span data-ttu-id="724b5-116">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="724b5-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="724b5-117">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="724b5-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="724b5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="724b5-118">CommonParameters</span></span>
<span data-ttu-id="724b5-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="724b5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="724b5-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="724b5-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="724b5-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="724b5-121">INPUTS</span></span>

### <span data-ttu-id="724b5-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="724b5-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="724b5-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="724b5-123">OUTPUTS</span></span>

### <span data-ttu-id="724b5-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="724b5-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="724b5-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="724b5-125">NOTES</span></span>

## <span data-ttu-id="724b5-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="724b5-126">RELATED LINKS</span></span>

[<span data-ttu-id="724b5-127">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="724b5-127">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="724b5-128">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="724b5-128">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="724b5-129">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="724b5-129">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)


