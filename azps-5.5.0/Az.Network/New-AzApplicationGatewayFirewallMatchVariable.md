---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallmatchvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
ms.openlocfilehash: c3ff96a2c1d06fdfba5879244b058ef1a7845f40
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202963"
---
# <span data-ttu-id="0dbd7-101">New-AzApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="0dbd7-101">New-AzApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="0dbd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0dbd7-102">SYNOPSIS</span></span>
<span data-ttu-id="0dbd7-103">Egyező változót hoz létre a tűzfal állapotához.</span><span class="sxs-lookup"><span data-stu-id="0dbd7-103">Creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="0dbd7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0dbd7-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallMatchVariable -VariableName <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0dbd7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0dbd7-105">DESCRIPTION</span></span>
<span data-ttu-id="0dbd7-106">A **New-AzApplicationGatewayFirewallMatchVariable** létrehoz egy egyező változót a tűzfal állapotához.</span><span class="sxs-lookup"><span data-stu-id="0dbd7-106">The **New-AzApplicationGatewayFirewallMatchVariable** creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="0dbd7-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0dbd7-107">EXAMPLES</span></span>

### <span data-ttu-id="0dbd7-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="0dbd7-108">Example 1</span></span>
```powershell
PS C:\> $variable = New-AzApplicationGatewayFirewallMatchVariable -VariableName RequestHeaders -Selector Content-Length
```

<span data-ttu-id="0dbd7-109">A parancs létrehoz egy új egyezésváltozót a kérésfejlécek nevével, a választó pedig a Content-Length (Tartalom hossza) mező.</span><span class="sxs-lookup"><span data-stu-id="0dbd7-109">The command creates a new match variable with name of request headers and selector is Content-Length field.</span></span> <span data-ttu-id="0dbd7-110">Az új egyezésváltozót a rendszer a $variable.</span><span class="sxs-lookup"><span data-stu-id="0dbd7-110">The new match variable is saved in $variable.</span></span>

## <span data-ttu-id="0dbd7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0dbd7-111">PARAMETERS</span></span>

### <span data-ttu-id="0dbd7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dbd7-112">-DefaultProfile</span></span>
<span data-ttu-id="0dbd7-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0dbd7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0dbd7-114">-Választó</span><span class="sxs-lookup"><span data-stu-id="0dbd7-114">-Selector</span></span>
<span data-ttu-id="0dbd7-115">A matchVariable gyűjtemény mezőjét ismerteti.</span><span class="sxs-lookup"><span data-stu-id="0dbd7-115">Describes field of the matchVariable collection.</span></span>

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

### <span data-ttu-id="0dbd7-116">-VariableName</span><span class="sxs-lookup"><span data-stu-id="0dbd7-116">-VariableName</span></span>
<span data-ttu-id="0dbd7-117">Változó egyeztetése</span><span class="sxs-lookup"><span data-stu-id="0dbd7-117">Match Variable.</span></span>

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

### <span data-ttu-id="0dbd7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dbd7-118">CommonParameters</span></span>
<span data-ttu-id="0dbd7-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dbd7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dbd7-120">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dbd7-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dbd7-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0dbd7-121">INPUTS</span></span>

### <span data-ttu-id="0dbd7-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="0dbd7-122">None</span></span>

## <span data-ttu-id="0dbd7-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0dbd7-123">OUTPUTS</span></span>

### <span data-ttu-id="0dbd7-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="0dbd7-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="0dbd7-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0dbd7-125">NOTES</span></span>

## <span data-ttu-id="0dbd7-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0dbd7-126">RELATED LINKS</span></span>
