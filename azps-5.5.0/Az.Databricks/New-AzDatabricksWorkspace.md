---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/new-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
ms.openlocfilehash: 0626559fd80a9ebd212c8f6ebb032755d25ba59c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204303"
---
# <span data-ttu-id="fd2ea-101">New-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="fd2ea-101">New-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="fd2ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd2ea-102">SYNOPSIS</span></span>
<span data-ttu-id="fd2ea-103">Új munkaterületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-103">Creates a new workspace.</span></span>

## <span data-ttu-id="fd2ea-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fd2ea-104">SYNTAX</span></span>

```
New-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-EnableNoPublicIP] [-ManagedResourceGroupName <String>] [-PrepareEncryption]
 [-PrivateSubnetName <String>] [-PublicSubnetName <String>] [-RequireInfrastructureEncryption] [-Sku <String>]
 [-Tag <Hashtable>] [-VirtualNetworkId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fd2ea-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fd2ea-105">DESCRIPTION</span></span>
<span data-ttu-id="fd2ea-106">Új munkaterületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-106">Creates a new workspace.</span></span>

## <span data-ttu-id="fd2ea-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fd2ea-107">EXAMPLES</span></span>

### <span data-ttu-id="fd2ea-108">1. példa: Adatkapcsolati munkaterület létrehozása</span><span class="sxs-lookup"><span data-stu-id="fd2ea-108">Example 1: Create a Databricks workspace</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup -Location eastus -ManagedResourceGroupName databricks-group -Sku standard

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="fd2ea-109">Ez a parancs egy Datab workspace-munkaterületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-109">This command creates a Databricks workspace.</span></span>

### <span data-ttu-id="fd2ea-110">2. példa: Adatkapcsolatú munkaterület létrehozása testre szabott virtuális hálózattal</span><span class="sxs-lookup"><span data-stu-id="fd2ea-110">Example 2: Create a Databricks workspace with a customized virtual network</span></span>
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

<span data-ttu-id="fd2ea-111">Ez a parancs létrehoz egy Datab workspace with customized virtual network in a resource group.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-111">This command creates a Databricks workspace with customized virtual network in a resource group.</span></span>

### <span data-ttu-id="fd2ea-112">3. példa: Adatkapcsolati munkaterület létrehozása titkosítás engedélyezésével</span><span class="sxs-lookup"><span data-stu-id="fd2ea-112">Example 3: Create a Databricks workspace with enable encryption</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test02 -ResourceGroupName testgroup -PrepareEncryption -Location "East US 2 EUAP" -Sku premium

Location Name            Type
-------- ----            ----
eastus   databricks-test02 Microsoft.Databricks/workspaces
```

<span data-ttu-id="fd2ea-113">Ez a parancs létrehoz egy Datab workspace-munkaterületet, és beállítja a titkosításra való felkészüléshez.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-113">This command creates a Databricks workspace and sets it to prepare for encryption.</span></span>
<span data-ttu-id="fd2ea-114">A titkosításra vonatkozó Update-AzDatabricksWorkspace további beállításokért tanulmányozza az itt látható példákat.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-114">Please refer to the examples of Update-AzDatabricksWorkspace for more settings to encryption.</span></span>

## <span data-ttu-id="fd2ea-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd2ea-115">PARAMETERS</span></span>

### <span data-ttu-id="fd2ea-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd2ea-116">-AsJob</span></span>
<span data-ttu-id="fd2ea-117">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="fd2ea-117">Run the command as a job</span></span>

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

### <span data-ttu-id="fd2ea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd2ea-118">-DefaultProfile</span></span>
<span data-ttu-id="fd2ea-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd2ea-120">-EnableNoPublicIP</span><span class="sxs-lookup"><span data-stu-id="fd2ea-120">-EnableNoPublicIP</span></span>
<span data-ttu-id="fd2ea-121">Az az érték, amelyet ehhez a mezőhöz kell használni.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-121">The value which should be used for this field.</span></span>

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

### <span data-ttu-id="fd2ea-122">-Location</span><span class="sxs-lookup"><span data-stu-id="fd2ea-122">-Location</span></span>
<span data-ttu-id="fd2ea-123">Az a földrajzi hely, ahol az erőforrás található</span><span class="sxs-lookup"><span data-stu-id="fd2ea-123">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="fd2ea-124">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd2ea-124">-ManagedResourceGroupName</span></span>
<span data-ttu-id="fd2ea-125">A felügyelt erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-125">The managed resource group name.</span></span>

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

