---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
ms.openlocfilehash: 5d7d73b3c7f49babc9e80929dab7b3fa2adad20a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159083"
---
# <span data-ttu-id="99d2f-101">New-AzPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="99d2f-101">New-AzPublicIpTag</span></span>

## <span data-ttu-id="99d2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99d2f-102">SYNOPSIS</span></span>
<span data-ttu-id="99d2f-103">IP-címkét hoz létre.</span><span class="sxs-lookup"><span data-stu-id="99d2f-103">Creates an IP Tag.</span></span>

## <span data-ttu-id="99d2f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="99d2f-104">SYNTAX</span></span>

```
New-AzPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99d2f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="99d2f-105">DESCRIPTION</span></span>
<span data-ttu-id="99d2f-106">A **New-AzPublicIpTag** parancsmag létrehoz egy IP-címkét.</span><span class="sxs-lookup"><span data-stu-id="99d2f-106">The **New-AzPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="99d2f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="99d2f-107">EXAMPLES</span></span>

### <span data-ttu-id="99d2f-108">1. példa: Új IP-címke létrehozása</span><span class="sxs-lookup"><span data-stu-id="99d2f-108">Example 1: Create a new IP Tag</span></span>
```powershell
$ipTag = New-AzPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="99d2f-109">Ez a parancs létrehoz egy új IP-címkét a "FirstPartyUsage" címkével és a "/Sql" címkével.</span><span class="sxs-lookup"><span data-stu-id="99d2f-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="99d2f-110">Ezt használja a publicIpAddress létrehozása ezekkel a konkrét címkékkel a kiosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="99d2f-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="99d2f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99d2f-111">PARAMETERS</span></span>

### <span data-ttu-id="99d2f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99d2f-112">-DefaultProfile</span></span>
<span data-ttu-id="99d2f-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="99d2f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99d2f-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="99d2f-114">-IpTagType</span></span>
<span data-ttu-id="99d2f-115">IpTag type Example:FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="99d2f-115">IpTag type Example:FirstPartyUsage</span></span>

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

### <span data-ttu-id="99d2f-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="99d2f-116">-Tag</span></span>
<span data-ttu-id="99d2f-117">Példa IPTag értékre:/Sql</span><span class="sxs-lookup"><span data-stu-id="99d2f-117">IpTag value Example:/Sql</span></span>

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

### <span data-ttu-id="99d2f-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="99d2f-118">-Confirm</span></span>
<span data-ttu-id="99d2f-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="99d2f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99d2f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99d2f-120">-WhatIf</span></span>
<span data-ttu-id="99d2f-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="99d2f-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99d2f-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="99d2f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99d2f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99d2f-123">CommonParameters</span></span>
<span data-ttu-id="99d2f-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99d2f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99d2f-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="99d2f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99d2f-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="99d2f-126">INPUTS</span></span>

### <span data-ttu-id="99d2f-127">System.String</span><span class="sxs-lookup"><span data-stu-id="99d2f-127">System.String</span></span>

## <span data-ttu-id="99d2f-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99d2f-128">OUTPUTS</span></span>

### <span data-ttu-id="99d2f-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="99d2f-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>

## <span data-ttu-id="99d2f-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="99d2f-130">NOTES</span></span>

## <span data-ttu-id="99d2f-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99d2f-131">RELATED LINKS</span></span>
