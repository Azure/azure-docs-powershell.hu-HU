---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
ms.openlocfilehash: 51d322ea738a56e4b1fa24cccdb7bb59a6cd0d21
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147706"
---
# <span data-ttu-id="a6439-101">Backup-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a6439-101">Backup-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="a6439-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6439-102">SYNOPSIS</span></span>
<span data-ttu-id="a6439-103">Egy kulcstárolóban tárolt tanúsítvány biztonsági biztonsági ának biztonságira van stb.</span><span class="sxs-lookup"><span data-stu-id="a6439-103">Backs up a certificate in a key vault.</span></span>

## <span data-ttu-id="a6439-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a6439-104">SYNTAX</span></span>

### <span data-ttu-id="a6439-105">ByCertificateName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a6439-105">ByCertificateName (Default)</span></span>
```
Backup-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6439-106">ByCertificate</span><span class="sxs-lookup"><span data-stu-id="a6439-106">ByCertificate</span></span>
```
Backup-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6439-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a6439-107">DESCRIPTION</span></span>
<span data-ttu-id="a6439-108">A **Backup-AzKeyVaultCertificate** parancsmag egy adott tanúsítványról biztonsági másolatot készít egy kulcstárolóban letöltésével és egy fájlban való tárolásával.</span><span class="sxs-lookup"><span data-stu-id="a6439-108">The **Backup-AzKeyVaultCertificate** cmdlet backs up a specified certificate in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="a6439-109">Ha a tanúsítványnak több verziója van, annak összes verziója szerepelni fog a biztonsági másolatban.</span><span class="sxs-lookup"><span data-stu-id="a6439-109">If the certificate has multiple versions, all its versions will be included in the backup.</span></span>
<span data-ttu-id="a6439-110">Mivel a letöltött tartalom titkosítva van, nem használható az Azure-kulcstáron kívül.</span><span class="sxs-lookup"><span data-stu-id="a6439-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="a6439-111">Visszaállíthatja a biztonsági másolatokat az előfizetés bármely kulcstárába, amelyről biztonsági másolat lett, felhasználhatja, ha a tároló ugyanabban az Azure geographyban van.</span><span class="sxs-lookup"><span data-stu-id="a6439-111">You can restore a backed-up certificate to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="a6439-112">A parancsmag használatának tipikus okai:</span><span class="sxs-lookup"><span data-stu-id="a6439-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="a6439-113">Meg szeretné őrizni a tanúsítvány offline másolatát arra az esetre, ha véletlenül törli az eredetit a tárolóból.</span><span class="sxs-lookup"><span data-stu-id="a6439-113">You want to retain an offline copy of the certificate in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="a6439-114">Létrehozott egy tanúsítványt a kulcstárolóval, és most egy másik Azure-régióba szeretné klónozni az objektumot, hogy az elosztott alkalmazás összes példányából felhasználja.</span><span class="sxs-lookup"><span data-stu-id="a6439-114">You created a certificate using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="a6439-115">A **Backup-AzKeyVaultCertificate** parancsmagot használva titkosított formátumban olvassa be a tanúsítványt, majd használja a **Restore-AzKeyVaultCertificate** parancsmagot, és adjon meg egy kulcstárolót a második régióban.</span><span class="sxs-lookup"><span data-stu-id="a6439-115">Use the **Backup-AzKeyVaultCertificate** cmdlet to retrieve the certificate in encrypted format and then use the **Restore-AzKeyVaultCertificate** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="a6439-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a6439-116">EXAMPLES</span></span>

### <span data-ttu-id="a6439-117">1. példa: Tanúsítvány biztonsági mentése automatikusan létrehozott fájlnévvel</span><span class="sxs-lookup"><span data-stu-id="a6439-117">Example 1: Back up a certificate with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

<span data-ttu-id="a6439-118">Ez a parancs beolvassa a MyCert nevű tanúsítványt a MyKeyVault nevű kulcstárolóból, és egy automatikusan elnevezett fájlba menti a tanúsítvány biztonsági másolatát, és megjeleníti a fájl nevét.</span><span class="sxs-lookup"><span data-stu-id="a6439-118">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="a6439-119">2. példa: Tanúsítvány biztonsági mentése egy megadott fájlnévre</span><span class="sxs-lookup"><span data-stu-id="a6439-119">Example 2: Back up a certificate to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="a6439-120">Ez a parancs beolvassa a MyCert nevű tanúsítványt a MyKeyVault nevű kulcstárolóból, és biztonsági másolatot készít a tanúsítványról egy Backup.blob nevű fájlba.</span><span class="sxs-lookup"><span data-stu-id="a6439-120">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file named Backup.blob.</span></span>

