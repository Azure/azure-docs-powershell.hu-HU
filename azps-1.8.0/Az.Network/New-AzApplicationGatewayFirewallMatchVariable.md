---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallmatchvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
ms.openlocfilehash: 05a1929f79799be8006ae82c4948dc0a81839040
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670414"
---
# <span data-ttu-id="9c389-101">New-AzApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="9c389-101">New-AzApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="9c389-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9c389-102">SYNOPSIS</span></span>
<span data-ttu-id="9c389-103">Egyeztető változót hoz létre a tűzfal feltételéhez.</span><span class="sxs-lookup"><span data-stu-id="9c389-103">Creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="9c389-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9c389-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallMatchVariable -VariableName <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c389-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9c389-105">DESCRIPTION</span></span>
<span data-ttu-id="9c389-106">A **New-AzApplicationGatewayFirewallMatchVariable** létrehoz egy egyeztetési változót a tűzfal feltételéhez.</span><span class="sxs-lookup"><span data-stu-id="9c389-106">The **New-AzApplicationGatewayFirewallMatchVariable** creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="9c389-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9c389-107">EXAMPLES</span></span>

### <span data-ttu-id="9c389-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9c389-108">Example 1</span></span>
```powershell
PS C:\> $variable = New-AzureRmApplicationGatewayFirewallMatchVariable -VariableName RequestHeaders -Selector Content-Length
```

<span data-ttu-id="9c389-109">A parancs új egyeztetési változót hoz létre a kérés fejlécek és a választó név mezővel.</span><span class="sxs-lookup"><span data-stu-id="9c389-109">The command creates a new match variable with name of request headers and selector is Content-Length field.</span></span> <span data-ttu-id="9c389-110">Az új egyeztetési változót a program a $variableba menti.</span><span class="sxs-lookup"><span data-stu-id="9c389-110">The new match variable is saved in $variable.</span></span>

## <span data-ttu-id="9c389-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9c389-111">PARAMETERS</span></span>

### <span data-ttu-id="9c389-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c389-112">-DefaultProfile</span></span>
<span data-ttu-id="9c389-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9c389-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c389-114">-Választó</span><span class="sxs-lookup"><span data-stu-id="9c389-114">-Selector</span></span>
<span data-ttu-id="9c389-115">Ez a cikk a matchVariable gyűjtemény mezőjét mutatja be.</span><span class="sxs-lookup"><span data-stu-id="9c389-115">Describes field of the matchVariable collection.</span></span>

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

### <span data-ttu-id="9c389-116">-VariableName</span><span class="sxs-lookup"><span data-stu-id="9c389-116">-VariableName</span></span>
<span data-ttu-id="9c389-117">Egyezés változó</span><span class="sxs-lookup"><span data-stu-id="9c389-117">Match Variable.</span></span>

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

### <span data-ttu-id="9c389-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c389-118">CommonParameters</span></span>
<span data-ttu-id="9c389-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9c389-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c389-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c389-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c389-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c389-121">INPUTS</span></span>

### <span data-ttu-id="9c389-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="9c389-122">None</span></span>

## <span data-ttu-id="9c389-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c389-123">OUTPUTS</span></span>

### <span data-ttu-id="9c389-124">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="9c389-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="9c389-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9c389-125">NOTES</span></span>

## <span data-ttu-id="9c389-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9c389-126">RELATED LINKS</span></span>
