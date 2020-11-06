---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 1520acb94ffe587fb96eaa9c2ba565bcf31cc87e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503635"
---
# <span data-ttu-id="74521-101">Backup-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="74521-101">Backup-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="74521-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="74521-102">SYNOPSIS</span></span>
<span data-ttu-id="74521-103">Biztonsági másolatot készíthet egy parancssori tárolási fiókról.</span><span class="sxs-lookup"><span data-stu-id="74521-103">Backs up a KeyVault-managed storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74521-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="74521-104">SYNTAX</span></span>

### <span data-ttu-id="74521-105">ByStorageAccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="74521-105">ByStorageAccountName (Default)</span></span>
```
Backup-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74521-106">ByStorageAccount</span><span class="sxs-lookup"><span data-stu-id="74521-106">ByStorageAccount</span></span>
```
Backup-AzureKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-OutputFile] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="74521-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="74521-107">DESCRIPTION</span></span>
<span data-ttu-id="74521-108">A **biztonsági másolat-AzureKeyVaultManagedStorageAccount** parancsmag egy megadott felügyelt tárterületet készít a kulcsfájl letöltésével és egy fájlban való tárolásával.</span><span class="sxs-lookup"><span data-stu-id="74521-108">The **Backup-AzureKeyVaultManagedStorageAccount** cmdlet backs up a specified managed storage account in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="74521-109">Mivel a letöltött tartalom titkosítva van, nem használható az Azure Key Vault-on kívül.</span><span class="sxs-lookup"><span data-stu-id="74521-109">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="74521-110">Visszaállíthat egy biztonsági mentett tárterületet az előfizetésben szereplő bármelyik kulcsos fiókba, amelyből biztonsági másolat készül, amíg a boltozat ugyanahhoz az Azure-földrajzhoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="74521-110">You can restore a backed-up storage account to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="74521-111">A parancsmag használatának tipikus okai a következők:</span><span class="sxs-lookup"><span data-stu-id="74521-111">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="74521-112">Szeretné megőrizni a tárolási fiók kapcsolat nélküli másolatát, ha véletlenül törli az eredetit a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="74521-112">You want to retain an offline copy of the storage account in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="74521-113">A tagkártya segítségével létrehozott egy felügyelt tárterületet, és most szeretné az objektumot egy másik Azure-területre beilleszteni, így a kiosztott alkalmazás minden példányában használhatja azt.</span><span class="sxs-lookup"><span data-stu-id="74521-113">You created a managed storage account using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="74521-114">Használja a **Backup-AzureKeyVaultManagedStorageAccount** parancsmagot a felügyelt tárterület titkosított formátumban való visszakereséséhez, majd használja a **Restore-AzureKeyVaultManagedStorageAccount** parancsmagot, és adjon meg egy kulcspárt a második régióban.</span><span class="sxs-lookup"><span data-stu-id="74521-114">Use the **Backup-AzureKeyVaultManagedStorageAccount** cmdlet to retrieve the managed storage account in encrypted format and then use the **Restore-AzureKeyVaultManagedStorageAccount** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="74521-115">Példák</span><span class="sxs-lookup"><span data-stu-id="74521-115">EXAMPLES</span></span>

### <span data-ttu-id="74521-116">1. példa: felügyelt tárterületű fiók biztonsági mentése automatikusan generált fájlnévvel</span><span class="sxs-lookup"><span data-stu-id="74521-116">Example 1: Back up a managed storage account with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzureKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

