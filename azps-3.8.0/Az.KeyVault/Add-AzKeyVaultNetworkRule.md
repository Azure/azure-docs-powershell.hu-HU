---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultNetworkRule.md
ms.openlocfilehash: ee7b9672869bba13b72ddd7b5a1d0b26325e9f62
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847041"
---
# <span data-ttu-id="e9b57-101">Add-AzKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e9b57-101">Add-AzKeyVaultNetworkRule</span></span>

## <span data-ttu-id="e9b57-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e9b57-102">SYNOPSIS</span></span>
<span data-ttu-id="e9b57-103">Felvesz egy olyan szabályt, amely az ügyfél internetes címén alapuló fő boltozathoz való hozzáférés korlátozását jelenti.</span><span class="sxs-lookup"><span data-stu-id="e9b57-103">Adds a rule meant to restrict access to a key vault based on the client's internet address.</span></span>

## <span data-ttu-id="e9b57-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e9b57-104">SYNTAX</span></span>

### <span data-ttu-id="e9b57-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e9b57-105">ByVaultName (Default)</span></span>
```
Add-AzKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9b57-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e9b57-106">ByInputObject</span></span>
```
Add-AzKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9b57-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e9b57-107">ByResourceId</span></span>
```
Add-AzKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9b57-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e9b57-108">DESCRIPTION</span></span>
<span data-ttu-id="e9b57-109">Az **Add-AzKeyVaultNetworkRule** parancsmag hozzáférést ad vagy korlátoz a kulcsfájl eléréséhez az IP-címük vagy a virtuális hálózat által kijelölt hívók számára.</span><span class="sxs-lookup"><span data-stu-id="e9b57-109">The **Add-AzKeyVaultNetworkRule** cmdlet grants or restricts access to a key vault to a set of caller designated by their IP addresses or the virtual network to which they belong.</span></span> <span data-ttu-id="e9b57-110">A szabály lehetővé tette a hozzáférés korlátozását más felhasználók, alkalmazások vagy biztonsági csoportok számára, amelyekre a hozzáférési házirenden keresztül engedélyt kapott.</span><span class="sxs-lookup"><span data-stu-id="e9b57-110">The rule has the potential to restrict access for other users, applications, or security groups which have been granted permissions via the access policy.</span></span>

## <span data-ttu-id="e9b57-111">Példák</span><span class="sxs-lookup"><span data-stu-id="e9b57-111">EXAMPLES</span></span>

### <span data-ttu-id="e9b57-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e9b57-112">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault 
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Add-AzKeyVaultNetworkRule -VaultName myvault -IpAddressRange "10.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId -PassThru

Vault Name                       : myvault
Resource Group Name              : myRG
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myRG/providers
                                   /Microsoft.KeyVault/vaults/myvault
Vault URI                        : https://myvault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : True
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
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
                                   setissuers, recover
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update


Network Rule Set                 :
                                   Default Action                             : Allow
                                   Bypass                                     : AzureServices
                                   IP Rules                                   : 10.0.1.0/24
                                   Virtual Network Rules                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-
                                   xxxxxxxxxxxxx/resourcegroups/myRG/providers/microsoft.network/virtualnetworks/myvn
                                   et/subnets/frontendsubnet

Tags                             :
```

<span data-ttu-id="e9b57-113">Ez a parancs hálózati szabályt ad hozzá a megadott tárolóhoz, amely lehetővé teszi a megadott IP-cím elérését az $myNetworkResId által azonosított virtuális hálózatból.</span><span class="sxs-lookup"><span data-stu-id="e9b57-113">This command adds a network rule to the specified vault, allowing access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="e9b57-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e9b57-114">PARAMETERS</span></span>

### <span data-ttu-id="e9b57-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9b57-115">-DefaultProfile</span></span>
<span data-ttu-id="e9b57-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e9b57-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9b57-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9b57-117">-InputObject</span></span>
<span data-ttu-id="e9b57-118">A boltozat objektum</span><span class="sxs-lookup"><span data-stu-id="e9b57-118">KeyVault object</span></span>

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

### <span data-ttu-id="e9b57-119">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="e9b57-119">-IpAddressRange</span></span>
<span data-ttu-id="e9b57-120">A hálózati szabály engedélyezett hálózati IP-címének hatókörét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e9b57-120">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="e9b57-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9b57-121">-PassThru</span></span>
<span data-ttu-id="e9b57-122">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="e9b57-122">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e9b57-123">Ha meg van adva ez a kapcsoló, a program a frissített kulcsfájl-objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="e9b57-123">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="e9b57-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9b57-124">-ResourceGroupName</span></span>
<span data-ttu-id="e9b57-125">Annak a kulcsfájl-csoportnak a nevét adja meg, akinek a hálózati szabálya módosul.</span><span class="sxs-lookup"><span data-stu-id="e9b57-125">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="e9b57-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9b57-126">-ResourceId</span></span>
<span data-ttu-id="e9b57-127">A főkészlet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="e9b57-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="e9b57-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e9b57-128">-VaultName</span></span>
<span data-ttu-id="e9b57-129">Annak a kulcsnak a nevét adja meg, amelynek a hálózati szabályait módosították.</span><span class="sxs-lookup"><span data-stu-id="e9b57-129">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="e9b57-130">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="e9b57-130">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="e9b57-131">A hálózati szabály engedélyezett virtuális hálózati erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e9b57-131">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="e9b57-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e9b57-132">-Confirm</span></span>
<span data-ttu-id="e9b57-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e9b57-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9b57-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9b57-134">-WhatIf</span></span>
<span data-ttu-id="e9b57-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e9b57-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9b57-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e9b57-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9b57-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9b57-137">CommonParameters</span></span>
<span data-ttu-id="e9b57-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e9b57-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9b57-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e9b57-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9b57-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9b57-140">INPUTS</span></span>

### <span data-ttu-id="e9b57-141">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="e9b57-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="e9b57-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e9b57-142">System.String</span></span>

## <span data-ttu-id="e9b57-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9b57-143">OUTPUTS</span></span>

### <span data-ttu-id="e9b57-144">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="e9b57-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="e9b57-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e9b57-145">NOTES</span></span>

## <span data-ttu-id="e9b57-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e9b57-146">RELATED LINKS</span></span>
