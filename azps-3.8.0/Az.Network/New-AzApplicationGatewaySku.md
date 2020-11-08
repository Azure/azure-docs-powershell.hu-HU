---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 212ba438a701b9abbd2fd290f4fb0f867b551497
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014775"
---
# <span data-ttu-id="e6b56-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e6b56-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="e6b56-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e6b56-102">SYNOPSIS</span></span>
<span data-ttu-id="e6b56-103">Egy alkalmazás-átjáró SKU-ának létrehozása.</span><span class="sxs-lookup"><span data-stu-id="e6b56-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="e6b56-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e6b56-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> [-Capacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6b56-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e6b56-105">DESCRIPTION</span></span>
<span data-ttu-id="e6b56-106">A **New-AzApplicationGatewaySku** parancsmag létrehoz egy árfolyamdiagram-egységet (SKU) az Azure Application Gateway számára.</span><span class="sxs-lookup"><span data-stu-id="e6b56-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="e6b56-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e6b56-107">EXAMPLES</span></span>

### <span data-ttu-id="e6b56-108">1. példa: SKU létrehozása Azure Application Gateway-hez</span><span class="sxs-lookup"><span data-stu-id="e6b56-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="e6b56-109">Ezzel a paranccsal létrehoz egy Standard_Small nevű SKU-t egy Azure Application Gateway-nek, és az eredményt a $SKU nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e6b56-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="e6b56-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e6b56-110">PARAMETERS</span></span>

### <span data-ttu-id="e6b56-111">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="e6b56-111">-Capacity</span></span>
<span data-ttu-id="e6b56-112">Az alkalmazás-átjáró példányainak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e6b56-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="e6b56-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6b56-113">-DefaultProfile</span></span>
<span data-ttu-id="e6b56-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6b56-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6b56-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e6b56-115">-Name</span></span>
<span data-ttu-id="e6b56-116">A SKU nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e6b56-116">Specifies the name of the SKU.</span></span>
<span data-ttu-id="e6b56-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e6b56-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e6b56-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="e6b56-118">Standard_Small</span></span>
- <span data-ttu-id="e6b56-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="e6b56-119">Standard_Medium</span></span>
- <span data-ttu-id="e6b56-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="e6b56-120">Standard_Large</span></span>
- <span data-ttu-id="e6b56-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="e6b56-121">WAF_Medium</span></span>
- <span data-ttu-id="e6b56-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="e6b56-122">WAF_Large</span></span>
- <span data-ttu-id="e6b56-123">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="e6b56-123">Standard_v2</span></span>
- <span data-ttu-id="e6b56-124">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="e6b56-124">WAF_v2</span></span>

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

### <span data-ttu-id="e6b56-125">-Tier (Tier)</span><span class="sxs-lookup"><span data-stu-id="e6b56-125">-Tier</span></span>
<span data-ttu-id="e6b56-126">Az SKU-típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="e6b56-126">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="e6b56-127">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e6b56-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e6b56-128">Standard</span><span class="sxs-lookup"><span data-stu-id="e6b56-128">Standard</span></span>
- <span data-ttu-id="e6b56-129">WAF</span><span class="sxs-lookup"><span data-stu-id="e6b56-129">WAF</span></span>
- <span data-ttu-id="e6b56-130">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="e6b56-130">Standard_v2</span></span>
- <span data-ttu-id="e6b56-131">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="e6b56-131">WAF_v2</span></span>

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

### <span data-ttu-id="e6b56-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6b56-132">CommonParameters</span></span>
<span data-ttu-id="e6b56-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e6b56-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6b56-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6b56-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6b56-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6b56-135">INPUTS</span></span>

### <span data-ttu-id="e6b56-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="e6b56-136">None</span></span>

## <span data-ttu-id="e6b56-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6b56-137">OUTPUTS</span></span>

### <span data-ttu-id="e6b56-138">Microsoft. Azure. commands. Network. models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e6b56-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="e6b56-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e6b56-139">NOTES</span></span>

## <span data-ttu-id="e6b56-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6b56-140">RELATED LINKS</span></span>

[<span data-ttu-id="e6b56-141">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e6b56-141">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="e6b56-142">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e6b56-142">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


