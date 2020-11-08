---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c01d07f9408804b229921394c24e444b2a4deb8b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025308"
---
# <span data-ttu-id="402a9-101">Backup-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="402a9-101">Backup-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="402a9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="402a9-102">SYNOPSIS</span></span>
<span data-ttu-id="402a9-103">Biztonsági másolatot készíthet egy parancssori tárolási fiókról.</span><span class="sxs-lookup"><span data-stu-id="402a9-103">Backs up a KeyVault-managed storage account.</span></span>

## <span data-ttu-id="402a9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="402a9-104">SYNTAX</span></span>

### <span data-ttu-id="402a9-105">ByStorageAccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="402a9-105">ByStorageAccountName (Default)</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="402a9-106">ByStorageAccount</span><span class="sxs-lookup"><span data-stu-id="402a9-106">ByStorageAccount</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-OutputFile] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="402a9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="402a9-107">DESCRIPTION</span></span>
<span data-ttu-id="402a9-108">A **biztonsági másolat-AzKeyVaultManagedStorageAccount** parancsmag egy megadott felügyelt tárterületet készít a kulcsfájl letöltésével és egy fájlban való tárolásával.</span><span class="sxs-lookup"><span data-stu-id="402a9-108">The **Backup-AzKeyVaultManagedStorageAccount** cmdlet backs up a specified managed storage account in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="402a9-109">Mivel a letöltött tartalom titkosítva van, nem használható az Azure Key Vault-on kívül.</span><span class="sxs-lookup"><span data-stu-id="402a9-109">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="402a9-110">Visszaállíthat egy biztonsági mentett tárterületet az előfizetésben szereplő bármelyik kulcsos fiókba, amelyből biztonsági másolat készül, amíg a boltozat ugyanahhoz az Azure-földrajzhoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="402a9-110">You can restore a backed-up storage account to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="402a9-111">A parancsmag használatának tipikus okai a következők:</span><span class="sxs-lookup"><span data-stu-id="402a9-111">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="402a9-112">Szeretné megőrizni a tárolási fiók kapcsolat nélküli másolatát, ha véletlenül törli az eredetit a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="402a9-112">You want to retain an offline copy of the storage account in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="402a9-113">A tagkártya segítségével létrehozott egy felügyelt tárterületet, és most szeretné az objektumot egy másik Azure-területre beilleszteni, így a kiosztott alkalmazás minden példányában használhatja azt.</span><span class="sxs-lookup"><span data-stu-id="402a9-113">You created a managed storage account using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="402a9-114">Használja a **Backup-AzKeyVaultManagedStorageAccount** parancsmagot a felügyelt tárterület titkosított formátumban való visszakereséséhez, majd használja a **Restore-AzKeyVaultManagedStorageAccount** parancsmagot, és adjon meg egy kulcspárt a második régióban.</span><span class="sxs-lookup"><span data-stu-id="402a9-114">Use the **Backup-AzKeyVaultManagedStorageAccount** cmdlet to retrieve the managed storage account in encrypted format and then use the **Restore-AzKeyVaultManagedStorageAccount** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="402a9-115">Példák</span><span class="sxs-lookup"><span data-stu-id="402a9-115">EXAMPLES</span></span>

### <span data-ttu-id="402a9-116">1. példa: felügyelt tárterületű fiók biztonsági mentése automatikusan generált fájlnévvel</span><span class="sxs-lookup"><span data-stu-id="402a9-116">Example 1: Back up a managed storage account with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

<span data-ttu-id="402a9-117">Ez a parancs beolvassa a MyMSAK nevű felügyelt tárterületet a MyKeyVault nevű kulcs-tárolóból, és menti a távtárolású tárterület biztonsági másolatát egy automatikusan megnevezett fájlba, és megjeleníti a fájl nevét.</span><span class="sxs-lookup"><span data-stu-id="402a9-117">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="402a9-118">2. példa: felügyelt tárterület-fiók biztonsági mentése egy megadott fájlnévre</span><span class="sxs-lookup"><span data-stu-id="402a9-118">Example 2: Back up a managed storage account to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="402a9-119">Ez a parancs beolvassa a MyMSAK nevű felügyelt tárterületet a MyKeyVault nevű kulcskezelő-fiókból, és biztonsági másolatot ment a felügyelt tárterület-fiókról egy backup. blob nevű fájlra.</span><span class="sxs-lookup"><span data-stu-id="402a9-119">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file named Backup.blob.</span></span>

