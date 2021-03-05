---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySku.md
ms.openlocfilehash: d8b7e4280ae9c73486fd5a62fe866c2241cb16a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003446"
---
# <span data-ttu-id="66d4c-101">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="66d4c-101">Set-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="66d4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66d4c-102">SYNOPSIS</span></span>
<span data-ttu-id="66d4c-103">Módosítja egy alkalmazás-átjáró termékváltozatát.</span><span class="sxs-lookup"><span data-stu-id="66d4c-103">Modifies the SKU of an application gateway.</span></span>

## <span data-ttu-id="66d4c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="66d4c-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 [-Capacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66d4c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="66d4c-105">DESCRIPTION</span></span>
<span data-ttu-id="66d4c-106">A **Set-AzApplicationGatewaySku** parancsmag módosítja egy alkalmazás-átjáró készlet-készletegységét (SKU).</span><span class="sxs-lookup"><span data-stu-id="66d4c-106">The **Set-AzApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="66d4c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="66d4c-107">EXAMPLES</span></span>

### <span data-ttu-id="66d4c-108">1. példa: Az alkalmazás-átjáró termékváltozatának frissítése</span><span class="sxs-lookup"><span data-stu-id="66d4c-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="66d4c-109">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót kapja meg, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a helyi $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="66d4c-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="66d4c-110">A második parancs frissíti az alkalmazás átjáró termékváltozatát.</span><span class="sxs-lookup"><span data-stu-id="66d4c-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="66d4c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66d4c-111">PARAMETERS</span></span>

### <span data-ttu-id="66d4c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="66d4c-112">-ApplicationGateway</span></span>
<span data-ttu-id="66d4c-113">Azt az alkalmazás-átjáróobjektumot adja meg, amellyel a parancsmag társítja a termékváltozatot.</span><span class="sxs-lookup"><span data-stu-id="66d4c-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

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

### <span data-ttu-id="66d4c-114">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="66d4c-114">-Capacity</span></span>
<span data-ttu-id="66d4c-115">Az alkalmazás átjáró példányszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="66d4c-115">Specifies the instance count of the application gateway.</span></span>

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

### <span data-ttu-id="66d4c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66d4c-116">-DefaultProfile</span></span>
<span data-ttu-id="66d4c-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="66d4c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66d4c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="66d4c-118">-Name</span></span>
<span data-ttu-id="66d4c-119">Az alkalmazás-átjáró nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="66d4c-119">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="66d4c-120">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="66d4c-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="66d4c-121">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="66d4c-121">Standard_Small</span></span>
- <span data-ttu-id="66d4c-122">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="66d4c-122">Standard_Medium</span></span>
- <span data-ttu-id="66d4c-123">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="66d4c-123">Standard_Large</span></span>
- <span data-ttu-id="66d4c-124">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="66d4c-124">WAF_Medium</span></span>
- <span data-ttu-id="66d4c-125">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="66d4c-125">WAF_Large</span></span>

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

### <span data-ttu-id="66d4c-126">-Tier</span><span class="sxs-lookup"><span data-stu-id="66d4c-126">-Tier</span></span>
<span data-ttu-id="66d4c-127">Az alkalmazás-átjáró rétegét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="66d4c-127">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="66d4c-128">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="66d4c-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="66d4c-129">Normál</span><span class="sxs-lookup"><span data-stu-id="66d4c-129">Standard</span></span>
- <span data-ttu-id="66d4c-130">WAF</span><span class="sxs-lookup"><span data-stu-id="66d4c-130">WAF</span></span>

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

### <span data-ttu-id="66d4c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66d4c-131">CommonParameters</span></span>
<span data-ttu-id="66d4c-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66d4c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66d4c-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66d4c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66d4c-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="66d4c-134">INPUTS</span></span>

### <span data-ttu-id="66d4c-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="66d4c-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="66d4c-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66d4c-136">OUTPUTS</span></span>

### <span data-ttu-id="66d4c-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="66d4c-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="66d4c-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="66d4c-138">NOTES</span></span>

## <span data-ttu-id="66d4c-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66d4c-139">RELATED LINKS</span></span>

[<span data-ttu-id="66d4c-140">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="66d4c-140">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="66d4c-141">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="66d4c-141">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)


