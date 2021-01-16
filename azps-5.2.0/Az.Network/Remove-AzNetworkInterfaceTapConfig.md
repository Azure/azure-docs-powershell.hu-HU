---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 52fc2a3c84c70d52c173bc256ca2b0d952307e91
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333461"
---
# <span data-ttu-id="1f329-101">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="1f329-101">Remove-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="1f329-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f329-102">SYNOPSIS</span></span>
<span data-ttu-id="1f329-103">Koppintás beállítása a megadott hálózati felületről</span><span class="sxs-lookup"><span data-stu-id="1f329-103">Removes a tap configuration from given network interface</span></span>

## <span data-ttu-id="1f329-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1f329-104">SYNTAX</span></span>

### <span data-ttu-id="1f329-105">RemoveByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1f329-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f329-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f329-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f329-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f329-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -InputObject <PSNetworkInterfaceTapConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f329-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1f329-108">DESCRIPTION</span></span>
<span data-ttu-id="1f329-109">A **Remove-AzNetworkInterfaceTapConfig** parancsmag eltávolítja az Azure-koppintás konfigurációját a hálózati felület listájáról.</span><span class="sxs-lookup"><span data-stu-id="1f329-109">The **Remove-AzNetworkInterfaceTapConfig** cmdlet removes an Azure tap configuration from a network interface list.</span></span>

## <span data-ttu-id="1f329-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1f329-110">EXAMPLES</span></span>

### <span data-ttu-id="1f329-111">1. példa: Koppintásos konfiguráció eltávolítása</span><span class="sxs-lookup"><span data-stu-id="1f329-111">Example 1: Remove a tap configuration</span></span>
```
PS C:\>Remove-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="1f329-112">Ez a parancs eltávolítja a TapConfigurationt a NetworkInterface1-ről az ResourceGroup1 erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="1f329-112">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="1f329-113">Mivel a *Force* paramétert nem használja, a rendszer kérni fogja a felhasználótól a művelet megerősítését.</span><span class="sxs-lookup"><span data-stu-id="1f329-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="1f329-114">2. példa: Hálózati felület eltávolítása</span><span class="sxs-lookup"><span data-stu-id="1f329-114">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1" | Remove-AzNetworkInterfaceTapConfig -Force
```

<span data-ttu-id="1f329-115">Ez a parancs eltávolítja a TapConfigurationt a NetworkInterface1-ről az ResourceGroup1 erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="1f329-115">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="1f329-116">Mivel a *Force* paramétert használja, a felhasználó nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1f329-116">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="1f329-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f329-117">PARAMETERS</span></span>

### <span data-ttu-id="1f329-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f329-118">-DefaultProfile</span></span>
<span data-ttu-id="1f329-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1f329-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f329-120">-Force</span><span class="sxs-lookup"><span data-stu-id="1f329-120">-Force</span></span>
<span data-ttu-id="1f329-121">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1f329-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1f329-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f329-122">-InputObject</span></span>
<span data-ttu-id="1f329-123">Hivatkozás a NetworkInterfaceTapConfig hálózatra.</span><span class="sxs-lookup"><span data-stu-id="1f329-123">Reference to NetworkInterfaceTapConfig.</span></span>

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

### <span data-ttu-id="1f329-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1f329-124">-Name</span></span>
<span data-ttu-id="1f329-125">A virtuális hálózat társviszony-neve.</span><span class="sxs-lookup"><span data-stu-id="1f329-125">The virtual network peering name.</span></span>

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

### <span data-ttu-id="1f329-126">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="1f329-126">-NetworkInterfaceName</span></span>
<span data-ttu-id="1f329-127">A virtuális hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="1f329-127">The virtual network name.</span></span>

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

### <span data-ttu-id="1f329-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f329-128">-PassThru</span></span>
<span data-ttu-id="1f329-129">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="1f329-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1f329-130">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="1f329-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1f329-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f329-131">-ResourceGroupName</span></span>
<span data-ttu-id="1f329-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1f329-132">The resource group name.</span></span>

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

### <span data-ttu-id="1f329-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f329-133">-ResourceId</span></span>
<span data-ttu-id="1f329-134">NetworkInterfaceTapConfig erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="1f329-134">NetworkInterfaceTapConfig resource id.</span></span>

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

### <span data-ttu-id="1f329-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f329-135">-Confirm</span></span>
<span data-ttu-id="1f329-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1f329-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f329-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f329-137">-WhatIf</span></span>
<span data-ttu-id="1f329-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1f329-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f329-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1f329-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f329-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f329-140">CommonParameters</span></span>
<span data-ttu-id="1f329-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f329-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f329-142">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f329-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f329-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1f329-143">INPUTS</span></span>

### <span data-ttu-id="1f329-144">System.String</span><span class="sxs-lookup"><span data-stu-id="1f329-144">System.String</span></span>

### <span data-ttu-id="1f329-145">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="1f329-145">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="1f329-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f329-146">OUTPUTS</span></span>

### <span data-ttu-id="1f329-147">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="1f329-147">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="1f329-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1f329-148">NOTES</span></span>

## <span data-ttu-id="1f329-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f329-149">RELATED LINKS</span></span>

[<span data-ttu-id="1f329-150">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="1f329-150">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="1f329-151">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="1f329-151">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="1f329-152">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="1f329-152">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
