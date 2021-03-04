---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 122e011336b9fcdb8b8eb19622632e1ff295a01c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941762"
---
# <span data-ttu-id="4369f-101">Get-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="4369f-101">Get-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="4369f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4369f-102">SYNOPSIS</span></span>
<span data-ttu-id="4369f-103">Alkalmazásátjáró tűzfal házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="4369f-103">Gets an application gateway firewall policy.</span></span>

## <span data-ttu-id="4369f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4369f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFirewallPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4369f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4369f-105">DESCRIPTION</span></span>
<span data-ttu-id="4369f-106">A **Get-AzApplicationGatewayFirewallPolicy parancsmag** egy alkalmazás-átjáró tűzfalházirata-házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="4369f-106">The **Get-AzApplicationGatewayFirewallPolicy** cmdlet gets an application gateway firewall policy..</span></span>

## <span data-ttu-id="4369f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4369f-107">EXAMPLES</span></span>

### <span data-ttu-id="4369f-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="4369f-108">Example 1</span></span>
```powershell
PS C:\> $AppGwFirewallPolicy = Get-AzApplicationGatewayFirewallPolicy -Name "FirewallPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4369f-109">Ez a parancs a FirewallPolicy1 nevű alkalmazás-átjáró tűzfal házirendet kapja meg, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a $AppGwFirewallPolicy tárolja.</span><span class="sxs-lookup"><span data-stu-id="4369f-109">This command gets the application gateway firewall policy named FirewallPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="4369f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4369f-110">PARAMETERS</span></span>

### <span data-ttu-id="4369f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4369f-111">-DefaultProfile</span></span>
<span data-ttu-id="4369f-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4369f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4369f-113">-Name</span><span class="sxs-lookup"><span data-stu-id="4369f-113">-Name</span></span>
<span data-ttu-id="4369f-114">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="4369f-114">The resource name.</span></span>

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

### <span data-ttu-id="4369f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4369f-115">-ResourceGroupName</span></span>
<span data-ttu-id="4369f-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4369f-116">The resource group name.</span></span>

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

### <span data-ttu-id="4369f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4369f-117">CommonParameters</span></span>
<span data-ttu-id="4369f-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4369f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4369f-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4369f-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4369f-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4369f-120">INPUTS</span></span>

### <span data-ttu-id="4369f-121">System.String</span><span class="sxs-lookup"><span data-stu-id="4369f-121">System.String</span></span>

## <span data-ttu-id="4369f-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4369f-122">OUTPUTS</span></span>

### <span data-ttu-id="4369f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="4369f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="4369f-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4369f-124">NOTES</span></span>

## <span data-ttu-id="4369f-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4369f-125">RELATED LINKS</span></span>
