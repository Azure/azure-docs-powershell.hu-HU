---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurermkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultNetworkRule.md
ms.openlocfilehash: f1ff73a753c794ce7528c9af2b480f75d1460815
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496040"
---
# <span data-ttu-id="8f2ba-101">Remove-AzureRmKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="8f2ba-101">Remove-AzureRmKeyVaultNetworkRule</span></span>

## <span data-ttu-id="8f2ba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8f2ba-102">SYNOPSIS</span></span>
<span data-ttu-id="8f2ba-103">Hálózati szabály eltávolítása a fő boltozatról.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-103">Removes a network rule from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f2ba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8f2ba-104">SYNTAX</span></span>

### <span data-ttu-id="8f2ba-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8f2ba-105">ByVaultName (Default)</span></span>
```
Remove-AzureRmKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f2ba-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8f2ba-106">ByInputObject</span></span>
```
Remove-AzureRmKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f2ba-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8f2ba-107">ByResourceId</span></span>
```
Remove-AzureRmKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f2ba-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8f2ba-108">DESCRIPTION</span></span>
<span data-ttu-id="8f2ba-109">Hálózati szabály eltávolítása a fő boltozatról.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-109">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="8f2ba-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8f2ba-110">EXAMPLES</span></span>

### <span data-ttu-id="8f2ba-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8f2ba-111">Example 1</span></span>
```powershell
PS C:\> $myNetworkResId = (Get-AzureRmVirtualNetwork -Name myVNetName -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Remove-AzureRmKeyVaultNetworkRule -VaultName myVault -IpAddressRange "10.0.0.1/26" -VirtualNetworkResourceId $myNetworkResId -PassThru

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

<span data-ttu-id="8f2ba-112">Ez a parancs eltávolítja a megadott tároló hálózati szabályát, feltéve, hogy a megadott IP-cím és a virtuális hálózat erőforrás-azonosítójának megfelelő szabály található.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-112">This command removes a network rule from the specified vault, provided a rule is found matching the specified IP address and the virtual network resource identifier.</span></span>

## <span data-ttu-id="8f2ba-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8f2ba-113">PARAMETERS</span></span>

### <span data-ttu-id="8f2ba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f2ba-114">-DefaultProfile</span></span>
<span data-ttu-id="8f2ba-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f2ba-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f2ba-116">-InputObject</span></span>
<span data-ttu-id="8f2ba-117">A boltozat objektum</span><span class="sxs-lookup"><span data-stu-id="8f2ba-117">KeyVault object</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f2ba-118">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="8f2ba-118">-IpAddressRange</span></span>
<span data-ttu-id="8f2ba-119">A hálózati szabály engedélyezett hálózati IP-címének hatókörét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-119">Specifies allowed network IP address range of network rule.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f2ba-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f2ba-120">-PassThru</span></span>
<span data-ttu-id="8f2ba-121">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="8f2ba-122">Ha meg van adva ez a kapcsoló, a program a frissített kulcsfájl-objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-122">If this switch is specified, it returns the updated key vault object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f2ba-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f2ba-123">-ResourceGroupName</span></span>
<span data-ttu-id="8f2ba-124">Annak a kulcsfájl-csoportnak a nevét adja meg, akinek a hálózati szabálya módosul.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-124">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f2ba-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f2ba-125">-ResourceId</span></span>
<span data-ttu-id="8f2ba-126">A főkészlet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="8f2ba-126">KeyVault Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f2ba-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8f2ba-127">-VaultName</span></span>
<span data-ttu-id="8f2ba-128">Annak a kulcsnak a nevét adja meg, amelynek a hálózati szabályait módosították.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-128">Specifies the name of a key vault whose network rule is being modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f2ba-129">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="8f2ba-129">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="8f2ba-130">A hálózati szabály engedélyezett virtuális hálózati erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-130">Specifies allowed virtual network resource identifier of network rule.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f2ba-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8f2ba-131">-Confirm</span></span>
<span data-ttu-id="8f2ba-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f2ba-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f2ba-133">-WhatIf</span></span>
<span data-ttu-id="8f2ba-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f2ba-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f2ba-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f2ba-136">CommonParameters</span></span>
<span data-ttu-id="8f2ba-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8f2ba-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f2ba-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f2ba-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f2ba-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f2ba-139">INPUTS</span></span>

### <span data-ttu-id="8f2ba-140">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="8f2ba-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f2ba-141">OUTPUTS</span></span>

### <span data-ttu-id="8f2ba-142">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="8f2ba-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="8f2ba-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8f2ba-143">NOTES</span></span>

## <span data-ttu-id="8f2ba-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f2ba-144">RELATED LINKS</span></span>
