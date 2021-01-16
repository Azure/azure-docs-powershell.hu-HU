---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
ms.openlocfilehash: a171f967a937873b85adcfca732987037e6db0a6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386384"
---
# <span data-ttu-id="149c0-101">Backup-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="149c0-101">Backup-AzKeyVaultSecret</span></span>

## <span data-ttu-id="149c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="149c0-102">SYNOPSIS</span></span>
<span data-ttu-id="149c0-103">Egy kulcstárban tárolt kulcsról biztonsági biztonsági ként biztonsági szerepet bevetve.</span><span class="sxs-lookup"><span data-stu-id="149c0-103">Backs up a secret in a key vault.</span></span>

## <span data-ttu-id="149c0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="149c0-104">SYNTAX</span></span>

### <span data-ttu-id="149c0-105">BySecretName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="149c0-105">BySecretName (Default)</span></span>
```
Backup-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="149c0-106">BySecret</span><span class="sxs-lookup"><span data-stu-id="149c0-106">BySecret</span></span>
```
Backup-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="149c0-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="149c0-107">DESCRIPTION</span></span>
<span data-ttu-id="149c0-108">A **Backup-AzKeyVaultSecret** parancsmag egy adott titkos kulcsról biztonsági másolatot készít egy kulcstárban letöltésével és egy fájlban való tárolásával.</span><span class="sxs-lookup"><span data-stu-id="149c0-108">The **Backup-AzKeyVaultSecret** cmdlet backs up a specified secret in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="149c0-109">Ha a titkos fájlnak több verziója is van, az összes verzió szerepelni fog a biztonsági másolatban.</span><span class="sxs-lookup"><span data-stu-id="149c0-109">If there are multiple versions of the secret, all versions are included in the backup.</span></span>
<span data-ttu-id="149c0-110">Mivel a letöltött tartalom titkosítva van, nem használható az Azure-kulcstáron kívül.</span><span class="sxs-lookup"><span data-stu-id="149c0-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="149c0-111">Visszaállíthatja a biztonsági másolatokat az előfizetés bármely kulcstárába, amelyről biztonsági másolat volt.</span><span class="sxs-lookup"><span data-stu-id="149c0-111">You can restore a backed-up secret to any key vault in the subscription that it was backed up from.</span></span>
<span data-ttu-id="149c0-112">A parancsmag használatának tipikus okai:</span><span class="sxs-lookup"><span data-stu-id="149c0-112">Typical reasons to use this cmdlet are:</span></span>
- <span data-ttu-id="149c0-113">El szeretné tartani a titkos másolata másolatát, hogy offline példánya legyen arra az esetre, ha véletlenül töröl egy titkos példányt a kulcstárból.</span><span class="sxs-lookup"><span data-stu-id="149c0-113">You want to escrow a copy of your secret, so that you have an offline copy in case you accidentally delete your secret in your key vault.</span></span>
- <span data-ttu-id="149c0-114">Felvett egy titkos kulcsot egy kulcstárba, és most egy másik Azure-régióba szeretné azt klónozni, hogy az elosztott alkalmazás összes példányából használva használható.</span><span class="sxs-lookup"><span data-stu-id="149c0-114">You added a secret to a key vault and now want to clone the secret into a different Azure region, so that you can use it from all instances of your distributed application.</span></span> <span data-ttu-id="149c0-115">A Backup-AzKeyVaultSecret parancsmag használatával titkosított formátumban olvassa be a titkos kulcsot, majd a Restore-AzKeyVaultSecret parancsmagot használva adjon meg egy kulcstárat a második régióban.</span><span class="sxs-lookup"><span data-stu-id="149c0-115">Use the Backup-AzKeyVaultSecret cmdlet to retrieve the secret in encrypted format and then use the Restore-AzKeyVaultSecret cmdlet and specify a key vault in the second region.</span></span> <span data-ttu-id="149c0-116">(Ne feledje, hogy a régióknak ugyanannak a földrajzi helynek kell lennie.)</span><span class="sxs-lookup"><span data-stu-id="149c0-116">(Note that the regions must belong to the same geography.)</span></span>

## <span data-ttu-id="149c0-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="149c0-117">EXAMPLES</span></span>

### <span data-ttu-id="149c0-118">1. példa: Titkos fájl biztonsági mentése automatikusan létrehozott fájlnévvel</span><span class="sxs-lookup"><span data-stu-id="149c0-118">Example 1: Back up a secret with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'

