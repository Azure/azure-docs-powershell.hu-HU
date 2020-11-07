---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkavailableendpointservice
schema: 2.0.0
ms.openlocfilehash: ed33d1a683e10e0e39d0b722dec92b7f7ba11254
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848773"
---
# <span data-ttu-id="3c81b-101">Get-AzureRmVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="3c81b-101">Get-AzureRmVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="3c81b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3c81b-102">SYNOPSIS</span></span>
<span data-ttu-id="3c81b-103">A rendelkezésre álló végpont-szolgáltatások listája a helyhez.</span><span class="sxs-lookup"><span data-stu-id="3c81b-103">Lists available endpoint services for location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c81b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3c81b-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c81b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3c81b-105">DESCRIPTION</span></span>
<span data-ttu-id="3c81b-106">A Get-AzureRmVirtualNetworkAvailableEndpointService a megadott helyen elérhető végpont-szolgáltatásokat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="3c81b-106">Get-AzureRmVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="3c81b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3c81b-107">EXAMPLES</span></span>

### <span data-ttu-id="3c81b-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3c81b-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="3c81b-109">Elérhető végpont-szolgáltatásokat kap a westus régióban.</span><span class="sxs-lookup"><span data-stu-id="3c81b-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="3c81b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3c81b-110">PARAMETERS</span></span>

### <span data-ttu-id="3c81b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c81b-111">-DefaultProfile</span></span>
<span data-ttu-id="3c81b-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3c81b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c81b-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="3c81b-113">-Location</span></span>
<span data-ttu-id="3c81b-114">A végponti szolgáltatások beolvasásának helye.</span><span class="sxs-lookup"><span data-stu-id="3c81b-114">The location to retrieve the endpoint services from.</span></span>

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

### <span data-ttu-id="3c81b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c81b-115">CommonParameters</span></span>
<span data-ttu-id="3c81b-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3c81b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c81b-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c81b-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c81b-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c81b-118">INPUTS</span></span>

### <span data-ttu-id="3c81b-119">System. String</span><span class="sxs-lookup"><span data-stu-id="3c81b-119">System.String</span></span>

## <span data-ttu-id="3c81b-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c81b-120">OUTPUTS</span></span>

### <span data-ttu-id="3c81b-121">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. models. PSEndpointServiceResult, Microsoft. Azure. commands. Network, Version = 4.2.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="3c81b-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult, Microsoft.Azure.Commands.Network, Version=4.2.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="3c81b-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3c81b-122">NOTES</span></span>

## <span data-ttu-id="3c81b-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c81b-123">RELATED LINKS</span></span>

