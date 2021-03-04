---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
ms.openlocfilehash: c458973a5cff000cab13c4602e1a73234314c0d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924265"
---
# <span data-ttu-id="c373d-101">Get-AzCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="c373d-101">Get-AzCdnProfileSsoUrl</span></span>

## <span data-ttu-id="c373d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c373d-102">SYNOPSIS</span></span>
<span data-ttu-id="c373d-103">Egy CDN-profil egyszeri bejelentkezési URL-címét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c373d-103">Gets the single sign-on URL of a CDN profile.</span></span>

## <span data-ttu-id="c373d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c373d-104">SYNTAX</span></span>

### <span data-ttu-id="c373d-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c373d-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c373d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c373d-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c373d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c373d-107">DESCRIPTION</span></span>
<span data-ttu-id="c373d-108">A **Get-AzCdnProfileSsoUrl** parancsmag megkapja az Azure Content Delivery Network (CDN) profil egyszeri bejelentkezési URL-címét.</span><span class="sxs-lookup"><span data-stu-id="c373d-108">The **Get-AzCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="c373d-109">Ez az URL lehetővé teszi a felhasználóknak, hogy egy kiegészítő portálhoz csatlakozzon, és a CDN további funkcióit használják.</span><span class="sxs-lookup"><span data-stu-id="c373d-109">This URL lets users connect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="c373d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c373d-110">EXAMPLES</span></span>

## <span data-ttu-id="c373d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c373d-111">PARAMETERS</span></span>

### <span data-ttu-id="c373d-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="c373d-112">-CdnProfile</span></span>
<span data-ttu-id="c373d-113">A CDN-profil megadása.</span><span class="sxs-lookup"><span data-stu-id="c373d-113">Specifies the CDN profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c373d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c373d-114">-DefaultProfile</span></span>
<span data-ttu-id="c373d-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c373d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c373d-116">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="c373d-116">-ProfileName</span></span>
<span data-ttu-id="c373d-117">A CDN-profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c373d-117">Specifies the name of the CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c373d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c373d-118">-ResourceGroupName</span></span>
<span data-ttu-id="c373d-119">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a profil tartozik.</span><span class="sxs-lookup"><span data-stu-id="c373d-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c373d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c373d-120">CommonParameters</span></span>
<span data-ttu-id="c373d-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c373d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c373d-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c373d-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c373d-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c373d-123">INPUTS</span></span>

### <span data-ttu-id="c373d-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="c373d-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="c373d-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c373d-125">OUTPUTS</span></span>

### <span data-ttu-id="c373d-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span><span class="sxs-lookup"><span data-stu-id="c373d-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span></span>

## <span data-ttu-id="c373d-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c373d-127">NOTES</span></span>

## <span data-ttu-id="c373d-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c373d-128">RELATED LINKS</span></span>

[<span data-ttu-id="c373d-129">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="c373d-129">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)


