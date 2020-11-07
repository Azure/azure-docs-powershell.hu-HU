---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
ms.openlocfilehash: cd5e869b1f1d367002b33c5976434f16b22744e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666211"
---
# <span data-ttu-id="60449-101">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="60449-101">Backup-AzKeyVaultKey</span></span>

## <span data-ttu-id="60449-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="60449-102">SYNOPSIS</span></span>
<span data-ttu-id="60449-103">Biztonsági másolatot készíthet egy kulcsról a boltívben.</span><span class="sxs-lookup"><span data-stu-id="60449-103">Backs up a key in a key vault.</span></span>

## <span data-ttu-id="60449-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="60449-104">SYNTAX</span></span>

### <span data-ttu-id="60449-105">ByKeyName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="60449-105">ByKeyName (Default)</span></span>
```
Backup-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60449-106">ByKey</span><span class="sxs-lookup"><span data-stu-id="60449-106">ByKey</span></span>
```
Backup-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60449-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="60449-107">DESCRIPTION</span></span>
<span data-ttu-id="60449-108">A **biztonsági másolat-AzKeyVaultKey** parancsmag a megadott kulcs biztonsági másolatát biztonsági másolatokkal, letöltéssel és fájlba való tárolással támogatja.</span><span class="sxs-lookup"><span data-stu-id="60449-108">The **Backup-AzKeyVaultKey** cmdlet backs up a specified key in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="60449-109">Ha a kulcs több verziója is létezik, az összes verzió megtalálható a biztonsági másolatban.</span><span class="sxs-lookup"><span data-stu-id="60449-109">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="60449-110">Mivel a letöltött tartalom titkosítva van, nem használható az Azure Key Vault-on kívül.</span><span class="sxs-lookup"><span data-stu-id="60449-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="60449-111">A mentett billentyűket visszaállíthatja annak az előfizetésnek a fő boltozatára, amelyről biztonsági másolatot készített.</span><span class="sxs-lookup"><span data-stu-id="60449-111">You can restore a backed-up key to any key vault in the subscription that it was backed up from.</span></span>
<span data-ttu-id="60449-112">A parancsmag használatának tipikus okai a következők:</span><span class="sxs-lookup"><span data-stu-id="60449-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="60449-113">Szeretne a kulcs egy példányát letétbe helyezni, hogy legyen kapcsolat nélküli példánya, ha véletlenül törli a billentyűt a kulcs-boltozatban.</span><span class="sxs-lookup"><span data-stu-id="60449-113">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your key vault.</span></span>
 
- <span data-ttu-id="60449-114">A Key Vault segítségével létrehozta a kulcsot, és most szeretné egy másik Azure-területre beilleszteni a kulcsot, így a kiosztott alkalmazás minden példányában használhatja azt.</span><span class="sxs-lookup"><span data-stu-id="60449-114">You created a key using Key Vault and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="60449-115">Használja a **Backup-AzKeyVaultKey** parancsmagot a kulcs titkosított formátumban való visszakereséséhez, majd használja az Restore-AzKeyVaultKey parancsmagot, és adja meg a második régióban a kulcs boltozatát.</span><span class="sxs-lookup"><span data-stu-id="60449-115">Use the **Backup-AzKeyVaultKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzKeyVaultKey cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="60449-116">Példák</span><span class="sxs-lookup"><span data-stu-id="60449-116">EXAMPLES</span></span>

### <span data-ttu-id="60449-117">1. példa: kulcs biztonsági mentése automatikusan generált fájlnévvel</span><span class="sxs-lookup"><span data-stu-id="60449-117">Example 1: Back up a key with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'

