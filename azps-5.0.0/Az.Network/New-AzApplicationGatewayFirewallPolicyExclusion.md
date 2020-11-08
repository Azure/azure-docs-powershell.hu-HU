---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicyexclusion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
ms.openlocfilehash: e5ad76625a171e1fd12fc583c6ad8acf593ed817
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195560"
---
# <span data-ttu-id="f05b9-101">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="f05b9-101">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="f05b9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f05b9-102">SYNOPSIS</span></span>
<span data-ttu-id="f05b9-103">Kizárást hoz létre a tűzfal házirendjében.</span><span class="sxs-lookup"><span data-stu-id="f05b9-103">Creates an exclusion on the Firewall Policy</span></span>

## <span data-ttu-id="f05b9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f05b9-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable <String> -SelectorMatchOperator <String>
 -Selector <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f05b9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f05b9-105">DESCRIPTION</span></span>
<span data-ttu-id="f05b9-106">A **New-AzApplicationGatewayFirewallPolicyExclusion** parancsmag új kizárási szabály listája a tűzfal házirendjében.</span><span class="sxs-lookup"><span data-stu-id="f05b9-106">The **New-AzApplicationGatewayFirewallPolicyExclusion** cmdlet a new exclusion rule list for firewall policy.</span></span>

## <span data-ttu-id="f05b9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f05b9-107">EXAMPLES</span></span>

### <span data-ttu-id="f05b9-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f05b9-108">Example 1</span></span>
```powershell
PS C:\> $exclusionEntry = New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable "RequestHeaderNames" -SelectorMatchOperator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="f05b9-109">Ez a parancs létrehoz egy új kivonási bejegyzést a RequestHeaderNames és a StartsWith nevű műveleti nevű változóhoz, az XYZ nevűt.</span><span class="sxs-lookup"><span data-stu-id="f05b9-109">This command creates a new exclusion-entry for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="f05b9-110">A program a kizárási bejegyzést $exclusionEntry menti.</span><span class="sxs-lookup"><span data-stu-id="f05b9-110">The exclusion entry is saved in $exclusionEntry.</span></span>

## <span data-ttu-id="f05b9-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f05b9-111">PARAMETERS</span></span>

### <span data-ttu-id="f05b9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f05b9-112">-DefaultProfile</span></span>
<span data-ttu-id="f05b9-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f05b9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f05b9-114">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="f05b9-114">-MatchVariable</span></span>
<span data-ttu-id="f05b9-115">A kizárni kívánt változó.</span><span class="sxs-lookup"><span data-stu-id="f05b9-115">The variable to be excluded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RequestHeaderNames, RequestCookieNames, RequestArgNames

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f05b9-116">-Választó</span><span class="sxs-lookup"><span data-stu-id="f05b9-116">-Selector</span></span>
<span data-ttu-id="f05b9-117">Ha a változó egy gyűjtemény, az operátor a gyűjteményben szereplő elemek meghatározására szolgál.</span><span class="sxs-lookup"><span data-stu-id="f05b9-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f05b9-118">-SelectorMatchOperator</span><span class="sxs-lookup"><span data-stu-id="f05b9-118">-SelectorMatchOperator</span></span>
<span data-ttu-id="f05b9-119">Ha a változó egy gyűjtemény, a választóval megadhatja, hogy a gyűjtemény mely elemei érvényesek.</span><span class="sxs-lookup"><span data-stu-id="f05b9-119">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Equals, Contains, StartsWith, EndsWith, EqualsAny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f05b9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f05b9-120">CommonParameters</span></span>
<span data-ttu-id="f05b9-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f05b9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f05b9-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f05b9-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f05b9-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f05b9-123">INPUTS</span></span>

### <span data-ttu-id="f05b9-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="f05b9-124">None</span></span>

## <span data-ttu-id="f05b9-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f05b9-125">OUTPUTS</span></span>

### <span data-ttu-id="f05b9-126">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="f05b9-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="f05b9-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f05b9-127">NOTES</span></span>

## <span data-ttu-id="f05b9-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f05b9-128">RELATED LINKS</span></span>