### <span data-ttu-id="402a9-120">3. példa: biztonsági másolat készítése korábban lekérdezett felügyelt tárterületről egy megadott fájlnévre, a célfájl felülírása a kérdés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="402a9-120">Example 3: Back up a previously retrieved managed storage account to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $msak = Get-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="402a9-121">Ez a parancs létrehoz egy biztonsági másolatot a $msak nevű felügyelt tárterület-fiókról. Nevezze el a $msak nevű boltozatot. VaultName egy backup. blob nevű fájlhoz, a fájl csendes felülírásával, ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="402a9-121">This command creates a backup of the managed storage account named $msak.Name in the vault named $msak.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="402a9-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="402a9-122">PARAMETERS</span></span>

### <span data-ttu-id="402a9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="402a9-123">-DefaultProfile</span></span>
<span data-ttu-id="402a9-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="402a9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="402a9-125">-Force</span><span class="sxs-lookup"><span data-stu-id="402a9-125">-Force</span></span>
<span data-ttu-id="402a9-126">A megadott fájl felülírása ha létezik</span><span class="sxs-lookup"><span data-stu-id="402a9-126">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="402a9-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="402a9-127">-InputObject</span></span>
<span data-ttu-id="402a9-128">A raktározási fiók kötegének biztonsági mentése a lekérési hívás kimenetéről.</span><span class="sxs-lookup"><span data-stu-id="402a9-128">Storage account bundle to be backed up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="402a9-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="402a9-129">-Name</span></span>
<span data-ttu-id="402a9-130">Titkos név.</span><span class="sxs-lookup"><span data-stu-id="402a9-130">Secret name.</span></span>
<span data-ttu-id="402a9-131">A parancsmag a boltozat nevéből, az aktuálisan kijelölt környezetből és a titkos névvel elkészíti a titkos FQDN-t.</span><span class="sxs-lookup"><span data-stu-id="402a9-131">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="402a9-132">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="402a9-132">-OutputFile</span></span>
<span data-ttu-id="402a9-133">Kimeneti fájl.</span><span class="sxs-lookup"><span data-stu-id="402a9-133">Output file.</span></span>
<span data-ttu-id="402a9-134">A kimeneti fájl a tárterület biztonsági másolatának tárolásához.</span><span class="sxs-lookup"><span data-stu-id="402a9-134">The output file to store the storage account backup.</span></span>
<span data-ttu-id="402a9-135">Ha nincs megadva, a program egy alapértelmezett fájlnevet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="402a9-135">If not specified, a default filename will be generated.</span></span>

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

### <span data-ttu-id="402a9-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="402a9-136">-VaultName</span></span>
<span data-ttu-id="402a9-137">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="402a9-137">Vault name.</span></span>
<span data-ttu-id="402a9-138">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="402a9-138">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="402a9-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="402a9-139">-Confirm</span></span>
<span data-ttu-id="402a9-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="402a9-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="402a9-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="402a9-141">-WhatIf</span></span>
<span data-ttu-id="402a9-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="402a9-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="402a9-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="402a9-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="402a9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="402a9-144">CommonParameters</span></span>
<span data-ttu-id="402a9-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="402a9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="402a9-146">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="402a9-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="402a9-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="402a9-147">INPUTS</span></span>

### <span data-ttu-id="402a9-148">Microsoft. Azure. Command. PSKeyVaultManagedStorageAccountIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="402a9-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="402a9-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="402a9-149">OUTPUTS</span></span>

### <span data-ttu-id="402a9-150">System. String</span><span class="sxs-lookup"><span data-stu-id="402a9-150">System.String</span></span>

## <span data-ttu-id="402a9-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="402a9-151">NOTES</span></span>

## <span data-ttu-id="402a9-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="402a9-152">RELATED LINKS</span></span>
