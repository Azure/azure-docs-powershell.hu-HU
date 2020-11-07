---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
ms.openlocfilehash: 4ce1f2d1c388b531ee960688ba8296ef1632ac25
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849249"
---
# <span data-ttu-id="d26e2-101">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d26e2-101">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="d26e2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d26e2-102">SYNOPSIS</span></span>
<span data-ttu-id="d26e2-103">A back-end-címkészlet egy alkalmazás átjárója számára.</span><span class="sxs-lookup"><span data-stu-id="d26e2-103">Gets a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d26e2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d26e2-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d26e2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d26e2-105">DESCRIPTION</span></span>

## <span data-ttu-id="d26e2-106">Példák</span><span class="sxs-lookup"><span data-stu-id="d26e2-106">EXAMPLES</span></span>

### <span data-ttu-id="d26e2-107">Példa 1: meghatározott back-end Server-készlet beszerzése</span><span class="sxs-lookup"><span data-stu-id="d26e2-107">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="d26e2-108">Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d26e2-108">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d26e2-109">A második parancs a $AppGw nevű Pool01 társított back-end címkészletet kapja meg, és a $BackendPool változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d26e2-109">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="d26e2-110">2. példa: a back-end Server-készlet listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="d26e2-110">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="d26e2-111">Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d26e2-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d26e2-112">A második parancs a $AppGwhoz társított back-end-címkészlet listáját kapja, és a listát a $BackendPools változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d26e2-112">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="d26e2-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d26e2-113">PARAMETERS</span></span>

### <span data-ttu-id="d26e2-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d26e2-114">-ApplicationGateway</span></span>
<span data-ttu-id="d26e2-115">A **Get-AzureRmApplicationGatewayBackendAddressPool** parancsmag a back-end címkészletet adja az alkalmazás-átjárók számára.</span><span class="sxs-lookup"><span data-stu-id="d26e2-115">The **Get-AzureRmApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d26e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d26e2-116">-DefaultProfile</span></span>
<span data-ttu-id="d26e2-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d26e2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d26e2-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d26e2-118">-Name</span></span>
<span data-ttu-id="d26e2-119">Annak a végpontnak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="d26e2-119">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d26e2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d26e2-120">CommonParameters</span></span>
<span data-ttu-id="d26e2-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d26e2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d26e2-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d26e2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d26e2-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d26e2-123">INPUTS</span></span>

### <span data-ttu-id="d26e2-124">System. String</span><span class="sxs-lookup"><span data-stu-id="d26e2-124">System.String</span></span>

## <span data-ttu-id="d26e2-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d26e2-125">OUTPUTS</span></span>

### <span data-ttu-id="d26e2-126">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d26e2-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="d26e2-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d26e2-127">NOTES</span></span>

## <span data-ttu-id="d26e2-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d26e2-128">RELATED LINKS</span></span>

[<span data-ttu-id="d26e2-129">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d26e2-129">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="d26e2-130">Új – AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d26e2-130">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="d26e2-131">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d26e2-131">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="d26e2-132">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d26e2-132">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


