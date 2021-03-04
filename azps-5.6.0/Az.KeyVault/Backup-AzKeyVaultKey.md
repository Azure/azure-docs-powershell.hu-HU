---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/powershell/module/az.keyvault/backup-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
ms.openlocfilehash: 3123d0fa188e0e9a4c419ceaa567969fc3a2f8b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931122"
---
# <span data-ttu-id="b8c67-101">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b8c67-101">Backup-AzKeyVaultKey</span></span>

## <span data-ttu-id="b8c67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8c67-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c67-103">Kulcs biztonsági biztonsági hátramentve a kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="b8c67-103">Backs up a key in a key vault.</span></span>

## <span data-ttu-id="b8c67-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b8c67-104">SYNTAX</span></span>

### <span data-ttu-id="b8c67-105">ByKeyName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b8c67-105">ByKeyName (Default)</span></span>
```
Backup-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8c67-106">HsmByKeyName</span><span class="sxs-lookup"><span data-stu-id="b8c67-106">HsmByKeyName</span></span>
```
Backup-AzKeyVaultKey -HsmName <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8c67-107">ByKey</span><span class="sxs-lookup"><span data-stu-id="b8c67-107">ByKey</span></span>
```
Backup-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8c67-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b8c67-108">DESCRIPTION</span></span>
<span data-ttu-id="b8c67-109">A **Backup-AzKeyVaultKey** parancsmag egy adott kulcsról biztonsági másolatot készít egy kulcstárban úgy, hogy letölti és egy fájlban tárolja azt.</span><span class="sxs-lookup"><span data-stu-id="b8c67-109">The **Backup-AzKeyVaultKey** cmdlet backs up a specified key in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="b8c67-110">Ha a kulcsnak több verziója is van, az összes verzió szerepelni fog a biztonsági másolatban.</span><span class="sxs-lookup"><span data-stu-id="b8c67-110">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="b8c67-111">Mivel a letöltött tartalom titkosítva van, nem használható az Azure-kulcstáron kívül.</span><span class="sxs-lookup"><span data-stu-id="b8c67-111">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="b8c67-112">Az előfizetés bármely kulcstárában visszaállíthat egy biztonsági másolati kulcsot, amelyről biztonsági másolat volt.</span><span class="sxs-lookup"><span data-stu-id="b8c67-112">You can restore a backed-up key to any key vault in the subscription that it was backed up from.</span></span>
<span data-ttu-id="b8c67-113">A parancsmag használatának tipikus okai:</span><span class="sxs-lookup"><span data-stu-id="b8c67-113">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="b8c67-114">A kulcs egy példányát el szeretné escrow-nak, hogy offline példánya legyen arra az esetre, ha véletlenül törli a kulcsot a kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="b8c67-114">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your key vault.</span></span>
 
- <span data-ttu-id="b8c67-115">A kulcstár segítségével létrehozott egy kulcsot, és most egy másik Azure-régióba szeretné a kulcsot klónozni, hogy az elosztott alkalmazás összes példányából használva használható.</span><span class="sxs-lookup"><span data-stu-id="b8c67-115">You created a key using Key Vault and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="b8c67-116">A **Backup-AzKeyVaultKey** parancsmag használatával titkosított formátumban olvassa be a kulcsot, majd használja a Restore-AzKeyVaultKey-parancsmagot, és adjon meg egy kulcstárat a második régióban.</span><span class="sxs-lookup"><span data-stu-id="b8c67-116">Use the **Backup-AzKeyVaultKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzKeyVaultKey cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="b8c67-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b8c67-117">EXAMPLES</span></span>

### <span data-ttu-id="b8c67-118">1. példa: Kulcs biztonsági mentése automatikusan létrehozott fájlnévvel</span><span class="sxs-lookup"><span data-stu-id="b8c67-118">Example 1: Back up a key with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'

C:\Users\username\mykeyvault-mykey-1527029447.01191
```

<span data-ttu-id="b8c67-119">Ez a parancs beolvassa a MyKeyVault nevű kulcstárból a MyKeyVault nevű kulcsot, és egy automatikusan elnevezett fájlba menti a kulcs biztonsági másolatát, és megjeleníti a fájl nevét.</span><span class="sxs-lookup"><span data-stu-id="b8c67-119">This command retrieves the key named MyKey from the key vault named MyKeyVault and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="b8c67-120">2. példa: Kulcs biztonsági mentése egy megadott fájlnévre</span><span class="sxs-lookup"><span data-stu-id="b8c67-120">Example 2: Back up a key to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="b8c67-121">Ez a parancs lekéri a MyKey nevű kulcskulcsot a MyKeyVault nevű kulcstárból, és biztonsági másolatot készít róla egy Backup.blob nevű fájlba.</span><span class="sxs-lookup"><span data-stu-id="b8c67-121">This command retrieves the key named MyKey from the key vaultnamed MyKeyVault and saves a backup of that key to a file named Backup.blob.</span></span>

