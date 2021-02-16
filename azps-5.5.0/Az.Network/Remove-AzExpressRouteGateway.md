---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
ms.openlocfilehash: 73bf40456b1fa99093f2c84c11f71e945004a8fa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146722"
---
# <span data-ttu-id="faa85-101">Remove-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="faa85-101">Remove-AzExpressRouteGateway</span></span>

## <span data-ttu-id="faa85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="faa85-102">SYNOPSIS</span></span>
<span data-ttu-id="faa85-103">A Remove-AzExpressRouteGateway parancsmag eltávolít egy Azure ExpressRoute-átjárót.</span><span class="sxs-lookup"><span data-stu-id="faa85-103">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="faa85-104">Ez egy azure virtual WAN szoftverrel definiált kapcsolatra jellemző átjáró.</span><span class="sxs-lookup"><span data-stu-id="faa85-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="faa85-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="faa85-105">SYNTAX</span></span>

### <span data-ttu-id="faa85-106">ByExpressRouteGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="faa85-106">ByExpressRouteGatewayName (Default)</span></span>
```
Remove-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="faa85-107">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="faa85-107">ByExpressRouteGatewayObject</span></span>
```
Remove-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="faa85-108">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="faa85-108">ByExpressRouteGatewayResourceId</span></span>
```
Remove-AzExpressRouteGateway -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="faa85-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="faa85-109">DESCRIPTION</span></span>
<span data-ttu-id="faa85-110">A Remove-AzExpressRouteGateway parancsmag eltávolít egy Azure ExpressRoute-átjárót.</span><span class="sxs-lookup"><span data-stu-id="faa85-110">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="faa85-111">Ez egy olyan átjáró, amely az Azure Virtual WAN szoftverrel definiált kapcsolatát használja.</span><span class="sxs-lookup"><span data-stu-id="faa85-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="faa85-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="faa85-112">EXAMPLES</span></span>

### <span data-ttu-id="faa85-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="faa85-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Remove-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -Passthru
```

<span data-ttu-id="faa85-114">Ebben a példában egy Erőforráscsoport (Virtual WAN, Virtual Hub, scalable ExpressRoute) átjárót hoz létre az Egyesült Államok központjában, majd azonnal törli azt.</span><span class="sxs-lookup"><span data-stu-id="faa85-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="faa85-115">A virtuális átjáró törlésekor megjelenő üzenet elrejtését a -Force jelölővel használhatja.</span><span class="sxs-lookup"><span data-stu-id="faa85-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="faa85-116">Ezzel törli az ExpressRouteGatewayt és a hozzá csatolt ExpressRouteConnectionst.</span><span class="sxs-lookup"><span data-stu-id="faa85-116">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

### <span data-ttu-id="faa85-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="faa85-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" | Remove-AzExpressRouteGateway-Passthru
```

<span data-ttu-id="faa85-118">Ebben a példában egy Erőforráscsoport (Virtual WAN, Virtual Hub, scalable ExpressRoute) átjárót hoz létre az Egyesült Államok nyugati részén, majd azonnal törli azt.</span><span class="sxs-lookup"><span data-stu-id="faa85-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in West Central US and then immediately deletes it.</span></span> <span data-ttu-id="faa85-119">Ez a törlés powershell-pipázás használatával történik, amely a parancs által visszaadott ExpressRouteGateway Get-AzExpressRouteGateway használ.</span><span class="sxs-lookup"><span data-stu-id="faa85-119">This deletion happens using powershell piping, which uses the ExpressRouteGateway object returned by the Get-AzExpressRouteGateway command.</span></span>
<span data-ttu-id="faa85-120">A virtuális átjáró törlésekor megjelenő üzenet elrejtését a -Force jelölővel használhatja.</span><span class="sxs-lookup"><span data-stu-id="faa85-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="faa85-121">Ezzel törli az ExpressRouteGatewayt és a hozzá csatolt ExpressRouteConnectionst.</span><span class="sxs-lookup"><span data-stu-id="faa85-121">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

## <span data-ttu-id="faa85-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="faa85-122">PARAMETERS</span></span>

### <span data-ttu-id="faa85-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faa85-123">-DefaultProfile</span></span>
<span data-ttu-id="faa85-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="faa85-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="faa85-125">-Force</span><span class="sxs-lookup"><span data-stu-id="faa85-125">-Force</span></span>
<span data-ttu-id="faa85-126">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="faa85-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="faa85-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="faa85-127">-InputObject</span></span>
<span data-ttu-id="faa85-128">Az ExpressRouteGateway-objektum, amit törölni kell.</span><span class="sxs-lookup"><span data-stu-id="faa85-128">The ExpressRouteGateway object to be deleted.</span></span>

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

### <span data-ttu-id="faa85-129">-Name</span><span class="sxs-lookup"><span data-stu-id="faa85-129">-Name</span></span>
<span data-ttu-id="faa85-130">Az ExpressRouteGateway neve.</span><span class="sxs-lookup"><span data-stu-id="faa85-130">The ExpressRouteGateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases: ResourceName, ExpressRouteGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faa85-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="faa85-131">-PassThru</span></span>
<span data-ttu-id="faa85-132">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="faa85-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="faa85-133">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="faa85-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="faa85-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faa85-134">-ResourceGroupName</span></span>
<span data-ttu-id="faa85-135">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="faa85-135">The resource group name.</span></span>

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

### <span data-ttu-id="faa85-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="faa85-136">-ResourceId</span></span>
<span data-ttu-id="faa85-137">Az ExpressRouteGateway törölnie kell Azure-erőforrásazonosítóját.</span><span class="sxs-lookup"><span data-stu-id="faa85-137">The Azure resource ID for the ExpressRouteGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: expressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="faa85-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="faa85-138">-Confirm</span></span>
<span data-ttu-id="faa85-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="faa85-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faa85-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faa85-140">-WhatIf</span></span>
<span data-ttu-id="faa85-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="faa85-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="faa85-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="faa85-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faa85-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faa85-143">CommonParameters</span></span>
<span data-ttu-id="faa85-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faa85-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faa85-145">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faa85-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faa85-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="faa85-146">INPUTS</span></span>

### <span data-ttu-id="faa85-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="faa85-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="faa85-148">System.String</span><span class="sxs-lookup"><span data-stu-id="faa85-148">System.String</span></span>

## <span data-ttu-id="faa85-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="faa85-149">OUTPUTS</span></span>

### <span data-ttu-id="faa85-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="faa85-150">System.Boolean</span></span>

## <span data-ttu-id="faa85-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="faa85-151">NOTES</span></span>

## <span data-ttu-id="faa85-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="faa85-152">RELATED LINKS</span></span>
