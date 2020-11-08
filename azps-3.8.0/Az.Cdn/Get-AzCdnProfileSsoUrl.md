---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
ms.openlocfilehash: 74bc4fae4dd55a85c4aca811819a0348f5df5f2c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011491"
---
# <span data-ttu-id="68665-101">Get-AzCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="68665-101">Get-AzCdnProfileSsoUrl</span></span>

## <span data-ttu-id="68665-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="68665-102">SYNOPSIS</span></span>
<span data-ttu-id="68665-103">Beilleszti a CDN-profil egyszeri bejelentkezést tartalmazó URL-címét.</span><span class="sxs-lookup"><span data-stu-id="68665-103">Gets the single sign-on URL of a CDN profile.</span></span>

## <span data-ttu-id="68665-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="68665-104">SYNTAX</span></span>

### <span data-ttu-id="68665-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="68665-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68665-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68665-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68665-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="68665-107">DESCRIPTION</span></span>
<span data-ttu-id="68665-108">A **Get-AzCdnProfileSsoUrl** parancsmag az Azure Content Delivery Network (CDN) profiljának egyszeri bejelentkezés URL-címét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="68665-108">The **Get-AzCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="68665-109">Ez az URL-cím lehetővé teszi a felhasználóknak, hogy csatlakozzanak egy további portálhoz, és használják a CDN további funkcióit.</span><span class="sxs-lookup"><span data-stu-id="68665-109">This URL lets users connect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="68665-110">Példák</span><span class="sxs-lookup"><span data-stu-id="68665-110">EXAMPLES</span></span>

## <span data-ttu-id="68665-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="68665-111">PARAMETERS</span></span>

### <span data-ttu-id="68665-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="68665-112">-CdnProfile</span></span>
<span data-ttu-id="68665-113">A CDN-profilt adja meg.</span><span class="sxs-lookup"><span data-stu-id="68665-113">Specifies the CDN profile.</span></span>

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

### <span data-ttu-id="68665-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68665-114">-DefaultProfile</span></span>
<span data-ttu-id="68665-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="68665-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68665-116">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="68665-116">-ProfileName</span></span>
<span data-ttu-id="68665-117">A CDN-profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="68665-117">Specifies the name of the CDN profile.</span></span>

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

### <span data-ttu-id="68665-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68665-118">-ResourceGroupName</span></span>
<span data-ttu-id="68665-119">Annak az erőforráscsoport-névnek a nevét adja meg, amelyhez a profil tartozik.</span><span class="sxs-lookup"><span data-stu-id="68665-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

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

### <span data-ttu-id="68665-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68665-120">CommonParameters</span></span>
<span data-ttu-id="68665-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="68665-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68665-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="68665-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68665-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="68665-123">INPUTS</span></span>

### <span data-ttu-id="68665-124">Microsoft. Azure. Command. CDN. models. profil. PSProfile</span><span class="sxs-lookup"><span data-stu-id="68665-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="68665-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="68665-125">OUTPUTS</span></span>

### <span data-ttu-id="68665-126">Microsoft. Azure. Command. CDN. models. profil. PSSsoUri</span><span class="sxs-lookup"><span data-stu-id="68665-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span></span>

## <span data-ttu-id="68665-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="68665-127">NOTES</span></span>

## <span data-ttu-id="68665-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="68665-128">RELATED LINKS</span></span>

[<span data-ttu-id="68665-129">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="68665-129">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)


