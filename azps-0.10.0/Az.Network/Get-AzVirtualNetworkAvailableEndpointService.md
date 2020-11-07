---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkavailableendpointservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: bcd4ba14a14fdacdcdaa0ea85ec8059d2639bdc6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841525"
---
# <span data-ttu-id="d24cd-101">Get-AzVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="d24cd-101">Get-AzVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="d24cd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d24cd-102">SYNOPSIS</span></span>
<span data-ttu-id="d24cd-103">A rendelkezésre álló végpont-szolgáltatások listája a helyhez.</span><span class="sxs-lookup"><span data-stu-id="d24cd-103">Lists available endpoint services for location.</span></span>

## <span data-ttu-id="d24cd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d24cd-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d24cd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d24cd-105">DESCRIPTION</span></span>
<span data-ttu-id="d24cd-106">A Get-AzVirtualNetworkAvailableEndpointService a megadott helyen elérhető végpont-szolgáltatásokat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="d24cd-106">Get-AzVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="d24cd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d24cd-107">EXAMPLES</span></span>

### <span data-ttu-id="d24cd-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d24cd-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="d24cd-109">Elérhető végpont-szolgáltatásokat kap a westus régióban.</span><span class="sxs-lookup"><span data-stu-id="d24cd-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="d24cd-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d24cd-110">PARAMETERS</span></span>

### <span data-ttu-id="d24cd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d24cd-111">-DefaultProfile</span></span>
<span data-ttu-id="d24cd-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d24cd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24cd-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="d24cd-113">-Location</span></span>
<span data-ttu-id="d24cd-114">A végponti szolgáltatások beolvasásának helye.</span><span class="sxs-lookup"><span data-stu-id="d24cd-114">The location to retrieve the endpoint services from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d24cd-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d24cd-115">CommonParameters</span></span>
<span data-ttu-id="d24cd-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d24cd-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d24cd-117">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d24cd-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d24cd-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d24cd-118">INPUTS</span></span>

### <span data-ttu-id="d24cd-119">System. String</span><span class="sxs-lookup"><span data-stu-id="d24cd-119">System.String</span></span>

## <span data-ttu-id="d24cd-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d24cd-120">OUTPUTS</span></span>

### <span data-ttu-id="d24cd-121">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. models. PSEndpointServiceResult, Microsoft. Azure. commands. Network, Version = 4.2.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d24cd-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult, Microsoft.Azure.Commands.Network, Version=4.2.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d24cd-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d24cd-122">NOTES</span></span>

## <span data-ttu-id="d24cd-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d24cd-123">RELATED LINKS</span></span>

