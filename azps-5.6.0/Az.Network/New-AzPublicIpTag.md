---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
ms.openlocfilehash: 2f46b13570ef1f538658dae6d02000848822c150
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919561"
---
# <span data-ttu-id="6b0c6-101">New-AzPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="6b0c6-101">New-AzPublicIpTag</span></span>

## <span data-ttu-id="6b0c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b0c6-102">SYNOPSIS</span></span>
<span data-ttu-id="6b0c6-103">IP-címkét hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6b0c6-103">Creates an IP Tag.</span></span>

## <span data-ttu-id="6b0c6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6b0c6-104">SYNTAX</span></span>

```
New-AzPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b0c6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6b0c6-105">DESCRIPTION</span></span>
<span data-ttu-id="6b0c6-106">A **New-AzPublicIpTag** parancsmag létrehoz egy IP-címkét.</span><span class="sxs-lookup"><span data-stu-id="6b0c6-106">The **New-AzPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="6b0c6-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6b0c6-107">EXAMPLES</span></span>

### <span data-ttu-id="6b0c6-108">1. példa: Új IP-címke létrehozása</span><span class="sxs-lookup"><span data-stu-id="6b0c6-108">Example 1: Create a new IP Tag</span></span>
```powershell
$ipTag = New-AzPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="6b0c6-109">Ez a parancs létrehoz egy új IP-címkét a "FirstPartyUsage" címkével és a "/Sql" címkével.</span><span class="sxs-lookup"><span data-stu-id="6b0c6-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="6b0c6-110">Ezt használja a publicIpAddress létrehozása ezekkel a konkrét címkékkel a kiosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="6b0c6-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="6b0c6-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b0c6-111">PARAMETERS</span></span>

### <span data-ttu-id="6b0c6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b0c6-112">-DefaultProfile</span></span>
<span data-ttu-id="6b0c6-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b0c6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b0c6-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="6b0c6-114">-IpTagType</span></span>
<span data-ttu-id="6b0c6-115">IpTag type Example:FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="6b0c6-115">IpTag type Example:FirstPartyUsage</span></span>

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

### <span data-ttu-id="6b0c6-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="6b0c6-116">-Tag</span></span>
<span data-ttu-id="6b0c6-117">Példa IPTag értékre:/Sql</span><span class="sxs-lookup"><span data-stu-id="6b0c6-117">IpTag value Example:/Sql</span></span>

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

### <span data-ttu-id="6b0c6-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b0c6-118">-Confirm</span></span>
<span data-ttu-id="6b0c6-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6b0c6-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b0c6-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b0c6-120">-WhatIf</span></span>
<span data-ttu-id="6b0c6-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6b0c6-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b0c6-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6b0c6-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b0c6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b0c6-123">CommonParameters</span></span>
<span data-ttu-id="6b0c6-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b0c6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b0c6-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b0c6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b0c6-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b0c6-126">INPUTS</span></span>

### <span data-ttu-id="6b0c6-127">System.String</span><span class="sxs-lookup"><span data-stu-id="6b0c6-127">System.String</span></span>

## <span data-ttu-id="6b0c6-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b0c6-128">OUTPUTS</span></span>

### <span data-ttu-id="6b0c6-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="6b0c6-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>

## <span data-ttu-id="6b0c6-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6b0c6-130">NOTES</span></span>

## <span data-ttu-id="6b0c6-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b0c6-131">RELATED LINKS</span></span>