### <span data-ttu-id="b8c67-122">3. példa: Korábban lekért kulcs biztonsági mentése egy megadott fájlnévre, a célfájl felülírása kérés nélkül.</span><span class="sxs-lookup"><span data-stu-id="b8c67-122">Example 3: Back up a previously retrieved key to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $key = Get-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\> Backup-AzKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="b8c67-123">Ezzel a paranccsal biztonsági másolatot készít a $key. Név a tárolóban $key. VaultName – a Backup.blob nevű fájlhoz, csendesen felülírva a fájlt, ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="b8c67-123">This command creates a backup of the key named $key.Name in the vault named $key.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="b8c67-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8c67-124">PARAMETERS</span></span>

### <span data-ttu-id="b8c67-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8c67-125">-DefaultProfile</span></span>
<span data-ttu-id="b8c67-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b8c67-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8c67-127">-Force</span><span class="sxs-lookup"><span data-stu-id="b8c67-127">-Force</span></span>
<span data-ttu-id="b8c67-128">A megadott fájl felülírása( ha létezik)</span><span class="sxs-lookup"><span data-stu-id="b8c67-128">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="b8c67-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="b8c67-129">-HsmName</span></span>
<span data-ttu-id="b8c67-130">HSM-név.</span><span class="sxs-lookup"><span data-stu-id="b8c67-130">HSM name.</span></span> <span data-ttu-id="b8c67-131">A parancsmag a felügyelt HSM teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="b8c67-131">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByKeyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c67-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8c67-132">-InputObject</span></span>
<span data-ttu-id="b8c67-133">Key bundle to back up, pipelined in from the output of a retrieval call.</span><span class="sxs-lookup"><span data-stu-id="b8c67-133">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="b8c67-134">-Name</span><span class="sxs-lookup"><span data-stu-id="b8c67-134">-Name</span></span>
<span data-ttu-id="b8c67-135">A biztonságimentő kulcs nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8c67-135">Specifies the name of the key to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, HsmByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c67-136">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="b8c67-136">-OutputFile</span></span>
<span data-ttu-id="b8c67-137">Azt a kimeneti fájlt adja meg, amelyben a biztonságimásolat-blob található.</span><span class="sxs-lookup"><span data-stu-id="b8c67-137">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="b8c67-138">Ha nem adja meg ezt a paramétert, ez a parancsmag létrehoz egy fájlnevet.</span><span class="sxs-lookup"><span data-stu-id="b8c67-138">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="b8c67-139">Ha megadja egy meglévő kimeneti fájl nevét, a művelet nem fejeződik be, és hibaüzenetet ad vissza arról, hogy a biztonsági másolat már létezik.</span><span class="sxs-lookup"><span data-stu-id="b8c67-139">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="b8c67-140">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b8c67-140">-VaultName</span></span>
<span data-ttu-id="b8c67-141">Annak a kulcstárnak a nevét adja meg, amely a biztonsági adatokat tartalmazó kulcsot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b8c67-141">Specifies the name of the key vault that contains the key to back up.</span></span>

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

### <span data-ttu-id="b8c67-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8c67-142">-Confirm</span></span>
<span data-ttu-id="b8c67-143">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b8c67-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8c67-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8c67-144">-WhatIf</span></span>
<span data-ttu-id="b8c67-145">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b8c67-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8c67-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b8c67-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8c67-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c67-147">CommonParameters</span></span>
<span data-ttu-id="b8c67-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8c67-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c67-149">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8c67-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c67-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b8c67-150">INPUTS</span></span>

### <span data-ttu-id="b8c67-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="b8c67-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="b8c67-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8c67-152">OUTPUTS</span></span>

### <span data-ttu-id="b8c67-153">System.String</span><span class="sxs-lookup"><span data-stu-id="b8c67-153">System.String</span></span>

## <span data-ttu-id="b8c67-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b8c67-154">NOTES</span></span>

## <span data-ttu-id="b8c67-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8c67-155">RELATED LINKS</span></span>

[<span data-ttu-id="b8c67-156">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b8c67-156">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="b8c67-157">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b8c67-157">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="b8c67-158">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b8c67-158">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="b8c67-159">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b8c67-159">Restore-AzKeyVaultKey</span></span>](./Restore-AzKeyVaultKey.md)

