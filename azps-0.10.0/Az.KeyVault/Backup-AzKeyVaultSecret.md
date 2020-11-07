---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/backup-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
ms.openlocfilehash: b1f26123579589c15ac4eff6b577706270a7e15a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842170"
---
# <span data-ttu-id="54e8e-101">Backup-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="54e8e-101">Backup-AzKeyVaultSecret</span></span>

## <span data-ttu-id="54e8e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="54e8e-102">SYNOPSIS</span></span>
<span data-ttu-id="54e8e-103">Titkos biztonsági másolat készítése a fő boltozatról.</span><span class="sxs-lookup"><span data-stu-id="54e8e-103">Backs up a secret in a key vault.</span></span>

## <span data-ttu-id="54e8e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="54e8e-104">SYNTAX</span></span>

### <span data-ttu-id="54e8e-105">BySecretName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="54e8e-105">BySecretName (Default)</span></span>
```
Backup-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54e8e-106">BySecret</span><span class="sxs-lookup"><span data-stu-id="54e8e-106">BySecret</span></span>
```
Backup-AzKeyVaultSecret [-Secret] <Secret> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54e8e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="54e8e-107">DESCRIPTION</span></span>
<span data-ttu-id="54e8e-108">A **biztonsági másolat-AzKeyVaultSecret** parancsmag a megadott titkot biztonsági másolatot készíti a kulcsfájl letöltésével és egy fájlban való tárolásával.</span><span class="sxs-lookup"><span data-stu-id="54e8e-108">The **Backup-AzKeyVaultSecret** cmdlet backs up a specified secret in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="54e8e-109">Ha a titok több verziója is létezik, az összes verzió megtalálható a biztonsági másolatban.</span><span class="sxs-lookup"><span data-stu-id="54e8e-109">If there are multiple versions of the secret, all versions are included in the backup.</span></span>
<span data-ttu-id="54e8e-110">Mivel a letöltött tartalom titkosítva van, nem használható az Azure Key Vault-on kívül.</span><span class="sxs-lookup"><span data-stu-id="54e8e-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="54e8e-111">Az előfizetésben biztonsági másolatot kapott titkos kulcsokat visszaállíthatja a biztonsági másolatból.</span><span class="sxs-lookup"><span data-stu-id="54e8e-111">You can restore a backed-up secret to any key vault in the subscription that it was backed up from.</span></span>

<span data-ttu-id="54e8e-112">A parancsmag használatának tipikus okai a következők:</span><span class="sxs-lookup"><span data-stu-id="54e8e-112">Typical reasons to use this cmdlet are:</span></span>

- <span data-ttu-id="54e8e-113">Szeretne titkos másolatát letétbe helyezni, hogy legyen kapcsolat nélküli példánya, ha véletlenül törölni szeretné a titkát a kulcs boltozatával.</span><span class="sxs-lookup"><span data-stu-id="54e8e-113">You want to escrow a copy of your secret, so that you have an offline copy in case you accidentally delete your secret in your key vault.</span></span>
- <span data-ttu-id="54e8e-114">Titkot vett fel egy kulcsfájl számára, és most szeretné a titkot egy másik Azure-területre beilleszteni, így a kiosztott alkalmazás minden példányában használhatja azt.</span><span class="sxs-lookup"><span data-stu-id="54e8e-114">You added a secret to a key vault and now want to clone the secret into a different Azure region, so that you can use it from all instances of your distributed application.</span></span> <span data-ttu-id="54e8e-115">A Backup-AzKeyVaultSecret parancsmaggal Titkosítsa a titkot titkosított formátumban, majd használja a Restore-AzKeyVaultSecret parancsmagot, és adja meg a második régióban a kulcs boltozatát.</span><span class="sxs-lookup"><span data-stu-id="54e8e-115">Use the Backup-AzKeyVaultSecret cmdlet to retrieve the secret in encrypted format and then use the Restore-AzKeyVaultSecret cmdlet and specify a key vault in the second region.</span></span> <span data-ttu-id="54e8e-116">(Fontos megjegyezni, hogy a régióknak ugyanahhoz a földrajzi területhez kell tartozniuk.)</span><span class="sxs-lookup"><span data-stu-id="54e8e-116">(Note that the regions must belong to the same geography.)</span></span>

## <span data-ttu-id="54e8e-117">Példák</span><span class="sxs-lookup"><span data-stu-id="54e8e-117">EXAMPLES</span></span>