<span data-ttu-id="74521-117">Ez a parancs beolvassa a MyMSAK nevű felügyelt tárterületet a MyKeyVault nevű kulcs-tárolóból, és menti a távtárolású tárterület biztonsági másolatát egy automatikusan megnevezett fájlba, és megjeleníti a fájl nevét.</span><span class="sxs-lookup"><span data-stu-id="74521-117">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="74521-118">2. példa: felügyelt tárterület-fiók biztonsági mentése egy megadott fájlnévre</span><span class="sxs-lookup"><span data-stu-id="74521-118">Example 2: Back up a managed storage account to a specified file name</span></span>
```powershell
PS C:\> Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="74521-119">Ez a parancs beolvassa a MyMSAK nevű felügyelt tárterületet a MyKeyVault nevű kulcskezelő-fiókból, és biztonsági másolatot ment a felügyelt tárterület-fiókról egy backup. blob nevű fájlra.</span><span class="sxs-lookup"><span data-stu-id="74521-119">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file named Backup.blob.</span></span>

### <span data-ttu-id="74521-120">3. példa: biztonsági másolat készítése korábban lekérdezett felügyelt tárterületről egy megadott fájlnévre, a célfájl felülírása a kérdés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="74521-120">Example 3: Back up a previously retrieved managed storage account to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $msak = Get-AzureKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzureKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="74521-121">Ez a parancs létrehoz egy biztonsági másolatot a $msak nevű felügyelt tárterület-fiókról. Nevezze el a $msak nevű boltozatot. VaultName egy backup. blob nevű fájlhoz, a fájl csendes felülírásával, ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="74521-121">This command creates a backup of the managed storage account named $msak.Name in the vault named $msak.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="74521-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="74521-122">PARAMETERS</span></span>

### <span data-ttu-id="74521-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74521-123">-DefaultProfile</span></span>
<span data-ttu-id="74521-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="74521-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74521-125">-Force</span><span class="sxs-lookup"><span data-stu-id="74521-125">-Force</span></span>
<span data-ttu-id="74521-126">A megadott fájl felülírása ha létezik</span><span class="sxs-lookup"><span data-stu-id="74521-126">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="74521-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74521-127">-InputObject</span></span>
<span data-ttu-id="74521-128">A raktározási fiók kötegének biztonsági mentése a lekérési hívás kimenetéről.</span><span class="sxs-lookup"><span data-stu-id="74521-128">Storage account bundle to be backed up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByStorageAccount
Aliases: StorageAccount

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74521-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="74521-129">-Name</span></span>
<span data-ttu-id="74521-130">Titkos név.</span><span class="sxs-lookup"><span data-stu-id="74521-130">Secret name.</span></span>
<span data-ttu-id="74521-131">A parancsmag a boltozat nevéből, az aktuálisan kijelölt környezetből és a titkos névvel elkészíti a titkos FQDN-t.</span><span class="sxs-lookup"><span data-stu-id="74521-131">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74521-132">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="74521-132">-OutputFile</span></span>
<span data-ttu-id="74521-133">Kimeneti fájl.</span><span class="sxs-lookup"><span data-stu-id="74521-133">Output file.</span></span>
<span data-ttu-id="74521-134">A kimeneti fájl a tárterület biztonsági másolatának tárolásához.</span><span class="sxs-lookup"><span data-stu-id="74521-134">The output file to store the storage account backup.</span></span>
<span data-ttu-id="74521-135">Ha nincs megadva, a program egy alapértelmezett fájlnevet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="74521-135">If not specified, a default filename will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74521-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="74521-136">-VaultName</span></span>
<span data-ttu-id="74521-137">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="74521-137">Vault name.</span></span>
<span data-ttu-id="74521-138">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="74521-138">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74521-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="74521-139">-Confirm</span></span>
<span data-ttu-id="74521-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="74521-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74521-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74521-141">-WhatIf</span></span>
<span data-ttu-id="74521-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="74521-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74521-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="74521-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74521-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74521-144">CommonParameters</span></span>
<span data-ttu-id="74521-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="74521-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74521-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74521-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74521-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="74521-147">INPUTS</span></span>

### <span data-ttu-id="74521-148">Microsoft. Azure. Command. PSKeyVaultManagedStorageAccountIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="74521-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>
<span data-ttu-id="74521-149">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="74521-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="74521-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="74521-150">OUTPUTS</span></span>

### <span data-ttu-id="74521-151">System. String</span><span class="sxs-lookup"><span data-stu-id="74521-151">System.String</span></span>

## <span data-ttu-id="74521-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="74521-152">NOTES</span></span>

## <span data-ttu-id="74521-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="74521-153">RELATED LINKS</span></span>
