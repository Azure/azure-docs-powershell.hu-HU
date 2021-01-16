---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 212ba438a701b9abbd2fd290f4fb0f867b551497
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358845"
---
# <span data-ttu-id="32d00-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="32d00-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="32d00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32d00-102">SYNOPSIS</span></span>
<span data-ttu-id="32d00-103">Termékváltozatot hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="32d00-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="32d00-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="32d00-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> [-Capacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32d00-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="32d00-105">DESCRIPTION</span></span>
<span data-ttu-id="32d00-106">A **New-AzApplicationGatewaySku** parancsmag létrehoz egy készletet (SKU) egy Azure-alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="32d00-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="32d00-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="32d00-107">EXAMPLES</span></span>

### <span data-ttu-id="32d00-108">1. példa: Termékváltozat létrehozása Azure-alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="32d00-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="32d00-109">Ez a parancs létrehoz egy Standard_Small nevű termékváltozatot egy Azure-alkalmazás-átjáróhoz, és az eredményt a következő nevű változóban $SKU.</span><span class="sxs-lookup"><span data-stu-id="32d00-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="32d00-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32d00-110">PARAMETERS</span></span>

### <span data-ttu-id="32d00-111">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="32d00-111">-Capacity</span></span>
<span data-ttu-id="32d00-112">Egy alkalmazás-átjáró példányainak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="32d00-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="32d00-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32d00-113">-DefaultProfile</span></span>
<span data-ttu-id="32d00-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="32d00-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32d00-115">-Name</span><span class="sxs-lookup"><span data-stu-id="32d00-115">-Name</span></span>
<span data-ttu-id="32d00-116">A termékváltozat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="32d00-116">Specifies the name of the SKU.</span></span>
<span data-ttu-id="32d00-117">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="32d00-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="32d00-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="32d00-118">Standard_Small</span></span>
- <span data-ttu-id="32d00-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="32d00-119">Standard_Medium</span></span>
- <span data-ttu-id="32d00-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="32d00-120">Standard_Large</span></span>
- <span data-ttu-id="32d00-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="32d00-121">WAF_Medium</span></span>
- <span data-ttu-id="32d00-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="32d00-122">WAF_Large</span></span>
- <span data-ttu-id="32d00-123">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="32d00-123">Standard_v2</span></span>
- <span data-ttu-id="32d00-124">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="32d00-124">WAF_v2</span></span>

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

### <span data-ttu-id="32d00-125">-Tier</span><span class="sxs-lookup"><span data-stu-id="32d00-125">-Tier</span></span>
<span data-ttu-id="32d00-126">A termékváltozat rétegét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="32d00-126">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="32d00-127">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="32d00-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="32d00-128">Normál</span><span class="sxs-lookup"><span data-stu-id="32d00-128">Standard</span></span>
- <span data-ttu-id="32d00-129">WAF</span><span class="sxs-lookup"><span data-stu-id="32d00-129">WAF</span></span>
- <span data-ttu-id="32d00-130">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="32d00-130">Standard_v2</span></span>
- <span data-ttu-id="32d00-131">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="32d00-131">WAF_v2</span></span>

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

### <span data-ttu-id="32d00-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32d00-132">CommonParameters</span></span>
<span data-ttu-id="32d00-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32d00-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32d00-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32d00-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32d00-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="32d00-135">INPUTS</span></span>

### <span data-ttu-id="32d00-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="32d00-136">None</span></span>

## <span data-ttu-id="32d00-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="32d00-137">OUTPUTS</span></span>

### <span data-ttu-id="32d00-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="32d00-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="32d00-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="32d00-139">NOTES</span></span>

## <span data-ttu-id="32d00-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="32d00-140">RELATED LINKS</span></span>

[<span data-ttu-id="32d00-141">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="32d00-141">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="32d00-142">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="32d00-142">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


