---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 9b3991a24430afa74853f742bffa12b772dbeaf2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466773"
---
# <span data-ttu-id="f666f-101">New-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="f666f-101">New-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="f666f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f666f-102">SYNOPSIS</span></span>
<span data-ttu-id="f666f-103">Hozzon létre egy hálózati virtuális eszköz típusú erőforrást.</span><span class="sxs-lookup"><span data-stu-id="f666f-103">Create a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="f666f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f666f-104">SYNTAX</span></span>

### <span data-ttu-id="f666f-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f666f-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> -Location <String>
 -VirtualHubId <String> -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32>
 [-Identity <PSManagedServiceIdentity>] [-BootStrapConfigurationBlob <String[]>]
 [-CloudInitConfigurationBlob <String[]>] [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f666f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f666f-106">ResourceIdParameterSet</span></span>
```
New-AzNetworkVirtualAppliance -ResourceId <String> -Location <String> -VirtualHubId <String>
 -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32> [-Identity <PSManagedServiceIdentity>]
 [-BootStrapConfigurationBlob <String[]>] [-CloudInitConfigurationBlob <String[]>]
 [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f666f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f666f-107">DESCRIPTION</span></span>
<span data-ttu-id="f666f-108">A New-AzNetworkVirtualAppliance parancs létrehoz egy virtuális hálózati eszköz típusú erőforrást az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="f666f-108">The New-AzNetworkVirtualAppliance command creates a Network Virtual Appliance resource in Azure.</span></span>

## <span data-ttu-id="f666f-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f666f-109">EXAMPLES</span></span>

### <span data-ttu-id="f666f-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="f666f-110">Example 1</span></span>
```powershell
PS C:\> $sku=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
PS C:\> $hub=Get-AzVirtualHub -ResourceGroupName testrg -Name hub
PS C:\> $nva=New-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva -Location eastus2 -VirtualApplianceAsn 1270 -VirtualHubId $hub.Id -Sku $sku -CloudInitConfiguration "echo Hello World!"

```

<span data-ttu-id="f666f-111">Létrehoz egy új hálózati virtuális eszköz típusú erőforrást az erőforráscsoportban: testrg.</span><span class="sxs-lookup"><span data-stu-id="f666f-111">Creates a new Network Virtual Appliance resource in resource group: testrg.</span></span>

## <span data-ttu-id="f666f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f666f-112">PARAMETERS</span></span>

### <span data-ttu-id="f666f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f666f-113">-AsJob</span></span>
<span data-ttu-id="f666f-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f666f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f666f-115">-BootStrapConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="f666f-115">-BootStrapConfigurationBlob</span></span>
<span data-ttu-id="f666f-116">A Bootstrap konfigurációs blob URL-címe.</span><span class="sxs-lookup"><span data-stu-id="f666f-116">The Bootstrap configuration blob URL.</span></span>

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

### <span data-ttu-id="f666f-117">-CloudInitConfiguration</span><span class="sxs-lookup"><span data-stu-id="f666f-117">-CloudInitConfiguration</span></span>
<span data-ttu-id="f666f-118">A Cloudinit beállítása egyszerű szövegként.</span><span class="sxs-lookup"><span data-stu-id="f666f-118">The Cloudinit configuration as plain text.</span></span>

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

### <span data-ttu-id="f666f-119">-CloudInitConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="f666f-119">-CloudInitConfigurationBlob</span></span>
<span data-ttu-id="f666f-120">A Cloudinit konfigurációs blobtároló URL-címe.</span><span class="sxs-lookup"><span data-stu-id="f666f-120">The Cloudinit configuration blob storage URL.</span></span>

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

### <span data-ttu-id="f666f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f666f-121">-DefaultProfile</span></span>
<span data-ttu-id="f666f-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f666f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f666f-123">-Force</span><span class="sxs-lookup"><span data-stu-id="f666f-123">-Force</span></span>
<span data-ttu-id="f666f-124">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="f666f-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f666f-125">-Identity</span><span class="sxs-lookup"><span data-stu-id="f666f-125">-Identity</span></span>
<span data-ttu-id="f666f-126">A Felügyelt identitás.</span><span class="sxs-lookup"><span data-stu-id="f666f-126">The Managed identity.</span></span>

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

### <span data-ttu-id="f666f-127">-Location</span><span class="sxs-lookup"><span data-stu-id="f666f-127">-Location</span></span>
<span data-ttu-id="f666f-128">A nyilvános IP-cím helye.</span><span class="sxs-lookup"><span data-stu-id="f666f-128">The public IP address location.</span></span>

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

### <span data-ttu-id="f666f-129">-Name</span><span class="sxs-lookup"><span data-stu-id="f666f-129">-Name</span></span>
<span data-ttu-id="f666f-130">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f666f-130">The resource name.</span></span>

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

### <span data-ttu-id="f666f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f666f-131">-ResourceGroupName</span></span>
<span data-ttu-id="f666f-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f666f-132">The resource group name.</span></span>

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

### <span data-ttu-id="f666f-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f666f-133">-ResourceId</span></span>
<span data-ttu-id="f666f-134">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f666f-134">The resource Id.</span></span>

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

### <span data-ttu-id="f666f-135">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="f666f-135">-Sku</span></span>
<span data-ttu-id="f666f-136">A virtuális eszköz termékváltozata.</span><span class="sxs-lookup"><span data-stu-id="f666f-136">The Sku of the Virtual Appliance.</span></span>

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

### <span data-ttu-id="f666f-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="f666f-137">-Tag</span></span>
<span data-ttu-id="f666f-138">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="f666f-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f666f-139">-VirtualApplianceAsn</span><span class="sxs-lookup"><span data-stu-id="f666f-139">-VirtualApplianceAsn</span></span>
<span data-ttu-id="f666f-140">A virtuális eszköz ASN-száma.</span><span class="sxs-lookup"><span data-stu-id="f666f-140">The ASN number of the Virtual Appliance.</span></span>

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

### <span data-ttu-id="f666f-141">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="f666f-141">-VirtualHubId</span></span>
<span data-ttu-id="f666f-142">A virtuális központ erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f666f-142">The Resource Id of the Virtual Hub.</span></span>

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

### <span data-ttu-id="f666f-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f666f-143">-Confirm</span></span>
<span data-ttu-id="f666f-144">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f666f-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f666f-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f666f-145">-WhatIf</span></span>
<span data-ttu-id="f666f-146">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f666f-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f666f-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f666f-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f666f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f666f-148">CommonParameters</span></span>
<span data-ttu-id="f666f-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f666f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f666f-150">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f666f-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f666f-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f666f-151">INPUTS</span></span>

### <span data-ttu-id="f666f-152">System.String</span><span class="sxs-lookup"><span data-stu-id="f666f-152">System.String</span></span>

### <span data-ttu-id="f666f-153">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="f666f-153">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

### <span data-ttu-id="f666f-154">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f666f-154">System.Int32</span></span>

### <span data-ttu-id="f666f-155">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="f666f-155">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

### <span data-ttu-id="f666f-156">System.String[]</span><span class="sxs-lookup"><span data-stu-id="f666f-156">System.String[]</span></span>

### <span data-ttu-id="f666f-157">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f666f-157">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f666f-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f666f-158">OUTPUTS</span></span>

### <span data-ttu-id="f666f-159">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="f666f-159">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="f666f-160">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f666f-160">NOTES</span></span>

## <span data-ttu-id="f666f-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f666f-161">RELATED LINKS</span></span>
