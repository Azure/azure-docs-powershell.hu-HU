---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultKey.md
ms.openlocfilehash: 2cf7c569a8c8d25f89c5006be4295a980186cbe3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680088"
---
# <span data-ttu-id="67985-101">Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="67985-101">Backup-AzureKeyVaultKey</span></span>

## <span data-ttu-id="67985-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="67985-102">SYNOPSIS</span></span>
<span data-ttu-id="67985-103">Biztonsági másolatot készíthet egy kulcsról a boltívben.</span><span class="sxs-lookup"><span data-stu-id="67985-103">Backs up a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67985-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="67985-104">SYNTAX</span></span>

### <span data-ttu-id="67985-105">ByKeyName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="67985-105">ByKeyName (Default)</span></span>
```
Backup-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67985-106">ByKey</span><span class="sxs-lookup"><span data-stu-id="67985-106">ByKey</span></span>
```
Backup-AzureKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67985-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="67985-107">DESCRIPTION</span></span>
<span data-ttu-id="67985-108">A **biztonsági másolat-AzureKeyVaultKey** parancsmag a megadott kulcs biztonsági másolatát biztonsági másolatokkal, letöltéssel és fájlba való tárolással támogatja.</span><span class="sxs-lookup"><span data-stu-id="67985-108">The **Backup-AzureKeyVaultKey** cmdlet backs up a specified key in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="67985-109">Ha a kulcs több verziója is létezik, az összes verzió megtalálható a biztonsági másolatban.</span><span class="sxs-lookup"><span data-stu-id="67985-109">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="67985-110">Mivel a letöltött tartalom titkosítva van, nem használható az Azure Key Vault-on kívül.</span><span class="sxs-lookup"><span data-stu-id="67985-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="67985-111">A mentett billentyűket visszaállíthatja annak az előfizetésnek a fő boltozatára, amelyről biztonsági másolatot készített.</span><span class="sxs-lookup"><span data-stu-id="67985-111">You can restore a backed-up key to any key vault in the subscription that it was backed up from.</span></span>
<span data-ttu-id="67985-112">A parancsmag használatának tipikus okai a következők:</span><span class="sxs-lookup"><span data-stu-id="67985-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="67985-113">Szeretne a kulcs egy példányát letétbe helyezni, hogy legyen kapcsolat nélküli példánya, ha véletlenül törli a billentyűt a kulcs-boltozatban.</span><span class="sxs-lookup"><span data-stu-id="67985-113">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your key vault.</span></span>
 
- <span data-ttu-id="67985-114">A Key Vault segítségével létrehozta a kulcsot, és most szeretné egy másik Azure-területre beilleszteni a kulcsot, így a kiosztott alkalmazás minden példányában használhatja azt.</span><span class="sxs-lookup"><span data-stu-id="67985-114">You created a key using Key Vault and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="67985-115">Használja a **Backup-AzureKeyVaultKey** parancsmagot a kulcs titkosított formátumban való visszakereséséhez, majd használja az Restore-AzureKeyVaultKey parancsmagot, és adja meg a második régióban a kulcs boltozatát.</span><span class="sxs-lookup"><span data-stu-id="67985-115">Use the **Backup-AzureKeyVaultKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzureKeyVaultKey cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="67985-116">Példák</span><span class="sxs-lookup"><span data-stu-id="67985-116">EXAMPLES</span></span>

### <span data-ttu-id="67985-117">1. példa: kulcs biztonsági mentése automatikusan generált fájlnévvel</span><span class="sxs-lookup"><span data-stu-id="67985-117">Example 1: Back up a key with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'

C:\Users\username\mykeyvault-mykey-1527029447.01191
```

<span data-ttu-id="67985-118">Ez a parancs beolvassa a MyKey nevű kulcsot a MyKeyVault nevű kulcskezelő szolgáltatásból, és menti az adott kulcs biztonsági másolatát egy automatikusan megnevezett fájlba, és megjeleníti a fájl nevét.</span><span class="sxs-lookup"><span data-stu-id="67985-118">This command retrieves the key named MyKey from the key vault named MyKeyVault and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="67985-119">2. példa: kulcs biztonsági mentése megadott fájlnévre</span><span class="sxs-lookup"><span data-stu-id="67985-119">Example 2: Back up a key to a specified file name</span></span>
```powershell
PS C:\> Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="67985-120">Ez a parancs beolvassa a MyKey nevű kulcsot a vaultnamed MyKeyVault, és menti az adott kulcs biztonsági másolatát egy backup. blob nevű fájlba.</span><span class="sxs-lookup"><span data-stu-id="67985-120">This command retrieves the key named MyKey from the key vaultnamed MyKeyVault and saves a backup of that key to a file named Backup.blob.</span></span>

