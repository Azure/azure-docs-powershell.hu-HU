---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultNetworkRuleSet.md
ms.openlocfilehash: 6d264ff7e2f12777845edbf2d56cae3d8b59ddb0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152602"
---
# <span data-ttu-id="4afdf-101">Update-AzKeyVaultNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="4afdf-101">Update-AzKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="4afdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4afdf-102">SYNOPSIS</span></span>
<span data-ttu-id="4afdf-103">Frissíti a hálózati szabálykészletet egy kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="4afdf-103">Updates the network rule set on a key vault.</span></span>

## <span data-ttu-id="4afdf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4afdf-104">SYNTAX</span></span>

### <span data-ttu-id="4afdf-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4afdf-105">ByVaultName (Default)</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4afdf-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4afdf-106">ByInputObject</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-InputObject] <PSKeyVault>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4afdf-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4afdf-107">ByResourceId</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-ResourceId] <String>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4afdf-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4afdf-108">DESCRIPTION</span></span>
<span data-ttu-id="4afdf-109">Az **Update-AzKeyVaultNetworkRuleSet** parancs frissíti a hálózati szabályokat a megadott kulcstárra érvényben.</span><span class="sxs-lookup"><span data-stu-id="4afdf-109">The **Update-AzKeyVaultNetworkRuleSet** command updates the network rules in effect on the specified key vault.</span></span> 

## <span data-ttu-id="4afdf-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4afdf-110">EXAMPLES</span></span>

### <span data-ttu-id="4afdf-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="4afdf-111">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault 
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Update-AzKeyVaultNetworkRuleSet -VaultName 'myVault' -ResourceGroupName myRG -Bypass AzureServices -IpAddressRange "10.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId -PassThru

Vault Name                       : myVault
Resource Group Name              : myRG
Location                         : West US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/myvault
Vault URI                        : https://myvault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover, backup, restore
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update, recover, backup, restore


Network Rule Set                 :
                                   Default Action                             : Allow
                                   Bypass                                     : AzureServices
                                   IP Rules                                   : 10.0.1.0/24
                                   Virtual Network Rules                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-
                                   xxxxxxxxxxxxx/resourcegroups/myrg/providers/microsoft.network/virtualnetworks/myvn
                                   et/subnets/frontendsubnet

Tags                             :
```

<span data-ttu-id="4afdf-112">Ez a parancs frissíti a "myVault" nevű hálózati szabálykészletet a megadott IP-tartományra és a virtuális hálózatra, lehetővé téve ezzel a hálózati szabály megkerülését az Azure-szolgáltatásokban.</span><span class="sxs-lookup"><span data-stu-id="4afdf-112">This command updates the network ruleset on the vault named 'myVault' for the specified IP range and the virtual network, allowing bypassing of the network rule for Azure services.</span></span>

### <span data-ttu-id="4afdf-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="4afdf-113">Example 2</span></span>

<span data-ttu-id="4afdf-114">Frissíti a hálózati szabálykészletet egy kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="4afdf-114">Updates the network rule set on a key vault.</span></span> <span data-ttu-id="4afdf-115">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="4afdf-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Update-AzKeyVaultNetworkRuleSet -DefaultAction Allow -VaultName 'myVault'
```

## <span data-ttu-id="4afdf-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4afdf-116">PARAMETERS</span></span>

### <span data-ttu-id="4afdf-117">-Bypass</span><span class="sxs-lookup"><span data-stu-id="4afdf-117">-Bypass</span></span>
<span data-ttu-id="4afdf-118">A hálózati szabály megkerülését adja meg.</span><span class="sxs-lookup"><span data-stu-id="4afdf-118">Specifies bypass of network rule.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum]
Parameter Sets: (All)
Aliases:
Accepted values: None, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4afdf-119">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="4afdf-119">-DefaultAction</span></span>
<span data-ttu-id="4afdf-120">A hálózati szabály alapértelmezett műveletét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="4afdf-120">Specifies default action of network rule.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum]
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4afdf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4afdf-121">-DefaultProfile</span></span>
<span data-ttu-id="4afdf-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4afdf-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4afdf-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4afdf-123">-InputObject</span></span>
<span data-ttu-id="4afdf-124">KeyVault objektum</span><span class="sxs-lookup"><span data-stu-id="4afdf-124">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4afdf-125">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="4afdf-125">-IpAddressRange</span></span>
<span data-ttu-id="4afdf-126">Megadja a hálózati szabály engedélyezett IP-címtartományát.</span><span class="sxs-lookup"><span data-stu-id="4afdf-126">Specifies allowed network IP address range of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4afdf-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4afdf-127">-PassThru</span></span>
<span data-ttu-id="4afdf-128">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="4afdf-128">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="4afdf-129">Ha ez a kapcsoló meg van adva, akkor a frissített kulcs tárolóobjektumot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="4afdf-129">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="4afdf-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4afdf-130">-ResourceGroupName</span></span>
<span data-ttu-id="4afdf-131">Annak az erőforráscsoportnak a nevét adja meg, amely annak a kulcstárnak a nevét adja meg, amelynek a hálózati szabályát módosítják.</span><span class="sxs-lookup"><span data-stu-id="4afdf-131">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4afdf-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4afdf-132">-ResourceId</span></span>
<span data-ttu-id="4afdf-133">KeyVault Resource Id</span><span class="sxs-lookup"><span data-stu-id="4afdf-133">KeyVault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4afdf-134">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4afdf-134">-VaultName</span></span>
<span data-ttu-id="4afdf-135">Annak a kulcstárnak a nevét adja meg, amelynek a hálózati szabályát módosítják.</span><span class="sxs-lookup"><span data-stu-id="4afdf-135">Specifies the name of a key vault whose network rule is being modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4afdf-136">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="4afdf-136">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="4afdf-137">Megadja a hálózati szabály engedélyezett virtuális hálózati erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="4afdf-137">Specifies allowed virtual network resource identifier of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4afdf-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4afdf-138">-Confirm</span></span>
<span data-ttu-id="4afdf-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4afdf-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4afdf-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4afdf-140">-WhatIf</span></span>
<span data-ttu-id="4afdf-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4afdf-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4afdf-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4afdf-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4afdf-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4afdf-143">CommonParameters</span></span>
<span data-ttu-id="4afdf-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4afdf-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4afdf-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4afdf-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4afdf-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4afdf-146">INPUTS</span></span>

### <span data-ttu-id="4afdf-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="4afdf-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="4afdf-148">System.String</span><span class="sxs-lookup"><span data-stu-id="4afdf-148">System.String</span></span>

### <span data-ttu-id="4afdf-149">System.Nullable'1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="4afdf-149">System.Nullable\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="4afdf-150">System.Nullable'1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="4afdf-150">System.Nullable\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4afdf-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4afdf-151">OUTPUTS</span></span>

### <span data-ttu-id="4afdf-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="4afdf-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="4afdf-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4afdf-153">NOTES</span></span>

## <span data-ttu-id="4afdf-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4afdf-154">RELATED LINKS</span></span>
