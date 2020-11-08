---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/new-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
ms.openlocfilehash: 09f1cd27e9af0c6442afa00d5301975cae8fbdeb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017811"
---
# <span data-ttu-id="44fdf-101">New-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="44fdf-101">New-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="44fdf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="44fdf-102">SYNOPSIS</span></span>
<span data-ttu-id="44fdf-103">Új munkaterületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="44fdf-103">Creates a new workspace.</span></span>

## <span data-ttu-id="44fdf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="44fdf-104">SYNTAX</span></span>

```
New-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-ManagedResourceGroupName <String>] [-PrepareEncryption]
 [-PrivateSubnetName <String>] [-PublicSubnetName <String>] [-RequireInfrastructureEncryption] [-Sku <String>]
 [-Tag <Hashtable>] [-VirtualNetworkId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="44fdf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="44fdf-105">DESCRIPTION</span></span>
<span data-ttu-id="44fdf-106">Új munkaterületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="44fdf-106">Creates a new workspace.</span></span>

## <span data-ttu-id="44fdf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="44fdf-107">EXAMPLES</span></span>

### <span data-ttu-id="44fdf-108">Példa 1: Databricks-munkaterület létrehozása</span><span class="sxs-lookup"><span data-stu-id="44fdf-108">Example 1: Create a Databricks workspace</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup -Location eastus -ManagedResourceGroupName databricks-group -Sku standard

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="44fdf-109">Ez a parancs létrehoz egy Databricks-munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="44fdf-109">This command creates a Databricks workspace.</span></span>

### <span data-ttu-id="44fdf-110">2. példa: Databricks-munkaterület létrehozása testreszabott virtuális hálózattal</span><span class="sxs-lookup"><span data-stu-id="44fdf-110">Example 2: Create a Databricks workspace with a customized virtual network</span></span>
```powershell
PS C:\> $dlg = New-AzDelegation -Name dbrdl -ServiceName "Microsoft.Databricks/workspaces"
PS C:\> $rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName testgroup -Location eastus -Name nsg-test -SecurityRules $rdpRule
PS C:\> $privSubnet = New-AzVirtualNetworkSubnetConfig -Name priv-sub -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup -Delegation $dlg
PS C:\> $pubSubnet = New-AzVirtualNetworkSubnetConfig -Name pub-sub  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup -Delegation $dlg
PS C:\> $testVN = New-AzVirtualNetwork -Name testvn -ResourceGroupName testgroup -Location eastus -AddressPrefix "10.0.0.0/16" -Subnet $privSubnet,$pubSubnet
PS C:\> New-AzDatabricksWorkspace -Name databricks-test-with-custom-vn -ResourceGroupName testgroup -Location eastus -VirtualNetworkId $testVN.Id -PrivateSubnetName $privSubnet.Name -PublicSubnetName $privSubnet.Name -Sku standard

Location Name                           Type
-------- ----                           ----
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="44fdf-111">Ez a parancs létrehoz egy Databricks-munkaterületet egy erőforrás-csoportban testre szabott virtuális hálózattal.</span><span class="sxs-lookup"><span data-stu-id="44fdf-111">This command creates a Databricks workspace with customized virtual network in a resource group.</span></span>

### <span data-ttu-id="44fdf-112">3. példa: Databricks munkaterület létrehozása a titkosítás engedélyezésével</span><span class="sxs-lookup"><span data-stu-id="44fdf-112">Example 3: Create a Databricks workspace with enable encryption</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test02 -ResourceGroupName testgroup -PrepareEncryption -Location "East US 2 EUAP" -Sku premium

