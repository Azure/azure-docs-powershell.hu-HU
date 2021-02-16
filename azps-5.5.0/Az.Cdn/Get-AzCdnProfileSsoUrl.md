---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
ms.openlocfilehash: 74bc4fae4dd55a85c4aca811819a0348f5df5f2c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149082"
---
# <span data-ttu-id="b0b10-101">Get-AzCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="b0b10-101">Get-AzCdnProfileSsoUrl</span></span>

## <span data-ttu-id="b0b10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0b10-102">SYNOPSIS</span></span>
<span data-ttu-id="b0b10-103">Egy CDN-profil egyszeri bejelentkezési URL-címét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b0b10-103">Gets the single sign-on URL of a CDN profile.</span></span>

## <span data-ttu-id="b0b10-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b0b10-104">SYNTAX</span></span>

### <span data-ttu-id="b0b10-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b0b10-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0b10-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0b10-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0b10-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b0b10-107">DESCRIPTION</span></span>
<span data-ttu-id="b0b10-108">A **Get-AzCdnProfileSsoUrl** parancsmag megkapja az Azure Content Delivery Network (CDN) profil egyszeri bejelentkezési URL-címét.</span><span class="sxs-lookup"><span data-stu-id="b0b10-108">The **Get-AzCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="b0b10-109">Ez az URL lehetővé teszi a felhasználóknak, hogy egy kiegészítő portálhoz csatlakozzon, és a CDN további funkcióit használják.</span><span class="sxs-lookup"><span data-stu-id="b0b10-109">This URL lets users connect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="b0b10-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b0b10-110">EXAMPLES</span></span>

## <span data-ttu-id="b0b10-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0b10-111">PARAMETERS</span></span>

### <span data-ttu-id="b0b10-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="b0b10-112">-CdnProfile</span></span>
<span data-ttu-id="b0b10-113">A CDN-profil megadása.</span><span class="sxs-lookup"><span data-stu-id="b0b10-113">Specifies the CDN profile.</span></span>

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

### <span data-ttu-id="b0b10-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0b10-114">-DefaultProfile</span></span>
<span data-ttu-id="b0b10-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b0b10-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b0b10-116">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="b0b10-116">-ProfileName</span></span>
<span data-ttu-id="b0b10-117">A CDN-profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b0b10-117">Specifies the name of the CDN profile.</span></span>

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

### <span data-ttu-id="b0b10-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0b10-118">-ResourceGroupName</span></span>
<span data-ttu-id="b0b10-119">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a profil tartozik.</span><span class="sxs-lookup"><span data-stu-id="b0b10-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

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

### <span data-ttu-id="b0b10-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0b10-120">CommonParameters</span></span>
<span data-ttu-id="b0b10-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0b10-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0b10-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0b10-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0b10-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0b10-123">INPUTS</span></span>

### <span data-ttu-id="b0b10-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="b0b10-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="b0b10-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0b10-125">OUTPUTS</span></span>

### <span data-ttu-id="b0b10-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span><span class="sxs-lookup"><span data-stu-id="b0b10-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span></span>

## <span data-ttu-id="b0b10-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b0b10-127">NOTES</span></span>

## <span data-ttu-id="b0b10-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b0b10-128">RELATED LINKS</span></span>

[<span data-ttu-id="b0b10-129">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="b0b10-129">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)


