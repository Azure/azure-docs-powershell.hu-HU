---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
ms.openlocfilehash: 2d78e7136fe42187cbabc2345e2ad2314af1d9c5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156731"
---
# <span data-ttu-id="40dee-101">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="40dee-101">Set-AzIpGroup</span></span>

## <span data-ttu-id="40dee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40dee-102">SYNOPSIS</span></span>
<span data-ttu-id="40dee-103">Módosított tűzfalat ment.</span><span class="sxs-lookup"><span data-stu-id="40dee-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="40dee-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="40dee-104">SYNTAX</span></span>

```
Set-AzIpGroup -IpGroup <PSIpGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="40dee-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="40dee-105">DESCRIPTION</span></span>
<span data-ttu-id="40dee-106">A **Set-AzIpGroup parancsmag** frissíti az Azure IpGroup-et</span><span class="sxs-lookup"><span data-stu-id="40dee-106">The **Set-AzIpGroup** cmdlet updates an Azure IpGroup</span></span>

## <span data-ttu-id="40dee-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="40dee-107">EXAMPLES</span></span>

### <span data-ttu-id="40dee-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="40dee-108">Example 1</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
$ipGroup.IpAddresses.Add("11.11.0.0/24")
Set-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="40dee-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40dee-109">PARAMETERS</span></span>

### <span data-ttu-id="40dee-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40dee-110">-AsJob</span></span>
<span data-ttu-id="40dee-111">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="40dee-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="40dee-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40dee-112">-DefaultProfile</span></span>
<span data-ttu-id="40dee-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="40dee-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40dee-114">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="40dee-114">-IpGroup</span></span>
<span data-ttu-id="40dee-115">Az IpGroup</span><span class="sxs-lookup"><span data-stu-id="40dee-115">The IpGroup</span></span>

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

### <span data-ttu-id="40dee-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40dee-116">-Confirm</span></span>
<span data-ttu-id="40dee-117">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="40dee-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40dee-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40dee-118">-WhatIf</span></span>
<span data-ttu-id="40dee-119">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="40dee-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40dee-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="40dee-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40dee-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40dee-121">CommonParameters</span></span>
<span data-ttu-id="40dee-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40dee-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40dee-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40dee-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40dee-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="40dee-124">INPUTS</span></span>

### <span data-ttu-id="40dee-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="40dee-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="40dee-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40dee-126">OUTPUTS</span></span>

### <span data-ttu-id="40dee-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="40dee-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="40dee-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="40dee-128">NOTES</span></span>

## <span data-ttu-id="40dee-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40dee-129">RELATED LINKS</span></span>
