---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpTag.md
ms.openlocfilehash: 6d46be31d443bdfeeda850cd03ce2a050e25549f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505308"
---
# <span data-ttu-id="0169f-101">New-AzureRmPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="0169f-101">New-AzureRmPublicIpTag</span></span>

## <span data-ttu-id="0169f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0169f-102">SYNOPSIS</span></span>
<span data-ttu-id="0169f-103">IP-címkét hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0169f-103">Creates an IP Tag.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0169f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0169f-104">SYNTAX</span></span>

```
New-AzureRmPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0169f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0169f-105">DESCRIPTION</span></span>
<span data-ttu-id="0169f-106">A **New-AzureRmPublicIpTag** parancsmag létrehoz egy IP-címkét.</span><span class="sxs-lookup"><span data-stu-id="0169f-106">The **New-AzureRmPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="0169f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0169f-107">EXAMPLES</span></span>

### <span data-ttu-id="0169f-108">1: új IP-címke létrehozása</span><span class="sxs-lookup"><span data-stu-id="0169f-108">1: Create a new IP Tag</span></span>
```
$ipTag = New-AzureRmPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="0169f-109">A parancs új IP-címkét hoz létre a TagType, például "FirstPartyUsage" és "/SQL" (például "") címkével.</span><span class="sxs-lookup"><span data-stu-id="0169f-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="0169f-110">Ez a funkció a publicIpAddress való létrehozásban használható a kiosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="0169f-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="0169f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0169f-111">PARAMETERS</span></span>

### <span data-ttu-id="0169f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0169f-112">-DefaultProfile</span></span>
<span data-ttu-id="0169f-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0169f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0169f-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="0169f-114">-IpTagType</span></span>
<span data-ttu-id="0169f-115">IpTag típusa példa: FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="0169f-115">IpTag type Example:FirstPartyUsage</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: FirstPartyUsage, NetworkDomain

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0169f-116">-Címke</span><span class="sxs-lookup"><span data-stu-id="0169f-116">-Tag</span></span>
<span data-ttu-id="0169f-117">IpTag-érték példa:/SQL</span><span class="sxs-lookup"><span data-stu-id="0169f-117">IpTag value Example:/Sql</span></span>

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

### <span data-ttu-id="0169f-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0169f-118">-Confirm</span></span>
<span data-ttu-id="0169f-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0169f-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0169f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0169f-120">-WhatIf</span></span>
<span data-ttu-id="0169f-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0169f-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0169f-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0169f-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0169f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0169f-123">CommonParameters</span></span>
<span data-ttu-id="0169f-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0169f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0169f-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0169f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0169f-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0169f-126">INPUTS</span></span>

### <span data-ttu-id="0169f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="0169f-127">System.String</span></span>

## <span data-ttu-id="0169f-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0169f-128">OUTPUTS</span></span>

### <span data-ttu-id="0169f-129">Microsoft. Azure. commands. Network. models. PSPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="0169f-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>

## <span data-ttu-id="0169f-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0169f-130">NOTES</span></span>

## <span data-ttu-id="0169f-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0169f-131">RELATED LINKS</span></span>
