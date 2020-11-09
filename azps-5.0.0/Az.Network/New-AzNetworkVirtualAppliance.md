---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 9b3991a24430afa74853f742bffa12b772dbeaf2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301481"
---
# <span data-ttu-id="3d67c-101">New-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="3d67c-101">New-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="3d67c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3d67c-102">SYNOPSIS</span></span>
<span data-ttu-id="3d67c-103">Hozzon létre egy hálózati virtuális készülék erőforrást.</span><span class="sxs-lookup"><span data-stu-id="3d67c-103">Create a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="3d67c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3d67c-104">SYNTAX</span></span>

### <span data-ttu-id="3d67c-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3d67c-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> -Location <String>
 -VirtualHubId <String> -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32>
 [-Identity <PSManagedServiceIdentity>] [-BootStrapConfigurationBlob <String[]>]
 [-CloudInitConfigurationBlob <String[]>] [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d67c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d67c-106">ResourceIdParameterSet</span></span>
```
New-AzNetworkVirtualAppliance -ResourceId <String> -Location <String> -VirtualHubId <String>
 -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32> [-Identity <PSManagedServiceIdentity>]
 [-BootStrapConfigurationBlob <String[]>] [-CloudInitConfigurationBlob <String[]>]
 [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d67c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3d67c-107">DESCRIPTION</span></span>
<span data-ttu-id="3d67c-108">A New-AzNetworkVirtualAppliance parancs létrehoz egy hálózati Virtual Appliance-erőforrást az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="3d67c-108">The New-AzNetworkVirtualAppliance command creates a Network Virtual Appliance resource in Azure.</span></span>

## <span data-ttu-id="3d67c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3d67c-109">EXAMPLES</span></span>

### <span data-ttu-id="3d67c-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3d67c-110">Example 1</span></span>
```powershell
PS C:\> $sku=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
PS C:\> $hub=Get-AzVirtualHub -ResourceGroupName testrg -Name hub
PS C:\> $nva=New-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva -Location eastus2 -VirtualApplianceAsn 1270 -VirtualHubId $hub.Id -Sku $sku -CloudInitConfiguration "echo Hello World!"

```

<span data-ttu-id="3d67c-111">Új hálózati virtuális készülék erőforrást hoz létre az erőforráscsoport: testrg.</span><span class="sxs-lookup"><span data-stu-id="3d67c-111">Creates a new Network Virtual Appliance resource in resource group: testrg.</span></span>

## <span data-ttu-id="3d67c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3d67c-112">PARAMETERS</span></span>

### <span data-ttu-id="3d67c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d67c-113">-AsJob</span></span>
<span data-ttu-id="3d67c-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3d67c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d67c-115">-BootStrapConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="3d67c-115">-BootStrapConfigurationBlob</span></span>
<span data-ttu-id="3d67c-116">A bootstrap konfigurációs blob URL-címe.</span><span class="sxs-lookup"><span data-stu-id="3d67c-116">The Bootstrap configuration blob URL.</span></span>

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

### <span data-ttu-id="3d67c-117">-CloudInitConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d67c-117">-CloudInitConfiguration</span></span>
<span data-ttu-id="3d67c-118">A Cloudinit-konfiguráció egyszerű szövegként van formázva.</span><span class="sxs-lookup"><span data-stu-id="3d67c-118">The Cloudinit configuration as plain text.</span></span>

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

### <span data-ttu-id="3d67c-119">-CloudInitConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="3d67c-119">-CloudInitConfigurationBlob</span></span>
<span data-ttu-id="3d67c-120">A Cloudinit-konfiguráció blob-tárolójának URL-címe.</span><span class="sxs-lookup"><span data-stu-id="3d67c-120">The Cloudinit configuration blob storage URL.</span></span>

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

### <span data-ttu-id="3d67c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d67c-121">-DefaultProfile</span></span>
<span data-ttu-id="3d67c-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3d67c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d67c-123">-Force</span><span class="sxs-lookup"><span data-stu-id="3d67c-123">-Force</span></span>
<span data-ttu-id="3d67c-124">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3d67c-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="3d67c-125">– Identitás</span><span class="sxs-lookup"><span data-stu-id="3d67c-125">-Identity</span></span>
<span data-ttu-id="3d67c-126">A felügyelt identitás.</span><span class="sxs-lookup"><span data-stu-id="3d67c-126">The Managed identity.</span></span>

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

### <span data-ttu-id="3d67c-127">-Hely</span><span class="sxs-lookup"><span data-stu-id="3d67c-127">-Location</span></span>
<span data-ttu-id="3d67c-128">A nyilvános IP-cím helye.</span><span class="sxs-lookup"><span data-stu-id="3d67c-128">The public IP address location.</span></span>

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

### <span data-ttu-id="3d67c-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3d67c-129">-Name</span></span>
<span data-ttu-id="3d67c-130">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="3d67c-130">The resource name.</span></span>

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

### <span data-ttu-id="3d67c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d67c-131">-ResourceGroupName</span></span>
<span data-ttu-id="3d67c-132">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="3d67c-132">The resource group name.</span></span>

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

### <span data-ttu-id="3d67c-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d67c-133">-ResourceId</span></span>
<span data-ttu-id="3d67c-134">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="3d67c-134">The resource Id.</span></span>

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

### <span data-ttu-id="3d67c-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="3d67c-135">-Sku</span></span>
<span data-ttu-id="3d67c-136">A virtuális készülék SKU-je.</span><span class="sxs-lookup"><span data-stu-id="3d67c-136">The Sku of the Virtual Appliance.</span></span>

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

### <span data-ttu-id="3d67c-137">-Címke</span><span class="sxs-lookup"><span data-stu-id="3d67c-137">-Tag</span></span>
<span data-ttu-id="3d67c-138">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="3d67c-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="3d67c-139">-VirtualApplianceAsn</span><span class="sxs-lookup"><span data-stu-id="3d67c-139">-VirtualApplianceAsn</span></span>
<span data-ttu-id="3d67c-140">A virtuális készülék ASN-száma.</span><span class="sxs-lookup"><span data-stu-id="3d67c-140">The ASN number of the Virtual Appliance.</span></span>

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

### <span data-ttu-id="3d67c-141">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="3d67c-141">-VirtualHubId</span></span>
<span data-ttu-id="3d67c-142">A virtuális hub erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3d67c-142">The Resource Id of the Virtual Hub.</span></span>

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

### <span data-ttu-id="3d67c-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3d67c-143">-Confirm</span></span>
<span data-ttu-id="3d67c-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3d67c-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d67c-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d67c-145">-WhatIf</span></span>
<span data-ttu-id="3d67c-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3d67c-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d67c-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3d67c-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d67c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d67c-148">CommonParameters</span></span>
<span data-ttu-id="3d67c-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3d67c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d67c-150">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3d67c-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d67c-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d67c-151">INPUTS</span></span>

### <span data-ttu-id="3d67c-152">System. String</span><span class="sxs-lookup"><span data-stu-id="3d67c-152">System.String</span></span>

### <span data-ttu-id="3d67c-153">Microsoft. Azure. commands. Network. models. PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="3d67c-153">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

### <span data-ttu-id="3d67c-154">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3d67c-154">System.Int32</span></span>

### <span data-ttu-id="3d67c-155">Microsoft. Azure. commands. Network. models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="3d67c-155">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

### <span data-ttu-id="3d67c-156">System. string []</span><span class="sxs-lookup"><span data-stu-id="3d67c-156">System.String[]</span></span>

### <span data-ttu-id="3d67c-157">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3d67c-157">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3d67c-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d67c-158">OUTPUTS</span></span>

### <span data-ttu-id="3d67c-159">Microsoft. Azure. commands. Network. models. PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="3d67c-159">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="3d67c-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3d67c-160">NOTES</span></span>

## <span data-ttu-id="3d67c-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3d67c-161">RELATED LINKS</span></span>
