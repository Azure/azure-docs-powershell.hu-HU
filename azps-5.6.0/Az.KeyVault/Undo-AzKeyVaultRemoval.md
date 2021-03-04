---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/undo-azkeyvaultremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
ms.openlocfilehash: ff7dea63b4731b4a2a6becfc31d0b312345978bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931114"
---
# <span data-ttu-id="3ff3a-101">Undo-AzKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="3ff3a-101">Undo-AzKeyVaultRemoval</span></span>

## <span data-ttu-id="3ff3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ff3a-102">SYNOPSIS</span></span>
<span data-ttu-id="3ff3a-103">Helyreállít egy törölt kulcstárat egy aktív állapotba.</span><span class="sxs-lookup"><span data-stu-id="3ff3a-103">Recovers a deleted key vault into an active state.</span></span>

## <span data-ttu-id="3ff3a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3ff3a-104">SYNTAX</span></span>

### <span data-ttu-id="3ff3a-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3ff3a-105">Default (Default)</span></span>
```
Undo-AzKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ff3a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="3ff3a-106">InputObject</span></span>
```
Undo-AzKeyVaultRemoval [-InputObject] <PSDeletedKeyVault> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ff3a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3ff3a-107">DESCRIPTION</span></span>
<span data-ttu-id="3ff3a-108">Az **Undo-AzKeyVaultRemoval** parancsmag helyreállít egy korábban törölt kulcstárat.</span><span class="sxs-lookup"><span data-stu-id="3ff3a-108">The **Undo-AzKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="3ff3a-109">A helyreállított tároló a helyreállítás után aktív lesz</span><span class="sxs-lookup"><span data-stu-id="3ff3a-109">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="3ff3a-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3ff3a-110">EXAMPLES</span></span>

### <span data-ttu-id="3ff3a-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="3ff3a-111">Example 1</span></span>
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

<span data-ttu-id="3ff3a-112">Ez a parancs egy aktív és használható állapotba visszaállítja a korábban az eastus2 régióból és a MyResourceGroup erőforráscsoportból törölt MyKeyVault kulcstárat.</span><span class="sxs-lookup"><span data-stu-id="3ff3a-112">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="3ff3a-113">A címkéket új címkére is cseréli.</span><span class="sxs-lookup"><span data-stu-id="3ff3a-113">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="3ff3a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ff3a-114">PARAMETERS</span></span>

### <span data-ttu-id="3ff3a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ff3a-115">-DefaultProfile</span></span>
<span data-ttu-id="3ff3a-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3ff3a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ff3a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ff3a-117">-InputObject</span></span>
<span data-ttu-id="3ff3a-118">Törölt tárolóobjektum</span><span class="sxs-lookup"><span data-stu-id="3ff3a-118">Deleted vault object</span></span>

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

### <span data-ttu-id="3ff3a-119">-Location</span><span class="sxs-lookup"><span data-stu-id="3ff3a-119">-Location</span></span>
<span data-ttu-id="3ff3a-120">A törölt tároló eredeti Azure-régióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ff3a-120">Specifies the deleted vault original Azure region.</span></span>

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

### <span data-ttu-id="3ff3a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ff3a-121">-ResourceGroupName</span></span>
<span data-ttu-id="3ff3a-122">Egy meglévő erőforráscsoport nevét adja meg, amelyben létre kell hoznia a kulcstárat.</span><span class="sxs-lookup"><span data-stu-id="3ff3a-122">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="3ff3a-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="3ff3a-123">-Tag</span></span>
<span data-ttu-id="3ff3a-124">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="3ff3a-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3ff3a-125">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="3ff3a-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3ff3a-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3ff3a-126">-VaultName</span></span>
<span data-ttu-id="3ff3a-127">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="3ff3a-127">Vault name.</span></span>
<span data-ttu-id="3ff3a-128">A parancsmag a név és a jelenleg kijelölt környezet alapján építi fel egy tároló teljes tartománynevét.</span><span class="sxs-lookup"><span data-stu-id="3ff3a-128">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="3ff3a-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ff3a-129">-Confirm</span></span>
<span data-ttu-id="3ff3a-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3ff3a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ff3a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ff3a-131">-WhatIf</span></span>
<span data-ttu-id="3ff3a-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3ff3a-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ff3a-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3ff3a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ff3a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ff3a-134">CommonParameters</span></span>
<span data-ttu-id="3ff3a-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ff3a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ff3a-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ff3a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ff3a-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3ff3a-137">INPUTS</span></span>

### <span data-ttu-id="3ff3a-138">Microsoft.Azure.Commands.KeyVault.Models.PSDKeyVault</span><span class="sxs-lookup"><span data-stu-id="3ff3a-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

## <span data-ttu-id="3ff3a-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ff3a-139">OUTPUTS</span></span>

### <span data-ttu-id="3ff3a-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="3ff3a-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="3ff3a-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3ff3a-141">NOTES</span></span>

## <span data-ttu-id="3ff3a-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ff3a-142">RELATED LINKS</span></span>

[<span data-ttu-id="3ff3a-143">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="3ff3a-143">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)

[<span data-ttu-id="3ff3a-144">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="3ff3a-144">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="3ff3a-145">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="3ff3a-145">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)
