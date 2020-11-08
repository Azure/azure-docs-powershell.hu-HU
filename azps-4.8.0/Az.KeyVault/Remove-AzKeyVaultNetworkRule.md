---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultNetworkRule.md
ms.openlocfilehash: b1c0326be98efed91ce53c9cf04cdee6fce658f8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181720"
---
# <span data-ttu-id="05c80-101">Remove-AzKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="05c80-101">Remove-AzKeyVaultNetworkRule</span></span>

## <span data-ttu-id="05c80-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="05c80-102">SYNOPSIS</span></span>
<span data-ttu-id="05c80-103">Hálózati szabály eltávolítása a fő boltozatról.</span><span class="sxs-lookup"><span data-stu-id="05c80-103">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="05c80-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="05c80-104">SYNTAX</span></span>

### <span data-ttu-id="05c80-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="05c80-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05c80-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="05c80-106">ByInputObject</span></span>
```
Remove-AzKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05c80-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="05c80-107">ByResourceId</span></span>
```
Remove-AzKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05c80-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="05c80-108">DESCRIPTION</span></span>
<span data-ttu-id="05c80-109">Hálózati szabály eltávolítása a fő boltozatról.</span><span class="sxs-lookup"><span data-stu-id="05c80-109">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="05c80-110">Példák</span><span class="sxs-lookup"><span data-stu-id="05c80-110">EXAMPLES</span></span>

### <span data-ttu-id="05c80-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="05c80-111">Example 1</span></span>
```powershell
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNetName -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Remove-AzKeyVaultNetworkRule -VaultName myVault -IpAddressRange "10.0.0.1/26" -VirtualNetworkResourceId $myNetworkResId -PassThru

Vault Name                       : myVault
Resource Group Name              : myrg
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
                                   IP Rules                                   :
                                   Virtual Network Rules                      :

Tags                             :
```

<span data-ttu-id="05c80-112">Ez a parancs eltávolítja a megadott tároló hálózati szabályát, feltéve, hogy a megadott IP-cím és a virtuális hálózat erőforrás-azonosítójának megfelelő szabály található.</span><span class="sxs-lookup"><span data-stu-id="05c80-112">This command removes a network rule from the specified vault, provided a rule is found matching the specified IP address and the virtual network resource identifier.</span></span>

## <span data-ttu-id="05c80-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="05c80-113">PARAMETERS</span></span>

### <span data-ttu-id="05c80-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05c80-114">-DefaultProfile</span></span>
<span data-ttu-id="05c80-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="05c80-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05c80-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05c80-116">-InputObject</span></span>
<span data-ttu-id="05c80-117">A boltozat objektum</span><span class="sxs-lookup"><span data-stu-id="05c80-117">KeyVault object</span></span>

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

### <span data-ttu-id="05c80-118">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="05c80-118">-IpAddressRange</span></span>
<span data-ttu-id="05c80-119">A hálózati szabály engedélyezett hálózati IP-címének hatókörét adja meg.</span><span class="sxs-lookup"><span data-stu-id="05c80-119">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="05c80-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05c80-120">-PassThru</span></span>
<span data-ttu-id="05c80-121">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="05c80-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="05c80-122">Ha meg van adva ez a kapcsoló, a program a frissített kulcsfájl-objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="05c80-122">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="05c80-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05c80-123">-ResourceGroupName</span></span>
<span data-ttu-id="05c80-124">Annak a kulcsfájl-csoportnak a nevét adja meg, akinek a hálózati szabálya módosul.</span><span class="sxs-lookup"><span data-stu-id="05c80-124">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="05c80-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05c80-125">-ResourceId</span></span>
<span data-ttu-id="05c80-126">A főkészlet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="05c80-126">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="05c80-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="05c80-127">-VaultName</span></span>
<span data-ttu-id="05c80-128">Annak a kulcsnak a nevét adja meg, amelynek a hálózati szabályait módosították.</span><span class="sxs-lookup"><span data-stu-id="05c80-128">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="05c80-129">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="05c80-129">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="05c80-130">A hálózati szabály engedélyezett virtuális hálózati erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="05c80-130">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="05c80-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="05c80-131">-Confirm</span></span>
<span data-ttu-id="05c80-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="05c80-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05c80-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05c80-133">-WhatIf</span></span>
<span data-ttu-id="05c80-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="05c80-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05c80-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="05c80-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05c80-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05c80-136">CommonParameters</span></span>
<span data-ttu-id="05c80-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="05c80-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05c80-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="05c80-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05c80-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="05c80-139">INPUTS</span></span>

### <span data-ttu-id="05c80-140">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="05c80-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="05c80-141">System. String</span><span class="sxs-lookup"><span data-stu-id="05c80-141">System.String</span></span>

## <span data-ttu-id="05c80-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="05c80-142">OUTPUTS</span></span>

### <span data-ttu-id="05c80-143">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="05c80-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="05c80-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="05c80-144">NOTES</span></span>

## <span data-ttu-id="05c80-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="05c80-145">RELATED LINKS</span></span>
