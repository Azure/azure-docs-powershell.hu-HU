---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azinterfaceendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzInterfaceEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzInterfaceEndpoint.md
ms.openlocfilehash: 55133225b380e16112301620a52f857fca50dc0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670563"
---
# <span data-ttu-id="d246e-101">Get-AzInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="d246e-101">Get-AzInterfaceEndpoint</span></span>

## <span data-ttu-id="d246e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d246e-102">SYNOPSIS</span></span>
<span data-ttu-id="d246e-103">A Get-AzInterfaceEndpoint parancsmag a felület végpontját kapja.</span><span class="sxs-lookup"><span data-stu-id="d246e-103">The Get-AzInterfaceEndpoint cmdlet gets a Interface Endpoint.</span></span>

## <span data-ttu-id="d246e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d246e-104">SYNTAX</span></span>

### <span data-ttu-id="d246e-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d246e-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzInterfaceEndpoint [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d246e-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d246e-106">GetByResourceIdParameterSet</span></span>
```
Get-AzInterfaceEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d246e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d246e-107">DESCRIPTION</span></span>
<span data-ttu-id="d246e-108">A **Get-AzInterfaceEndpoint** parancsmag a felület végpontját kapja.</span><span class="sxs-lookup"><span data-stu-id="d246e-108">The **Get-AzInterfaceEndpoint** cmdlet gets a Interface Endpoint.</span></span>

## <span data-ttu-id="d246e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d246e-109">EXAMPLES</span></span>

### <span data-ttu-id="d246e-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d246e-110">Example 1</span></span>
```
$interfaceendpoint = Get-AzInterfaceEndpoint -Name "InterfaceEndpoint1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d246e-111">Ez a parancs a InterfaceEndpoint1 nevű Interface végpontot kapja, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $interfaceendpoint változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d246e-111">This command gets the interface endpoint named InterfaceEndpoint1 that belongs to the resource group named ResourceGroup01 and stores it in the $interfaceendpoint variable.</span></span>

### <span data-ttu-id="d246e-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="d246e-112">Example 2</span></span>
```
$interfaceendpoint = Get-AzInterfaceEndpoint -ResourceId "/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10"
```

<span data-ttu-id="d246e-113">Ez a parancs beilleszti az interface végpontot a resourceId/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10, és a $interfaceendpoint változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d246e-113">This command gets the interface endpoint with resourceId /subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 and stores it in the $interfaceendpoint variable.</span></span>

### <span data-ttu-id="d246e-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="d246e-114">Example 3</span></span>
```
$interfaceendpoint = Get-AzInterfaceEndpoint -Name InterfaceEndpoint*
```

<span data-ttu-id="d246e-115">Ez a parancs a "InterfaceEndpoint" kezdetű kapcsolati végpontokat kapja meg</span><span class="sxs-lookup"><span data-stu-id="d246e-115">This command gets the interface endpoints that start with "InterfaceEndpoint"</span></span>

## <span data-ttu-id="d246e-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d246e-116">PARAMETERS</span></span>

### <span data-ttu-id="d246e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d246e-117">-DefaultProfile</span></span>
<span data-ttu-id="d246e-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d246e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d246e-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d246e-119">-Name</span></span>
<span data-ttu-id="d246e-120">A felület végpontjának neve</span><span class="sxs-lookup"><span data-stu-id="d246e-120">The name of the interface endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="d246e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d246e-121">-ResourceGroupName</span></span>
<span data-ttu-id="d246e-122">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="d246e-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="d246e-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d246e-123">-ResourceId</span></span>
<span data-ttu-id="d246e-124">A felület végpontjának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d246e-124">The ID of the interface endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d246e-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d246e-125">-Confirm</span></span>
<span data-ttu-id="d246e-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d246e-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d246e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d246e-127">-WhatIf</span></span>
<span data-ttu-id="d246e-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d246e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d246e-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d246e-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d246e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d246e-130">CommonParameters</span></span>
<span data-ttu-id="d246e-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d246e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d246e-132">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d246e-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d246e-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d246e-133">INPUTS</span></span>

### <span data-ttu-id="d246e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d246e-134">System.String</span></span>

## <span data-ttu-id="d246e-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d246e-135">OUTPUTS</span></span>

### <span data-ttu-id="d246e-136">Microsoft. Azure. commands. Network. models. PSInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="d246e-136">Microsoft.Azure.Commands.Network.Models.PSInterfaceEndpoint</span></span>

## <span data-ttu-id="d246e-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d246e-137">NOTES</span></span>

## <span data-ttu-id="d246e-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d246e-138">RELATED LINKS</span></span>
