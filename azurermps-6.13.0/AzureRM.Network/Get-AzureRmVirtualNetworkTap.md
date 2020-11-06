---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: ff9ed8220cf2b30f2e652e207cb4d63db969a8dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495072"
---
# <span data-ttu-id="ff4d1-101">Get-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="ff4d1-101">Get-AzureRmVirtualNetworkTap</span></span>

## <span data-ttu-id="ff4d1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ff4d1-102">SYNOPSIS</span></span>
<span data-ttu-id="ff4d1-103">Virtuális hálózat beolvasása koppintással</span><span class="sxs-lookup"><span data-stu-id="ff4d1-103">Gets a virtual network tap</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff4d1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ff4d1-104">SYNTAX</span></span>

### <span data-ttu-id="ff4d1-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ff4d1-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzureRmVirtualNetworkTap -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff4d1-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff4d1-106">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmVirtualNetworkTap -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff4d1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ff4d1-107">DESCRIPTION</span></span>
<span data-ttu-id="ff4d1-108">A **Get-AzureRmVirtualNetworkTap** parancsmag Azure virtuális hálózati koppintással vagy Azure virtuális hálózati koppintásokat tartalmazó listával jelenik meg egy erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="ff4d1-108">The **Get-AzureRmVirtualNetworkTap** cmdlet gets an Azure virtual network tap or a list of Azure virtual network taps in a resource group.</span></span>

## <span data-ttu-id="ff4d1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ff4d1-109">EXAMPLES</span></span>

### <span data-ttu-id="ff4d1-110">Példa 1: virtuális hálózat beszerzése koppintással</span><span class="sxs-lookup"><span data-stu-id="ff4d1-110">Example 1: Get a virtual network tap</span></span>
```
PS C:\>Get-AzureRmVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
```

<span data-ttu-id="ff4d1-111">Ez a parancs a "ResourceGroup1"-ban a "VirtualTap1" kifejezésre koppintva egy VirtualNetwork-koppintást kap.</span><span class="sxs-lookup"><span data-stu-id="ff4d1-111">This command gets a VirtualNetwork tap reference for given "VirtualTap1" in "ResourceGroup1".</span></span>

## <span data-ttu-id="ff4d1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ff4d1-112">PARAMETERS</span></span>

### <span data-ttu-id="ff4d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff4d1-113">-DefaultProfile</span></span>
<span data-ttu-id="ff4d1-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ff4d1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff4d1-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ff4d1-115">-Name</span></span>
<span data-ttu-id="ff4d1-116">A koppintás neve.</span><span class="sxs-lookup"><span data-stu-id="ff4d1-116">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff4d1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff4d1-117">-ResourceGroupName</span></span>
<span data-ttu-id="ff4d1-118">A virtuális hálózat erőforráscsoport neve koppintással.</span><span class="sxs-lookup"><span data-stu-id="ff4d1-118">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff4d1-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff4d1-119">-ResourceId</span></span>
<span data-ttu-id="ff4d1-120">A VirtualNetworkTap-erőforrás ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff4d1-120">ResourceId of the VirtualNetworkTap resource</span></span>

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

### <span data-ttu-id="ff4d1-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ff4d1-121">-Confirm</span></span>
<span data-ttu-id="ff4d1-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ff4d1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff4d1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff4d1-123">-WhatIf</span></span>
<span data-ttu-id="ff4d1-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ff4d1-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff4d1-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ff4d1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff4d1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff4d1-126">CommonParameters</span></span>
<span data-ttu-id="ff4d1-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ff4d1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff4d1-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff4d1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff4d1-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff4d1-129">INPUTS</span></span>

### <span data-ttu-id="ff4d1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ff4d1-130">System.String</span></span>

## <span data-ttu-id="ff4d1-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff4d1-131">OUTPUTS</span></span>

### <span data-ttu-id="ff4d1-132">Microsoft. Azure. commands. Network. models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="ff4d1-132">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="ff4d1-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ff4d1-133">NOTES</span></span>

## <span data-ttu-id="ff4d1-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ff4d1-134">RELATED LINKS</span></span>
