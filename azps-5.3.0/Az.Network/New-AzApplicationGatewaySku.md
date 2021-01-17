---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 212ba438a701b9abbd2fd290f4fb0f867b551497
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466796"
---
# <span data-ttu-id="07f30-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="07f30-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="07f30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07f30-102">SYNOPSIS</span></span>
<span data-ttu-id="07f30-103">Termékváltozatot hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="07f30-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="07f30-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="07f30-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> [-Capacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07f30-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="07f30-105">DESCRIPTION</span></span>
<span data-ttu-id="07f30-106">A **New-AzApplicationGatewaySku** parancsmag létrehoz egy készletet (SKU) egy Azure-alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="07f30-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="07f30-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="07f30-107">EXAMPLES</span></span>

### <span data-ttu-id="07f30-108">1. példa: Termékváltozat létrehozása Azure-alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="07f30-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="07f30-109">Ez a parancs létrehoz egy Standard_Small nevű termékváltozatot egy Azure-alkalmazás-átjáróhoz, és az eredményt a következő nevű változóban $SKU.</span><span class="sxs-lookup"><span data-stu-id="07f30-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="07f30-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07f30-110">PARAMETERS</span></span>

### <span data-ttu-id="07f30-111">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="07f30-111">-Capacity</span></span>
<span data-ttu-id="07f30-112">Egy alkalmazás-átjáró példányainak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="07f30-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="07f30-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07f30-113">-DefaultProfile</span></span>
<span data-ttu-id="07f30-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="07f30-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07f30-115">-Name</span><span class="sxs-lookup"><span data-stu-id="07f30-115">-Name</span></span>
<span data-ttu-id="07f30-116">A termékváltozat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="07f30-116">Specifies the name of the SKU.</span></span>
<span data-ttu-id="07f30-117">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="07f30-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="07f30-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="07f30-118">Standard_Small</span></span>
- <span data-ttu-id="07f30-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="07f30-119">Standard_Medium</span></span>
- <span data-ttu-id="07f30-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="07f30-120">Standard_Large</span></span>
- <span data-ttu-id="07f30-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="07f30-121">WAF_Medium</span></span>
- <span data-ttu-id="07f30-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="07f30-122">WAF_Large</span></span>
- <span data-ttu-id="07f30-123">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="07f30-123">Standard_v2</span></span>
- <span data-ttu-id="07f30-124">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="07f30-124">WAF_v2</span></span>

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

### <span data-ttu-id="07f30-125">-Tier</span><span class="sxs-lookup"><span data-stu-id="07f30-125">-Tier</span></span>
<span data-ttu-id="07f30-126">A termékváltozat rétegét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="07f30-126">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="07f30-127">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="07f30-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="07f30-128">Normál</span><span class="sxs-lookup"><span data-stu-id="07f30-128">Standard</span></span>
- <span data-ttu-id="07f30-129">WAF</span><span class="sxs-lookup"><span data-stu-id="07f30-129">WAF</span></span>
- <span data-ttu-id="07f30-130">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="07f30-130">Standard_v2</span></span>
- <span data-ttu-id="07f30-131">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="07f30-131">WAF_v2</span></span>

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

### <span data-ttu-id="07f30-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07f30-132">CommonParameters</span></span>
<span data-ttu-id="07f30-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07f30-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07f30-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07f30-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07f30-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07f30-135">INPUTS</span></span>

### <span data-ttu-id="07f30-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="07f30-136">None</span></span>

## <span data-ttu-id="07f30-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07f30-137">OUTPUTS</span></span>

### <span data-ttu-id="07f30-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="07f30-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="07f30-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="07f30-139">NOTES</span></span>

## <span data-ttu-id="07f30-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07f30-140">RELATED LINKS</span></span>

[<span data-ttu-id="07f30-141">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="07f30-141">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="07f30-142">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="07f30-142">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


