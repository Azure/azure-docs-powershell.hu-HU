---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
ms.openlocfilehash: 2d78e7136fe42187cbabc2345e2ad2314af1d9c5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012508"
---
# <span data-ttu-id="2e659-101">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="2e659-101">Set-AzIpGroup</span></span>

## <span data-ttu-id="2e659-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2e659-102">SYNOPSIS</span></span>
<span data-ttu-id="2e659-103">Módosított tűzfal mentése</span><span class="sxs-lookup"><span data-stu-id="2e659-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="2e659-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2e659-104">SYNTAX</span></span>

```
Set-AzIpGroup -IpGroup <PSIpGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2e659-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2e659-105">DESCRIPTION</span></span>
<span data-ttu-id="2e659-106">A **set-AzIpGroup** parancsmag egy Azure-IpGroup frissít</span><span class="sxs-lookup"><span data-stu-id="2e659-106">The **Set-AzIpGroup** cmdlet updates an Azure IpGroup</span></span>

## <span data-ttu-id="2e659-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2e659-107">EXAMPLES</span></span>

### <span data-ttu-id="2e659-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2e659-108">Example 1</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
$ipGroup.IpAddresses.Add("11.11.0.0/24")
Set-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="2e659-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2e659-109">PARAMETERS</span></span>

### <span data-ttu-id="2e659-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e659-110">-AsJob</span></span>
<span data-ttu-id="2e659-111">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2e659-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2e659-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e659-112">-DefaultProfile</span></span>
<span data-ttu-id="2e659-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e659-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e659-114">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="2e659-114">-IpGroup</span></span>
<span data-ttu-id="2e659-115">A IpGroup</span><span class="sxs-lookup"><span data-stu-id="2e659-115">The IpGroup</span></span>

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

### <span data-ttu-id="2e659-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2e659-116">-Confirm</span></span>
<span data-ttu-id="2e659-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2e659-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e659-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e659-118">-WhatIf</span></span>
<span data-ttu-id="2e659-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2e659-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e659-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2e659-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e659-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e659-121">CommonParameters</span></span>
<span data-ttu-id="2e659-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2e659-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e659-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2e659-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e659-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e659-124">INPUTS</span></span>

### <span data-ttu-id="2e659-125">Microsoft. Azure. commands. Network. models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="2e659-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="2e659-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e659-126">OUTPUTS</span></span>

### <span data-ttu-id="2e659-127">Microsoft. Azure. commands. Network. models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="2e659-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="2e659-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2e659-128">NOTES</span></span>

## <span data-ttu-id="2e659-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e659-129">RELATED LINKS</span></span>
