---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultNetworkRuleSet.md
ms.openlocfilehash: 6d264ff7e2f12777845edbf2d56cae3d8b59ddb0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195899"
---
# <span data-ttu-id="43b68-101">Update-AzKeyVaultNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="43b68-101">Update-AzKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="43b68-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="43b68-102">SYNOPSIS</span></span>
<span data-ttu-id="43b68-103">A Hálózatfigyelő által beállított hálózati szabály frissítése</span><span class="sxs-lookup"><span data-stu-id="43b68-103">Updates the network rule set on a key vault.</span></span>

## <span data-ttu-id="43b68-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="43b68-104">SYNTAX</span></span>

### <span data-ttu-id="43b68-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="43b68-105">ByVaultName (Default)</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43b68-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="43b68-106">ByInputObject</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-InputObject] <PSKeyVault>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43b68-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="43b68-107">ByResourceId</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-ResourceId] <String>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43b68-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="43b68-108">DESCRIPTION</span></span>
<span data-ttu-id="43b68-109">Az **Update-AzKeyVaultNetworkRuleSet** parancs a megadott kulcs boltozatára érvényes hálózati szabályokat frissíti.</span><span class="sxs-lookup"><span data-stu-id="43b68-109">The **Update-AzKeyVaultNetworkRuleSet** command updates the network rules in effect on the specified key vault.</span></span> 

## <span data-ttu-id="43b68-110">Példák</span><span class="sxs-lookup"><span data-stu-id="43b68-110">EXAMPLES</span></span>

### <span data-ttu-id="43b68-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="43b68-111">Example 1</span></span>
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

<span data-ttu-id="43b68-112">Ez a parancs frissíti a megadott IP-tartománnyal és a virtuális hálózat "myVault" nevű boltozatát, amely lehetővé teszi az Azure Services hálózati szabályának megkerülését.</span><span class="sxs-lookup"><span data-stu-id="43b68-112">This command updates the network ruleset on the vault named 'myVault' for the specified IP range and the virtual network, allowing bypassing of the network rule for Azure services.</span></span>

### <span data-ttu-id="43b68-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="43b68-113">Example 2</span></span>

<span data-ttu-id="43b68-114">A Hálózatfigyelő által beállított hálózati szabály frissítése</span><span class="sxs-lookup"><span data-stu-id="43b68-114">Updates the network rule set on a key vault.</span></span> <span data-ttu-id="43b68-115">autogenerated</span><span class="sxs-lookup"><span data-stu-id="43b68-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Update-AzKeyVaultNetworkRuleSet -DefaultAction Allow -VaultName 'myVault'
```

## <span data-ttu-id="43b68-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="43b68-116">PARAMETERS</span></span>

### <span data-ttu-id="43b68-117">-Kitérő</span><span class="sxs-lookup"><span data-stu-id="43b68-117">-Bypass</span></span>
<span data-ttu-id="43b68-118">A hálózati szabály megkerülését adja meg.</span><span class="sxs-lookup"><span data-stu-id="43b68-118">Specifies bypass of network rule.</span></span>

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

### <span data-ttu-id="43b68-119">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="43b68-119">-DefaultAction</span></span>
<span data-ttu-id="43b68-120">A hálózati szabály alapértelmezett működését adja meg.</span><span class="sxs-lookup"><span data-stu-id="43b68-120">Specifies default action of network rule.</span></span>

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

### <span data-ttu-id="43b68-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43b68-121">-DefaultProfile</span></span>
<span data-ttu-id="43b68-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="43b68-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43b68-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43b68-123">-InputObject</span></span>
<span data-ttu-id="43b68-124">A boltozat objektum</span><span class="sxs-lookup"><span data-stu-id="43b68-124">KeyVault object</span></span>

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

### <span data-ttu-id="43b68-125">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="43b68-125">-IpAddressRange</span></span>
<span data-ttu-id="43b68-126">A hálózati szabály engedélyezett hálózati IP-címének hatókörét adja meg.</span><span class="sxs-lookup"><span data-stu-id="43b68-126">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="43b68-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43b68-127">-PassThru</span></span>
<span data-ttu-id="43b68-128">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="43b68-128">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="43b68-129">Ha meg van adva ez a kapcsoló, a program a frissített kulcsfájl-objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="43b68-129">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="43b68-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43b68-130">-ResourceGroupName</span></span>
<span data-ttu-id="43b68-131">Annak a kulcsfájl-csoportnak a nevét adja meg, akinek a hálózati szabálya módosul.</span><span class="sxs-lookup"><span data-stu-id="43b68-131">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="43b68-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43b68-132">-ResourceId</span></span>
<span data-ttu-id="43b68-133">A főkészlet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="43b68-133">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="43b68-134">-VaultName</span><span class="sxs-lookup"><span data-stu-id="43b68-134">-VaultName</span></span>
<span data-ttu-id="43b68-135">Annak a kulcsnak a nevét adja meg, amelynek a hálózati szabályait módosították.</span><span class="sxs-lookup"><span data-stu-id="43b68-135">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="43b68-136">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="43b68-136">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="43b68-137">A hálózati szabály engedélyezett virtuális hálózati erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="43b68-137">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="43b68-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="43b68-138">-Confirm</span></span>
<span data-ttu-id="43b68-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="43b68-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43b68-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43b68-140">-WhatIf</span></span>
<span data-ttu-id="43b68-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="43b68-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43b68-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="43b68-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43b68-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43b68-143">CommonParameters</span></span>
<span data-ttu-id="43b68-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="43b68-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43b68-145">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="43b68-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43b68-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="43b68-146">INPUTS</span></span>

### <span data-ttu-id="43b68-147">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="43b68-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="43b68-148">System. String</span><span class="sxs-lookup"><span data-stu-id="43b68-148">System.String</span></span>

### <span data-ttu-id="43b68-149">System. null ' 1 [[Microsoft. Azure. commands. PSKeyVaultNetworkRuleDefaultActionEnum. models., Microsoft. Azure. PowerShell. parancsmagok. Vault, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="43b68-149">System.Nullable\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="43b68-150">System. null ' 1 [[Microsoft. Azure. commands. PSKeyVaultNetworkRuleBypassEnum. models., Microsoft. Azure. PowerShell. parancsmagok. Vault, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="43b68-150">System.Nullable\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="43b68-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43b68-151">OUTPUTS</span></span>

### <span data-ttu-id="43b68-152">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="43b68-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="43b68-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="43b68-153">NOTES</span></span>

## <span data-ttu-id="43b68-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43b68-154">RELATED LINKS</span></span>