### <span data-ttu-id="67985-121">3. példa: biztonsági másolat készítése korábban lekérdezett kulcsról egy megadott fájlnévre, a célfájl felülírása a kérdés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="67985-121">Example 3: Back up a previously retrieved key to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $key = Get-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\> Backup-AzureKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="67985-122">Ez a parancs létrehoz egy biztonsági másolatot a $key nevű kulcsról. Nevezze el a $key nevű boltozatot. VaultName egy backup. blob nevű fájlhoz, a fájl csendes felülírásával, ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="67985-122">This command creates a backup of the key named $key.Name in the vault named $key.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="67985-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="67985-123">PARAMETERS</span></span>

### <span data-ttu-id="67985-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67985-124">-DefaultProfile</span></span>
<span data-ttu-id="67985-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="67985-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67985-126">-Force</span><span class="sxs-lookup"><span data-stu-id="67985-126">-Force</span></span>
<span data-ttu-id="67985-127">A megadott fájl felülírása ha létezik</span><span class="sxs-lookup"><span data-stu-id="67985-127">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="67985-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67985-128">-InputObject</span></span>
<span data-ttu-id="67985-129">Fontos köteg a lekérési hívás kimenetéről való biztonsági mentéshez.</span><span class="sxs-lookup"><span data-stu-id="67985-129">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByKey
Aliases: Key

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67985-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="67985-130">-Name</span></span>
<span data-ttu-id="67985-131">Annak a kulcsnak a neve, amelyről biztonsági másolatot szeretne készíteni.</span><span class="sxs-lookup"><span data-stu-id="67985-131">Specifies the name of the key to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67985-132">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="67985-132">-OutputFile</span></span>
<span data-ttu-id="67985-133">Azt a kimeneti fájlt adja meg, amelyben a biztonsági másolat blobja van tárolva.</span><span class="sxs-lookup"><span data-stu-id="67985-133">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="67985-134">Ha nem adja meg ezt a paramétert, ez a parancsmag létrehoz egy fájlnevet.</span><span class="sxs-lookup"><span data-stu-id="67985-134">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="67985-135">Ha megad egy meglévő kimeneti fájl nevét, a művelet nem fejeződik be, és egy hibaüzenet jelenik meg, amely szerint már létezik a biztonságimásolat-fájl.</span><span class="sxs-lookup"><span data-stu-id="67985-135">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="67985-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="67985-136">-VaultName</span></span>
<span data-ttu-id="67985-137">Annak a kulcsnak a neve, amely a biztonsági másolatot tartalmazó kulcsot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="67985-137">Specifies the name of the key vault that contains the key to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67985-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="67985-138">-Confirm</span></span>
<span data-ttu-id="67985-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="67985-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67985-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67985-140">-WhatIf</span></span>
<span data-ttu-id="67985-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="67985-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67985-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="67985-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67985-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67985-143">CommonParameters</span></span>
<span data-ttu-id="67985-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="67985-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67985-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67985-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67985-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="67985-146">INPUTS</span></span>

### <span data-ttu-id="67985-147">Microsoft. Azure. Command. PSKeyVaultKeyIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="67985-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>
<span data-ttu-id="67985-148">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="67985-148">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="67985-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="67985-149">OUTPUTS</span></span>

### <span data-ttu-id="67985-150">System. String</span><span class="sxs-lookup"><span data-stu-id="67985-150">System.String</span></span>

## <span data-ttu-id="67985-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="67985-151">NOTES</span></span>

## <span data-ttu-id="67985-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="67985-152">RELATED LINKS</span></span>

[<span data-ttu-id="67985-153">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="67985-153">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="67985-154">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="67985-154">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="67985-155">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="67985-155">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="67985-156">Restore-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="67985-156">Restore-AzureKeyVaultKey</span></span>](./Restore-AzureKeyVaultKey.md)

