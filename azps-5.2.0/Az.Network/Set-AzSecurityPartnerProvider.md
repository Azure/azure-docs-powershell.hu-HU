---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
ms.openlocfilehash: 07a29a17a1a7c17a0bbf7b202b019e7d833a5050
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357501"
---
# <span data-ttu-id="54e34-101">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="54e34-101">Set-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="54e34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54e34-102">SYNOPSIS</span></span>
<span data-ttu-id="54e34-103">Egy módosított Azure SecurityPartnerProvidert ment.</span><span class="sxs-lookup"><span data-stu-id="54e34-103">Saves a modified Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="54e34-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="54e34-104">SYNTAX</span></span>

```
Set-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54e34-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="54e34-105">DESCRIPTION</span></span>
<span data-ttu-id="54e34-106">A **Set-AzSecurityPartnerProvider** parancsmag frissíti az Azure SecurityPartnerProvider-t</span><span class="sxs-lookup"><span data-stu-id="54e34-106">The **Set-AzSecurityPartnerProvider** cmdlet updates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="54e34-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="54e34-107">EXAMPLES</span></span>

### <span data-ttu-id="54e34-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="54e34-108">Example 1</span></span>
```powershell
$securityPartnerProvider = Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
Set-AzSecurityPartnerProvider -SecurityPartnerProvider $securityPartnerProvider
```


## <span data-ttu-id="54e34-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54e34-109">PARAMETERS</span></span>

### <span data-ttu-id="54e34-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54e34-110">-AsJob</span></span>
<span data-ttu-id="54e34-111">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="54e34-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="54e34-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54e34-112">-DefaultProfile</span></span>
<span data-ttu-id="54e34-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="54e34-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54e34-114">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="54e34-114">-SecurityPartnerProvider</span></span>
<span data-ttu-id="54e34-115">The SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="54e34-115">The SecurityPartnerProvider</span></span>

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

### <span data-ttu-id="54e34-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54e34-116">-Confirm</span></span>
<span data-ttu-id="54e34-117">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="54e34-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54e34-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54e34-118">-WhatIf</span></span>
<span data-ttu-id="54e34-119">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="54e34-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54e34-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="54e34-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54e34-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54e34-121">CommonParameters</span></span>
<span data-ttu-id="54e34-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54e34-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54e34-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54e34-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54e34-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="54e34-124">INPUTS</span></span>

### <span data-ttu-id="54e34-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="54e34-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="54e34-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="54e34-126">OUTPUTS</span></span>

### <span data-ttu-id="54e34-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="54e34-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="54e34-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="54e34-128">NOTES</span></span>

## <span data-ttu-id="54e34-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="54e34-129">RELATED LINKS</span></span>
