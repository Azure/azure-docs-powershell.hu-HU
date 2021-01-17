---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
ms.openlocfilehash: 1af77b3fec469b9bb60d5531c89534d5de11b4f0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348162"
---
# <span data-ttu-id="51c9c-101">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="51c9c-101">Get-AzCdnProfile</span></span>

## <span data-ttu-id="51c9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51c9c-102">SYNOPSIS</span></span>
<span data-ttu-id="51c9c-103">CDN-profilt kap.</span><span class="sxs-lookup"><span data-stu-id="51c9c-103">Gets a CDN profile.</span></span>

## <span data-ttu-id="51c9c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="51c9c-104">SYNTAX</span></span>

```
Get-AzCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51c9c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="51c9c-105">DESCRIPTION</span></span>
<span data-ttu-id="51c9c-106">A **Get-AzCdnProfile** parancsmag kap egy Azure Content Delivery Network -profilt (CDN) és annak kapcsolódó adatait.</span><span class="sxs-lookup"><span data-stu-id="51c9c-106">The **Get-AzCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="51c9c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="51c9c-107">EXAMPLES</span></span>

## <span data-ttu-id="51c9c-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51c9c-108">PARAMETERS</span></span>

### <span data-ttu-id="51c9c-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51c9c-109">-DefaultProfile</span></span>
<span data-ttu-id="51c9c-110">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="51c9c-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51c9c-111">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="51c9c-111">-ProfileName</span></span>
<span data-ttu-id="51c9c-112">A profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="51c9c-112">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51c9c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51c9c-113">-ResourceGroupName</span></span>
<span data-ttu-id="51c9c-114">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a profil tartozik.</span><span class="sxs-lookup"><span data-stu-id="51c9c-114">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51c9c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51c9c-115">CommonParameters</span></span>
<span data-ttu-id="51c9c-116">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51c9c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51c9c-117">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="51c9c-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51c9c-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="51c9c-118">INPUTS</span></span>

### <span data-ttu-id="51c9c-119">System.String</span><span class="sxs-lookup"><span data-stu-id="51c9c-119">System.String</span></span>

## <span data-ttu-id="51c9c-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="51c9c-120">OUTPUTS</span></span>

### <span data-ttu-id="51c9c-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="51c9c-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="51c9c-122">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="51c9c-122">NOTES</span></span>

## <span data-ttu-id="51c9c-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="51c9c-123">RELATED LINKS</span></span>

[<span data-ttu-id="51c9c-124">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="51c9c-124">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="51c9c-125">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="51c9c-125">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="51c9c-126">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="51c9c-126">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


