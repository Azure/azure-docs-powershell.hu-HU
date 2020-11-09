---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/new-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
ms.openlocfilehash: 09f1cd27e9af0c6442afa00d5301975cae8fbdeb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297320"
---
# <span data-ttu-id="51e58-101">New-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="51e58-101">New-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="51e58-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="51e58-102">SYNOPSIS</span></span>
<span data-ttu-id="51e58-103">Új munkaterületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="51e58-103">Creates a new workspace.</span></span>

## <span data-ttu-id="51e58-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="51e58-104">SYNTAX</span></span>

```
New-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-ManagedResourceGroupName <String>] [-PrepareEncryption]
 [-PrivateSubnetName <String>] [-PublicSubnetName <String>] [-RequireInfrastructureEncryption] [-Sku <String>]
 [-Tag <Hashtable>] [-VirtualNetworkId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="51e58-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="51e58-105">DESCRIPTION</span></span>
<span data-ttu-id="51e58-106">Új munkaterületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="51e58-106">Creates a new workspace.</span></span>

## <span data-ttu-id="51e58-107">Példák</span><span class="sxs-lookup"><span data-stu-id="51e58-107">EXAMPLES</span></span>

### <span data-ttu-id="51e58-108">Példa 1: Databricks-munkaterület létrehozása</span><span class="sxs-lookup"><span data-stu-id="51e58-108">Example 1: Create a Databricks workspace</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup -Location eastus -ManagedResourceGroupName databricks-group -Sku standard

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="51e58-109">Ez a parancs létrehoz egy Databricks-munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="51e58-109">This command creates a Databricks workspace.</span></span>

### <span data-ttu-id="51e58-110">2. példa: Databricks-munkaterület létrehozása testreszabott virtuális hálózattal</span><span class="sxs-lookup"><span data-stu-id="51e58-110">Example 2: Create a Databricks workspace with a customized virtual network</span></span>
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

<span data-ttu-id="51e58-111">Ez a parancs létrehoz egy Databricks-munkaterületet egy erőforrás-csoportban testre szabott virtuális hálózattal.</span><span class="sxs-lookup"><span data-stu-id="51e58-111">This command creates a Databricks workspace with customized virtual network in a resource group.</span></span>

### <span data-ttu-id="51e58-112">3. példa: Databricks munkaterület létrehozása a titkosítás engedélyezésével</span><span class="sxs-lookup"><span data-stu-id="51e58-112">Example 3: Create a Databricks workspace with enable encryption</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test02 -ResourceGroupName testgroup -PrepareEncryption -Location "East US 2 EUAP" -Sku premium

Location Name            Type
-------- ----            ----
eastus   databricks-test02 Microsoft.Databricks/workspaces
```

<span data-ttu-id="51e58-113">Ez a parancs létrehoz egy Databricks-munkaterületet, és a titkosításra való felkészülésre állítja be.</span><span class="sxs-lookup"><span data-stu-id="51e58-113">This command creates a Databricks workspace and sets it to prepare for encryption.</span></span>
<span data-ttu-id="51e58-114">További információt a titkosítással kapcsolatos további beállítások Update-AzDatabricksWorkspace című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="51e58-114">Please refer to the examples of Update-AzDatabricksWorkspace for more settings to encryption.</span></span>

## <span data-ttu-id="51e58-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="51e58-115">PARAMETERS</span></span>

### <span data-ttu-id="51e58-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51e58-116">-AsJob</span></span>
<span data-ttu-id="51e58-117">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="51e58-117">Run the command as a job</span></span>

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

### <span data-ttu-id="51e58-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51e58-118">-DefaultProfile</span></span>
<span data-ttu-id="51e58-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="51e58-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51e58-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="51e58-120">-Location</span></span>
<span data-ttu-id="51e58-121">Az a földrajzi hely, ahol az erőforrás él</span><span class="sxs-lookup"><span data-stu-id="51e58-121">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="51e58-122">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51e58-122">-ManagedResourceGroupName</span></span>
<span data-ttu-id="51e58-123">A felügyelt erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="51e58-123">The managed resource group name.</span></span>

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

