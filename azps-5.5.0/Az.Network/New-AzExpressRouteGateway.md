---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
ms.openlocfilehash: 5fe97366784b3513515ee90ce70fe518c36a8585
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151746"
---
# <span data-ttu-id="44154-101">New-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="44154-101">New-AzExpressRouteGateway</span></span>

## <span data-ttu-id="44154-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44154-102">SYNOPSIS</span></span>
<span data-ttu-id="44154-103">Scalable ExpressRoute-átjárót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="44154-103">Creates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="44154-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="44154-104">SYNTAX</span></span>

### <span data-ttu-id="44154-105">ByVirtualHubName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="44154-105">ByVirtualHubName (Default)</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubName <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44154-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="44154-106">ByVirtualHubObject</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHub <PSVirtualHub> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44154-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="44154-107">ByVirtualHubResourceId</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubId <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44154-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="44154-108">DESCRIPTION</span></span>

<span data-ttu-id="44154-109">New-AzExpressRouteGateway scalable ExpressRoute-átjárót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="44154-109">New-AzExpressRouteGateway creates a scalable ExpressRoute Gateway.</span></span> <span data-ttu-id="44154-110">Ez egy szoftveres kapcsolat, amely a virtuálisHubon belüli Azure-hoz való kapcsolódáshoz szükséges.</span><span class="sxs-lookup"><span data-stu-id="44154-110">This is software defined connectivity for on premise to Azure inside the VirtualHub.</span></span> 

<span data-ttu-id="44154-111">Ezt az átjárót az ebben vagy a parancsmagban megadott méretarány Set-AzExpressRouteGateway lehet.</span><span class="sxs-lookup"><span data-stu-id="44154-111">This gateway can be scaled based on the scale unit specified in this or the Set-AzExpressRouteGateway cmdlet.</span></span> 

<span data-ttu-id="44154-112">A kapcsolat egy on-premise ExpressRoute-áramkörről van beállítva a méretezhető átjáróval.</span><span class="sxs-lookup"><span data-stu-id="44154-112">A connection is set up from a on-premise ExpressRoute circuit to the scalable gateway.</span></span>

<span data-ttu-id="44154-113">Az ExpressRouteGateway ugyanazon a helyen lesz, mint a hivatkozott VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="44154-113">The ExpressRouteGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="44154-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="44154-114">EXAMPLES</span></span>

### <span data-ttu-id="44154-115">1. példa</span><span class="sxs-lookup"><span data-stu-id="44154-115">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2

ResourceGroupName   : testRG
Name                : testergw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/expressRouteGateways/testergw
Location            : West US
MinScaleUnits       : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/expressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="44154-116">A fenti létrehoz egy erőforráscsoportot (Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure).</span><span class="sxs-lookup"><span data-stu-id="44154-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="44154-117">Ezután létrejön egy ExpressRoute-átjáró a virtuális központban 2 méretarányú egységben.</span><span class="sxs-lookup"><span data-stu-id="44154-117">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="44154-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44154-118">PARAMETERS</span></span>

### <span data-ttu-id="44154-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44154-119">-AsJob</span></span>
<span data-ttu-id="44154-120">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="44154-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="44154-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44154-121">-DefaultProfile</span></span>
<span data-ttu-id="44154-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="44154-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44154-123">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="44154-123">-MaxScaleUnits</span></span>
<span data-ttu-id="44154-124">Az ExpressRouteGateway méretarányos egységeinek maximális száma.</span><span class="sxs-lookup"><span data-stu-id="44154-124">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="44154-125">Érvényes tartomány > 2</span><span class="sxs-lookup"><span data-stu-id="44154-125">Valid range > 2</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44154-126">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="44154-126">-MinScaleUnits</span></span>
<span data-ttu-id="44154-127">Az ExpressRouteGateway méretarányának minimális száma.</span><span class="sxs-lookup"><span data-stu-id="44154-127">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="44154-128">Érvényes tartomány > 2</span><span class="sxs-lookup"><span data-stu-id="44154-128">Valid range > 2</span></span>

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

### <span data-ttu-id="44154-129">-Name</span><span class="sxs-lookup"><span data-stu-id="44154-129">-Name</span></span>
<span data-ttu-id="44154-130">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="44154-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44154-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44154-131">-ResourceGroupName</span></span>
<span data-ttu-id="44154-132">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="44154-132">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44154-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="44154-133">-Tag</span></span>
<span data-ttu-id="44154-134">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="44154-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="44154-135">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="44154-135">-VirtualHub</span></span>
<span data-ttu-id="44154-136">A VirtualHubhoz, a VpnGatewayhez társítva kell lennie.</span><span class="sxs-lookup"><span data-stu-id="44154-136">The VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44154-137">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="44154-137">-VirtualHubId</span></span>
<span data-ttu-id="44154-138">Annak a VirtualHubnak az azonosítóját, amelyhez a VpnGatewaynek társítva kell lennie.</span><span class="sxs-lookup"><span data-stu-id="44154-138">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44154-139">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="44154-139">-VirtualHubName</span></span>
<span data-ttu-id="44154-140">Annak a VirtualHubnak az azonosítóját, amelyhez a VpnGatewaynek társítva kell lennie.</span><span class="sxs-lookup"><span data-stu-id="44154-140">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44154-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44154-141">-Confirm</span></span>
<span data-ttu-id="44154-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="44154-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44154-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44154-143">-WhatIf</span></span>
<span data-ttu-id="44154-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="44154-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44154-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="44154-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44154-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44154-146">CommonParameters</span></span>
<span data-ttu-id="44154-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44154-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44154-148">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44154-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44154-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="44154-149">INPUTS</span></span>

### <span data-ttu-id="44154-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="44154-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="44154-151">System.String</span><span class="sxs-lookup"><span data-stu-id="44154-151">System.String</span></span>

## <span data-ttu-id="44154-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="44154-152">OUTPUTS</span></span>

### <span data-ttu-id="44154-153">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="44154-153">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="44154-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="44154-154">NOTES</span></span>

## <span data-ttu-id="44154-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="44154-155">RELATED LINKS</span></span>