### <span data-ttu-id="a6439-121">3. példa: Korábban lekért tanúsítvány biztonsági mentése egy megadott fájlnévre, a célfájl felülírása kérés nélkül.</span><span class="sxs-lookup"><span data-stu-id="a6439-121">Example 3: Back up a previously retrieved certificate to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $cert = Get-AzKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="a6439-122">Ezzel a paranccsal biztonsági másolatot készít a $cert. Név a tárolóban $cert. A VaultName paramétert a Backup.blob nevű fájlhoz írja, és ha már létezik, csendesen felülírja a fájlt.</span><span class="sxs-lookup"><span data-stu-id="a6439-122">This command creates a backup of the certificate named $cert.Name in the vault named $cert.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="a6439-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6439-123">PARAMETERS</span></span>

### <span data-ttu-id="a6439-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6439-124">-DefaultProfile</span></span>
<span data-ttu-id="a6439-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a6439-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6439-126">-Force</span><span class="sxs-lookup"><span data-stu-id="a6439-126">-Force</span></span>
<span data-ttu-id="a6439-127">A megadott fájl felülírása( ha létezik)</span><span class="sxs-lookup"><span data-stu-id="a6439-127">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="a6439-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6439-128">-InputObject</span></span>
<span data-ttu-id="a6439-129">Titkos adat, amelyről biztonsági hívást kell biztonságivinni, és a beolvasási hívás kimeneteként kell bevinni.</span><span class="sxs-lookup"><span data-stu-id="a6439-129">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByCertificate
Aliases: Certificate

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6439-130">-Name</span><span class="sxs-lookup"><span data-stu-id="a6439-130">-Name</span></span>
<span data-ttu-id="a6439-131">Titkos név.</span><span class="sxs-lookup"><span data-stu-id="a6439-131">Secret name.</span></span>
<span data-ttu-id="a6439-132">A parancsmag a tárolónévből ( jelenleg kijelölt környezetből és titkos névből ) egy titkos kulcs teljes tartománynevét építi fel.</span><span class="sxs-lookup"><span data-stu-id="a6439-132">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6439-133">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="a6439-133">-OutputFile</span></span>
<span data-ttu-id="a6439-134">Kimeneti fájl.</span><span class="sxs-lookup"><span data-stu-id="a6439-134">Output file.</span></span>
<span data-ttu-id="a6439-135">A tanúsítvány biztonsági másolatát tároló kimeneti fájl.</span><span class="sxs-lookup"><span data-stu-id="a6439-135">The output file to store the backup of the certificate.</span></span>
<span data-ttu-id="a6439-136">Ha nincs megadva, a rendszer létrehoz egy alapértelmezett fájlnevet.</span><span class="sxs-lookup"><span data-stu-id="a6439-136">If not specified, a default filename will be generated.</span></span>

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

### <span data-ttu-id="a6439-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a6439-137">-VaultName</span></span>
<span data-ttu-id="a6439-138">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="a6439-138">Vault name.</span></span>
<span data-ttu-id="a6439-139">A parancsmag a név és a jelenleg kijelölt környezet alapján építi fel egy tároló teljes tartománynevét.</span><span class="sxs-lookup"><span data-stu-id="a6439-139">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6439-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6439-140">-Confirm</span></span>
<span data-ttu-id="a6439-141">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a6439-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6439-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6439-142">-WhatIf</span></span>
<span data-ttu-id="a6439-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a6439-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6439-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a6439-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6439-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6439-145">CommonParameters</span></span>
<span data-ttu-id="a6439-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6439-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6439-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6439-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6439-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a6439-148">INPUTS</span></span>

### <span data-ttu-id="a6439-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a6439-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="a6439-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6439-150">OUTPUTS</span></span>

### <span data-ttu-id="a6439-151">System.String</span><span class="sxs-lookup"><span data-stu-id="a6439-151">System.String</span></span>

## <span data-ttu-id="a6439-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a6439-152">NOTES</span></span>

## <span data-ttu-id="a6439-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a6439-153">RELATED LINKS</span></span>
