---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkavailableendpointservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: 79517dc748a0599fca588e18d18a9d1e41f5e7fa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356105"
---
# <span data-ttu-id="fff5f-101">Get-AzVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="fff5f-101">Get-AzVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="fff5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fff5f-102">SYNOPSIS</span></span>
<span data-ttu-id="fff5f-103">A helyhez elérhető végpontszolgáltatások listája.</span><span class="sxs-lookup"><span data-stu-id="fff5f-103">Lists available endpoint services for location.</span></span>

## <span data-ttu-id="fff5f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fff5f-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fff5f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fff5f-105">DESCRIPTION</span></span>
<span data-ttu-id="fff5f-106">Get-AzVirtualNetworkAvailableEndpointService a megadott helyen elérhető végpontszolgáltatásokat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="fff5f-106">Get-AzVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="fff5f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fff5f-107">EXAMPLES</span></span>

### <span data-ttu-id="fff5f-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="fff5f-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="fff5f-109">Elérhető végpontszolgáltatások a westus régióban.</span><span class="sxs-lookup"><span data-stu-id="fff5f-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="fff5f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fff5f-110">PARAMETERS</span></span>

### <span data-ttu-id="fff5f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fff5f-111">-DefaultProfile</span></span>
<span data-ttu-id="fff5f-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fff5f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fff5f-113">-Location</span><span class="sxs-lookup"><span data-stu-id="fff5f-113">-Location</span></span>
<span data-ttu-id="fff5f-114">A végpontszolgáltatások lekérésének helye.</span><span class="sxs-lookup"><span data-stu-id="fff5f-114">The location to retrieve the endpoint services from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fff5f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fff5f-115">CommonParameters</span></span>
<span data-ttu-id="fff5f-116">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fff5f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fff5f-117">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fff5f-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fff5f-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fff5f-118">INPUTS</span></span>

### <span data-ttu-id="fff5f-119">System.String</span><span class="sxs-lookup"><span data-stu-id="fff5f-119">System.String</span></span>

## <span data-ttu-id="fff5f-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fff5f-120">OUTPUTS</span></span>

### <span data-ttu-id="fff5f-121">Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult</span><span class="sxs-lookup"><span data-stu-id="fff5f-121">Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult</span></span>

## <span data-ttu-id="fff5f-122">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fff5f-122">NOTES</span></span>

## <span data-ttu-id="fff5f-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fff5f-123">RELATED LINKS</span></span>
