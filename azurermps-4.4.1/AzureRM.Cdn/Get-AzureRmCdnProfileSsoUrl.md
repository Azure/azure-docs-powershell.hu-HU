---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSsoUrl.md
ms.openlocfilehash: 2365502bb681cafe8ed7fedb05a4a862e54a3cc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679114"
---
# <span data-ttu-id="115a3-101">Get-AzureRmCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="115a3-101">Get-AzureRmCdnProfileSsoUrl</span></span>

## <span data-ttu-id="115a3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="115a3-102">SYNOPSIS</span></span>
<span data-ttu-id="115a3-103">Beilleszti a CDN-profil egyszeri bejelentkezést tartalmazó URL-címét.</span><span class="sxs-lookup"><span data-stu-id="115a3-103">Gets the single sign-on URL of a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="115a3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="115a3-104">SYNTAX</span></span>

### <span data-ttu-id="115a3-105">Paraméterérték a mezők paramétereinek beállításához (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="115a3-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="115a3-106">Az objektum paramétereinek beállítása paraméter</span><span class="sxs-lookup"><span data-stu-id="115a3-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="115a3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="115a3-107">DESCRIPTION</span></span>
<span data-ttu-id="115a3-108">A **Get-AzureRmCdnProfileSsoUrl** parancsmag az Azure Content Delivery Network (CDN) profiljának egyszeri bejelentkezés URL-címét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="115a3-108">The **Get-AzureRmCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="115a3-109">Ez az URL lehetővé teszi a felhasználóknak, hogy Conntect egy kiegészítő portálon, és használják a CDN további funkcióit.</span><span class="sxs-lookup"><span data-stu-id="115a3-109">This URL lets users conntect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="115a3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="115a3-110">EXAMPLES</span></span>

## <span data-ttu-id="115a3-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="115a3-111">PARAMETERS</span></span>

### <span data-ttu-id="115a3-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="115a3-112">-CdnProfile</span></span>
<span data-ttu-id="115a3-113">A CDN-profilt adja meg.</span><span class="sxs-lookup"><span data-stu-id="115a3-113">Specifies the CDN profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="115a3-114">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="115a3-114">-ProfileName</span></span>
<span data-ttu-id="115a3-115">A CDN-profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="115a3-115">Specifies the name of the CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="115a3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="115a3-116">-ResourceGroupName</span></span>
<span data-ttu-id="115a3-117">Annak az erőforráscsoport-névnek a nevét adja meg, amelyhez a profil tartozik.</span><span class="sxs-lookup"><span data-stu-id="115a3-117">Specifies the name of the resource group name to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="115a3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="115a3-118">-DefaultProfile</span></span>
<span data-ttu-id="115a3-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="115a3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="115a3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="115a3-120">CommonParameters</span></span>
<span data-ttu-id="115a3-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="115a3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="115a3-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="115a3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="115a3-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="115a3-123">INPUTS</span></span>

### <span data-ttu-id="115a3-124">PSProfile</span><span class="sxs-lookup"><span data-stu-id="115a3-124">PSProfile</span></span>
<span data-ttu-id="115a3-125">A ' CdnProfile ' paraméter az "PSProfile" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="115a3-125">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="115a3-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="115a3-126">OUTPUTS</span></span>

###  
<span data-ttu-id="115a3-127">Ez a parancsmag URL-címet ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="115a3-127">This cmdlet returns a URL.</span></span>

## <span data-ttu-id="115a3-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="115a3-128">NOTES</span></span>

## <span data-ttu-id="115a3-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="115a3-129">RELATED LINKS</span></span>

[<span data-ttu-id="115a3-130">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="115a3-130">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)


