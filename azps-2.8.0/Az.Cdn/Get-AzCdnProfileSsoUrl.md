---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
ms.openlocfilehash: e32d8312d0046786e6fd36ce30e525241fe78c6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667597"
---
# <span data-ttu-id="00fba-101">Get-AzCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="00fba-101">Get-AzCdnProfileSsoUrl</span></span>

## <span data-ttu-id="00fba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="00fba-102">SYNOPSIS</span></span>
<span data-ttu-id="00fba-103">Beilleszti a CDN-profil egyszeri bejelentkezést tartalmazó URL-címét.</span><span class="sxs-lookup"><span data-stu-id="00fba-103">Gets the single sign-on URL of a CDN profile.</span></span>

## <span data-ttu-id="00fba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="00fba-104">SYNTAX</span></span>

### <span data-ttu-id="00fba-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="00fba-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00fba-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="00fba-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00fba-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="00fba-107">DESCRIPTION</span></span>
<span data-ttu-id="00fba-108">A **Get-AzCdnProfileSsoUrl** parancsmag az Azure Content Delivery Network (CDN) profiljának egyszeri bejelentkezés URL-címét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="00fba-108">The **Get-AzCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="00fba-109">Ez az URL-cím lehetővé teszi a felhasználóknak, hogy csatlakozzanak egy további portálhoz, és használják a CDN további funkcióit.</span><span class="sxs-lookup"><span data-stu-id="00fba-109">This URL lets users connect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="00fba-110">Példák</span><span class="sxs-lookup"><span data-stu-id="00fba-110">EXAMPLES</span></span>

## <span data-ttu-id="00fba-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="00fba-111">PARAMETERS</span></span>

### <span data-ttu-id="00fba-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="00fba-112">-CdnProfile</span></span>
<span data-ttu-id="00fba-113">A CDN-profilt adja meg.</span><span class="sxs-lookup"><span data-stu-id="00fba-113">Specifies the CDN profile.</span></span>

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

### <span data-ttu-id="00fba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00fba-114">-DefaultProfile</span></span>
<span data-ttu-id="00fba-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="00fba-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00fba-116">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="00fba-116">-ProfileName</span></span>
<span data-ttu-id="00fba-117">A CDN-profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="00fba-117">Specifies the name of the CDN profile.</span></span>

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

### <span data-ttu-id="00fba-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00fba-118">-ResourceGroupName</span></span>
<span data-ttu-id="00fba-119">Annak az erőforráscsoport-névnek a nevét adja meg, amelyhez a profil tartozik.</span><span class="sxs-lookup"><span data-stu-id="00fba-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

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

### <span data-ttu-id="00fba-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00fba-120">CommonParameters</span></span>
<span data-ttu-id="00fba-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="00fba-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00fba-122">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="00fba-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00fba-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="00fba-123">INPUTS</span></span>

### <span data-ttu-id="00fba-124">Microsoft. Azure. Command. CDN. models. profil. PSProfile</span><span class="sxs-lookup"><span data-stu-id="00fba-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="00fba-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00fba-125">OUTPUTS</span></span>

### <span data-ttu-id="00fba-126">Microsoft. Azure. Command. CDN. models. profil. PSSsoUri</span><span class="sxs-lookup"><span data-stu-id="00fba-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span></span>

## <span data-ttu-id="00fba-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="00fba-127">NOTES</span></span>

## <span data-ttu-id="00fba-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00fba-128">RELATED LINKS</span></span>

[<span data-ttu-id="00fba-129">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="00fba-129">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)