C:\Users\username\mykeyvault-mykey-1527029447.01191
```

<span data-ttu-id="60449-118">Ez a parancs beolvassa a MyKey nevű kulcsot a MyKeyVault nevű kulcskezelő szolgáltatásból, és menti az adott kulcs biztonsági másolatát egy automatikusan megnevezett fájlba, és megjeleníti a fájl nevét.</span><span class="sxs-lookup"><span data-stu-id="60449-118">This command retrieves the key named MyKey from the key vault named MyKeyVault and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="60449-119">2. példa: kulcs biztonsági mentése megadott fájlnévre</span><span class="sxs-lookup"><span data-stu-id="60449-119">Example 2: Back up a key to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="60449-120">Ez a parancs beolvassa a MyKey nevű kulcsot a vaultnamed MyKeyVault, és menti az adott kulcs biztonsági másolatát egy backup. blob nevű fájlba.</span><span class="sxs-lookup"><span data-stu-id="60449-120">This command retrieves the key named MyKey from the key vaultnamed MyKeyVault and saves a backup of that key to a file named Backup.blob.</span></span>

### <span data-ttu-id="60449-121">3. példa: biztonsági másolat készítése korábban lekérdezett kulcsról egy megadott fájlnévre, a célfájl felülírása a kérdés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="60449-121">Example 3: Back up a previously retrieved key to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $key = Get-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\> Backup-AzKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="60449-122">Ez a parancs létrehoz egy biztonsági másolatot a $key nevű kulcsról. Nevezze el a $key nevű boltozatot. VaultName egy backup. blob nevű fájlhoz, a fájl csendes felülírásával, ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="60449-122">This command creates a backup of the key named $key.Name in the vault named $key.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="60449-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="60449-123">PARAMETERS</span></span>

### <span data-ttu-id="60449-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60449-124">-DefaultProfile</span></span>
<span data-ttu-id="60449-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="60449-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60449-126">-Force</span><span class="sxs-lookup"><span data-stu-id="60449-126">-Force</span></span>
<span data-ttu-id="60449-127">A megadott fájl felülírása ha létezik</span><span class="sxs-lookup"><span data-stu-id="60449-127">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="60449-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60449-128">-InputObject</span></span>
<span data-ttu-id="60449-129">Fontos köteg a lekérési hívás kimenetéről való biztonsági mentéshez.</span><span class="sxs-lookup"><span data-stu-id="60449-129">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="60449-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="60449-130">-Name</span></span>
<span data-ttu-id="60449-131">Annak a kulcsnak a neve, amelyről biztonsági másolatot szeretne készíteni.</span><span class="sxs-lookup"><span data-stu-id="60449-131">Specifies the name of the key to back up.</span></span>

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

### <span data-ttu-id="60449-132">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="60449-132">-OutputFile</span></span>
<span data-ttu-id="60449-133">Azt a kimeneti fájlt adja meg, amelyben a biztonsági másolat blobja van tárolva.</span><span class="sxs-lookup"><span data-stu-id="60449-133">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="60449-134">Ha nem adja meg ezt a paramétert, ez a parancsmag létrehoz egy fájlnevet.</span><span class="sxs-lookup"><span data-stu-id="60449-134">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="60449-135">Ha megad egy meglévő kimeneti fájl nevét, a művelet nem fejeződik be, és egy hibaüzenet jelenik meg, amely szerint már létezik a biztonságimásolat-fájl.</span><span class="sxs-lookup"><span data-stu-id="60449-135">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="60449-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="60449-136">-VaultName</span></span>
<span data-ttu-id="60449-137">Annak a kulcsnak a neve, amely a biztonsági másolatot tartalmazó kulcsot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="60449-137">Specifies the name of the key vault that contains the key to back up.</span></span>

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

### <span data-ttu-id="60449-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="60449-138">-Confirm</span></span>
<span data-ttu-id="60449-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="60449-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60449-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60449-140">-WhatIf</span></span>
<span data-ttu-id="60449-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="60449-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60449-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="60449-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60449-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60449-143">CommonParameters</span></span>
<span data-ttu-id="60449-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="60449-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60449-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60449-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60449-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="60449-146">INPUTS</span></span>

### <span data-ttu-id="60449-147">Microsoft. Azure. Command. PSKeyVaultKeyIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="60449-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="60449-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="60449-148">OUTPUTS</span></span>

### <span data-ttu-id="60449-149">System. String</span><span class="sxs-lookup"><span data-stu-id="60449-149">System.String</span></span>

## <span data-ttu-id="60449-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="60449-150">NOTES</span></span>

## <span data-ttu-id="60449-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="60449-151">RELATED LINKS</span></span>

[<span data-ttu-id="60449-152">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="60449-152">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="60449-153">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="60449-153">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="60449-154">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="60449-154">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="60449-155">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="60449-155">Restore-AzKeyVaultKey</span></span>](./Restore-AzKeyVaultKey.md)

