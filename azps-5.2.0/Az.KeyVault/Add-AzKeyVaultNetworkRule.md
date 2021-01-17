---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultNetworkRule.md
ms.openlocfilehash: c437611603bab6b2c4b9fff5cd0696e306182afa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346674"
---
# <span data-ttu-id="154e8-101">Add-AzKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="154e8-101">Add-AzKeyVaultNetworkRule</span></span>

## <span data-ttu-id="154e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="154e8-102">SYNOPSIS</span></span>
<span data-ttu-id="154e8-103">Hozzáad egy szabályt, amely az ügyfél internetcíme alapján korlátozza a kulcstárhoz való hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="154e8-103">Adds a rule meant to restrict access to a key vault based on the client's internet address.</span></span>

## <span data-ttu-id="154e8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="154e8-104">SYNTAX</span></span>

### <span data-ttu-id="154e8-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="154e8-105">ByVaultName (Default)</span></span>
```
Add-AzKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="154e8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="154e8-106">ByInputObject</span></span>
```
Add-AzKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="154e8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="154e8-107">ByResourceId</span></span>
```
Add-AzKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="154e8-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="154e8-108">DESCRIPTION</span></span>
<span data-ttu-id="154e8-109">Az **Add-AzKeyVaultNetworkRule** parancsmag hozzáférést biztosít vagy korlátozza a kulcstárhoz való hozzáférést az IP-címük vagy a virtuális hálózat által kijelölt hívókészlethez.</span><span class="sxs-lookup"><span data-stu-id="154e8-109">The **Add-AzKeyVaultNetworkRule** cmdlet grants or restricts access to a key vault to a set of caller designated by their IP addresses or the virtual network to which they belong.</span></span> <span data-ttu-id="154e8-110">A szabály korlátozhatja a hozzáférést más felhasználók, alkalmazások vagy biztonsági csoportok számára, akik a hozzáférési házirenden keresztül kaptak engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="154e8-110">The rule has the potential to restrict access for other users, applications, or security groups which have been granted permissions via the access policy.</span></span>

<span data-ttu-id="154e8-111">Felhívjuk a figyelmét arra, hogy a (privát IP-címeken) belüli IP-tartományok nem használhatók hálózati `10.0.0.0-10.255.255.255` szabályok hozzáadására.</span><span class="sxs-lookup"><span data-stu-id="154e8-111">Please note that any IP range inside `10.0.0.0-10.255.255.255` (private IP addresses) cannot be used to add network rules.</span></span>

## <span data-ttu-id="154e8-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="154e8-112">EXAMPLES</span></span>

### <span data-ttu-id="154e8-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="154e8-113">Example 1</span></span>
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

<span data-ttu-id="154e8-114">Ez a parancs hozzáad egy hálózati szabályt a megadott tárolóhoz, amely lehetővé teszi a hozzáférést a megadott IP-címhez a $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="154e8-114">This command adds a network rule to the specified vault, allowing access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="154e8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="154e8-115">PARAMETERS</span></span>

### <span data-ttu-id="154e8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="154e8-116">-DefaultProfile</span></span>
<span data-ttu-id="154e8-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="154e8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="154e8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="154e8-118">-InputObject</span></span>
<span data-ttu-id="154e8-119">KeyVault objektum</span><span class="sxs-lookup"><span data-stu-id="154e8-119">KeyVault object</span></span>

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

### <span data-ttu-id="154e8-120">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="154e8-120">-IpAddressRange</span></span>
<span data-ttu-id="154e8-121">Megadja a hálózati szabály engedélyezett IP-címtartományát.</span><span class="sxs-lookup"><span data-stu-id="154e8-121">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="154e8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="154e8-122">-PassThru</span></span>
<span data-ttu-id="154e8-123">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="154e8-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="154e8-124">Ha ez a kapcsoló meg van adva, akkor a frissített kulcs tárolóobjektumot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="154e8-124">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="154e8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="154e8-125">-ResourceGroupName</span></span>
<span data-ttu-id="154e8-126">Annak az erőforráscsoportnak a nevét adja meg, amely annak a kulcstárnak a nevét adja meg, amelynek a hálózati szabályát módosítják.</span><span class="sxs-lookup"><span data-stu-id="154e8-126">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="154e8-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="154e8-127">-ResourceId</span></span>
<span data-ttu-id="154e8-128">KeyVault Resource Id</span><span class="sxs-lookup"><span data-stu-id="154e8-128">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="154e8-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="154e8-129">-VaultName</span></span>
<span data-ttu-id="154e8-130">Annak a kulcstárnak a nevét adja meg, amelynek a hálózati szabályát módosítják.</span><span class="sxs-lookup"><span data-stu-id="154e8-130">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="154e8-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="154e8-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="154e8-132">Megadja a hálózati szabály engedélyezett virtuális hálózati erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="154e8-132">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="154e8-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="154e8-133">-Confirm</span></span>
<span data-ttu-id="154e8-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="154e8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="154e8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="154e8-135">-WhatIf</span></span>
<span data-ttu-id="154e8-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="154e8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="154e8-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="154e8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="154e8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="154e8-138">CommonParameters</span></span>
<span data-ttu-id="154e8-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="154e8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="154e8-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="154e8-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="154e8-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="154e8-141">INPUTS</span></span>

### <span data-ttu-id="154e8-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="154e8-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="154e8-143">System.String</span><span class="sxs-lookup"><span data-stu-id="154e8-143">System.String</span></span>

## <span data-ttu-id="154e8-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="154e8-144">OUTPUTS</span></span>

### <span data-ttu-id="154e8-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="154e8-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="154e8-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="154e8-146">NOTES</span></span>

## <span data-ttu-id="154e8-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="154e8-147">RELATED LINKS</span></span>
