---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 3f95ad6b11e8ddf7baaf5bcdf312ec172a9d397a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008725"
---
# <span data-ttu-id="c5753-101">New-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="c5753-101">New-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="c5753-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5753-102">SYNOPSIS</span></span>
<span data-ttu-id="c5753-103">Hozzon létre egy hálózati virtuális eszköz típusú erőforrást.</span><span class="sxs-lookup"><span data-stu-id="c5753-103">Create a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="c5753-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c5753-104">SYNTAX</span></span>

### <span data-ttu-id="c5753-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c5753-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> -Location <String>
 -VirtualHubId <String> -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32>
 [-Identity <PSManagedServiceIdentity>] [-BootStrapConfigurationBlob <String[]>]
 [-CloudInitConfigurationBlob <String[]>] [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5753-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5753-106">ResourceIdParameterSet</span></span>
```
New-AzNetworkVirtualAppliance -ResourceId <String> -Location <String> -VirtualHubId <String>
 -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32> [-Identity <PSManagedServiceIdentity>]
 [-BootStrapConfigurationBlob <String[]>] [-CloudInitConfigurationBlob <String[]>]
 [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5753-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c5753-107">DESCRIPTION</span></span>
<span data-ttu-id="c5753-108">A New-AzNetworkVirtualAppliance parancs létrehoz egy virtuális hálózati eszköz típusú erőforrást az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="c5753-108">The New-AzNetworkVirtualAppliance command creates a Network Virtual Appliance resource in Azure.</span></span>

## <span data-ttu-id="c5753-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c5753-109">EXAMPLES</span></span>

### <span data-ttu-id="c5753-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="c5753-110">Example 1</span></span>
```powershell
PS C:\> $sku=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
PS C:\> $hub=Get-AzVirtualHub -ResourceGroupName testrg -Name hub
PS C:\> $nva=New-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva -Location eastus2 -VirtualApplianceAsn 1270 -VirtualHubId $hub.Id -Sku $sku -CloudInitConfiguration "echo Hello World!"

```

<span data-ttu-id="c5753-111">Létrehoz egy új hálózati virtuális eszköz típusú erőforrást az erőforráscsoportban: testrg.</span><span class="sxs-lookup"><span data-stu-id="c5753-111">Creates a new Network Virtual Appliance resource in resource group: testrg.</span></span>

## <span data-ttu-id="c5753-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5753-112">PARAMETERS</span></span>

### <span data-ttu-id="c5753-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c5753-113">-AsJob</span></span>
<span data-ttu-id="c5753-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c5753-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c5753-115">-BootStrapConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="c5753-115">-BootStrapConfigurationBlob</span></span>
<span data-ttu-id="c5753-116">A Bootstrap konfigurációs blob URL-címe.</span><span class="sxs-lookup"><span data-stu-id="c5753-116">The Bootstrap configuration blob URL.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5753-117">-CloudInitConfiguration</span><span class="sxs-lookup"><span data-stu-id="c5753-117">-CloudInitConfiguration</span></span>
<span data-ttu-id="c5753-118">A Cloudinit beállítása egyszerű szövegként.</span><span class="sxs-lookup"><span data-stu-id="c5753-118">The Cloudinit configuration as plain text.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5753-119">-CloudInitConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="c5753-119">-CloudInitConfigurationBlob</span></span>
<span data-ttu-id="c5753-120">A Cloudinit konfigurációs blobtároló URL-címe.</span><span class="sxs-lookup"><span data-stu-id="c5753-120">The Cloudinit configuration blob storage URL.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5753-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5753-121">-DefaultProfile</span></span>
<span data-ttu-id="c5753-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c5753-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5753-123">-Force</span><span class="sxs-lookup"><span data-stu-id="c5753-123">-Force</span></span>
<span data-ttu-id="c5753-124">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="c5753-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="c5753-125">-Identity</span><span class="sxs-lookup"><span data-stu-id="c5753-125">-Identity</span></span>
<span data-ttu-id="c5753-126">A Felügyelt identitás.</span><span class="sxs-lookup"><span data-stu-id="c5753-126">The Managed identity.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5753-127">-Location</span><span class="sxs-lookup"><span data-stu-id="c5753-127">-Location</span></span>
<span data-ttu-id="c5753-128">A nyilvános IP-cím helye.</span><span class="sxs-lookup"><span data-stu-id="c5753-128">The public IP address location.</span></span>

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

### <span data-ttu-id="c5753-129">-Name</span><span class="sxs-lookup"><span data-stu-id="c5753-129">-Name</span></span>
<span data-ttu-id="c5753-130">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="c5753-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5753-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5753-131">-ResourceGroupName</span></span>
<span data-ttu-id="c5753-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c5753-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5753-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5753-133">-ResourceId</span></span>
<span data-ttu-id="c5753-134">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c5753-134">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5753-135">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="c5753-135">-Sku</span></span>
<span data-ttu-id="c5753-136">A virtuális eszköz termékváltozata.</span><span class="sxs-lookup"><span data-stu-id="c5753-136">The Sku of the Virtual Appliance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5753-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="c5753-137">-Tag</span></span>
<span data-ttu-id="c5753-138">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="c5753-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="c5753-139">-VirtualApplianceAsn</span><span class="sxs-lookup"><span data-stu-id="c5753-139">-VirtualApplianceAsn</span></span>
<span data-ttu-id="c5753-140">A virtuális eszköz ASN-száma.</span><span class="sxs-lookup"><span data-stu-id="c5753-140">The ASN number of the Virtual Appliance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5753-141">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="c5753-141">-VirtualHubId</span></span>
<span data-ttu-id="c5753-142">A virtuális központ erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c5753-142">The Resource Id of the Virtual Hub.</span></span>

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

### <span data-ttu-id="c5753-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5753-143">-Confirm</span></span>
<span data-ttu-id="c5753-144">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c5753-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5753-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5753-145">-WhatIf</span></span>
<span data-ttu-id="c5753-146">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c5753-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5753-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c5753-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5753-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5753-148">CommonParameters</span></span>
<span data-ttu-id="c5753-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5753-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5753-150">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5753-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5753-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5753-151">INPUTS</span></span>

### <span data-ttu-id="c5753-152">System.String</span><span class="sxs-lookup"><span data-stu-id="c5753-152">System.String</span></span>

### <span data-ttu-id="c5753-153">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="c5753-153">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

### <span data-ttu-id="c5753-154">System.Int32</span><span class="sxs-lookup"><span data-stu-id="c5753-154">System.Int32</span></span>

### <span data-ttu-id="c5753-155">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="c5753-155">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

### <span data-ttu-id="c5753-156">System.String[]</span><span class="sxs-lookup"><span data-stu-id="c5753-156">System.String[]</span></span>

### <span data-ttu-id="c5753-157">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c5753-157">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c5753-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5753-158">OUTPUTS</span></span>

### <span data-ttu-id="c5753-159">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="c5753-159">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="c5753-160">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c5753-160">NOTES</span></span>

## <span data-ttu-id="c5753-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5753-161">RELATED LINKS</span></span>
