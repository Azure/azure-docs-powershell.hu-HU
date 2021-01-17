---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
ms.openlocfilehash: 2d78e7136fe42187cbabc2345e2ad2314af1d9c5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98481153"
---
# <span data-ttu-id="198c4-101">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="198c4-101">Set-AzIpGroup</span></span>

## <span data-ttu-id="198c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="198c4-102">SYNOPSIS</span></span>
<span data-ttu-id="198c4-103">Módosított tűzfalat ment.</span><span class="sxs-lookup"><span data-stu-id="198c4-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="198c4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="198c4-104">SYNTAX</span></span>

```
Set-AzIpGroup -IpGroup <PSIpGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="198c4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="198c4-105">DESCRIPTION</span></span>
<span data-ttu-id="198c4-106">A **Set-AzIpGroup parancsmag** frissíti az Azure IpGroup-et</span><span class="sxs-lookup"><span data-stu-id="198c4-106">The **Set-AzIpGroup** cmdlet updates an Azure IpGroup</span></span>

## <span data-ttu-id="198c4-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="198c4-107">EXAMPLES</span></span>

### <span data-ttu-id="198c4-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="198c4-108">Example 1</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
$ipGroup.IpAddresses.Add("11.11.0.0/24")
Set-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="198c4-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="198c4-109">PARAMETERS</span></span>

### <span data-ttu-id="198c4-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="198c4-110">-AsJob</span></span>
<span data-ttu-id="198c4-111">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="198c4-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="198c4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="198c4-112">-DefaultProfile</span></span>
<span data-ttu-id="198c4-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="198c4-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="198c4-114">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="198c4-114">-IpGroup</span></span>
<span data-ttu-id="198c4-115">Az IpGroup</span><span class="sxs-lookup"><span data-stu-id="198c4-115">The IpGroup</span></span>

```yaml
Type: PSIpGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="198c4-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="198c4-116">-Confirm</span></span>
<span data-ttu-id="198c4-117">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="198c4-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="198c4-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="198c4-118">-WhatIf</span></span>
<span data-ttu-id="198c4-119">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="198c4-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="198c4-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="198c4-120">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="198c4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="198c4-121">CommonParameters</span></span>
<span data-ttu-id="198c4-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="198c4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="198c4-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="198c4-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="198c4-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="198c4-124">INPUTS</span></span>

### <span data-ttu-id="198c4-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="198c4-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="198c4-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="198c4-126">OUTPUTS</span></span>

### <span data-ttu-id="198c4-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="198c4-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="198c4-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="198c4-128">NOTES</span></span>

## <span data-ttu-id="198c4-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="198c4-129">RELATED LINKS</span></span>
