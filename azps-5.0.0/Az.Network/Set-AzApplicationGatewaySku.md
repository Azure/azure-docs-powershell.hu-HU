---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySku.md
ms.openlocfilehash: bfaf9773582b201de8f6066a30a55c0fd5f5b7ac
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186063"
---
# <span data-ttu-id="98016-101">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="98016-101">Set-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="98016-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="98016-102">SYNOPSIS</span></span>
<span data-ttu-id="98016-103">Egy alkalmazás-átjáró SKU-ának módosítása.</span><span class="sxs-lookup"><span data-stu-id="98016-103">Modifies the SKU of an application gateway.</span></span>

## <span data-ttu-id="98016-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="98016-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 [-Capacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98016-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="98016-105">DESCRIPTION</span></span>
<span data-ttu-id="98016-106">A **set-AzApplicationGatewaySku** parancsmag az alkalmazás-átjárók készletezési egységét (SKU) módosítja.</span><span class="sxs-lookup"><span data-stu-id="98016-106">The **Set-AzApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="98016-107">Példák</span><span class="sxs-lookup"><span data-stu-id="98016-107">EXAMPLES</span></span>

### <span data-ttu-id="98016-108">Példa 1: az Application Gateway SKU frissítése</span><span class="sxs-lookup"><span data-stu-id="98016-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="98016-109">Az első parancs megkapja a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="98016-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="98016-110">A második parancs frissíti az alkalmazás-átjáró SKU-ának tartalmát.</span><span class="sxs-lookup"><span data-stu-id="98016-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="98016-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="98016-111">PARAMETERS</span></span>

### <span data-ttu-id="98016-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="98016-112">-ApplicationGateway</span></span>
<span data-ttu-id="98016-113">Azt az alkalmazásobjektum-objektumot adja meg, amelyhez ez a parancsmag társítja a SKU-t.</span><span class="sxs-lookup"><span data-stu-id="98016-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

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

### <span data-ttu-id="98016-114">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="98016-114">-Capacity</span></span>
<span data-ttu-id="98016-115">Az alkalmazás-átjáró példányának számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="98016-115">Specifies the instance count of the application gateway.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98016-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98016-116">-DefaultProfile</span></span>
<span data-ttu-id="98016-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="98016-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98016-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="98016-118">-Name</span></span>
<span data-ttu-id="98016-119">Az alkalmazás-átjáró nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="98016-119">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="98016-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="98016-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="98016-121">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="98016-121">Standard_Small</span></span>
- <span data-ttu-id="98016-122">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="98016-122">Standard_Medium</span></span>
- <span data-ttu-id="98016-123">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="98016-123">Standard_Large</span></span>
- <span data-ttu-id="98016-124">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="98016-124">WAF_Medium</span></span>
- <span data-ttu-id="98016-125">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="98016-125">WAF_Large</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large, Standard_v2, WAF_v2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98016-126">-Tier (Tier)</span><span class="sxs-lookup"><span data-stu-id="98016-126">-Tier</span></span>
<span data-ttu-id="98016-127">Az alkalmazás átjárójának a rétegét adja meg.</span><span class="sxs-lookup"><span data-stu-id="98016-127">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="98016-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="98016-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="98016-129">Standard</span><span class="sxs-lookup"><span data-stu-id="98016-129">Standard</span></span>
- <span data-ttu-id="98016-130">WAF</span><span class="sxs-lookup"><span data-stu-id="98016-130">WAF</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, WAF, Standard_v2, WAF_v2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98016-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98016-131">CommonParameters</span></span>
<span data-ttu-id="98016-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="98016-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98016-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98016-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98016-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="98016-134">INPUTS</span></span>

### <span data-ttu-id="98016-135">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="98016-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="98016-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98016-136">OUTPUTS</span></span>

### <span data-ttu-id="98016-137">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="98016-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="98016-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="98016-138">NOTES</span></span>

## <span data-ttu-id="98016-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98016-139">RELATED LINKS</span></span>

[<span data-ttu-id="98016-140">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="98016-140">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="98016-141">Új – AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="98016-141">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)


