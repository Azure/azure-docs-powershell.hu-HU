---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGatewayNatRule.md
ms.openlocfilehash: 35a59b24297efe3fd94a66d19a778913f488b800
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146634"
---
# <span data-ttu-id="06bc5-101">Remove-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="06bc5-101">Remove-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="06bc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06bc5-102">SYNOPSIS</span></span>
<span data-ttu-id="06bc5-103">Eltávolítja a VpnGatewayhez társított NAT-szabályt.</span><span class="sxs-lookup"><span data-stu-id="06bc5-103">Removes a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="06bc5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="06bc5-104">SYNTAX</span></span>

### <span data-ttu-id="06bc5-105">ByVpnGatewayNatRuleName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="06bc5-105">ByVpnGatewayNatRuleName (Default)</span></span>
```
Remove-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06bc5-106">ByVpnGatewayNatRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="06bc5-106">ByVpnGatewayNatRuleResourceId</span></span>
```
Remove-AzVpnGatewayNatRule -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06bc5-107">ByVpnGatewayNatRuleObject</span><span class="sxs-lookup"><span data-stu-id="06bc5-107">ByVpnGatewayNatRuleObject</span></span>
```
Remove-AzVpnGatewayNatRule -InputObject <PSVpnGatewayNatRule> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06bc5-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="06bc5-108">DESCRIPTION</span></span>
<span data-ttu-id="06bc5-109">Eltávolítja a VpnGatewayhez társított NAT-szabályt.</span><span class="sxs-lookup"><span data-stu-id="06bc5-109">Removes a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="06bc5-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="06bc5-110">EXAMPLES</span></span>

### <span data-ttu-id="06bc5-111">Példa1</span><span class="sxs-lookup"><span data-stu-id="06bc5-111">Example1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> New-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule" -Type Static -Mode EgressSnat -InternalMapping "10.0.0.1/26" -ExternalMapping "192.168.0.0/26"
PS C:\> Remove-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule"
```

<span data-ttu-id="06bc5-112">A fentiekkel a VpnGatewayhez társított erőforráscsoport (Virtual WAN, Virtual Network, Virtual Hub, VpnGateway és NAT) hozható létre.</span><span class="sxs-lookup"><span data-stu-id="06bc5-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub,VpnGateway and NAT rule associated with that VpnGateway.</span></span>
<span data-ttu-id="06bc5-113">Ezután eltávolítja a NAT-szabályt a NAT-szabály nevével.</span><span class="sxs-lookup"><span data-stu-id="06bc5-113">Then it removes the NAT rule using the NAT rule name.</span></span>


## <span data-ttu-id="06bc5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06bc5-114">PARAMETERS</span></span>

### <span data-ttu-id="06bc5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06bc5-115">-DefaultProfile</span></span>
<span data-ttu-id="06bc5-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06bc5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06bc5-117">-Force</span><span class="sxs-lookup"><span data-stu-id="06bc5-117">-Force</span></span>
<span data-ttu-id="06bc5-118">Ne kérjen megerősítést, ha törölni szeretne egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="06bc5-118">Do not ask for confirmation if you want to delete a resource</span></span>

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

### <span data-ttu-id="06bc5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06bc5-119">-InputObject</span></span>
<span data-ttu-id="06bc5-120">Frissítenünk kell a VpnGatewayNatRule objektumot.</span><span class="sxs-lookup"><span data-stu-id="06bc5-120">The VpnGatewayNatRule object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule
Parameter Sets: ByVpnGatewayNatRuleObject
Aliases: VpnGatewayNatRule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06bc5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="06bc5-121">-Name</span></span>
<span data-ttu-id="06bc5-122">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="06bc5-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleName
Aliases: ResourceName, VpnGatewayNatRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06bc5-123">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="06bc5-123">-ParentResourceName</span></span>
<span data-ttu-id="06bc5-124">A szülőerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="06bc5-124">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06bc5-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06bc5-125">-PassThru</span></span>
<span data-ttu-id="06bc5-126">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amelyen a műveletet végre kell hajtanunk.</span><span class="sxs-lookup"><span data-stu-id="06bc5-126">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="06bc5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06bc5-127">-ResourceGroupName</span></span>
<span data-ttu-id="06bc5-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="06bc5-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06bc5-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06bc5-129">-ResourceId</span></span>
<span data-ttu-id="06bc5-130">A törölni kívánt VpnGatewayNatRule objektum erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="06bc5-130">The resource id of the VpnGatewayNatRule object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleResourceId
Aliases: VpnGatewayNatRuleId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06bc5-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06bc5-131">-Confirm</span></span>
<span data-ttu-id="06bc5-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="06bc5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06bc5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06bc5-133">-WhatIf</span></span>
<span data-ttu-id="06bc5-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="06bc5-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06bc5-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="06bc5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06bc5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06bc5-136">CommonParameters</span></span>
<span data-ttu-id="06bc5-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06bc5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06bc5-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06bc5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06bc5-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="06bc5-139">INPUTS</span></span>

### <span data-ttu-id="06bc5-140">System.String</span><span class="sxs-lookup"><span data-stu-id="06bc5-140">System.String</span></span>

### <span data-ttu-id="06bc5-141">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="06bc5-141">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="06bc5-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06bc5-142">OUTPUTS</span></span>

### <span data-ttu-id="06bc5-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="06bc5-143">System.Boolean</span></span>

## <span data-ttu-id="06bc5-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="06bc5-144">NOTES</span></span>

## <span data-ttu-id="06bc5-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06bc5-145">RELATED LINKS</span></span>
