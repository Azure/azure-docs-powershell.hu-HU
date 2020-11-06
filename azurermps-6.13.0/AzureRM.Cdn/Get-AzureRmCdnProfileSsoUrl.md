---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSsoUrl.md
ms.openlocfilehash: 3ad44ba1edcec844dcb542defb1baf294aeaa89b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492848"
---
# <span data-ttu-id="da02b-101">Get-AzureRmCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="da02b-101">Get-AzureRmCdnProfileSsoUrl</span></span>

## <span data-ttu-id="da02b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="da02b-102">SYNOPSIS</span></span>
<span data-ttu-id="da02b-103">Beilleszti a CDN-profil egyszeri bejelentkezést tartalmazó URL-címét.</span><span class="sxs-lookup"><span data-stu-id="da02b-103">Gets the single sign-on URL of a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da02b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="da02b-104">SYNTAX</span></span>

### <span data-ttu-id="da02b-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="da02b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da02b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="da02b-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="da02b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="da02b-107">DESCRIPTION</span></span>
<span data-ttu-id="da02b-108">A **Get-AzureRmCdnProfileSsoUrl** parancsmag az Azure Content Delivery Network (CDN) profiljának egyszeri bejelentkezés URL-címét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="da02b-108">The **Get-AzureRmCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="da02b-109">Ez az URL lehetővé teszi a felhasználóknak, hogy Conntect egy kiegészítő portálon, és használják a CDN további funkcióit.</span><span class="sxs-lookup"><span data-stu-id="da02b-109">This URL lets users conntect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="da02b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="da02b-110">EXAMPLES</span></span>

## <span data-ttu-id="da02b-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="da02b-111">PARAMETERS</span></span>

### <span data-ttu-id="da02b-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="da02b-112">-CdnProfile</span></span>
<span data-ttu-id="da02b-113">A CDN-profilt adja meg.</span><span class="sxs-lookup"><span data-stu-id="da02b-113">Specifies the CDN profile.</span></span>

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

### <span data-ttu-id="da02b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da02b-114">-DefaultProfile</span></span>
<span data-ttu-id="da02b-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="da02b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da02b-116">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="da02b-116">-ProfileName</span></span>
<span data-ttu-id="da02b-117">A CDN-profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="da02b-117">Specifies the name of the CDN profile.</span></span>

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

### <span data-ttu-id="da02b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da02b-118">-ResourceGroupName</span></span>
<span data-ttu-id="da02b-119">Annak az erőforráscsoport-névnek a nevét adja meg, amelyhez a profil tartozik.</span><span class="sxs-lookup"><span data-stu-id="da02b-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

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

### <span data-ttu-id="da02b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da02b-120">CommonParameters</span></span>
<span data-ttu-id="da02b-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="da02b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da02b-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da02b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da02b-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="da02b-123">INPUTS</span></span>

### <span data-ttu-id="da02b-124">Microsoft. Azure. Command. CDN. models. profil. PSProfile</span><span class="sxs-lookup"><span data-stu-id="da02b-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="da02b-125">Paraméterek: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="da02b-125">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="da02b-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da02b-126">OUTPUTS</span></span>

### <span data-ttu-id="da02b-127">Microsoft. Azure. Command. CDN. models. profil. PSSsoUri</span><span class="sxs-lookup"><span data-stu-id="da02b-127">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span></span>

## <span data-ttu-id="da02b-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="da02b-128">NOTES</span></span>

## <span data-ttu-id="da02b-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da02b-129">RELATED LINKS</span></span>

[<span data-ttu-id="da02b-130">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="da02b-130">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)


