---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: fdcd725c79a6f789879ab3103cec90b09c828e74
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195717"
---
# <span data-ttu-id="bd2e8-101">Get-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="bd2e8-101">Get-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="bd2e8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bd2e8-102">SYNOPSIS</span></span>
<span data-ttu-id="bd2e8-103">Beolvassa az alkalmazás-átjáró tűzfalának házirendjét.</span><span class="sxs-lookup"><span data-stu-id="bd2e8-103">Gets an application gateway firewall policy.</span></span>

## <span data-ttu-id="bd2e8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bd2e8-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFirewallPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd2e8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bd2e8-105">DESCRIPTION</span></span>
<span data-ttu-id="bd2e8-106">A **Get-AzApplicationGatewayFirewallPolicy** parancsmag az alkalmazás-átjáró tűzfal-házirendjét kapja.</span><span class="sxs-lookup"><span data-stu-id="bd2e8-106">The **Get-AzApplicationGatewayFirewallPolicy** cmdlet gets an application gateway firewall policy..</span></span>

## <span data-ttu-id="bd2e8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bd2e8-107">EXAMPLES</span></span>

### <span data-ttu-id="bd2e8-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bd2e8-108">Example 1</span></span>
```powershell
PS C:\> $AppGwFirewallPolicy = Get-AzApplicationGatewayFirewallPolicy -Name "FirewallPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="bd2e8-109">Ez a parancs beolvassa a FirewallPolicy1 nevű, a ResourceGroup01 nevű erőforráscsoporthoz tartozó Application gateway tűzfal-házirendet, és a $AppGwFirewallPolicy változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="bd2e8-109">This command gets the application gateway firewall policy named FirewallPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="bd2e8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bd2e8-110">PARAMETERS</span></span>

### <span data-ttu-id="bd2e8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd2e8-111">-DefaultProfile</span></span>
<span data-ttu-id="bd2e8-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bd2e8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd2e8-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bd2e8-113">-Name</span></span>
<span data-ttu-id="bd2e8-114">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="bd2e8-114">The resource name.</span></span>

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

### <span data-ttu-id="bd2e8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd2e8-115">-ResourceGroupName</span></span>
<span data-ttu-id="bd2e8-116">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="bd2e8-116">The resource group name.</span></span>

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

### <span data-ttu-id="bd2e8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd2e8-117">CommonParameters</span></span>
<span data-ttu-id="bd2e8-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bd2e8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd2e8-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bd2e8-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd2e8-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd2e8-120">INPUTS</span></span>

### <span data-ttu-id="bd2e8-121">System. String</span><span class="sxs-lookup"><span data-stu-id="bd2e8-121">System.String</span></span>

## <span data-ttu-id="bd2e8-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd2e8-122">OUTPUTS</span></span>

### <span data-ttu-id="bd2e8-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="bd2e8-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="bd2e8-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bd2e8-124">NOTES</span></span>

## <span data-ttu-id="bd2e8-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd2e8-125">RELATED LINKS</span></span>