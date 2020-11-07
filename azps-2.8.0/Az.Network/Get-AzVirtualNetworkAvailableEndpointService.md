---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkavailableendpointservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: 2de970201456f941d8b35d40c569c41e114468c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837286"
---
# <span data-ttu-id="adbca-101">Get-AzVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="adbca-101">Get-AzVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="adbca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="adbca-102">SYNOPSIS</span></span>
<span data-ttu-id="adbca-103">A rendelkezésre álló végpont-szolgáltatások listája a helyhez.</span><span class="sxs-lookup"><span data-stu-id="adbca-103">Lists available endpoint services for location.</span></span>

## <span data-ttu-id="adbca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="adbca-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="adbca-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="adbca-105">DESCRIPTION</span></span>
<span data-ttu-id="adbca-106">A Get-AzVirtualNetworkAvailableEndpointService a megadott helyen elérhető végpont-szolgáltatásokat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="adbca-106">Get-AzVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="adbca-107">Példák</span><span class="sxs-lookup"><span data-stu-id="adbca-107">EXAMPLES</span></span>

### <span data-ttu-id="adbca-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="adbca-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="adbca-109">Elérhető végpont-szolgáltatásokat kap a westus régióban.</span><span class="sxs-lookup"><span data-stu-id="adbca-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="adbca-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="adbca-110">PARAMETERS</span></span>

### <span data-ttu-id="adbca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adbca-111">-DefaultProfile</span></span>
<span data-ttu-id="adbca-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="adbca-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="adbca-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="adbca-113">-Location</span></span>
<span data-ttu-id="adbca-114">A végponti szolgáltatások beolvasásának helye.</span><span class="sxs-lookup"><span data-stu-id="adbca-114">The location to retrieve the endpoint services from.</span></span>

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

### <span data-ttu-id="adbca-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adbca-115">CommonParameters</span></span>
<span data-ttu-id="adbca-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="adbca-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adbca-117">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="adbca-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adbca-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="adbca-118">INPUTS</span></span>

### <span data-ttu-id="adbca-119">System. String</span><span class="sxs-lookup"><span data-stu-id="adbca-119">System.String</span></span>

## <span data-ttu-id="adbca-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="adbca-120">OUTPUTS</span></span>

### <span data-ttu-id="adbca-121">Microsoft. Azure. commands. Network. models. PSEndpointServiceResult</span><span class="sxs-lookup"><span data-stu-id="adbca-121">Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult</span></span>

## <span data-ttu-id="adbca-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="adbca-122">NOTES</span></span>

## <span data-ttu-id="adbca-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="adbca-123">RELATED LINKS</span></span>