Location Name            Type
-------- ----            ----
eastus   databricks-test02 Microsoft.Databricks/workspaces
```

<span data-ttu-id="44fdf-113">Ez a parancs létrehoz egy Databricks-munkaterületet, és a titkosításra való felkészülésre állítja be.</span><span class="sxs-lookup"><span data-stu-id="44fdf-113">This command creates a Databricks workspace and sets it to prepare for encryption.</span></span>
<span data-ttu-id="44fdf-114">További információt a titkosítással kapcsolatos további beállítások Update-AzDatabricksWorkspace című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="44fdf-114">Please refer to the examples of Update-AzDatabricksWorkspace for more settings to encryption.</span></span>

## <span data-ttu-id="44fdf-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="44fdf-115">PARAMETERS</span></span>

### <span data-ttu-id="44fdf-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44fdf-116">-AsJob</span></span>
<span data-ttu-id="44fdf-117">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="44fdf-117">Run the command as a job</span></span>

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

### <span data-ttu-id="44fdf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44fdf-118">-DefaultProfile</span></span>
<span data-ttu-id="44fdf-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="44fdf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44fdf-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="44fdf-120">-Location</span></span>
<span data-ttu-id="44fdf-121">Az a földrajzi hely, ahol az erőforrás él</span><span class="sxs-lookup"><span data-stu-id="44fdf-121">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="44fdf-122">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44fdf-122">-ManagedResourceGroupName</span></span>
<span data-ttu-id="44fdf-123">A felügyelt erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="44fdf-123">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44fdf-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="44fdf-124">-Name</span></span>
<span data-ttu-id="44fdf-125">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="44fdf-125">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44fdf-126">-Várva</span><span class="sxs-lookup"><span data-stu-id="44fdf-126">-NoWait</span></span>
<span data-ttu-id="44fdf-127">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="44fdf-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="44fdf-128">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="44fdf-128">-PrepareEncryption</span></span>
<span data-ttu-id="44fdf-129">A munkaterület előkészítése titkosításhoz.</span><span class="sxs-lookup"><span data-stu-id="44fdf-129">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="44fdf-130">Engedélyezi a felügyelt tárterület-fiók felügyelt identitását.</span><span class="sxs-lookup"><span data-stu-id="44fdf-130">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="44fdf-131">-PrivateSubnetName</span><span class="sxs-lookup"><span data-stu-id="44fdf-131">-PrivateSubnetName</span></span>
<span data-ttu-id="44fdf-132">A virtuális hálózatban lévő privát alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="44fdf-132">The name of the Private Subnet within the Virtual Network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44fdf-133">-PublicSubnetName</span><span class="sxs-lookup"><span data-stu-id="44fdf-133">-PublicSubnetName</span></span>
<span data-ttu-id="44fdf-134">A virtuális hálózatban lévő nyilvános alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="44fdf-134">The name of a Public Subnet within the Virtual Network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44fdf-135">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="44fdf-135">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="44fdf-136">Logikai érték, amely azt jelzi, hogy a DBFS-os gyökérszintű fájlrendszer engedélyezve van-e a másodlagos titkosítási réteggel a REST-alapú adatok platformon kezelt kulcsaival.</span><span class="sxs-lookup"><span data-stu-id="44fdf-136">A boolean indicating whether or not the DBFS root file system will be enabled with secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="44fdf-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44fdf-137">-ResourceGroupName</span></span>
<span data-ttu-id="44fdf-138">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="44fdf-138">The name of the resource group.</span></span>
<span data-ttu-id="44fdf-139">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="44fdf-139">The name is case insensitive.</span></span>

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

### <span data-ttu-id="44fdf-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="44fdf-140">-Sku</span></span>
<span data-ttu-id="44fdf-141">A SKU neve.</span><span class="sxs-lookup"><span data-stu-id="44fdf-141">The SKU name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44fdf-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="44fdf-142">-SubscriptionId</span></span>
<span data-ttu-id="44fdf-143">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="44fdf-143">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44fdf-144">-Címke</span><span class="sxs-lookup"><span data-stu-id="44fdf-144">-Tag</span></span>
<span data-ttu-id="44fdf-145">Erőforrás-címkék.</span><span class="sxs-lookup"><span data-stu-id="44fdf-145">Resource tags.</span></span>

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

### <span data-ttu-id="44fdf-146">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="44fdf-146">-VirtualNetworkId</span></span>
<span data-ttu-id="44fdf-147">Annak a virtuális hálózatnak az azonosítója, amelyhez a Databricks-fürtöt létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="44fdf-147">The ID of a Virtual Network where this Databricks Cluster should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44fdf-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="44fdf-148">-Confirm</span></span>
<span data-ttu-id="44fdf-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="44fdf-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44fdf-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44fdf-150">-WhatIf</span></span>
<span data-ttu-id="44fdf-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="44fdf-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44fdf-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="44fdf-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44fdf-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44fdf-153">CommonParameters</span></span>
<span data-ttu-id="44fdf-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="44fdf-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44fdf-155">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="44fdf-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44fdf-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="44fdf-156">INPUTS</span></span>

## <span data-ttu-id="44fdf-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="44fdf-157">OUTPUTS</span></span>

### <span data-ttu-id="44fdf-158">Microsoft. Azure. PowerShell. parancsmagok. Databricks. modellek. Api20180401. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="44fdf-158">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="44fdf-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="44fdf-159">NOTES</span></span>

<span data-ttu-id="44fdf-160">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="44fdf-160">ALIASES</span></span>

## <span data-ttu-id="44fdf-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="44fdf-161">RELATED LINKS</span></span>

