---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
ms.openlocfilehash: f7ec596a73c3659584d1e0b80c899b4bf9aad8d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933793"
---
# <span data-ttu-id="a3c87-101">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a3c87-101">New-AzPrivateEndpoint</span></span>

## <span data-ttu-id="a3c87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3c87-102">SYNOPSIS</span></span>
<span data-ttu-id="a3c87-103">Létrehoz egy privát végpontot.</span><span class="sxs-lookup"><span data-stu-id="a3c87-103">Creates a private endpoint.</span></span>

## <span data-ttu-id="a3c87-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a3c87-104">SYNTAX</span></span>

### <span data-ttu-id="a3c87-105">Mind</span><span class="sxs-lookup"><span data-stu-id="a3c87-105">All</span></span>

```
New-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 -PrivateLinkServiceConnection <PSPrivateLinkServiceConnection[]> [-ByManualRequest] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3c87-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a3c87-106">DESCRIPTION</span></span>

<span data-ttu-id="a3c87-107">A **New-AzPrivateEndpoint** parancsmag létrehoz egy privát végpontot.</span><span class="sxs-lookup"><span data-stu-id="a3c87-107">The **New-AzPrivateEndpoint** cmdlet creates a private endpoint.</span></span>

## <span data-ttu-id="a3c87-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a3c87-108">EXAMPLES</span></span>

### <span data-ttu-id="a3c87-109">1. példa: Privát végpont létrehozása</span><span class="sxs-lookup"><span data-stu-id="a3c87-109">Example 1: Create a private endpoint</span></span>

<span data-ttu-id="a3c87-110">Az alábbi példa létrehoz egy privát végpontot egy virtuális hálózat megadott alhálózatában egy adott privát hivatkozásszolgáltatás-azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="a3c87-110">The following example creates a private endpoint with a specific private link service ID in the specified subnet in a virtual network.</span></span>

```powershell
$virtualNetwork = Get-AzVirtualNetwork -ResourceName 'myVirtualNetwork' -ResourceGroupName 'myResourceGroup'
$subnet = $virtualNetwork | Select-Object -ExpandProperty subnets | Where-Object Name -eq 'mySubnet'
$plsConnection= New-AzPrivateLinkServiceConnection -Name 'MyPLSConnections' -PrivateLinkServiceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService' -RequestMessage 'Please Approve my request'
New-AzPrivateEndpoint -Name 'MyPrivateEndpoint' -ResourceGroup 'myResourceGroup' -Location 'centralus' -PrivateLinkServiceConnection $plsConnection -Subnet $subnet
```

## <span data-ttu-id="a3c87-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3c87-111">PARAMETERS</span></span>

### <span data-ttu-id="a3c87-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3c87-112">-AsJob</span></span>

<span data-ttu-id="a3c87-113">Futtassa a parancsmagot feladatként a háttérben.</span><span class="sxs-lookup"><span data-stu-id="a3c87-113">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="a3c87-114">-ByManualRequest</span><span class="sxs-lookup"><span data-stu-id="a3c87-114">-ByManualRequest</span></span>

<span data-ttu-id="a3c87-115">A kapcsolat létesítését manuális kérés használatával használhatja.</span><span class="sxs-lookup"><span data-stu-id="a3c87-115">Use manual request to establish the connection.</span></span>

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

### <span data-ttu-id="a3c87-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3c87-116">-DefaultProfile</span></span>

<span data-ttu-id="a3c87-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a3c87-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3c87-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a3c87-118">-Force</span></span>

<span data-ttu-id="a3c87-119">Ne kérjen megerősítést egy erőforrás felülírása előtt.</span><span class="sxs-lookup"><span data-stu-id="a3c87-119">Do not ask for confirmation to overwrite a resource.</span></span>

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

### <span data-ttu-id="a3c87-120">-Location</span><span class="sxs-lookup"><span data-stu-id="a3c87-120">-Location</span></span>

<span data-ttu-id="a3c87-121">Megadja a magánjellegű végpont helyét.</span><span class="sxs-lookup"><span data-stu-id="a3c87-121">Specifies a location for the private endpoint.</span></span> <span data-ttu-id="a3c87-122">A [Get-AzLocation paramétert](/powershell/module/az.resources/get-azlocation) a paraméter érvényes értékeinek meghatározására használhatja.</span><span class="sxs-lookup"><span data-stu-id="a3c87-122">Use [Get-AzLocation](/powershell/module/az.resources/get-azlocation) to determine valid values for this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3c87-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a3c87-123">-Name</span></span>

<span data-ttu-id="a3c87-124">A magánjellegű végpont neve.</span><span class="sxs-lookup"><span data-stu-id="a3c87-124">Name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3c87-125">-PrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="a3c87-125">-PrivateLinkServiceConnection</span></span>

<span data-ttu-id="a3c87-126">A magánjellegű végpont csatlakoztatásának erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a3c87-126">The resource ID to connect the private endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3c87-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3c87-127">-ResourceGroupName</span></span>

<span data-ttu-id="a3c87-128">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3c87-128">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3c87-129">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="a3c87-129">-Subnet</span></span>

<span data-ttu-id="a3c87-130">A privát végpont alhálózata.</span><span class="sxs-lookup"><span data-stu-id="a3c87-130">The subnet of the private endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3c87-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="a3c87-131">-Tag</span></span>

<span data-ttu-id="a3c87-132">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="a3c87-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a3c87-133">Például: @{key0='érték0';key1=$null;key2='érték2'}</span><span class="sxs-lookup"><span data-stu-id="a3c87-133">For example: @{key0='value0';key1=$null;key2='value2'}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3c87-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3c87-134">-Confirm</span></span>

<span data-ttu-id="a3c87-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a3c87-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3c87-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3c87-136">-WhatIf</span></span>

<span data-ttu-id="a3c87-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a3c87-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3c87-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a3c87-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3c87-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3c87-139">CommonParameters</span></span>

<span data-ttu-id="a3c87-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3c87-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3c87-141">További információt a [about_CommonParameters.](/powershell/module/microsoft.powershell.core/about/about_commonparameters)</span><span class="sxs-lookup"><span data-stu-id="a3c87-141">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="a3c87-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a3c87-142">INPUTS</span></span>

### <span data-ttu-id="a3c87-143">System.String</span><span class="sxs-lookup"><span data-stu-id="a3c87-143">System.String</span></span>

### <span data-ttu-id="a3c87-144">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="a3c87-144">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="a3c87-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span><span class="sxs-lookup"><span data-stu-id="a3c87-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span></span>

## <span data-ttu-id="a3c87-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3c87-146">OUTPUTS</span></span>

### <span data-ttu-id="a3c87-147">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a3c87-147">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="a3c87-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a3c87-148">NOTES</span></span>

## <span data-ttu-id="a3c87-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a3c87-149">RELATED LINKS</span></span>

[<span data-ttu-id="a3c87-150">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a3c87-150">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="a3c87-151">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="a3c87-151">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)

[<span data-ttu-id="a3c87-152">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="a3c87-152">New-AzPrivateLinkServiceConnection</span></span>](./New-AzPrivateLinkServiceConnection.md)