---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 0b87119ccec521b85a210dc8685874bd4ba4b9ab
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841397"
---
# <span data-ttu-id="6f117-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="6f117-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="6f117-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6f117-102">SYNOPSIS</span></span>
<span data-ttu-id="6f117-103">Egy alkalmazás-átjáró SKU-ának létrehozása.</span><span class="sxs-lookup"><span data-stu-id="6f117-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="6f117-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6f117-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> -Capacity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f117-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6f117-105">DESCRIPTION</span></span>
<span data-ttu-id="6f117-106">A **New-AzApplicationGatewaySku** parancsmag létrehoz egy árfolyamdiagram-egységet (SKU) az Azure Application Gateway számára.</span><span class="sxs-lookup"><span data-stu-id="6f117-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="6f117-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6f117-107">EXAMPLES</span></span>

### <span data-ttu-id="6f117-108">1. példa: SKU létrehozása Azure Application Gateway-hez</span><span class="sxs-lookup"><span data-stu-id="6f117-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="6f117-109">Ezzel a paranccsal létrehoz egy Standard_Small nevű SKU-t egy Azure Application Gateway-nek, és az eredményt a $SKU nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="6f117-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="6f117-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6f117-110">PARAMETERS</span></span>

### <span data-ttu-id="6f117-111">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="6f117-111">-Capacity</span></span>
<span data-ttu-id="6f117-112">Az alkalmazás-átjáró példányainak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f117-112">Specifies the number of instances of an application gateway.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f117-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f117-113">-DefaultProfile</span></span>
<span data-ttu-id="6f117-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6f117-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f117-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6f117-115">-Name</span></span>
<span data-ttu-id="6f117-116">A SKU nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f117-116">Specifies the name of the SKU.</span></span>

<span data-ttu-id="6f117-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="6f117-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6f117-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="6f117-118">Standard_Small</span></span>
- <span data-ttu-id="6f117-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="6f117-119">Standard_Medium</span></span>
- <span data-ttu-id="6f117-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="6f117-120">Standard_Large</span></span>
- <span data-ttu-id="6f117-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="6f117-121">WAF_Medium</span></span>
- <span data-ttu-id="6f117-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="6f117-122">WAF_Large</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f117-123">-Tier (Tier)</span><span class="sxs-lookup"><span data-stu-id="6f117-123">-Tier</span></span>
<span data-ttu-id="6f117-124">Az SKU-típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f117-124">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="6f117-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="6f117-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6f117-126">Standard</span><span class="sxs-lookup"><span data-stu-id="6f117-126">Standard</span></span>
- <span data-ttu-id="6f117-127">WAF</span><span class="sxs-lookup"><span data-stu-id="6f117-127">WAF</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, WAF

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f117-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f117-128">CommonParameters</span></span>
<span data-ttu-id="6f117-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6f117-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f117-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f117-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f117-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f117-131">INPUTS</span></span>

### <span data-ttu-id="6f117-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6f117-132">System.String</span></span>

## <span data-ttu-id="6f117-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f117-133">OUTPUTS</span></span>

### <span data-ttu-id="6f117-134">Microsoft. Azure. commands. Network. models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="6f117-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="6f117-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6f117-135">NOTES</span></span>

## <span data-ttu-id="6f117-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6f117-136">RELATED LINKS</span></span>

[<span data-ttu-id="6f117-137">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="6f117-137">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="6f117-138">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="6f117-138">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


