---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermlocalnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 1a2a8aa8405be5dfc5275a07d253f06f1134e3e7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849613"
---
# <span data-ttu-id="d7542-101">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d7542-101">Get-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="d7542-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d7542-102">SYNOPSIS</span></span>
<span data-ttu-id="d7542-103">Helyi hálózati átjárót kap</span><span class="sxs-lookup"><span data-stu-id="d7542-103">Gets a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7542-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d7542-104">SYNTAX</span></span>

```
Get-AzureRmLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7542-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d7542-105">DESCRIPTION</span></span>
<span data-ttu-id="d7542-106">A helyi hálózat átjárója a helyszíni VPN-eszközt jelképező objektum.</span><span class="sxs-lookup"><span data-stu-id="d7542-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="d7542-107">A **Get-AzureRmLocalNetworkGateway** parancsmag a helyszíni átjáró nevét és az erőforráscsoport neve alapján adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="d7542-107">The **Get-AzureRmLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="d7542-108">Példák</span><span class="sxs-lookup"><span data-stu-id="d7542-108">EXAMPLES</span></span>

### <span data-ttu-id="d7542-109">1: helyi hálózati átjáró beszerzése</span><span class="sxs-lookup"><span data-stu-id="d7542-109">1: Get a Local Network Gateway</span></span>
```
Get-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="d7542-110">A helyi hálózati átjáró objektumát adja eredményül, az "myRG" erőforráscsoporthoz tartozó "myLocalGW" névvel</span><span class="sxs-lookup"><span data-stu-id="d7542-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="d7542-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d7542-111">PARAMETERS</span></span>

### <span data-ttu-id="d7542-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7542-112">-DefaultProfile</span></span>
<span data-ttu-id="d7542-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d7542-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7542-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d7542-114">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7542-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7542-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="d7542-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7542-116">CommonParameters</span></span>
<span data-ttu-id="d7542-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d7542-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7542-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7542-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7542-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7542-119">INPUTS</span></span>

## <span data-ttu-id="d7542-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7542-120">OUTPUTS</span></span>

### <span data-ttu-id="d7542-121">Microsoft. Azure. commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d7542-121">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="d7542-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d7542-122">NOTES</span></span>

## <span data-ttu-id="d7542-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7542-123">RELATED LINKS</span></span>

