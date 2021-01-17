---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: fdcd725c79a6f789879ab3103cec90b09c828e74
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359209"
---
# <span data-ttu-id="b080c-101">Get-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b080c-101">Get-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="b080c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b080c-102">SYNOPSIS</span></span>
<span data-ttu-id="b080c-103">Alkalmazásátjáró tűzfal házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="b080c-103">Gets an application gateway firewall policy.</span></span>

## <span data-ttu-id="b080c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b080c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFirewallPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b080c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b080c-105">DESCRIPTION</span></span>
<span data-ttu-id="b080c-106">A **Get-AzApplicationGatewayFirewallPolicy parancsmag** egy alkalmazás-átjáró tűzfalházirata-házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="b080c-106">The **Get-AzApplicationGatewayFirewallPolicy** cmdlet gets an application gateway firewall policy..</span></span>

## <span data-ttu-id="b080c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b080c-107">EXAMPLES</span></span>

### <span data-ttu-id="b080c-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="b080c-108">Example 1</span></span>
```powershell
PS C:\> $AppGwFirewallPolicy = Get-AzApplicationGatewayFirewallPolicy -Name "FirewallPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b080c-109">Ez a parancs a FirewallPolicy1 nevű alkalmazás-átjáró tűzfal házirendet kapja meg, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a $AppGwFirewallPolicy tárolja.</span><span class="sxs-lookup"><span data-stu-id="b080c-109">This command gets the application gateway firewall policy named FirewallPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="b080c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b080c-110">PARAMETERS</span></span>

### <span data-ttu-id="b080c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b080c-111">-DefaultProfile</span></span>
<span data-ttu-id="b080c-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b080c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b080c-113">-Name</span><span class="sxs-lookup"><span data-stu-id="b080c-113">-Name</span></span>
<span data-ttu-id="b080c-114">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="b080c-114">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b080c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b080c-115">-ResourceGroupName</span></span>
<span data-ttu-id="b080c-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b080c-116">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b080c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b080c-117">CommonParameters</span></span>
<span data-ttu-id="b080c-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b080c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b080c-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b080c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b080c-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b080c-120">INPUTS</span></span>

### <span data-ttu-id="b080c-121">System.String</span><span class="sxs-lookup"><span data-stu-id="b080c-121">System.String</span></span>

## <span data-ttu-id="b080c-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b080c-122">OUTPUTS</span></span>

### <span data-ttu-id="b080c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b080c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="b080c-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b080c-124">NOTES</span></span>

## <span data-ttu-id="b080c-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b080c-125">RELATED LINKS</span></span>
