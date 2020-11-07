---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 4b3acad1f0a9d5a516ee541f61bfee93fca532b8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670665"
---
# <span data-ttu-id="eada2-101">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="eada2-101">Get-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="eada2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eada2-102">SYNOPSIS</span></span>
<span data-ttu-id="eada2-103">A back-end-címkészlet egy alkalmazás átjárója számára.</span><span class="sxs-lookup"><span data-stu-id="eada2-103">Gets a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="eada2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eada2-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eada2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="eada2-105">DESCRIPTION</span></span>
<span data-ttu-id="eada2-106">A **Get-AzApplicationGatewayBackendAddressPool** parancsmag egy vagy több backend-címkészlet-konfigurációt kap egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="eada2-106">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets one or more backend address pool configurations from an application gateway.</span></span>

## <span data-ttu-id="eada2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="eada2-107">EXAMPLES</span></span>

### <span data-ttu-id="eada2-108">Példa 1: meghatározott back-end Server-készlet beszerzése</span><span class="sxs-lookup"><span data-stu-id="eada2-108">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="eada2-109">Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="eada2-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="eada2-110">A második parancs a $AppGw nevű Pool01 társított back-end címkészletet kapja meg, és a $BackendPool változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="eada2-110">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="eada2-111">2. példa: a back-end Server-készlet listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="eada2-111">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="eada2-112">Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="eada2-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="eada2-113">A második parancs a $AppGwhoz társított back-end-címkészlet listáját kapja, és a listát a $BackendPools változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="eada2-113">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="eada2-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eada2-114">PARAMETERS</span></span>

### <span data-ttu-id="eada2-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eada2-115">-ApplicationGateway</span></span>
<span data-ttu-id="eada2-116">A **Get-AzApplicationGatewayBackendAddressPool** parancsmag a back-end címkészletet adja az alkalmazás-átjárók számára.</span><span class="sxs-lookup"><span data-stu-id="eada2-116">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eada2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eada2-117">-DefaultProfile</span></span>
<span data-ttu-id="eada2-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eada2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eada2-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eada2-119">-Name</span></span>
<span data-ttu-id="eada2-120">Annak a végpontnak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="eada2-120">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eada2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eada2-121">CommonParameters</span></span>
<span data-ttu-id="eada2-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eada2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eada2-123">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="eada2-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eada2-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eada2-124">INPUTS</span></span>

### <span data-ttu-id="eada2-125">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eada2-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="eada2-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eada2-126">OUTPUTS</span></span>

### <span data-ttu-id="eada2-127">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="eada2-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="eada2-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eada2-128">NOTES</span></span>

## <span data-ttu-id="eada2-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eada2-129">RELATED LINKS</span></span>

[<span data-ttu-id="eada2-130">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="eada2-130">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="eada2-131">Új – AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="eada2-131">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="eada2-132">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="eada2-132">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="eada2-133">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="eada2-133">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


