---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
ms.openlocfilehash: 74bc4fae4dd55a85c4aca811819a0348f5df5f2c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480951"
---
# <span data-ttu-id="caeca-101">Get-AzCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="caeca-101">Get-AzCdnProfileSsoUrl</span></span>

## <span data-ttu-id="caeca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="caeca-102">SYNOPSIS</span></span>
<span data-ttu-id="caeca-103">Egy CDN-profil egyszeri bejelentkezési URL-címét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="caeca-103">Gets the single sign-on URL of a CDN profile.</span></span>

## <span data-ttu-id="caeca-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="caeca-104">SYNTAX</span></span>

### <span data-ttu-id="caeca-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="caeca-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="caeca-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="caeca-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="caeca-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="caeca-107">DESCRIPTION</span></span>
<span data-ttu-id="caeca-108">A **Get-AzCdnProfileSsoUrl** parancsmag megkapja az Azure Content Delivery Network (CDN) profil egyszeri bejelentkezési URL-címét.</span><span class="sxs-lookup"><span data-stu-id="caeca-108">The **Get-AzCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="caeca-109">Ez az URL lehetővé teszi a felhasználóknak, hogy egy kiegészítő portálhoz csatlakozzon, és a CDN további funkcióit használják.</span><span class="sxs-lookup"><span data-stu-id="caeca-109">This URL lets users connect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="caeca-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="caeca-110">EXAMPLES</span></span>

## <span data-ttu-id="caeca-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="caeca-111">PARAMETERS</span></span>

### <span data-ttu-id="caeca-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="caeca-112">-CdnProfile</span></span>
<span data-ttu-id="caeca-113">A CDN-profil megadása.</span><span class="sxs-lookup"><span data-stu-id="caeca-113">Specifies the CDN profile.</span></span>

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

### <span data-ttu-id="caeca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caeca-114">-DefaultProfile</span></span>
<span data-ttu-id="caeca-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="caeca-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="caeca-116">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="caeca-116">-ProfileName</span></span>
<span data-ttu-id="caeca-117">A CDN-profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="caeca-117">Specifies the name of the CDN profile.</span></span>

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

### <span data-ttu-id="caeca-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="caeca-118">-ResourceGroupName</span></span>
<span data-ttu-id="caeca-119">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a profil tartozik.</span><span class="sxs-lookup"><span data-stu-id="caeca-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

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

### <span data-ttu-id="caeca-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caeca-120">CommonParameters</span></span>
<span data-ttu-id="caeca-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="caeca-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caeca-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="caeca-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caeca-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="caeca-123">INPUTS</span></span>

### <span data-ttu-id="caeca-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="caeca-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="caeca-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="caeca-125">OUTPUTS</span></span>

### <span data-ttu-id="caeca-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span><span class="sxs-lookup"><span data-stu-id="caeca-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span></span>

## <span data-ttu-id="caeca-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="caeca-127">NOTES</span></span>

## <span data-ttu-id="caeca-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="caeca-128">RELATED LINKS</span></span>

[<span data-ttu-id="caeca-129">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="caeca-129">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)


