---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurerminterfaceendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmInterfaceEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmInterfaceEndpoint.md
ms.openlocfilehash: 8759546c9d7161f2bea139845c7d291c6d7832b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495955"
---
# <span data-ttu-id="187f1-101">Get-AzureRmInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="187f1-101">Get-AzureRmInterfaceEndpoint</span></span>

## <span data-ttu-id="187f1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="187f1-102">SYNOPSIS</span></span>
<span data-ttu-id="187f1-103">A Get-AzureRmInterfaceEndpoint parancsmag a felület végpontját kapja.</span><span class="sxs-lookup"><span data-stu-id="187f1-103">The Get-AzureRmInterfaceEndpoint cmdlet gets a Interface Endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="187f1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="187f1-104">SYNTAX</span></span>

### <span data-ttu-id="187f1-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="187f1-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzureRmInterfaceEndpoint [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="187f1-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="187f1-106">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmInterfaceEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="187f1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="187f1-107">DESCRIPTION</span></span>
<span data-ttu-id="187f1-108">A **Get-AzureRmInterfaceEndpoint** parancsmag a felület végpontját kapja.</span><span class="sxs-lookup"><span data-stu-id="187f1-108">The **Get-AzureRmInterfaceEndpoint** cmdlet gets a Interface Endpoint.</span></span>

## <span data-ttu-id="187f1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="187f1-109">EXAMPLES</span></span>

### <span data-ttu-id="187f1-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="187f1-110">Example 1</span></span>
```
$interfaceendpoint = Get-AzureRmInterfaceEndpoint -Name "InterfaceEndpoint1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="187f1-111">Ez a parancs a InterfaceEndpoint1 nevű Interface végpontot kapja, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $interfaceendpoint változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="187f1-111">This command gets the interface endpoint named InterfaceEndpoint1 that belongs to the resource group named ResourceGroup01 and stores it in the $interfaceendpoint variable.</span></span>

### <span data-ttu-id="187f1-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="187f1-112">Example 2</span></span>
```
$interfaceendpoint = Get-AzureRmInterfaceEndpoint -ResourceId "/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10"

```

<span data-ttu-id="187f1-113">Ez a parancs beilleszti az interface végpontot a resourceId/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10, és a $interfaceendpoint változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="187f1-113">This command gets the interface endpoint with resourceId  /subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 and stores it in the $interfaceendpoint variable.</span></span>


## <span data-ttu-id="187f1-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="187f1-114">PARAMETERS</span></span>

### <span data-ttu-id="187f1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="187f1-115">-DefaultProfile</span></span>
<span data-ttu-id="187f1-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="187f1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="187f1-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="187f1-117">-Name</span></span>
<span data-ttu-id="187f1-118">A felület végpontjának neve</span><span class="sxs-lookup"><span data-stu-id="187f1-118">The name of the interface endpoint</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="187f1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="187f1-119">-ResourceGroupName</span></span>
<span data-ttu-id="187f1-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="187f1-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="187f1-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="187f1-121">-ResourceId</span></span>
<span data-ttu-id="187f1-122">{{Fill ResourceId Description}}</span><span class="sxs-lookup"><span data-stu-id="187f1-122">{{Fill ResourceId Description}}</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="187f1-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="187f1-123">-Confirm</span></span>
<span data-ttu-id="187f1-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="187f1-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="187f1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="187f1-125">-WhatIf</span></span>
<span data-ttu-id="187f1-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="187f1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="187f1-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="187f1-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="187f1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="187f1-128">CommonParameters</span></span>
<span data-ttu-id="187f1-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="187f1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="187f1-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="187f1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="187f1-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="187f1-131">INPUTS</span></span>

### <span data-ttu-id="187f1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="187f1-132">System.String</span></span>


## <span data-ttu-id="187f1-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="187f1-133">OUTPUTS</span></span>

### <span data-ttu-id="187f1-134">Microsoft. Azure. commands. Network. models. PSInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="187f1-134">Microsoft.Azure.Commands.Network.Models.PSInterfaceEndpoint</span></span>


## <span data-ttu-id="187f1-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="187f1-135">NOTES</span></span>

## <span data-ttu-id="187f1-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="187f1-136">RELATED LINKS</span></span>
