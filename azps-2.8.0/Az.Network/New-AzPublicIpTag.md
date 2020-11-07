---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
ms.openlocfilehash: 10b2ab56e2a1075061f79a25608b42d5e67a5329
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837924"
---
# <span data-ttu-id="51c13-101">New-AzPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="51c13-101">New-AzPublicIpTag</span></span>

## <span data-ttu-id="51c13-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="51c13-102">SYNOPSIS</span></span>
<span data-ttu-id="51c13-103">IP-címkét hoz létre.</span><span class="sxs-lookup"><span data-stu-id="51c13-103">Creates an IP Tag.</span></span>

## <span data-ttu-id="51c13-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="51c13-104">SYNTAX</span></span>

```
New-AzPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51c13-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="51c13-105">DESCRIPTION</span></span>
<span data-ttu-id="51c13-106">A **New-AzPublicIpTag** parancsmag létrehoz egy IP-címkét.</span><span class="sxs-lookup"><span data-stu-id="51c13-106">The **New-AzPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="51c13-107">Példák</span><span class="sxs-lookup"><span data-stu-id="51c13-107">EXAMPLES</span></span>

### <span data-ttu-id="51c13-108">1: új IP-címke létrehozása</span><span class="sxs-lookup"><span data-stu-id="51c13-108">1: Create a new IP Tag</span></span>
```
$ipTag = New-AzPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="51c13-109">A parancs új IP-címkét hoz létre a TagType, például "FirstPartyUsage" és "/SQL" (például "") címkével.</span><span class="sxs-lookup"><span data-stu-id="51c13-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="51c13-110">Ez a funkció a publicIpAddress való létrehozásban használható a kiosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="51c13-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="51c13-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="51c13-111">PARAMETERS</span></span>

### <span data-ttu-id="51c13-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51c13-112">-DefaultProfile</span></span>
<span data-ttu-id="51c13-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="51c13-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51c13-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="51c13-114">-IpTagType</span></span>
<span data-ttu-id="51c13-115">IpTag típusa példa: FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="51c13-115">IpTag type Example:FirstPartyUsage</span></span>

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

### <span data-ttu-id="51c13-116">-Címke</span><span class="sxs-lookup"><span data-stu-id="51c13-116">-Tag</span></span>
<span data-ttu-id="51c13-117">IpTag-érték példa:/SQL</span><span class="sxs-lookup"><span data-stu-id="51c13-117">IpTag value Example:/Sql</span></span>

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

### <span data-ttu-id="51c13-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="51c13-118">-Confirm</span></span>
<span data-ttu-id="51c13-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="51c13-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51c13-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51c13-120">-WhatIf</span></span>
<span data-ttu-id="51c13-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="51c13-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51c13-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="51c13-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51c13-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51c13-123">CommonParameters</span></span>
<span data-ttu-id="51c13-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="51c13-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51c13-125">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="51c13-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51c13-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="51c13-126">INPUTS</span></span>

### <span data-ttu-id="51c13-127">System. String</span><span class="sxs-lookup"><span data-stu-id="51c13-127">System.String</span></span>

## <span data-ttu-id="51c13-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="51c13-128">OUTPUTS</span></span>

### <span data-ttu-id="51c13-129">Microsoft. Azure. commands. Network. models. PSPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="51c13-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>

## <span data-ttu-id="51c13-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="51c13-130">NOTES</span></span>

## <span data-ttu-id="51c13-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="51c13-131">RELATED LINKS</span></span>
