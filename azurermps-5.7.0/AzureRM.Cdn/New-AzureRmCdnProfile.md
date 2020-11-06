---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 2785A8E5-6905-4EDE-BFE1-FF7B1E386A39
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/new-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
ms.openlocfilehash: 5423844d7f466a827f3a452a05cf3999236198d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493228"
---
# <span data-ttu-id="5b6b7-101">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5b6b7-101">New-AzureRmCdnProfile</span></span>

## <span data-ttu-id="5b6b7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5b6b7-102">SYNOPSIS</span></span>
<span data-ttu-id="5b6b7-103">Egy CDN-profilt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="5b6b7-103">Creates a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b6b7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5b6b7-104">SYNTAX</span></span>

```
New-AzureRmCdnProfile -ProfileName <String> -Location <String> -Sku <PSSkuName> -ResourceGroupName <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b6b7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5b6b7-105">DESCRIPTION</span></span>
<span data-ttu-id="5b6b7-106">A **New-AzureRmCdnProfile** parancsmag az Azure Content Delivery Network (CDN) profilját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="5b6b7-106">The **New-AzureRmCdnProfile** cmdlet creates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="5b6b7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5b6b7-107">EXAMPLES</span></span>

## <span data-ttu-id="5b6b7-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5b6b7-108">PARAMETERS</span></span>

### <span data-ttu-id="5b6b7-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b6b7-109">-DefaultProfile</span></span>
<span data-ttu-id="5b6b7-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5b6b7-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b6b7-111">-Hely</span><span class="sxs-lookup"><span data-stu-id="5b6b7-111">-Location</span></span>
<span data-ttu-id="5b6b7-112">A profil erőforrás-helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b6b7-112">Specifies the resource location of the profile.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b6b7-113">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="5b6b7-113">-ProfileName</span></span>
<span data-ttu-id="5b6b7-114">A profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b6b7-114">Specifies the name of the profile.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b6b7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b6b7-115">-ResourceGroupName</span></span>
<span data-ttu-id="5b6b7-116">Annak az erőforrás-csoportnak a neve, amelyhez a profil tartozik.</span><span class="sxs-lookup"><span data-stu-id="5b6b7-116">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b6b7-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="5b6b7-117">-Sku</span></span>
<span data-ttu-id="5b6b7-118">A profil SKU-számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b6b7-118">Specifies the SKU of the profile.</span></span>

```yaml
Type: PSSkuName
Parameter Sets: (All)
Aliases:
Accepted values: Standard_Verizon, Premium_Verizon, Custom_Verizon, Standard_Akamai, Standard_ChinaCdn

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b6b7-119">-Címke</span><span class="sxs-lookup"><span data-stu-id="5b6b7-119">-Tag</span></span>
<span data-ttu-id="5b6b7-120">Az Azure CDN-profillal társítani kívánt címkék.</span><span class="sxs-lookup"><span data-stu-id="5b6b7-120">The tags to associate with the Azure CDN profile.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b6b7-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5b6b7-121">-Confirm</span></span>
<span data-ttu-id="5b6b7-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5b6b7-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b6b7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b6b7-123">-WhatIf</span></span>
<span data-ttu-id="5b6b7-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5b6b7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b6b7-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5b6b7-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b6b7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b6b7-126">CommonParameters</span></span>
<span data-ttu-id="5b6b7-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5b6b7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b6b7-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b6b7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b6b7-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b6b7-129">INPUTS</span></span>

### <span data-ttu-id="5b6b7-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="5b6b7-130">None</span></span>
<span data-ttu-id="5b6b7-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="5b6b7-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5b6b7-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b6b7-132">OUTPUTS</span></span>

### <span data-ttu-id="5b6b7-133">Microsoft. Azure. Command. CDN. models. profil. PSProfile</span><span class="sxs-lookup"><span data-stu-id="5b6b7-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="5b6b7-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5b6b7-134">NOTES</span></span>

## <span data-ttu-id="5b6b7-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b6b7-135">RELATED LINKS</span></span>

[<span data-ttu-id="5b6b7-136">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5b6b7-136">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="5b6b7-137">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5b6b7-137">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="5b6b7-138">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5b6b7-138">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


