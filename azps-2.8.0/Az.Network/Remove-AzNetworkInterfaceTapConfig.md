---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 8ad89a0f5fad61fea2ba898ea17f63b6f935ae84
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837847"
---
# <span data-ttu-id="9eda8-101">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="9eda8-101">Remove-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="9eda8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9eda8-102">SYNOPSIS</span></span>
<span data-ttu-id="9eda8-103">Egy koppintás konfigurációjának eltávolítása adott hálózati felületen</span><span class="sxs-lookup"><span data-stu-id="9eda8-103">Removes a tap configuration from given network interface</span></span>

## <span data-ttu-id="9eda8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9eda8-104">SYNTAX</span></span>

### <span data-ttu-id="9eda8-105">RemoveByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9eda8-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9eda8-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9eda8-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9eda8-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9eda8-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -InputObject <PSNetworkInterfaceTapConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9eda8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9eda8-108">DESCRIPTION</span></span>
<span data-ttu-id="9eda8-109">A **Remove-AzNetworkInterfaceTapConfig** parancsmag eltávolítja az Azure koppintás konfigurációját egy hálózati kapcsolat listából.</span><span class="sxs-lookup"><span data-stu-id="9eda8-109">The **Remove-AzNetworkInterfaceTapConfig** cmdlet removes an Azure tap configuration from a network interface list.</span></span>

## <span data-ttu-id="9eda8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9eda8-110">EXAMPLES</span></span>

### <span data-ttu-id="9eda8-111">Példa 1: koppintás konfigurációjának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9eda8-111">Example 1: Remove a tap configuration</span></span>
```
PS C:\>Remove-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="9eda8-112">Ez a parancs eltávolítja a TapConfiguration a NetworkInterface1-ról egy erőforráscsoport-ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="9eda8-112">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="9eda8-113">Mivel az *erő* paraméter nem használható, a rendszer kérni fogja a felhasználót, hogy erősítse meg ezt a lépést.</span><span class="sxs-lookup"><span data-stu-id="9eda8-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="9eda8-114">2. példa: hálózati felület eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9eda8-114">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1" | Remove-AzNetworkInterfaceTapConfig -Force
```

<span data-ttu-id="9eda8-115">Ez a parancs eltávolítja a TapConfiguration a NetworkInterface1-ról egy erőforráscsoport-ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="9eda8-115">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="9eda8-116">Mivel az *erő* paramétert használja, a rendszer nem kéri a felhasználó megerősítését.</span><span class="sxs-lookup"><span data-stu-id="9eda8-116">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="9eda8-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9eda8-117">PARAMETERS</span></span>

### <span data-ttu-id="9eda8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eda8-118">-DefaultProfile</span></span>
<span data-ttu-id="9eda8-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9eda8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9eda8-120">-Force</span><span class="sxs-lookup"><span data-stu-id="9eda8-120">-Force</span></span>
<span data-ttu-id="9eda8-121">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9eda8-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9eda8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9eda8-122">-InputObject</span></span>
<span data-ttu-id="9eda8-123">Hivatkozás a NetworkInterfaceTapConfig.</span><span class="sxs-lookup"><span data-stu-id="9eda8-123">Reference to NetworkInterfaceTapConfig.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9eda8-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9eda8-124">-Name</span></span>
<span data-ttu-id="9eda8-125">A virtuális hálózat társközi neve.</span><span class="sxs-lookup"><span data-stu-id="9eda8-125">The virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9eda8-126">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="9eda8-126">-NetworkInterfaceName</span></span>
<span data-ttu-id="9eda8-127">A virtuális hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="9eda8-127">The virtual network name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9eda8-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9eda8-128">-PassThru</span></span>
<span data-ttu-id="9eda8-129">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="9eda8-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9eda8-130">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="9eda8-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9eda8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9eda8-131">-ResourceGroupName</span></span>
<span data-ttu-id="9eda8-132">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="9eda8-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9eda8-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9eda8-133">-ResourceId</span></span>
<span data-ttu-id="9eda8-134">NetworkInterfaceTapConfig erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="9eda8-134">NetworkInterfaceTapConfig resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9eda8-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9eda8-135">-Confirm</span></span>
<span data-ttu-id="9eda8-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9eda8-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9eda8-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9eda8-137">-WhatIf</span></span>
<span data-ttu-id="9eda8-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9eda8-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9eda8-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9eda8-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9eda8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eda8-140">CommonParameters</span></span>
<span data-ttu-id="9eda8-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9eda8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eda8-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9eda8-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eda8-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9eda8-143">INPUTS</span></span>

### <span data-ttu-id="9eda8-144">System. String</span><span class="sxs-lookup"><span data-stu-id="9eda8-144">System.String</span></span>

### <span data-ttu-id="9eda8-145">Microsoft. Azure. commands. Network. models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="9eda8-145">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="9eda8-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9eda8-146">OUTPUTS</span></span>

### <span data-ttu-id="9eda8-147">Microsoft. Azure. commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="9eda8-147">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="9eda8-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9eda8-148">NOTES</span></span>

## <span data-ttu-id="9eda8-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9eda8-149">RELATED LINKS</span></span>

[<span data-ttu-id="9eda8-150">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="9eda8-150">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="9eda8-151">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="9eda8-151">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="9eda8-152">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="9eda8-152">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
