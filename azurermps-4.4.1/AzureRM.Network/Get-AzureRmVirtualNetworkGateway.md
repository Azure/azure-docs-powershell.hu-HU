---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: ed57a1832e3581d4d49b285fa9e61c93b17be02c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497796"
---
# <span data-ttu-id="f5225-101">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f5225-101">Get-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="f5225-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f5225-102">SYNOPSIS</span></span>
<span data-ttu-id="f5225-103">Virtuális hálózati átjárót kap</span><span class="sxs-lookup"><span data-stu-id="f5225-103">Gets a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5225-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f5225-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5225-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f5225-105">DESCRIPTION</span></span>
<span data-ttu-id="f5225-106">A virtuális hálózati átjáró az az objektum, amely az Azure-átjárót jelképezi.</span><span class="sxs-lookup"><span data-stu-id="f5225-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="f5225-107">A **Get-AzureRmVirtualNetworkGateway** parancsmag az Azure-átjáró objektumát adja eredményül a név és az erőforrás csoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="f5225-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="f5225-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f5225-108">EXAMPLES</span></span>

### <span data-ttu-id="f5225-109">1: virtuális hálózati átjáró beszerzése</span><span class="sxs-lookup"><span data-stu-id="f5225-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="f5225-110">A virtuális hálózati átjáró objektumát adja eredményül, az "myRG" erőforráscsoporthoz tartozó "myGateway" néven.</span><span class="sxs-lookup"><span data-stu-id="f5225-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="f5225-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f5225-111">PARAMETERS</span></span>

### <span data-ttu-id="f5225-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f5225-112">-Name</span></span>
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

### <span data-ttu-id="f5225-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5225-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="f5225-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5225-114">-DefaultProfile</span></span>
<span data-ttu-id="f5225-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f5225-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5225-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5225-116">CommonParameters</span></span>
<span data-ttu-id="f5225-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f5225-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5225-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5225-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5225-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5225-119">INPUTS</span></span>

## <span data-ttu-id="f5225-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5225-120">OUTPUTS</span></span>

### <span data-ttu-id="f5225-121">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f5225-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="f5225-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f5225-122">NOTES</span></span>

## <span data-ttu-id="f5225-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f5225-123">RELATED LINKS</span></span>

