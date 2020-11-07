---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 2785A8E5-6905-4EDE-BFE1-FF7B1E386A39
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnProfile.md
ms.openlocfilehash: 7f62d12fbed217fa744ed5753c9234fb0e558caf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667578"
---
# <span data-ttu-id="0eb00-101">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="0eb00-101">New-AzCdnProfile</span></span>

## <span data-ttu-id="0eb00-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0eb00-102">SYNOPSIS</span></span>
<span data-ttu-id="0eb00-103">Egy CDN-profilt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0eb00-103">Creates a CDN profile.</span></span>

## <span data-ttu-id="0eb00-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0eb00-104">SYNTAX</span></span>

```
New-AzCdnProfile -ProfileName <String> -Location <String> -Sku <PSSkuName> -ResourceGroupName <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0eb00-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0eb00-105">DESCRIPTION</span></span>
<span data-ttu-id="0eb00-106">A **New-AzCdnProfile** parancsmag az Azure Content Delivery Network (CDN) profilját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="0eb00-106">The **New-AzCdnProfile** cmdlet creates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="0eb00-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0eb00-107">EXAMPLES</span></span>

## <span data-ttu-id="0eb00-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0eb00-108">PARAMETERS</span></span>

### <span data-ttu-id="0eb00-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eb00-109">-DefaultProfile</span></span>
<span data-ttu-id="0eb00-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0eb00-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0eb00-111">-Hely</span><span class="sxs-lookup"><span data-stu-id="0eb00-111">-Location</span></span>
<span data-ttu-id="0eb00-112">A profil erőforrás-helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0eb00-112">Specifies the resource location of the profile.</span></span>

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

### <span data-ttu-id="0eb00-113">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="0eb00-113">-ProfileName</span></span>
<span data-ttu-id="0eb00-114">A profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0eb00-114">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="0eb00-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eb00-115">-ResourceGroupName</span></span>
<span data-ttu-id="0eb00-116">Annak az erőforrás-csoportnak a neve, amelyhez a profil tartozik.</span><span class="sxs-lookup"><span data-stu-id="0eb00-116">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="0eb00-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="0eb00-117">-Sku</span></span>
<span data-ttu-id="0eb00-118">A profil SKU-számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0eb00-118">Specifies the SKU of the profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSSkuName
Parameter Sets: (All)
Aliases:
Accepted values: Standard_Verizon, Premium_Verizon, Custom_Verizon, Standard_Akamai, Standard_ChinaCdn, Standard_Microsoft

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb00-119">-Címke</span><span class="sxs-lookup"><span data-stu-id="0eb00-119">-Tag</span></span>
<span data-ttu-id="0eb00-120">Az Azure CDN-profillal társítani kívánt címkék.</span><span class="sxs-lookup"><span data-stu-id="0eb00-120">The tags to associate with the Azure CDN profile.</span></span>

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

### <span data-ttu-id="0eb00-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0eb00-121">-Confirm</span></span>
<span data-ttu-id="0eb00-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0eb00-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0eb00-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0eb00-123">-WhatIf</span></span>
<span data-ttu-id="0eb00-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0eb00-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0eb00-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0eb00-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0eb00-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eb00-126">CommonParameters</span></span>
<span data-ttu-id="0eb00-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0eb00-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eb00-128">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0eb00-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eb00-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0eb00-129">INPUTS</span></span>

### <span data-ttu-id="0eb00-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0eb00-130">System.String</span></span>

## <span data-ttu-id="0eb00-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0eb00-131">OUTPUTS</span></span>

### <span data-ttu-id="0eb00-132">Microsoft. Azure. Command. CDN. models. profil. PSProfile</span><span class="sxs-lookup"><span data-stu-id="0eb00-132">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="0eb00-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0eb00-133">NOTES</span></span>

## <span data-ttu-id="0eb00-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0eb00-134">RELATED LINKS</span></span>

[<span data-ttu-id="0eb00-135">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="0eb00-135">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="0eb00-136">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="0eb00-136">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="0eb00-137">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="0eb00-137">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


