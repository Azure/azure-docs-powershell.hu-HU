---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: 522516df5d4500f55a17e769140149f021501210
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680807"
---
# <span data-ttu-id="8d1ca-101">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8d1ca-101">Get-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="8d1ca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8d1ca-102">SYNOPSIS</span></span>
<span data-ttu-id="8d1ca-103">Helyi hálózati átjárót kap</span><span class="sxs-lookup"><span data-stu-id="8d1ca-103">Gets a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d1ca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8d1ca-104">SYNTAX</span></span>

```
Get-AzureRmLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d1ca-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8d1ca-105">DESCRIPTION</span></span>
<span data-ttu-id="8d1ca-106">A helyi hálózat átjárója a helyszíni VPN-eszközt jelképező objektum.</span><span class="sxs-lookup"><span data-stu-id="8d1ca-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="8d1ca-107">A **Get-AzureRmLocalNetworkGateway** parancsmag a helyszíni átjáró nevét és az erőforráscsoport neve alapján adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="8d1ca-107">The **Get-AzureRmLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="8d1ca-108">Példák</span><span class="sxs-lookup"><span data-stu-id="8d1ca-108">EXAMPLES</span></span>

### <span data-ttu-id="8d1ca-109">1: helyi hálózati átjáró beszerzése</span><span class="sxs-lookup"><span data-stu-id="8d1ca-109">1: Get a Local Network Gateway</span></span>
```
Get-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="8d1ca-110">A helyi hálózati átjáró objektumát adja eredményül, az "myRG" erőforráscsoporthoz tartozó "myLocalGW" névvel</span><span class="sxs-lookup"><span data-stu-id="8d1ca-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="8d1ca-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8d1ca-111">PARAMETERS</span></span>

### <span data-ttu-id="8d1ca-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d1ca-112">-DefaultProfile</span></span>
<span data-ttu-id="8d1ca-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8d1ca-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d1ca-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8d1ca-114">-Name</span></span>
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

### <span data-ttu-id="8d1ca-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d1ca-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="8d1ca-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d1ca-116">CommonParameters</span></span>
<span data-ttu-id="8d1ca-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8d1ca-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d1ca-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d1ca-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d1ca-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d1ca-119">INPUTS</span></span>

### <span data-ttu-id="8d1ca-120">System. String</span><span class="sxs-lookup"><span data-stu-id="8d1ca-120">System.String</span></span>

## <span data-ttu-id="8d1ca-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d1ca-121">OUTPUTS</span></span>

### <span data-ttu-id="8d1ca-122">Microsoft. Azure. commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8d1ca-122">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="8d1ca-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8d1ca-123">NOTES</span></span>

## <span data-ttu-id="8d1ca-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d1ca-124">RELATED LINKS</span></span>
