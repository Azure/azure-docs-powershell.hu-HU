---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkavailableendpointservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: a1c28622a4bb3a43d9d91b2f991c402a3572a3f5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924769"
---
# <span data-ttu-id="8baa2-101">Get-AzVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="8baa2-101">Get-AzVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="8baa2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8baa2-102">SYNOPSIS</span></span>
<span data-ttu-id="8baa2-103">A helyhez elérhető végpontszolgáltatások listája.</span><span class="sxs-lookup"><span data-stu-id="8baa2-103">Lists available endpoint services for location.</span></span>

## <span data-ttu-id="8baa2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8baa2-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8baa2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8baa2-105">DESCRIPTION</span></span>
<span data-ttu-id="8baa2-106">Get-AzVirtualNetworkAvailableEndpointService a megadott helyen elérhető végpontszolgáltatásokat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="8baa2-106">Get-AzVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="8baa2-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8baa2-107">EXAMPLES</span></span>

### <span data-ttu-id="8baa2-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="8baa2-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="8baa2-109">Elérhető végpontszolgáltatások a westus régióban.</span><span class="sxs-lookup"><span data-stu-id="8baa2-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="8baa2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8baa2-110">PARAMETERS</span></span>

### <span data-ttu-id="8baa2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8baa2-111">-DefaultProfile</span></span>
<span data-ttu-id="8baa2-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8baa2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8baa2-113">-Location</span><span class="sxs-lookup"><span data-stu-id="8baa2-113">-Location</span></span>
<span data-ttu-id="8baa2-114">A végpontszolgáltatások lekérésének helye.</span><span class="sxs-lookup"><span data-stu-id="8baa2-114">The location to retrieve the endpoint services from.</span></span>

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

### <span data-ttu-id="8baa2-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8baa2-115">CommonParameters</span></span>
<span data-ttu-id="8baa2-116">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8baa2-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8baa2-117">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8baa2-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8baa2-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8baa2-118">INPUTS</span></span>

### <span data-ttu-id="8baa2-119">System.String</span><span class="sxs-lookup"><span data-stu-id="8baa2-119">System.String</span></span>

## <span data-ttu-id="8baa2-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8baa2-120">OUTPUTS</span></span>

### <span data-ttu-id="8baa2-121">Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult</span><span class="sxs-lookup"><span data-stu-id="8baa2-121">Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult</span></span>

## <span data-ttu-id="8baa2-122">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8baa2-122">NOTES</span></span>

## <span data-ttu-id="8baa2-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8baa2-123">RELATED LINKS</span></span>