### <span data-ttu-id="fd2ea-126">-Name</span><span class="sxs-lookup"><span data-stu-id="fd2ea-126">-Name</span></span>
<span data-ttu-id="fd2ea-127">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-127">The name of the workspace.</span></span>

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

### <span data-ttu-id="fd2ea-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fd2ea-128">-NoWait</span></span>
<span data-ttu-id="fd2ea-129">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="fd2ea-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fd2ea-130">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="fd2ea-130">-PrepareEncryption</span></span>
<span data-ttu-id="fd2ea-131">Készítse elő a munkaterületet titkosításra.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-131">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="fd2ea-132">Engedélyezi a Felügyelt identitást felügyelt tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-132">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="fd2ea-133">-PrivateSubnetName</span><span class="sxs-lookup"><span data-stu-id="fd2ea-133">-PrivateSubnetName</span></span>
<span data-ttu-id="fd2ea-134">A virtuális hálózaton belüli privát alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-134">The name of the Private Subnet within the Virtual Network.</span></span>

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

### <span data-ttu-id="fd2ea-135">-PublicSubnetName</span><span class="sxs-lookup"><span data-stu-id="fd2ea-135">-PublicSubnetName</span></span>
<span data-ttu-id="fd2ea-136">A virtuális hálózaton belüli nyilvános alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-136">The name of a Public Subnet within the Virtual Network.</span></span>

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

### <span data-ttu-id="fd2ea-137">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="fd2ea-137">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="fd2ea-138">Logikai érték, amely azt jelzi, hogy a DBFS-gyökérrendszer engedélyezve lesz-e másodlagos titkosítási réteggel, valamint platform felügyelt kulcsokkal az adatok nyugtatása esetén.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-138">A boolean indicating whether or not the DBFS root file system will be enabled with secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="fd2ea-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd2ea-139">-ResourceGroupName</span></span>
<span data-ttu-id="fd2ea-140">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-140">The name of the resource group.</span></span>
<span data-ttu-id="fd2ea-141">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="fd2ea-141">The name is case insensitive.</span></span>

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

### <span data-ttu-id="fd2ea-142">-Sku</span><span class="sxs-lookup"><span data-stu-id="fd2ea-142">-Sku</span></span>
<span data-ttu-id="fd2ea-143">Az termékváltozat neve.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-143">The SKU name.</span></span>

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

### <span data-ttu-id="fd2ea-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fd2ea-144">-SubscriptionId</span></span>
<span data-ttu-id="fd2ea-145">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="fd2ea-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="fd2ea-146">-Tag</span></span>
<span data-ttu-id="fd2ea-147">Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-147">Resource tags.</span></span>

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

### <span data-ttu-id="fd2ea-148">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="fd2ea-148">-VirtualNetworkId</span></span>
<span data-ttu-id="fd2ea-149">Annak a virtuális hálózatnak az azonosítója, ahol létre kell hoznunk ezt az adathalmazcsoportot.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-149">The ID of a Virtual Network where this Databricks Cluster should be created.</span></span>

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

### <span data-ttu-id="fd2ea-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd2ea-150">-Confirm</span></span>
<span data-ttu-id="fd2ea-151">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd2ea-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd2ea-152">-WhatIf</span></span>
<span data-ttu-id="fd2ea-153">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd2ea-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd2ea-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd2ea-155">CommonParameters</span></span>
<span data-ttu-id="fd2ea-156">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd2ea-157">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd2ea-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd2ea-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd2ea-158">INPUTS</span></span>

## <span data-ttu-id="fd2ea-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd2ea-159">OUTPUTS</span></span>

### <span data-ttu-id="fd2ea-160">Microsoft.Azure.PowerShell.Cmdlets.Databfüzets.Models.Api20180401.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="fd2ea-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="fd2ea-161">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fd2ea-161">NOTES</span></span>

<span data-ttu-id="fd2ea-162">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="fd2ea-162">ALIASES</span></span>

## <span data-ttu-id="fd2ea-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd2ea-163">RELATED LINKS</span></span>

