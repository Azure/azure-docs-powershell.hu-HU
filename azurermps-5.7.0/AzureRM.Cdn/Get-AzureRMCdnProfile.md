---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
ms.openlocfilehash: a345b69fdc6695706f61a85c2926392c9f522aeb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493241"
---
# <span data-ttu-id="5c1f5-101">Get-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5c1f5-101">Get-AzureRmCdnProfile</span></span>

## <span data-ttu-id="5c1f5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5c1f5-102">SYNOPSIS</span></span>
<span data-ttu-id="5c1f5-103">Kap egy CDN-profilt.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-103">Gets a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c1f5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5c1f5-104">SYNTAX</span></span>

```
Get-AzureRmCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c1f5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5c1f5-105">DESCRIPTION</span></span>
<span data-ttu-id="5c1f5-106">A **Get-AzureRMCdnProfile** parancsmag Azure Content Delivery Network (CDN) profilját és kapcsolódó információit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-106">The **Get-AzureRMCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="5c1f5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5c1f5-107">EXAMPLES</span></span>

## <span data-ttu-id="5c1f5-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5c1f5-108">PARAMETERS</span></span>

### <span data-ttu-id="5c1f5-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c1f5-109">-DefaultProfile</span></span>
<span data-ttu-id="5c1f5-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5c1f5-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c1f5-111">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="5c1f5-111">-ProfileName</span></span>
<span data-ttu-id="5c1f5-112">A profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-112">Specifies the name of the profile.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c1f5-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c1f5-113">-ResourceGroupName</span></span>
<span data-ttu-id="5c1f5-114">Annak az erőforrás-csoportnak a neve, amelyhez a profil tartozik.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-114">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c1f5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c1f5-115">CommonParameters</span></span>
<span data-ttu-id="5c1f5-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5c1f5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c1f5-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c1f5-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c1f5-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c1f5-118">INPUTS</span></span>

### <span data-ttu-id="5c1f5-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="5c1f5-119">None</span></span>
<span data-ttu-id="5c1f5-120">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5c1f5-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c1f5-121">OUTPUTS</span></span>

###  
<span data-ttu-id="5c1f5-122">Ez a parancsmag egy profil-objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="5c1f5-122">This cmdlet returns a profile object.</span></span>

## <span data-ttu-id="5c1f5-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5c1f5-123">NOTES</span></span>

## <span data-ttu-id="5c1f5-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5c1f5-124">RELATED LINKS</span></span>

[<span data-ttu-id="5c1f5-125">Új – AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5c1f5-125">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="5c1f5-126">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5c1f5-126">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="5c1f5-127">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5c1f5-127">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


