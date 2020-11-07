---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultsecret
schema: 2.0.0
ms.openlocfilehash: cd83d61c64e4111faf7fc6149107e172d0cf0c9f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848250"
---
# <span data-ttu-id="607fa-101">Backup-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="607fa-101">Backup-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="607fa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="607fa-102">SYNOPSIS</span></span>
<span data-ttu-id="607fa-103">Titkos biztonsági másolat készítése a fő boltozatról.</span><span class="sxs-lookup"><span data-stu-id="607fa-103">Backs up a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="607fa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="607fa-104">SYNTAX</span></span>

### <span data-ttu-id="607fa-105">BySecretName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="607fa-105">BySecretName (Default)</span></span>
```
Backup-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="607fa-106">BySecret</span><span class="sxs-lookup"><span data-stu-id="607fa-106">BySecret</span></span>
```
Backup-AzureKeyVaultSecret [-Secret] <Secret> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="607fa-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="607fa-107">DESCRIPTION</span></span>
<span data-ttu-id="607fa-108">A **biztonsági másolat-AzureKeyVaultSecret** parancsmag a megadott titkot biztonsági másolatot készíti a kulcsfájl letöltésével és egy fájlban való tárolásával.</span><span class="sxs-lookup"><span data-stu-id="607fa-108">The **Backup-AzureKeyVaultSecret** cmdlet backs up a specified secret in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="607fa-109">Ha a titok több verziója is létezik, az összes verzió megtalálható a biztonsági másolatban.</span><span class="sxs-lookup"><span data-stu-id="607fa-109">If there are multiple versions of the secret, all versions are included in the backup.</span></span>
<span data-ttu-id="607fa-110">Mivel a letöltött tartalom titkosítva van, nem használható az Azure Key Vault-on kívül.</span><span class="sxs-lookup"><span data-stu-id="607fa-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="607fa-111">Az előfizetésben biztonsági másolatot kapott titkos kulcsokat visszaállíthatja a biztonsági másolatból.</span><span class="sxs-lookup"><span data-stu-id="607fa-111">You can restore a backed-up secret to any key vault in the subscription that it was backed up from.</span></span>

<span data-ttu-id="607fa-112">A parancsmag használatának tipikus okai a következők:</span><span class="sxs-lookup"><span data-stu-id="607fa-112">Typical reasons to use this cmdlet are:</span></span>

- <span data-ttu-id="607fa-113">Szeretne titkos másolatát letétbe helyezni, hogy legyen kapcsolat nélküli példánya, ha véletlenül törölni szeretné a titkát a kulcs boltozatával.</span><span class="sxs-lookup"><span data-stu-id="607fa-113">You want to escrow a copy of your secret, so that you have an offline copy in case you accidentally delete your secret in your key vault.</span></span>
- <span data-ttu-id="607fa-114">Titkot vett fel egy kulcsfájl számára, és most szeretné a titkot egy másik Azure-területre beilleszteni, így a kiosztott alkalmazás minden példányában használhatja azt.</span><span class="sxs-lookup"><span data-stu-id="607fa-114">You added a secret to a key vault and now want to clone the secret into a different Azure region, so that you can use it from all instances of your distributed application.</span></span> <span data-ttu-id="607fa-115">A Backup-AzureKeyVaultSecret parancsmaggal Titkosítsa a titkot titkosított formátumban, majd használja a Restore-AzureKeyVaultSecret parancsmagot, és adja meg a második régióban a kulcs boltozatát.</span><span class="sxs-lookup"><span data-stu-id="607fa-115">Use the Backup-AzureKeyVaultSecret cmdlet to retrieve the secret in encrypted format and then use the Restore-AzureKeyVaultSecret cmdlet and specify a key vault in the second region.</span></span> <span data-ttu-id="607fa-116">(Fontos megjegyezni, hogy a régióknak ugyanahhoz a földrajzi területhez kell tartozniuk.)</span><span class="sxs-lookup"><span data-stu-id="607fa-116">(Note that the regions must belong to the same geography.)</span></span>

## <span data-ttu-id="607fa-117">Példák</span><span class="sxs-lookup"><span data-stu-id="607fa-117">EXAMPLES</span></span>