### <span data-ttu-id="54e8e-118">Példa 1: titkos másolat készítése automatikusan létrehozott fájlnévvel</span><span class="sxs-lookup"><span data-stu-id="54e8e-118">Example 1: Back up a secret with an automatically generated file name</span></span>
```
PS C:\>Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="54e8e-119">Ez a parancs beolvassa a keresési kifejezésként nevű titkos MyKeyVault, és menti az adott titok biztonsági másolatát egy automatikusan megnevezett fájlba, és megjeleníti a fájl nevét.</span><span class="sxs-lookup"><span data-stu-id="54e8e-119">This command retrieves the secret named MySecret from the key vault named MyKeyVault and saves a backup of that secret to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="54e8e-120">2. példa: titkos másolat készítése egy megadott fájlnévről, a meglévő fájl megkérdezése nélkül</span><span class="sxs-lookup"><span data-stu-id="54e8e-120">Example 2: Back up a secret to a specified file name, overwriting the existing file without prompting</span></span>
```
PS C:\>Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force
```

<span data-ttu-id="54e8e-121">Ez a parancs beolvassa a keresési kifejezésként nevű titkos vaultnamed MyKeyVault, és menti az adott titok biztonsági másolatát egy backup. blob nevű fájlba.</span><span class="sxs-lookup"><span data-stu-id="54e8e-121">This command retrieves the secret named MySecret from the key vaultnamed MyKeyVault and saves a backup of that secret to a file named Backup.blob.</span></span>

### <span data-ttu-id="54e8e-122">3. példa: biztonsági másolat készítése korábban megadott fájlnévre</span><span class="sxs-lookup"><span data-stu-id="54e8e-122">Example 3: Back up a secret previously retrieved to a specified file name</span></span>
```
PS C:\>$secret = Get-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\>Backup-AzKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'
```

<span data-ttu-id="54e8e-123">Ez a parancs a $secret objektum Vault-nevét és nevét használja a titkos elemre, és menti biztonsági másolatát egy backup. blob nevű fájlba.</span><span class="sxs-lookup"><span data-stu-id="54e8e-123">This command uses the $secret object's vault name and name to retrieves the secret and saves its backup to a file named Backup.blob.</span></span>

## <span data-ttu-id="54e8e-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="54e8e-124">PARAMETERS</span></span>

### <span data-ttu-id="54e8e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54e8e-125">-DefaultProfile</span></span>
<span data-ttu-id="54e8e-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="54e8e-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54e8e-127">-Force</span><span class="sxs-lookup"><span data-stu-id="54e8e-127">-Force</span></span>
<span data-ttu-id="54e8e-128">Megkéri, hogy erősítse meg a kimeneti fájl felülírását (ha létezik).</span><span class="sxs-lookup"><span data-stu-id="54e8e-128">Prompts you for confirmation before overwriting the output file, if that exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54e8e-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="54e8e-129">-Name</span></span>
<span data-ttu-id="54e8e-130">Annak a titoknak a neve, akinek biztonsági másolatot szeretne készíteni.</span><span class="sxs-lookup"><span data-stu-id="54e8e-130">Specifies the name of the secret to back up.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54e8e-131">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="54e8e-131">-OutputFile</span></span>
<span data-ttu-id="54e8e-132">Azt a kimeneti fájlt adja meg, amelyben a biztonsági másolat blobja van tárolva.</span><span class="sxs-lookup"><span data-stu-id="54e8e-132">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="54e8e-133">Ha nem adja meg ezt a paramétert, ez a parancsmag létrehoz egy fájlnevet.</span><span class="sxs-lookup"><span data-stu-id="54e8e-133">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="54e8e-134">Ha megad egy meglévő kimeneti fájl nevét, a művelet nem fejeződik be, és egy hibaüzenet jelenik meg, amely szerint már létezik a biztonságimásolat-fájl.</span><span class="sxs-lookup"><span data-stu-id="54e8e-134">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54e8e-135">-Secret</span><span class="sxs-lookup"><span data-stu-id="54e8e-135">-Secret</span></span>
<span data-ttu-id="54e8e-136">Azt az objektumot adja meg, amelynek a nevét és a boltozatát a biztonsági művelethez használni kell.</span><span class="sxs-lookup"><span data-stu-id="54e8e-136">Specifies the object whose name and vault should be used for the backup operation.</span></span>

```yaml
Type: Secret
Parameter Sets: BySecret
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54e8e-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="54e8e-137">-VaultName</span></span>
<span data-ttu-id="54e8e-138">Annak a kulcsnak a nevét adja meg, amely a titkot tartalmazza a biztonsági mentéshez.</span><span class="sxs-lookup"><span data-stu-id="54e8e-138">Specifies the name of the key vault that contains the secret to back up.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54e8e-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="54e8e-139">-Confirm</span></span>
<span data-ttu-id="54e8e-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="54e8e-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54e8e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54e8e-141">-WhatIf</span></span>
<span data-ttu-id="54e8e-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="54e8e-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54e8e-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="54e8e-143">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54e8e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54e8e-144">CommonParameters</span></span>
<span data-ttu-id="54e8e-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="54e8e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54e8e-146">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54e8e-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54e8e-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="54e8e-147">INPUTS</span></span>

### <span data-ttu-id="54e8e-148">Nincs</span><span class="sxs-lookup"><span data-stu-id="54e8e-148">None</span></span>
<span data-ttu-id="54e8e-149">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="54e8e-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="54e8e-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="54e8e-150">OUTPUTS</span></span>

### <span data-ttu-id="54e8e-151">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="54e8e-151">String</span></span>
<span data-ttu-id="54e8e-152">A parancsmag a kulcs biztonsági másolatát tartalmazó kimeneti fájl elérési útját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="54e8e-152">The cmdlet returns the path of the output file containing the backup of the key.</span></span>

## <span data-ttu-id="54e8e-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="54e8e-153">NOTES</span></span>

## <span data-ttu-id="54e8e-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="54e8e-154">RELATED LINKS</span></span>

[<span data-ttu-id="54e8e-155">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="54e8e-155">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="54e8e-156">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="54e8e-156">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="54e8e-157">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="54e8e-157">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="54e8e-158">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="54e8e-158">Restore-AzKeyVaultSecret</span></span>](./Restore-AzKeyVaultSecret.md)

