---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
ms.openlocfilehash: 98a3a023564c2c61f1398856e8a089276aeae7bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194750"
---
# <span data-ttu-id="8d2ef-101">Undo-AzKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="8d2ef-101">Undo-AzKeyVaultRemoval</span></span>

## <span data-ttu-id="8d2ef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8d2ef-102">SYNOPSIS</span></span>
<span data-ttu-id="8d2ef-103">Törölt kulcsfájl aktív állapotba való visszanyerése.</span><span class="sxs-lookup"><span data-stu-id="8d2ef-103">Recovers a deleted key vault into an active state.</span></span>

## <span data-ttu-id="8d2ef-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8d2ef-104">SYNTAX</span></span>

### <span data-ttu-id="8d2ef-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8d2ef-105">Default (Default)</span></span>
```
Undo-AzKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d2ef-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="8d2ef-106">InputObject</span></span>
```
Undo-AzKeyVaultRemoval [-InputObject] <PSDeletedKeyVault> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d2ef-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8d2ef-107">DESCRIPTION</span></span>
<span data-ttu-id="8d2ef-108">A **Visszavonás-AzKeyVaultRemoval** parancsmag egy korábban törölt fő boltozatot fog helyreállítani.</span><span class="sxs-lookup"><span data-stu-id="8d2ef-108">The **Undo-AzKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="8d2ef-109">A helyreállított boltozat aktívvá válik a helyreállítás után</span><span class="sxs-lookup"><span data-stu-id="8d2ef-109">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="8d2ef-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8d2ef-110">EXAMPLES</span></span>

### <span data-ttu-id="8d2ef-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8d2ef-111">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}

Vault Name                       : MyKeyVault
Resource Group Name              : MyResourceGroup
Location                         : eastus2
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers
                                   /Microsoft.KeyVault/vaults/mykeyvault
Vault URI                        : https://mykeyvault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : True
Enabled For Disk Encryption?     : True
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

Tags                             :
                                   Name  Value
                                   ====  =====
                                   x     y
```

<span data-ttu-id="8d2ef-112">Ez a parancs helyreállítja a "MyKeyVault" kulcsot, amelyet korábban törölt a eastus2-területről és a "MyResourceGroup" erőforráscsoport nevéből aktív és használható állapotba.</span><span class="sxs-lookup"><span data-stu-id="8d2ef-112">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="8d2ef-113">A címkék az új címkét is felváltják.</span><span class="sxs-lookup"><span data-stu-id="8d2ef-113">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="8d2ef-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8d2ef-114">PARAMETERS</span></span>

### <span data-ttu-id="8d2ef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d2ef-115">-DefaultProfile</span></span>
<span data-ttu-id="8d2ef-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8d2ef-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d2ef-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d2ef-117">-InputObject</span></span>
<span data-ttu-id="8d2ef-118">A Vault-objektum törlése</span><span class="sxs-lookup"><span data-stu-id="8d2ef-118">Deleted vault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d2ef-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="8d2ef-119">-Location</span></span>
<span data-ttu-id="8d2ef-120">A törölt Vault eredeti Azure-területét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8d2ef-120">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2ef-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d2ef-121">-ResourceGroupName</span></span>
<span data-ttu-id="8d2ef-122">Annak a meglévő erőforrás-csoportnak a nevét adja meg, amelybe a kulcs boltozatát létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="8d2ef-122">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2ef-123">-Címke</span><span class="sxs-lookup"><span data-stu-id="8d2ef-123">-Tag</span></span>
<span data-ttu-id="8d2ef-124">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="8d2ef-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8d2ef-125">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="8d2ef-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8d2ef-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8d2ef-126">-VaultName</span></span>
<span data-ttu-id="8d2ef-127">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="8d2ef-127">Vault name.</span></span>
<span data-ttu-id="8d2ef-128">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="8d2ef-128">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2ef-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8d2ef-129">-Confirm</span></span>
<span data-ttu-id="8d2ef-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8d2ef-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d2ef-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d2ef-131">-WhatIf</span></span>
<span data-ttu-id="8d2ef-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8d2ef-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8d2ef-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8d2ef-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d2ef-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d2ef-134">CommonParameters</span></span>
<span data-ttu-id="8d2ef-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8d2ef-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d2ef-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8d2ef-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d2ef-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d2ef-137">INPUTS</span></span>

### <span data-ttu-id="8d2ef-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="8d2ef-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

## <span data-ttu-id="8d2ef-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d2ef-139">OUTPUTS</span></span>

### <span data-ttu-id="8d2ef-140">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="8d2ef-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="8d2ef-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8d2ef-141">NOTES</span></span>

## <span data-ttu-id="8d2ef-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d2ef-142">RELATED LINKS</span></span>

[<span data-ttu-id="8d2ef-143">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="8d2ef-143">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)

[<span data-ttu-id="8d2ef-144">Új – AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="8d2ef-144">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="8d2ef-145">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="8d2ef-145">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)