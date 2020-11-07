---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
ms.openlocfilehash: 7e4bfae0479d4f37f6a73c8e07239112267ac182
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670285"
---
# <span data-ttu-id="0cff1-101">New-AzPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="0cff1-101">New-AzPublicIpTag</span></span>

## <span data-ttu-id="0cff1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0cff1-102">SYNOPSIS</span></span>
<span data-ttu-id="0cff1-103">IP-címkét hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0cff1-103">Creates an IP Tag.</span></span>

## <span data-ttu-id="0cff1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0cff1-104">SYNTAX</span></span>

```
New-AzPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cff1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0cff1-105">DESCRIPTION</span></span>
<span data-ttu-id="0cff1-106">A **New-AzPublicIpTag** parancsmag létrehoz egy IP-címkét.</span><span class="sxs-lookup"><span data-stu-id="0cff1-106">The **New-AzPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="0cff1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0cff1-107">EXAMPLES</span></span>

### <span data-ttu-id="0cff1-108">1: új IP-címke létrehozása</span><span class="sxs-lookup"><span data-stu-id="0cff1-108">1: Create a new IP Tag</span></span>
```
$ipTag = New-AzPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="0cff1-109">A parancs új IP-címkét hoz létre a TagType, például "FirstPartyUsage" és "/SQL" (például "") címkével.</span><span class="sxs-lookup"><span data-stu-id="0cff1-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="0cff1-110">Ez a funkció a publicIpAddress való létrehozásban használható a kiosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="0cff1-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="0cff1-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0cff1-111">PARAMETERS</span></span>

### <span data-ttu-id="0cff1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cff1-112">-DefaultProfile</span></span>
<span data-ttu-id="0cff1-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0cff1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0cff1-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="0cff1-114">-IpTagType</span></span>
<span data-ttu-id="0cff1-115">IpTag típusa példa: FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="0cff1-115">IpTag type Example:FirstPartyUsage</span></span>

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

### <span data-ttu-id="0cff1-116">-Címke</span><span class="sxs-lookup"><span data-stu-id="0cff1-116">-Tag</span></span>
<span data-ttu-id="0cff1-117">IpTag-érték példa:/SQL</span><span class="sxs-lookup"><span data-stu-id="0cff1-117">IpTag value Example:/Sql</span></span>

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

### <span data-ttu-id="0cff1-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0cff1-118">-Confirm</span></span>
<span data-ttu-id="0cff1-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0cff1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cff1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cff1-120">-WhatIf</span></span>
<span data-ttu-id="0cff1-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0cff1-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cff1-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0cff1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cff1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cff1-123">CommonParameters</span></span>
<span data-ttu-id="0cff1-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0cff1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cff1-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cff1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cff1-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0cff1-126">INPUTS</span></span>

### <span data-ttu-id="0cff1-127">System. String</span><span class="sxs-lookup"><span data-stu-id="0cff1-127">System.String</span></span>

## <span data-ttu-id="0cff1-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0cff1-128">OUTPUTS</span></span>

### <span data-ttu-id="0cff1-129">Microsoft. Azure. commands. Network. models. PSPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="0cff1-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>

## <span data-ttu-id="0cff1-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0cff1-130">NOTES</span></span>

## <span data-ttu-id="0cff1-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0cff1-131">RELATED LINKS</span></span>
