---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
ms.openlocfilehash: 0a9ed100121c0f6610bcb019571fd1779f28dff4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010309"
---
# <span data-ttu-id="26dac-101">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="26dac-101">Set-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="26dac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26dac-102">SYNOPSIS</span></span>
<span data-ttu-id="26dac-103">Egy módosított Azure SecurityPartnerProvidert ment.</span><span class="sxs-lookup"><span data-stu-id="26dac-103">Saves a modified Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="26dac-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="26dac-104">SYNTAX</span></span>

```
Set-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26dac-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="26dac-105">DESCRIPTION</span></span>
<span data-ttu-id="26dac-106">A **Set-AzSecurityPartnerProvider** parancsmag frissíti az Azure SecurityPartnerProvider-t</span><span class="sxs-lookup"><span data-stu-id="26dac-106">The **Set-AzSecurityPartnerProvider** cmdlet updates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="26dac-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="26dac-107">EXAMPLES</span></span>

### <span data-ttu-id="26dac-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="26dac-108">Example 1</span></span>
```powershell
$securityPartnerProvider = Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
Set-AzSecurityPartnerProvider -SecurityPartnerProvider $securityPartnerProvider
```


## <span data-ttu-id="26dac-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26dac-109">PARAMETERS</span></span>

### <span data-ttu-id="26dac-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26dac-110">-AsJob</span></span>
<span data-ttu-id="26dac-111">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="26dac-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26dac-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26dac-112">-DefaultProfile</span></span>
<span data-ttu-id="26dac-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="26dac-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26dac-114">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="26dac-114">-SecurityPartnerProvider</span></span>
<span data-ttu-id="26dac-115">The SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="26dac-115">The SecurityPartnerProvider</span></span>

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

### <span data-ttu-id="26dac-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26dac-116">-Confirm</span></span>
<span data-ttu-id="26dac-117">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="26dac-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26dac-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26dac-118">-WhatIf</span></span>
<span data-ttu-id="26dac-119">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="26dac-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26dac-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="26dac-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26dac-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26dac-121">CommonParameters</span></span>
<span data-ttu-id="26dac-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26dac-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26dac-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26dac-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26dac-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26dac-124">INPUTS</span></span>

### <span data-ttu-id="26dac-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="26dac-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="26dac-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26dac-126">OUTPUTS</span></span>

### <span data-ttu-id="26dac-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="26dac-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="26dac-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="26dac-128">NOTES</span></span>

## <span data-ttu-id="26dac-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26dac-129">RELATED LINKS</span></span>
