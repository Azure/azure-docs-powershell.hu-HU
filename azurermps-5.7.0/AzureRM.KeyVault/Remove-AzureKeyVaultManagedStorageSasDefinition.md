---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 9859c6f17f393a5ca691c34e3ee144e24ab59fa8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672857"
---
# <span data-ttu-id="f3a53-101">Remove-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="f3a53-101">Remove-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="f3a53-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f3a53-102">SYNOPSIS</span></span>
<span data-ttu-id="f3a53-103">Eltávolítja az Azure Managed Azure Storage SAS definícióit.</span><span class="sxs-lookup"><span data-stu-id="f3a53-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3a53-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f3a53-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3a53-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f3a53-105">DESCRIPTION</span></span>
<span data-ttu-id="f3a53-106">Eltávolítja az Azure Managed Azure Storage SAS definícióit.</span><span class="sxs-lookup"><span data-stu-id="f3a53-106">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="f3a53-107">Ez a beállítás eltávolítja azt a titkot is, amellyel a SAS-tokent a SAS-definícióval szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="f3a53-107">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="f3a53-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f3a53-108">EXAMPLES</span></span>

### <span data-ttu-id="f3a53-109">Példa 1: az Azure Managed Azure Storage SAS definíciójának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="f3a53-109">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef'
```

<span data-ttu-id="f3a53-110">Eltávolítja a "mystorageaccount" fiók "myvault" mysasdef társított "" fiókkal társított kulcs-Vault Managed Storage SAS-definíciót.</span><span class="sxs-lookup"><span data-stu-id="f3a53-110">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="f3a53-111">2. példa: távolítsa el a Key Vault Managed Azure Storage SAS definícióját felhasználó megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="f3a53-111">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -Force -Confirm:$False
```

<span data-ttu-id="f3a53-112">Eltávolítja a "mystorageaccount" fiók "myvault" mysasdef társított "" fiókkal társított kulcs-Vault Managed Storage SAS-definíciót.</span><span class="sxs-lookup"><span data-stu-id="f3a53-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="f3a53-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f3a53-113">PARAMETERS</span></span>

### <span data-ttu-id="f3a53-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f3a53-114">-AccountName</span></span>
<span data-ttu-id="f3a53-115">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="f3a53-115">Storage account name.</span></span>
<span data-ttu-id="f3a53-116">Parancsmag: a felügyelt tárterület-fióknév teljes tartománynevét építi a boltozat neve, a jelenleg kijelölt környezet és a tárolási fiók neve között.</span><span class="sxs-lookup"><span data-stu-id="f3a53-116">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3a53-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3a53-117">-DefaultProfile</span></span>
<span data-ttu-id="f3a53-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f3a53-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3a53-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f3a53-119">-Force</span></span>
<span data-ttu-id="f3a53-120">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f3a53-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f3a53-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f3a53-121">-Name</span></span>
<span data-ttu-id="f3a53-122">Storage sas-definíció neve.</span><span class="sxs-lookup"><span data-stu-id="f3a53-122">Storage sas definition name.</span></span>
<span data-ttu-id="f3a53-123">Parancsmag: a tároló biztonsági társításának FQDN-definícióját a boltozat neve, a jelenleg kijelölt környezet, a tárolási fiók neve és a sas-definíció neve alapján építi ki.</span><span class="sxs-lookup"><span data-stu-id="f3a53-123">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3a53-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3a53-124">-PassThru</span></span>
<span data-ttu-id="f3a53-125">A parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="f3a53-125">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f3a53-126">Ha meg van adva ez a kapcsoló, akkor a parancsmag a törölt tárterület-fiókot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="f3a53-126">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="f3a53-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f3a53-127">-VaultName</span></span>
<span data-ttu-id="f3a53-128">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="f3a53-128">Vault name.</span></span>
<span data-ttu-id="f3a53-129">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="f3a53-129">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3a53-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f3a53-130">-Confirm</span></span>
<span data-ttu-id="f3a53-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f3a53-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3a53-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3a53-132">-WhatIf</span></span>
<span data-ttu-id="f3a53-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f3a53-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3a53-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f3a53-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3a53-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3a53-135">CommonParameters</span></span>
<span data-ttu-id="f3a53-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f3a53-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3a53-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3a53-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3a53-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3a53-138">INPUTS</span></span>

### <span data-ttu-id="f3a53-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f3a53-139">System.String</span></span>

## <span data-ttu-id="f3a53-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3a53-140">OUTPUTS</span></span>

### <span data-ttu-id="f3a53-141">Microsoft. Azure. Command. ManagedStorageSasDefinition. models.</span><span class="sxs-lookup"><span data-stu-id="f3a53-141">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="f3a53-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f3a53-142">NOTES</span></span>

## <span data-ttu-id="f3a53-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3a53-143">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