C:\Users\username\mykeyvault-mysecret-1527029447.01191
```

<span data-ttu-id="149c0-119">Ez a parancs beolvassa a MyKeyVault nevű kulcstárból a MySecret nevű titkos másolatot, és egy automatikusan elnevezett fájlba menti annak biztonsági másolatát, és megjeleníti a fájl nevét.</span><span class="sxs-lookup"><span data-stu-id="149c0-119">This command retrieves the secret named MySecret from the key vault named MyKeyVault and saves a backup of that secret to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="149c0-120">2. példa: Titkos fájl biztonsági mentése egy megadott fájlnévre, a meglévő fájl felülírása rákérdezés nélkül</span><span class="sxs-lookup"><span data-stu-id="149c0-120">Example 2: Back up a secret to a specified file name, overwriting the existing file without prompting</span></span>
```powershell
PS C:\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="149c0-121">Ez a parancs beolvassa a MySecret nevű titkos fájlt a MyKeyVault nevű kulcstárból, és biztonsági másolatot készít róla egy Backup.blob nevű fájlba.</span><span class="sxs-lookup"><span data-stu-id="149c0-121">This command retrieves the secret named MySecret from the key vaultnamed MyKeyVault and saves a backup of that secret to a file named Backup.blob.</span></span>

### <span data-ttu-id="149c0-122">3. példa: Korábban egy megadott fájlnévre lekért titkos fájl biztonsági mentése</span><span class="sxs-lookup"><span data-stu-id="149c0-122">Example 3: Back up a secret previously retrieved to a specified file name</span></span>
```powershell
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\> Backup-AzKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="149c0-123">Ez a parancs a $secret objektum tárolónevét és nevét használva beolvassa a titkos fájlt, és a biztonsági másolatát egy Backup.blob nevű fájlba menti.</span><span class="sxs-lookup"><span data-stu-id="149c0-123">This command uses the $secret object's vault name and name to retrieves the secret and saves its backup to a file named Backup.blob.</span></span>

## <span data-ttu-id="149c0-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="149c0-124">PARAMETERS</span></span>

### <span data-ttu-id="149c0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="149c0-125">-DefaultProfile</span></span>
<span data-ttu-id="149c0-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="149c0-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="149c0-127">-Force</span><span class="sxs-lookup"><span data-stu-id="149c0-127">-Force</span></span>
<span data-ttu-id="149c0-128">Ha létezik ilyen, a kimeneti fájl felülírása előtt megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="149c0-128">Prompts you for confirmation before overwriting the output file, if that exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="149c0-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="149c0-129">-InputObject</span></span>
<span data-ttu-id="149c0-130">Titkos adat, amelyről biztonsági hívást kell biztonságivinni, és a beolvasási hívás kimeneteként kell bevinni.</span><span class="sxs-lookup"><span data-stu-id="149c0-130">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: BySecret
Aliases: Secret

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="149c0-131">-Name</span><span class="sxs-lookup"><span data-stu-id="149c0-131">-Name</span></span>
<span data-ttu-id="149c0-132">Megadja a biztonságimentő titkos fájl nevét.</span><span class="sxs-lookup"><span data-stu-id="149c0-132">Specifies the name of the secret to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="149c0-133">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="149c0-133">-OutputFile</span></span>
<span data-ttu-id="149c0-134">Azt a kimeneti fájlt adja meg, amelyben a biztonságimásolat-blob található.</span><span class="sxs-lookup"><span data-stu-id="149c0-134">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="149c0-135">Ha nem adja meg ezt a paramétert, ez a parancsmag létrehoz egy fájlnevet.</span><span class="sxs-lookup"><span data-stu-id="149c0-135">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="149c0-136">Ha megadja egy meglévő kimeneti fájl nevét, a művelet nem fejeződik be, és hibaüzenetet ad vissza arról, hogy a biztonsági másolat már létezik.</span><span class="sxs-lookup"><span data-stu-id="149c0-136">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="149c0-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="149c0-137">-VaultName</span></span>
<span data-ttu-id="149c0-138">Annak a kulcstárnak a nevét adja meg, amely a biztonsági adatokat tartalmazó titkos kulcsot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="149c0-138">Specifies the name of the key vault that contains the secret to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="149c0-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="149c0-139">-Confirm</span></span>
<span data-ttu-id="149c0-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="149c0-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="149c0-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="149c0-141">-WhatIf</span></span>
<span data-ttu-id="149c0-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="149c0-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="149c0-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="149c0-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="149c0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="149c0-144">CommonParameters</span></span>
<span data-ttu-id="149c0-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="149c0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="149c0-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="149c0-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="149c0-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="149c0-147">INPUTS</span></span>

### <span data-ttu-id="149c0-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="149c0-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="149c0-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="149c0-149">OUTPUTS</span></span>

### <span data-ttu-id="149c0-150">System.String</span><span class="sxs-lookup"><span data-stu-id="149c0-150">System.String</span></span>

## <span data-ttu-id="149c0-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="149c0-151">NOTES</span></span>

## <span data-ttu-id="149c0-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="149c0-152">RELATED LINKS</span></span>

[<span data-ttu-id="149c0-153">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="149c0-153">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="149c0-154">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="149c0-154">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="149c0-155">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="149c0-155">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="149c0-156">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="149c0-156">Restore-AzKeyVaultSecret</span></span>](./Restore-AzKeyVaultSecret.md)

