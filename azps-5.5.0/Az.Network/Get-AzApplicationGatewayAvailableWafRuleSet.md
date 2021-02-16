---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablewafruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: 7cb3f6d015f95ba6a72066714647eb7a0551398b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157106"
---
# <span data-ttu-id="cb7d7-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb7d7-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="cb7d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb7d7-102">SYNOPSIS</span></span>
<span data-ttu-id="cb7d7-103">A webalkalmazás tűzfalszabály-készletének összes elérhető beállítása.</span><span class="sxs-lookup"><span data-stu-id="cb7d7-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="cb7d7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cb7d7-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb7d7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cb7d7-105">DESCRIPTION</span></span>
<span data-ttu-id="cb7d7-106">A **Get-AzApplicationGatewayAvailableWafRuleSet** parancsmag minden elérhető webalkalmazás tűzfalszabály-készletét megkapja.</span><span class="sxs-lookup"><span data-stu-id="cb7d7-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="cb7d7-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cb7d7-107">EXAMPLES</span></span>

### <span data-ttu-id="cb7d7-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="cb7d7-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="cb7d7-109">Ez a parancs az összes elérhető webalkalmazás tűzfalszabály-készletét visszaadja.</span><span class="sxs-lookup"><span data-stu-id="cb7d7-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="cb7d7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb7d7-110">PARAMETERS</span></span>

### <span data-ttu-id="cb7d7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb7d7-111">-DefaultProfile</span></span>
<span data-ttu-id="cb7d7-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cb7d7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb7d7-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb7d7-113">CommonParameters</span></span>
<span data-ttu-id="cb7d7-114">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb7d7-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb7d7-115">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb7d7-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb7d7-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cb7d7-116">INPUTS</span></span>

### <span data-ttu-id="cb7d7-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="cb7d7-117">None</span></span>

## <span data-ttu-id="cb7d7-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb7d7-118">OUTPUTS</span></span>

### <span data-ttu-id="cb7d7-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="cb7d7-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="cb7d7-120">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cb7d7-120">NOTES</span></span>
<span data-ttu-id="cb7d7-121">**A List-AzApplicationGatewayAvailableWafRuleSets** a **Get-AzApplicationGatewayAvailableWafRuleSet** parancsmag aliasa.</span><span class="sxs-lookup"><span data-stu-id="cb7d7-121">**List-AzApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="cb7d7-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb7d7-122">RELATED LINKS</span></span>