### <span data-ttu-id="607fa-118">Példa 1: titkos másolat készítése automatikusan létrehozott fájlnévvel</span><span class="sxs-lookup"><span data-stu-id="607fa-118">Example 1: Back up a secret with an automatically generated file name</span></span>
```
PS C:\>Backup-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="607fa-119">Ez a parancs beolvassa a keresési kifejezésként nevű titkos MyKeyVault, és menti az adott titok biztonsági másolatát egy automatikusan megnevezett fájlba, és megjeleníti a fájl nevét.</span><span class="sxs-lookup"><span data-stu-id="607fa-119">This command retrieves the secret named MySecret from the key vault named MyKeyVault and saves a backup of that secret to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="607fa-120">2. példa: titkos másolat készítése egy megadott fájlnévről, a meglévő fájl megkérdezése nélkül</span><span class="sxs-lookup"><span data-stu-id="607fa-120">Example 2: Back up a secret to a specified file name, overwriting the existing file without prompting</span></span>
```
PS C:\>Backup-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force
```

<span data-ttu-id="607fa-121">Ez a parancs beolvassa a keresési kifejezésként nevű titkos vaultnamed MyKeyVault, és menti az adott titok biztonsági másolatát egy backup. blob nevű fájlba.</span><span class="sxs-lookup"><span data-stu-id="607fa-121">This command retrieves the secret named MySecret from the key vaultnamed MyKeyVault and saves a backup of that secret to a file named Backup.blob.</span></span>

### <span data-ttu-id="607fa-122">3. példa: biztonsági másolat készítése korábban megadott fájlnévre</span><span class="sxs-lookup"><span data-stu-id="607fa-122">Example 3: Back up a secret previously retrieved to a specified file name</span></span>
```
PS C:\>$secret = Get-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\>Backup-AzureKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'
```

<span data-ttu-id="607fa-123">Ez a parancs a $secret objektum Vault-nevét és nevét használja a titkos elemre, és menti biztonsági másolatát egy backup. blob nevű fájlba.</span><span class="sxs-lookup"><span data-stu-id="607fa-123">This command uses the $secret object's vault name and name to retrieves the secret and saves its backup to a file named Backup.blob.</span></span>

## <span data-ttu-id="607fa-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="607fa-124">PARAMETERS</span></span>

### <span data-ttu-id="607fa-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="607fa-125">-DefaultProfile</span></span>
<span data-ttu-id="607fa-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="607fa-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="607fa-127">-Force</span><span class="sxs-lookup"><span data-stu-id="607fa-127">-Force</span></span>
<span data-ttu-id="607fa-128">Megkéri, hogy erősítse meg a kimeneti fájl felülírását (ha létezik).</span><span class="sxs-lookup"><span data-stu-id="607fa-128">Prompts you for confirmation before overwriting the output file, if that exists.</span></span>

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

### <span data-ttu-id="607fa-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="607fa-129">-Name</span></span>
<span data-ttu-id="607fa-130">Annak a titoknak a neve, akinek biztonsági másolatot szeretne készíteni.</span><span class="sxs-lookup"><span data-stu-id="607fa-130">Specifies the name of the secret to back up.</span></span>

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

### <span data-ttu-id="607fa-131">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="607fa-131">-OutputFile</span></span>
<span data-ttu-id="607fa-132">Azt a kimeneti fájlt adja meg, amelyben a biztonsági másolat blobja van tárolva.</span><span class="sxs-lookup"><span data-stu-id="607fa-132">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="607fa-133">Ha nem adja meg ezt a paramétert, ez a parancsmag létrehoz egy fájlnevet.</span><span class="sxs-lookup"><span data-stu-id="607fa-133">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="607fa-134">Ha megad egy meglévő kimeneti fájl nevét, a művelet nem fejeződik be, és egy hibaüzenet jelenik meg, amely szerint már létezik a biztonságimásolat-fájl.</span><span class="sxs-lookup"><span data-stu-id="607fa-134">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="607fa-135">-Secret</span><span class="sxs-lookup"><span data-stu-id="607fa-135">-Secret</span></span>
<span data-ttu-id="607fa-136">Azt az objektumot adja meg, amelynek a nevét és a boltozatát a biztonsági művelethez használni kell.</span><span class="sxs-lookup"><span data-stu-id="607fa-136">Specifies the object whose name and vault should be used for the backup operation.</span></span>

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

### <span data-ttu-id="607fa-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="607fa-137">-VaultName</span></span>
<span data-ttu-id="607fa-138">Annak a kulcsnak a nevét adja meg, amely a titkot tartalmazza a biztonsági mentéshez.</span><span class="sxs-lookup"><span data-stu-id="607fa-138">Specifies the name of the key vault that contains the secret to back up.</span></span>

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

### <span data-ttu-id="607fa-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="607fa-139">-Confirm</span></span>
<span data-ttu-id="607fa-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="607fa-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="607fa-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="607fa-141">-WhatIf</span></span>
<span data-ttu-id="607fa-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="607fa-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="607fa-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="607fa-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="607fa-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="607fa-144">CommonParameters</span></span>
<span data-ttu-id="607fa-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="607fa-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="607fa-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="607fa-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="607fa-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="607fa-147">INPUTS</span></span>

## <span data-ttu-id="607fa-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="607fa-148">OUTPUTS</span></span>

### <span data-ttu-id="607fa-149">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="607fa-149">String</span></span>
<span data-ttu-id="607fa-150">A parancsmag a kulcs biztonsági másolatát tartalmazó kimeneti fájl elérési útját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="607fa-150">The cmdlet returns the path of the output file containing the backup of the key.</span></span>

## <span data-ttu-id="607fa-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="607fa-151">NOTES</span></span>

## <span data-ttu-id="607fa-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="607fa-152">RELATED LINKS</span></span>

[<span data-ttu-id="607fa-153">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="607fa-153">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="607fa-154">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="607fa-154">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="607fa-155">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="607fa-155">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="607fa-156">Restore-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="607fa-156">Restore-AzureKeyVaultSecret</span></span>](./Restore-AzureKeyVaultSecret.md)

