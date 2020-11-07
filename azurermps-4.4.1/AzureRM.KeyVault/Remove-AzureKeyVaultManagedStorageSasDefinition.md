---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: fadf6b15eb25f07d88254a5d3a998f1692e5cf29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679764"
---
# <span data-ttu-id="54cbf-101">Remove-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="54cbf-101">Remove-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="54cbf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="54cbf-102">SYNOPSIS</span></span>
<span data-ttu-id="54cbf-103">Eltávolítja az Azure Managed Azure Storage SAS definícióit.</span><span class="sxs-lookup"><span data-stu-id="54cbf-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54cbf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="54cbf-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54cbf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="54cbf-105">DESCRIPTION</span></span>
<span data-ttu-id="54cbf-106">Eltávolítja az Azure Managed Azure Storage SAS definícióit.</span><span class="sxs-lookup"><span data-stu-id="54cbf-106">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="54cbf-107">Ez a beállítás eltávolítja azt a titkot is, amellyel a SAS-tokent a SAS-definícióval szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="54cbf-107">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="54cbf-108">Példák</span><span class="sxs-lookup"><span data-stu-id="54cbf-108">EXAMPLES</span></span>

### <span data-ttu-id="54cbf-109">Példa 1: az Azure Managed Azure Storage SAS definíciójának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="54cbf-109">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef'
```

<span data-ttu-id="54cbf-110">Eltávolítja a "mystorageaccount" fiók "myvault" mysasdef társított "" fiókkal társított kulcs-Vault Managed Storage SAS-definíciót.</span><span class="sxs-lookup"><span data-stu-id="54cbf-110">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="54cbf-111">2. példa: távolítsa el a Key Vault Managed Azure Storage SAS definícióját felhasználó megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="54cbf-111">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -Force -Confirm:$False
```

<span data-ttu-id="54cbf-112">Eltávolítja a "mystorageaccount" fiók "myvault" mysasdef társított "" fiókkal társított kulcs-Vault Managed Storage SAS-definíciót.</span><span class="sxs-lookup"><span data-stu-id="54cbf-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="54cbf-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="54cbf-113">PARAMETERS</span></span>

### <span data-ttu-id="54cbf-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="54cbf-114">-AccountName</span></span>
<span data-ttu-id="54cbf-115">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="54cbf-115">Storage account name.</span></span>
<span data-ttu-id="54cbf-116">Parancsmag: a felügyelt tárterület-fióknév teljes tartománynevét építi a boltozat neve, a jelenleg kijelölt környezet és a tárolási fiók neve között.</span><span class="sxs-lookup"><span data-stu-id="54cbf-116">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54cbf-117">-Force</span><span class="sxs-lookup"><span data-stu-id="54cbf-117">-Force</span></span>
<span data-ttu-id="54cbf-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="54cbf-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="54cbf-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="54cbf-119">-Name</span></span>
<span data-ttu-id="54cbf-120">Storage sas-definíció neve.</span><span class="sxs-lookup"><span data-stu-id="54cbf-120">Storage sas definition name.</span></span>
<span data-ttu-id="54cbf-121">Parancsmag: a tároló biztonsági társításának FQDN-definícióját a boltozat neve, a jelenleg kijelölt környezet, a tárolási fiók neve és a sas-definíció neve alapján építi ki.</span><span class="sxs-lookup"><span data-stu-id="54cbf-121">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54cbf-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54cbf-122">-PassThru</span></span>
<span data-ttu-id="54cbf-123">A parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="54cbf-123">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="54cbf-124">Ha meg van adva ez a kapcsoló, akkor a parancsmag a törölt tárterület-fiókot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="54cbf-124">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="54cbf-125">-VaultName</span><span class="sxs-lookup"><span data-stu-id="54cbf-125">-VaultName</span></span>
<span data-ttu-id="54cbf-126">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="54cbf-126">Vault name.</span></span>
<span data-ttu-id="54cbf-127">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="54cbf-127">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54cbf-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="54cbf-128">-Confirm</span></span>
<span data-ttu-id="54cbf-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="54cbf-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54cbf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54cbf-130">-WhatIf</span></span>
<span data-ttu-id="54cbf-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="54cbf-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54cbf-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="54cbf-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54cbf-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54cbf-133">-DefaultProfile</span></span>
<span data-ttu-id="54cbf-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="54cbf-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54cbf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54cbf-135">CommonParameters</span></span>
<span data-ttu-id="54cbf-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="54cbf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54cbf-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54cbf-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54cbf-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="54cbf-138">INPUTS</span></span>

### <span data-ttu-id="54cbf-139">System. String</span><span class="sxs-lookup"><span data-stu-id="54cbf-139">System.String</span></span>

## <span data-ttu-id="54cbf-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="54cbf-140">OUTPUTS</span></span>

### <span data-ttu-id="54cbf-141">Microsoft. Azure. Command. ManagedStorageSasDefinition. models.</span><span class="sxs-lookup"><span data-stu-id="54cbf-141">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="54cbf-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="54cbf-142">NOTES</span></span>

## <span data-ttu-id="54cbf-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="54cbf-143">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

