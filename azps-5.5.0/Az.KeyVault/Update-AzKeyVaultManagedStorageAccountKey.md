---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultmanagedstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: b603cff68d2343a683718ca53e900aa5b667dc14
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152603"
---
# <span data-ttu-id="ff101-101">Update-AzKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ff101-101">Update-AzKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="ff101-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff101-102">SYNOPSIS</span></span>
<span data-ttu-id="ff101-103">A kulcstár által felügyelt Azure Storage-fiók megadott kulcsának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="ff101-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="ff101-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ff101-104">SYNTAX</span></span>

### <span data-ttu-id="ff101-105">ByDefinitionName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ff101-105">ByDefinitionName (Default)</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff101-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ff101-106">ByInputObject</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-KeyName] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ff101-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ff101-107">DESCRIPTION</span></span>
<span data-ttu-id="ff101-108">A kulcstár által kezelt Azure Storage-fiók megadott kulcsának újragenerálása, és a kulcs aktív kulcsként való beállítja.</span><span class="sxs-lookup"><span data-stu-id="ff101-108">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="ff101-109">A kulcstár a hívást az Azure Resource Managerhez proxyként használja a kulcs újragenerálása miatt.</span><span class="sxs-lookup"><span data-stu-id="ff101-109">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="ff101-110">A hívónak jogosultságokkal kell rendelkeznie ahhoz, hogy újragenerálja a kulcsokat az adott Azure Storage-fiókon.</span><span class="sxs-lookup"><span data-stu-id="ff101-110">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="ff101-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ff101-111">EXAMPLES</span></span>

### <span data-ttu-id="ff101-112">1. példa: Kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="ff101-112">Example 1: Regenerate a key</span></span>
```powershell
PS C:\> Update-AzKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key1
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="ff101-113">A "mystorageaccount" fiók "kulcs1" újragenerálása, és a kulcs1 aktívként állítja be a kulcstár felügyelt Azure Storage-fiókját.</span><span class="sxs-lookup"><span data-stu-id="ff101-113">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="ff101-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff101-114">PARAMETERS</span></span>

### <span data-ttu-id="ff101-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ff101-115">-AccountName</span></span>
<span data-ttu-id="ff101-116">Key Vault managed storage account name.</span><span class="sxs-lookup"><span data-stu-id="ff101-116">Key Vault managed storage account name.</span></span> <span data-ttu-id="ff101-117">A parancsmag egy felügyelt tárfiók nevének FQDN-ét építi fel a tárolónévből, az aktuálisan kijelölt környezetből és a felügyelt tárfiók nevéből.</span><span class="sxs-lookup"><span data-stu-id="ff101-117">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff101-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff101-118">-DefaultProfile</span></span>
<span data-ttu-id="ff101-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ff101-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff101-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ff101-120">-Force</span></span>
<span data-ttu-id="ff101-121">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ff101-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ff101-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff101-122">-InputObject</span></span>
<span data-ttu-id="ff101-123">ManagedStorageAccount objektum.</span><span class="sxs-lookup"><span data-stu-id="ff101-123">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff101-124">-KeyName</span><span class="sxs-lookup"><span data-stu-id="ff101-124">-KeyName</span></span>
<span data-ttu-id="ff101-125">A tárfiók kulcsának neve az újrageneráláshoz és az aktívvá tenni.</span><span class="sxs-lookup"><span data-stu-id="ff101-125">Name of storage account key to regenerate and make active.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff101-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff101-126">-PassThru</span></span>
<span data-ttu-id="ff101-127">A parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="ff101-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="ff101-128">Ha ez a kapcsoló meg van adva, a parancsmag a törölt felügyelt tárfiókot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="ff101-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="ff101-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ff101-129">-VaultName</span></span>
<span data-ttu-id="ff101-130">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="ff101-130">Vault name.</span></span>
<span data-ttu-id="ff101-131">A parancsmag a név és a jelenleg kijelölt környezet alapján építi fel egy tároló teljes tartománynevét.</span><span class="sxs-lookup"><span data-stu-id="ff101-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff101-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff101-132">-Confirm</span></span>
<span data-ttu-id="ff101-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ff101-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff101-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff101-134">-WhatIf</span></span>
<span data-ttu-id="ff101-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ff101-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff101-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ff101-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff101-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff101-137">CommonParameters</span></span>
<span data-ttu-id="ff101-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff101-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff101-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff101-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff101-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ff101-140">INPUTS</span></span>

### <span data-ttu-id="ff101-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ff101-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="ff101-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff101-142">OUTPUTS</span></span>

### <span data-ttu-id="ff101-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ff101-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="ff101-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ff101-144">NOTES</span></span>

## <span data-ttu-id="ff101-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ff101-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

