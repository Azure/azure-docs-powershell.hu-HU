---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: af925c1de08a5a615f5435bb20377582fedc0089
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505740"
---
# <span data-ttu-id="6bf3e-101">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6bf3e-101">Get-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="6bf3e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6bf3e-102">SYNOPSIS</span></span>
<span data-ttu-id="6bf3e-103">Virtuális hálózati átjárót kap</span><span class="sxs-lookup"><span data-stu-id="6bf3e-103">Gets a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6bf3e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6bf3e-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6bf3e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6bf3e-105">DESCRIPTION</span></span>
<span data-ttu-id="6bf3e-106">A virtuális hálózati átjáró az az objektum, amely az Azure-átjárót jelképezi.</span><span class="sxs-lookup"><span data-stu-id="6bf3e-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="6bf3e-107">A **Get-AzureRmVirtualNetworkGateway** parancsmag az Azure-átjáró objektumát adja eredményül a név és az erőforrás csoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="6bf3e-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="6bf3e-108">Példák</span><span class="sxs-lookup"><span data-stu-id="6bf3e-108">EXAMPLES</span></span>

### <span data-ttu-id="6bf3e-109">1: virtuális hálózati átjáró beszerzése</span><span class="sxs-lookup"><span data-stu-id="6bf3e-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="6bf3e-110">A virtuális hálózati átjáró objektumát adja eredményül, az "myRG" erőforráscsoporthoz tartozó "myGateway" néven.</span><span class="sxs-lookup"><span data-stu-id="6bf3e-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="6bf3e-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6bf3e-111">PARAMETERS</span></span>

### <span data-ttu-id="6bf3e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bf3e-112">-DefaultProfile</span></span>
<span data-ttu-id="6bf3e-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6bf3e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bf3e-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6bf3e-114">-Name</span></span>
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

### <span data-ttu-id="6bf3e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bf3e-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="6bf3e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bf3e-116">CommonParameters</span></span>
<span data-ttu-id="6bf3e-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6bf3e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bf3e-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bf3e-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bf3e-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6bf3e-119">INPUTS</span></span>

### <span data-ttu-id="6bf3e-120">System. String</span><span class="sxs-lookup"><span data-stu-id="6bf3e-120">System.String</span></span>

## <span data-ttu-id="6bf3e-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6bf3e-121">OUTPUTS</span></span>

### <span data-ttu-id="6bf3e-122">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6bf3e-122">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="6bf3e-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6bf3e-123">NOTES</span></span>

## <span data-ttu-id="6bf3e-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6bf3e-124">RELATED LINKS</span></span>
