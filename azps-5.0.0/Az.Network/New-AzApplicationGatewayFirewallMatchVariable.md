---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallmatchvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
ms.openlocfilehash: c3ff96a2c1d06fdfba5879244b058ef1a7845f40
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301985"
---
# <span data-ttu-id="3f18a-101">New-AzApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="3f18a-101">New-AzApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="3f18a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3f18a-102">SYNOPSIS</span></span>
<span data-ttu-id="3f18a-103">Egyeztető változót hoz létre a tűzfal feltételéhez.</span><span class="sxs-lookup"><span data-stu-id="3f18a-103">Creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="3f18a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3f18a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallMatchVariable -VariableName <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f18a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3f18a-105">DESCRIPTION</span></span>
<span data-ttu-id="3f18a-106">A **New-AzApplicationGatewayFirewallMatchVariable** létrehoz egy egyeztetési változót a tűzfal feltételéhez.</span><span class="sxs-lookup"><span data-stu-id="3f18a-106">The **New-AzApplicationGatewayFirewallMatchVariable** creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="3f18a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3f18a-107">EXAMPLES</span></span>

### <span data-ttu-id="3f18a-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3f18a-108">Example 1</span></span>
```powershell
PS C:\> $variable = New-AzApplicationGatewayFirewallMatchVariable -VariableName RequestHeaders -Selector Content-Length
```

<span data-ttu-id="3f18a-109">A parancs új egyeztetési változót hoz létre a kérés fejlécek és a választó név mezővel.</span><span class="sxs-lookup"><span data-stu-id="3f18a-109">The command creates a new match variable with name of request headers and selector is Content-Length field.</span></span> <span data-ttu-id="3f18a-110">Az új egyeztetési változót a program a $variableba menti.</span><span class="sxs-lookup"><span data-stu-id="3f18a-110">The new match variable is saved in $variable.</span></span>

## <span data-ttu-id="3f18a-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3f18a-111">PARAMETERS</span></span>

### <span data-ttu-id="3f18a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f18a-112">-DefaultProfile</span></span>
<span data-ttu-id="3f18a-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3f18a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f18a-114">-Választó</span><span class="sxs-lookup"><span data-stu-id="3f18a-114">-Selector</span></span>
<span data-ttu-id="3f18a-115">Ez a cikk a matchVariable gyűjtemény mezőjét mutatja be.</span><span class="sxs-lookup"><span data-stu-id="3f18a-115">Describes field of the matchVariable collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f18a-116">-VariableName</span><span class="sxs-lookup"><span data-stu-id="3f18a-116">-VariableName</span></span>
<span data-ttu-id="3f18a-117">Egyezés változó</span><span class="sxs-lookup"><span data-stu-id="3f18a-117">Match Variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestHeaders, RequestBody, RequestCookies

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f18a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f18a-118">CommonParameters</span></span>
<span data-ttu-id="3f18a-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3f18a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f18a-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f18a-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f18a-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f18a-121">INPUTS</span></span>

### <span data-ttu-id="3f18a-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="3f18a-122">None</span></span>

## <span data-ttu-id="3f18a-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f18a-123">OUTPUTS</span></span>

### <span data-ttu-id="3f18a-124">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="3f18a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="3f18a-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3f18a-125">NOTES</span></span>

## <span data-ttu-id="3f18a-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f18a-126">RELATED LINKS</span></span>
