---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
ms.openlocfilehash: bd800f362a1a5fb66968e0f75b1211b2f0bbdf72
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479921"
---
# <span data-ttu-id="53af9-101">Set-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="53af9-101">Set-AzExpressRouteGateway</span></span>

## <span data-ttu-id="53af9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53af9-102">SYNOPSIS</span></span>
<span data-ttu-id="53af9-103">Frissíti a Scalable ExpressRoute-átjárót.</span><span class="sxs-lookup"><span data-stu-id="53af9-103">Updates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="53af9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="53af9-104">SYNTAX</span></span>

### <span data-ttu-id="53af9-105">ByExpressRouteGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="53af9-105">ByExpressRouteGatewayName (Default)</span></span>
```
Set-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-MinScaleUnits <UInt32>]
 [-MaxScaleUnits <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53af9-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="53af9-106">ByExpressRouteGatewayObject</span></span>
```
Set-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-MinScaleUnits <UInt32>] [-MaxScaleUnits <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="53af9-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="53af9-107">ByExpressRouteGatewayResourceId</span></span>
```
Set-AzExpressRouteGateway -ResourceId <String> [-MinScaleUnits <UInt32>] [-MaxScaleUnits <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="53af9-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="53af9-108">DESCRIPTION</span></span>

<span data-ttu-id="53af9-109">A **Set-AzExpressRouteGateway** parancsmaggal frissítheti egy meglévő ExpressRouteGateway méretarányát, vagy frissítheti az erőforráscímkéket.</span><span class="sxs-lookup"><span data-stu-id="53af9-109">The **Set-AzExpressRouteGateway** cmdlet enables you to update the scale units for an existing ExpressRouteGateway or update the resource tags.</span></span>

## <span data-ttu-id="53af9-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="53af9-110">EXAMPLES</span></span>

### <span data-ttu-id="53af9-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="53af9-111">Example 1</span></span>

```powershell
PS C:\>Set-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan =Set-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub =Set-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\>New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\>Set-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -MinScaleUnits 3

ResourceGroupName   : testRG
Name                : testergw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/expressRouteGateways/testergw
Location            : West US
MinScaleUnits       : 3
Type                : Microsoft.Network/expressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="53af9-112">A fentiekkel létrehoz egy erőforráscsoportot (Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure).</span><span class="sxs-lookup"><span data-stu-id="53af9-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="53af9-113">Ezután létrejön egy ExpressRoute-átjáró a virtuális központban 2 méretarányú egységben, amelyet aztán 3 méretarányú egységekre módosítunk.</span><span class="sxs-lookup"><span data-stu-id="53af9-113">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units which will then be modified to 3 scale units</span></span>

## <span data-ttu-id="53af9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53af9-114">PARAMETERS</span></span>

### <span data-ttu-id="53af9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53af9-115">-AsJob</span></span>
<span data-ttu-id="53af9-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="53af9-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53af9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53af9-117">-DefaultProfile</span></span>
<span data-ttu-id="53af9-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="53af9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53af9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53af9-119">-InputObject</span></span>
<span data-ttu-id="53af9-120">Az ExpressRouteGateway, amit frissíteni kell.</span><span class="sxs-lookup"><span data-stu-id="53af9-120">The ExpressRouteGateway that needs to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53af9-121">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="53af9-121">-MaxScaleUnits</span></span>
<span data-ttu-id="53af9-122">Az ExpressRouteGateway méretarányos egységeinek maximális száma.</span><span class="sxs-lookup"><span data-stu-id="53af9-122">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="53af9-123">Érvényes tartomány > 2</span><span class="sxs-lookup"><span data-stu-id="53af9-123">Valid range > 2</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53af9-124">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="53af9-124">-MinScaleUnits</span></span>
<span data-ttu-id="53af9-125">Az ExpressRouteGateway méretarányának minimális száma.</span><span class="sxs-lookup"><span data-stu-id="53af9-125">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="53af9-126">Érvényes tartomány > 2</span><span class="sxs-lookup"><span data-stu-id="53af9-126">Valid range > 2</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53af9-127">-Name</span><span class="sxs-lookup"><span data-stu-id="53af9-127">-Name</span></span>
<span data-ttu-id="53af9-128">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="53af9-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases: ResourceName, ExpressRouteGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53af9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53af9-129">-ResourceGroupName</span></span>
<span data-ttu-id="53af9-130">A frissíthető ExpressRouteGateway erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="53af9-130">The resource group name of the ExpressRouteGateway to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53af9-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53af9-131">-ResourceId</span></span>
<span data-ttu-id="53af9-132">Az ExpressRouteGateway frissíthető azonosítója.</span><span class="sxs-lookup"><span data-stu-id="53af9-132">The Id of the ExpressRouteGateway that needs to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53af9-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="53af9-133">-Tag</span></span>
<span data-ttu-id="53af9-134">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="53af9-134">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53af9-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53af9-135">-Confirm</span></span>
<span data-ttu-id="53af9-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="53af9-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53af9-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53af9-137">-WhatIf</span></span>
<span data-ttu-id="53af9-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="53af9-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53af9-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="53af9-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53af9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53af9-140">CommonParameters</span></span>
<span data-ttu-id="53af9-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53af9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53af9-142">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53af9-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53af9-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53af9-143">INPUTS</span></span>

### <span data-ttu-id="53af9-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="53af9-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="53af9-145">System.String</span><span class="sxs-lookup"><span data-stu-id="53af9-145">System.String</span></span>

## <span data-ttu-id="53af9-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53af9-146">OUTPUTS</span></span>

### <span data-ttu-id="53af9-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="53af9-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="53af9-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="53af9-148">NOTES</span></span>

## <span data-ttu-id="53af9-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53af9-149">RELATED LINKS</span></span>
