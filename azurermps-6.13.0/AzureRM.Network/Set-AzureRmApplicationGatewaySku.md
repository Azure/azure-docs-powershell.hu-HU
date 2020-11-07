---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: 487a3cd096f1d27852f4472d478977ac0cbe2ccc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680031"
---
# <span data-ttu-id="7ea6f-101">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="7ea6f-101">Set-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="7ea6f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7ea6f-102">SYNOPSIS</span></span>
<span data-ttu-id="7ea6f-103">Egy alkalmazás-átjáró SKU-ának módosítása.</span><span class="sxs-lookup"><span data-stu-id="7ea6f-103">Modifies the SKU of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ea6f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7ea6f-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 [-Capacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ea6f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7ea6f-105">DESCRIPTION</span></span>
<span data-ttu-id="7ea6f-106">A **set-AzureRmApplicationGatewaySku** parancsmag az alkalmazás-átjárók készletezési egységét (SKU) módosítja.</span><span class="sxs-lookup"><span data-stu-id="7ea6f-106">The **Set-AzureRmApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="7ea6f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7ea6f-107">EXAMPLES</span></span>

### <span data-ttu-id="7ea6f-108">Példa 1: az Application Gateway SKU frissítése</span><span class="sxs-lookup"><span data-stu-id="7ea6f-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="7ea6f-109">Az első parancs megkapja a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7ea6f-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7ea6f-110">A második parancs frissíti az alkalmazás-átjáró SKU-ának tartalmát.</span><span class="sxs-lookup"><span data-stu-id="7ea6f-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="7ea6f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7ea6f-111">PARAMETERS</span></span>

### <span data-ttu-id="7ea6f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ea6f-112">-ApplicationGateway</span></span>
<span data-ttu-id="7ea6f-113">Azt az alkalmazásobjektum-objektumot adja meg, amelyhez ez a parancsmag társítja a SKU-t.</span><span class="sxs-lookup"><span data-stu-id="7ea6f-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

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

### <span data-ttu-id="7ea6f-114">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="7ea6f-114">-Capacity</span></span>
<span data-ttu-id="7ea6f-115">Az alkalmazás-átjáró példányának számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7ea6f-115">Specifies the instance count of the application gateway.</span></span>

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

### <span data-ttu-id="7ea6f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ea6f-116">-DefaultProfile</span></span>
<span data-ttu-id="7ea6f-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7ea6f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ea6f-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7ea6f-118">-Name</span></span>
<span data-ttu-id="7ea6f-119">Az alkalmazás-átjáró nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7ea6f-119">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="7ea6f-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7ea6f-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7ea6f-121">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="7ea6f-121">Standard_Small</span></span>
- <span data-ttu-id="7ea6f-122">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="7ea6f-122">Standard_Medium</span></span>
- <span data-ttu-id="7ea6f-123">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="7ea6f-123">Standard_Large</span></span>
- <span data-ttu-id="7ea6f-124">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="7ea6f-124">WAF_Medium</span></span>
- <span data-ttu-id="7ea6f-125">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="7ea6f-125">WAF_Large</span></span>

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

### <span data-ttu-id="7ea6f-126">-Tier (Tier)</span><span class="sxs-lookup"><span data-stu-id="7ea6f-126">-Tier</span></span>
<span data-ttu-id="7ea6f-127">Az alkalmazás átjárójának a rétegét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7ea6f-127">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="7ea6f-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7ea6f-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7ea6f-129">Standard</span><span class="sxs-lookup"><span data-stu-id="7ea6f-129">Standard</span></span>
- <span data-ttu-id="7ea6f-130">WAF</span><span class="sxs-lookup"><span data-stu-id="7ea6f-130">WAF</span></span>

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

### <span data-ttu-id="7ea6f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ea6f-131">CommonParameters</span></span>
<span data-ttu-id="7ea6f-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7ea6f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ea6f-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ea6f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ea6f-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ea6f-134">INPUTS</span></span>

### <span data-ttu-id="7ea6f-135">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ea6f-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="7ea6f-136">Paraméterek: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7ea6f-136">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="7ea6f-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ea6f-137">OUTPUTS</span></span>

### <span data-ttu-id="7ea6f-138">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ea6f-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7ea6f-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7ea6f-139">NOTES</span></span>

## <span data-ttu-id="7ea6f-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ea6f-140">RELATED LINKS</span></span>

[<span data-ttu-id="7ea6f-141">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="7ea6f-141">Get-AzureRmApplicationGatewaySku</span></span>](./Get-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="7ea6f-142">Új – AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="7ea6f-142">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)


