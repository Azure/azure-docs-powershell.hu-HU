---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
ms.openlocfilehash: 07a29a17a1a7c17a0bbf7b202b019e7d833a5050
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187938"
---
# <span data-ttu-id="ccdd5-101">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="ccdd5-101">Set-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="ccdd5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ccdd5-102">SYNOPSIS</span></span>
<span data-ttu-id="ccdd5-103">Módosított Azure-SecurityPartnerProvider mentése</span><span class="sxs-lookup"><span data-stu-id="ccdd5-103">Saves a modified Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="ccdd5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ccdd5-104">SYNTAX</span></span>

```
Set-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccdd5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ccdd5-105">DESCRIPTION</span></span>
<span data-ttu-id="ccdd5-106">A **set-AzSecurityPartnerProvider** parancsmag egy Azure-SecurityPartnerProvider frissít</span><span class="sxs-lookup"><span data-stu-id="ccdd5-106">The **Set-AzSecurityPartnerProvider** cmdlet updates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="ccdd5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ccdd5-107">EXAMPLES</span></span>

### <span data-ttu-id="ccdd5-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ccdd5-108">Example 1</span></span>
```powershell
$securityPartnerProvider = Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
Set-AzSecurityPartnerProvider -SecurityPartnerProvider $securityPartnerProvider
```


## <span data-ttu-id="ccdd5-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ccdd5-109">PARAMETERS</span></span>

### <span data-ttu-id="ccdd5-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ccdd5-110">-AsJob</span></span>
<span data-ttu-id="ccdd5-111">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ccdd5-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ccdd5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccdd5-112">-DefaultProfile</span></span>
<span data-ttu-id="ccdd5-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ccdd5-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccdd5-114">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="ccdd5-114">-SecurityPartnerProvider</span></span>
<span data-ttu-id="ccdd5-115">A SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="ccdd5-115">The SecurityPartnerProvider</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccdd5-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ccdd5-116">-Confirm</span></span>
<span data-ttu-id="ccdd5-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ccdd5-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccdd5-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccdd5-118">-WhatIf</span></span>
<span data-ttu-id="ccdd5-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ccdd5-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccdd5-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ccdd5-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccdd5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccdd5-121">CommonParameters</span></span>
<span data-ttu-id="ccdd5-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ccdd5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccdd5-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ccdd5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccdd5-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccdd5-124">INPUTS</span></span>

### <span data-ttu-id="ccdd5-125">Microsoft. Azure. commands. Network. models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="ccdd5-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="ccdd5-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccdd5-126">OUTPUTS</span></span>

### <span data-ttu-id="ccdd5-127">Microsoft. Azure. commands. Network. models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="ccdd5-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="ccdd5-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ccdd5-128">NOTES</span></span>

## <span data-ttu-id="ccdd5-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ccdd5-129">RELATED LINKS</span></span>
