---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 2785A8E5-6905-4EDE-BFE1-FF7B1E386A39
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
ms.openlocfilehash: 0e69e48d29c96163acbb82ffe691de6affe8d131
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500912"
---
# <span data-ttu-id="92638-101">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="92638-101">New-AzureRmCdnProfile</span></span>

## <span data-ttu-id="92638-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="92638-102">SYNOPSIS</span></span>
<span data-ttu-id="92638-103">Egy CDN-profilt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="92638-103">Creates a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92638-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="92638-104">SYNTAX</span></span>

```
New-AzureRmCdnProfile -ProfileName <String> -Location <String> -Sku <PSSkuName> -ResourceGroupName <String>
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92638-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="92638-105">DESCRIPTION</span></span>
<span data-ttu-id="92638-106">A **New-AzureRmCdnProfile** parancsmag az Azure Content Delivery Network (CDN) profilját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="92638-106">The **New-AzureRmCdnProfile** cmdlet creates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="92638-107">Példák</span><span class="sxs-lookup"><span data-stu-id="92638-107">EXAMPLES</span></span>

## <span data-ttu-id="92638-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="92638-108">PARAMETERS</span></span>

### <span data-ttu-id="92638-109">-Hely</span><span class="sxs-lookup"><span data-stu-id="92638-109">-Location</span></span>
<span data-ttu-id="92638-110">A profil erőforrás-helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="92638-110">Specifies the resource location of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92638-111">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="92638-111">-ProfileName</span></span>
<span data-ttu-id="92638-112">A profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="92638-112">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92638-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92638-113">-ResourceGroupName</span></span>
<span data-ttu-id="92638-114">Annak az erőforrás-csoportnak a neve, amelyhez a profil tartozik.</span><span class="sxs-lookup"><span data-stu-id="92638-114">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92638-115">-SKU</span><span class="sxs-lookup"><span data-stu-id="92638-115">-Sku</span></span>
<span data-ttu-id="92638-116">A profil SKU-számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="92638-116">Specifies the SKU of the profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSSkuName
Parameter Sets: (All)
Aliases: 
Accepted values: Standard_Verizon, Premium_Verizon, Custom_Verizon, Standard_Akamai, Standard_ChinaCdn

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92638-117">-Címkék</span><span class="sxs-lookup"><span data-stu-id="92638-117">-Tags</span></span>
<span data-ttu-id="92638-118">Sepcifies a profillal társított címkékről.</span><span class="sxs-lookup"><span data-stu-id="92638-118">Sepcifies a hash table of tags that are associated with this profile.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92638-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="92638-119">-Confirm</span></span>
<span data-ttu-id="92638-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="92638-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92638-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92638-121">-WhatIf</span></span>
<span data-ttu-id="92638-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="92638-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92638-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="92638-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92638-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92638-124">-DefaultProfile</span></span>
<span data-ttu-id="92638-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="92638-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92638-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92638-126">CommonParameters</span></span>
<span data-ttu-id="92638-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="92638-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92638-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92638-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92638-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="92638-129">INPUTS</span></span>

## <span data-ttu-id="92638-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92638-130">OUTPUTS</span></span>

### <span data-ttu-id="92638-131">Microsoft. Azure. Command. CDN. models. profil. PSProfile</span><span class="sxs-lookup"><span data-stu-id="92638-131">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="92638-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="92638-132">NOTES</span></span>

## <span data-ttu-id="92638-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92638-133">RELATED LINKS</span></span>

[<span data-ttu-id="92638-134">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="92638-134">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="92638-135">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="92638-135">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="92638-136">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="92638-136">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