### <span data-ttu-id="51e58-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="51e58-124">-Name</span></span>
<span data-ttu-id="51e58-125">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="51e58-125">The name of the workspace.</span></span>

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

### <span data-ttu-id="51e58-126">-Várva</span><span class="sxs-lookup"><span data-stu-id="51e58-126">-NoWait</span></span>
<span data-ttu-id="51e58-127">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="51e58-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="51e58-128">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="51e58-128">-PrepareEncryption</span></span>
<span data-ttu-id="51e58-129">A munkaterület előkészítése titkosításhoz.</span><span class="sxs-lookup"><span data-stu-id="51e58-129">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="51e58-130">Engedélyezi a felügyelt tárterület-fiók felügyelt identitását.</span><span class="sxs-lookup"><span data-stu-id="51e58-130">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="51e58-131">-PrivateSubnetName</span><span class="sxs-lookup"><span data-stu-id="51e58-131">-PrivateSubnetName</span></span>
<span data-ttu-id="51e58-132">A virtuális hálózatban lévő privát alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="51e58-132">The name of the Private Subnet within the Virtual Network.</span></span>

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

### <span data-ttu-id="51e58-133">-PublicSubnetName</span><span class="sxs-lookup"><span data-stu-id="51e58-133">-PublicSubnetName</span></span>
<span data-ttu-id="51e58-134">A virtuális hálózatban lévő nyilvános alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="51e58-134">The name of a Public Subnet within the Virtual Network.</span></span>

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

### <span data-ttu-id="51e58-135">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="51e58-135">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="51e58-136">Logikai érték, amely azt jelzi, hogy a DBFS-os gyökérszintű fájlrendszer engedélyezve van-e a másodlagos titkosítási réteggel a REST-alapú adatok platformon kezelt kulcsaival.</span><span class="sxs-lookup"><span data-stu-id="51e58-136">A boolean indicating whether or not the DBFS root file system will be enabled with secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="51e58-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51e58-137">-ResourceGroupName</span></span>
<span data-ttu-id="51e58-138">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="51e58-138">The name of the resource group.</span></span>
<span data-ttu-id="51e58-139">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="51e58-139">The name is case insensitive.</span></span>

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

### <span data-ttu-id="51e58-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="51e58-140">-Sku</span></span>
<span data-ttu-id="51e58-141">A SKU neve.</span><span class="sxs-lookup"><span data-stu-id="51e58-141">The SKU name.</span></span>

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

### <span data-ttu-id="51e58-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="51e58-142">-SubscriptionId</span></span>
<span data-ttu-id="51e58-143">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="51e58-143">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="51e58-144">-Címke</span><span class="sxs-lookup"><span data-stu-id="51e58-144">-Tag</span></span>
<span data-ttu-id="51e58-145">Erőforrás-címkék.</span><span class="sxs-lookup"><span data-stu-id="51e58-145">Resource tags.</span></span>

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

### <span data-ttu-id="51e58-146">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="51e58-146">-VirtualNetworkId</span></span>
<span data-ttu-id="51e58-147">Annak a virtuális hálózatnak az azonosítója, amelyhez a Databricks-fürtöt létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="51e58-147">The ID of a Virtual Network where this Databricks Cluster should be created.</span></span>

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

### <span data-ttu-id="51e58-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="51e58-148">-Confirm</span></span>
<span data-ttu-id="51e58-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="51e58-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51e58-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51e58-150">-WhatIf</span></span>
<span data-ttu-id="51e58-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="51e58-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51e58-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="51e58-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51e58-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51e58-153">CommonParameters</span></span>
<span data-ttu-id="51e58-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="51e58-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51e58-155">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="51e58-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51e58-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="51e58-156">INPUTS</span></span>

## <span data-ttu-id="51e58-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="51e58-157">OUTPUTS</span></span>

### <span data-ttu-id="51e58-158">Microsoft. Azure. PowerShell. parancsmagok. Databricks. modellek. Api20180401. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="51e58-158">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="51e58-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="51e58-159">NOTES</span></span>

<span data-ttu-id="51e58-160">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="51e58-160">ALIASES</span></span>

## <span data-ttu-id="51e58-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="51e58-161">RELATED LINKS</span></span>

