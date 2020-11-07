---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: ECC5C079-C9A0-4159-A039-EE216897D686
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: c2a1a63abb18f5f47ed155f24e8ac73a7bae83ec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672925"
---
# <span data-ttu-id="c1420-101">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="c1420-101">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="c1420-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c1420-102">SYNOPSIS</span></span>
<span data-ttu-id="c1420-103">A kapcsolathoz használt megosztott kulcs megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="c1420-103">Displays the shared key used for the connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1420-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c1420-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayConnectionSharedKey [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1420-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c1420-105">DESCRIPTION</span></span>
<span data-ttu-id="c1420-106">A kapcsolathoz használt megosztott kulcs megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="c1420-106">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="c1420-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c1420-107">EXAMPLES</span></span>

### <span data-ttu-id="c1420-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c1420-108">Example 1</span></span>
```
Get-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name 1 -ResourceGroupName P2SVPNGateway
xxxxxx
```

## <span data-ttu-id="c1420-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c1420-109">PARAMETERS</span></span>

### <span data-ttu-id="c1420-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1420-110">-DefaultProfile</span></span>
<span data-ttu-id="c1420-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c1420-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1420-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c1420-112">-Name</span></span>
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

### <span data-ttu-id="c1420-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1420-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="c1420-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1420-114">CommonParameters</span></span>
<span data-ttu-id="c1420-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c1420-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1420-116">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1420-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1420-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1420-117">INPUTS</span></span>

### <span data-ttu-id="c1420-118">System. String</span><span class="sxs-lookup"><span data-stu-id="c1420-118">System.String</span></span>

## <span data-ttu-id="c1420-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1420-119">OUTPUTS</span></span>

### <span data-ttu-id="c1420-120">System. String</span><span class="sxs-lookup"><span data-stu-id="c1420-120">System.String</span></span>

## <span data-ttu-id="c1420-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c1420-121">NOTES</span></span>

## <span data-ttu-id="c1420-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1420-122">RELATED LINKS</span></span>
