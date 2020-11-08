---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultmanagedstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: b603cff68d2343a683718ca53e900aa5b667dc14
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195901"
---
# <span data-ttu-id="3880e-101">Update-AzKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="3880e-101">Update-AzKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="3880e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3880e-102">SYNOPSIS</span></span>
<span data-ttu-id="3880e-103">Újragenerálja a Key Vault Managed Azure Storage-fiók megadott kulcsát.</span><span class="sxs-lookup"><span data-stu-id="3880e-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="3880e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3880e-104">SYNTAX</span></span>

### <span data-ttu-id="3880e-105">ByDefinitionName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3880e-105">ByDefinitionName (Default)</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3880e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3880e-106">ByInputObject</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-KeyName] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3880e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3880e-107">DESCRIPTION</span></span>
<span data-ttu-id="3880e-108">Újragenerálja a Key Vault Managed Azure Storage fiók megadott kulcsát, és az aktív kulcsként állítja be a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="3880e-108">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="3880e-109">A kulcsfájl az Azure Resource Manager hívásával hozza létre újra a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="3880e-109">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="3880e-110">A hívónak rendelkeznie kell engedélyekkel a megadott Azure-tárterületen lévő kulcsok újragenerálásához.</span><span class="sxs-lookup"><span data-stu-id="3880e-110">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="3880e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="3880e-111">EXAMPLES</span></span>

### <span data-ttu-id="3880e-112">1. példa: kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="3880e-112">Example 1: Regenerate a key</span></span>
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

<span data-ttu-id="3880e-113">Újragenerálja a "mystorageaccount" key1, és a "key1" értéket állítja be a Key Vault Managed Azure tárterület-fiókjának aktív állapotában.</span><span class="sxs-lookup"><span data-stu-id="3880e-113">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="3880e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3880e-114">PARAMETERS</span></span>

### <span data-ttu-id="3880e-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3880e-115">-AccountName</span></span>
<span data-ttu-id="3880e-116">Fontos: a boltozattal felügyelt tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="3880e-116">Key Vault managed storage account name.</span></span> <span data-ttu-id="3880e-117">Parancsmag: a felügyelt tárterület-fióknév teljes tartománynevét építi a Vault neve, a jelenleg kijelölt környezet és a Mangal-tároló fiók nevéből.</span><span class="sxs-lookup"><span data-stu-id="3880e-117">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="3880e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3880e-118">-DefaultProfile</span></span>
<span data-ttu-id="3880e-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3880e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3880e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="3880e-120">-Force</span></span>
<span data-ttu-id="3880e-121">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3880e-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3880e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3880e-122">-InputObject</span></span>
<span data-ttu-id="3880e-123">ManagedStorageAccount objektum</span><span class="sxs-lookup"><span data-stu-id="3880e-123">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="3880e-124">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="3880e-124">-KeyName</span></span>
<span data-ttu-id="3880e-125">A tárolási fiók kulcsának neve az újrageneráláshoz és az aktív állapotba tételéhez.</span><span class="sxs-lookup"><span data-stu-id="3880e-125">Name of storage account key to regenerate and make active.</span></span>

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

### <span data-ttu-id="3880e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3880e-126">-PassThru</span></span>
<span data-ttu-id="3880e-127">A parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="3880e-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="3880e-128">Ha meg van adva ez a kapcsoló, akkor a parancsmag a törölt tárterület-fiókot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="3880e-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="3880e-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3880e-129">-VaultName</span></span>
<span data-ttu-id="3880e-130">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="3880e-130">Vault name.</span></span>
<span data-ttu-id="3880e-131">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="3880e-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="3880e-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3880e-132">-Confirm</span></span>
<span data-ttu-id="3880e-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3880e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3880e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3880e-134">-WhatIf</span></span>
<span data-ttu-id="3880e-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3880e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3880e-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3880e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3880e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3880e-137">CommonParameters</span></span>
<span data-ttu-id="3880e-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3880e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3880e-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3880e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3880e-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3880e-140">INPUTS</span></span>

### <span data-ttu-id="3880e-141">Microsoft. Azure. Command. PSKeyVaultManagedStorageAccountIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="3880e-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="3880e-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3880e-142">OUTPUTS</span></span>

### <span data-ttu-id="3880e-143">Microsoft. Azure. Command. PSKeyVaultManagedStorageAccount. models.</span><span class="sxs-lookup"><span data-stu-id="3880e-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="3880e-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3880e-144">NOTES</span></span>

## <span data-ttu-id="3880e-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3880e-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)
