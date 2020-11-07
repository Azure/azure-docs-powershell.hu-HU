---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: b10863cf5e4af09ded0e98dbed76aff37dc48677
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841757"
---
# <span data-ttu-id="a9f7f-101">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a9f7f-101">Get-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="a9f7f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a9f7f-102">SYNOPSIS</span></span>
<span data-ttu-id="a9f7f-103">A back-end-címkészlet egy alkalmazás átjárója számára.</span><span class="sxs-lookup"><span data-stu-id="a9f7f-103">Gets a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="a9f7f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a9f7f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9f7f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a9f7f-105">DESCRIPTION</span></span>

## <span data-ttu-id="a9f7f-106">Példák</span><span class="sxs-lookup"><span data-stu-id="a9f7f-106">EXAMPLES</span></span>

### <span data-ttu-id="a9f7f-107">Példa 1: meghatározott back-end Server-készlet beszerzése</span><span class="sxs-lookup"><span data-stu-id="a9f7f-107">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="a9f7f-108">Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a9f7f-108">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a9f7f-109">A második parancs a $AppGw nevű Pool01 társított back-end címkészletet kapja meg, és a $BackendPool változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a9f7f-109">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="a9f7f-110">2. példa: a back-end Server-készlet listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="a9f7f-110">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="a9f7f-111">Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a9f7f-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a9f7f-112">A második parancs a $AppGwhoz társított back-end-címkészlet listáját kapja, és a listát a $BackendPools változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a9f7f-112">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="a9f7f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a9f7f-113">PARAMETERS</span></span>

### <span data-ttu-id="a9f7f-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a9f7f-114">-ApplicationGateway</span></span>
<span data-ttu-id="a9f7f-115">A **Get-AzApplicationGatewayBackendAddressPool** parancsmag a back-end címkészletet adja az alkalmazás-átjárók számára.</span><span class="sxs-lookup"><span data-stu-id="a9f7f-115">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

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

### <span data-ttu-id="a9f7f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9f7f-116">-DefaultProfile</span></span>
<span data-ttu-id="a9f7f-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a9f7f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9f7f-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a9f7f-118">-Name</span></span>
<span data-ttu-id="a9f7f-119">Annak a végpontnak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="a9f7f-119">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a9f7f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9f7f-120">CommonParameters</span></span>
<span data-ttu-id="a9f7f-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a9f7f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9f7f-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9f7f-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9f7f-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9f7f-123">INPUTS</span></span>

### <span data-ttu-id="a9f7f-124">System. String</span><span class="sxs-lookup"><span data-stu-id="a9f7f-124">System.String</span></span>

## <span data-ttu-id="a9f7f-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9f7f-125">OUTPUTS</span></span>

### <span data-ttu-id="a9f7f-126">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a9f7f-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="a9f7f-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a9f7f-127">NOTES</span></span>

## <span data-ttu-id="a9f7f-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9f7f-128">RELATED LINKS</span></span>

[<span data-ttu-id="a9f7f-129">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a9f7f-129">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="a9f7f-130">Új – AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a9f7f-130">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="a9f7f-131">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a9f7f-131">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="a9f7f-132">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a9f7f-132">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


