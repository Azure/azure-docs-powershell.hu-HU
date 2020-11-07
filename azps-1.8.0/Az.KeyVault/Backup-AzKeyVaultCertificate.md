---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
ms.openlocfilehash: 0c92dbea0127db82a1b1f4605cd581f31c872a57
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835785"
---
# <span data-ttu-id="a37d6-101">Backup-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a37d6-101">Backup-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="a37d6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a37d6-102">SYNOPSIS</span></span>
<span data-ttu-id="a37d6-103">Biztonsági másolatot készíthet a tanúsítványról egy kulcs boltozatáról.</span><span class="sxs-lookup"><span data-stu-id="a37d6-103">Backs up a certificate in a key vault.</span></span>

## <span data-ttu-id="a37d6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a37d6-104">SYNTAX</span></span>

### <span data-ttu-id="a37d6-105">ByCertificateName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a37d6-105">ByCertificateName (Default)</span></span>
```
Backup-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a37d6-106">ByCertificate</span><span class="sxs-lookup"><span data-stu-id="a37d6-106">ByCertificate</span></span>
```
Backup-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a37d6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a37d6-107">DESCRIPTION</span></span>
<span data-ttu-id="a37d6-108">A **biztonsági másolat-AzKeyVaultCertificate** parancsmag a megadott tanúsítvány biztonsági másolatát egy kulcsos tárolóban, letöltéssel és fájlba történő tárolással támogatja.</span><span class="sxs-lookup"><span data-stu-id="a37d6-108">The **Backup-AzKeyVaultCertificate** cmdlet backs up a specified certificate in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="a37d6-109">Ha a tanúsítvány több verzióból áll, a biztonsági másolatban minden verziója szerepelni fog.</span><span class="sxs-lookup"><span data-stu-id="a37d6-109">If the certificate has multiple versions, all its versions will be included in the backup.</span></span>
<span data-ttu-id="a37d6-110">Mivel a letöltött tartalom titkosítva van, nem használható az Azure Key Vault-on kívül.</span><span class="sxs-lookup"><span data-stu-id="a37d6-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="a37d6-111">A mentett tanúsítványokat visszaállíthatja az előfizetésből, amelyből biztonsági másolatot készít, mindaddig, amíg a boltozat ugyanahhoz az Azure-földrajzhoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="a37d6-111">You can restore a backed-up certificate to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="a37d6-112">A parancsmag használatának tipikus okai a következők:</span><span class="sxs-lookup"><span data-stu-id="a37d6-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="a37d6-113">Szeretné megőrizni a tanúsítvány kapcsolat nélküli másolatát abban az esetben, ha véletlenül törli az eredetit a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="a37d6-113">You want to retain an offline copy of the certificate in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="a37d6-114">A kulccsal létrehozta a tanúsítványt, és most szeretné az objektumot egy másik Azure-területre beilleszteni, így a kiosztott alkalmazás minden példányában használhatja azt.</span><span class="sxs-lookup"><span data-stu-id="a37d6-114">You created a certificate using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="a37d6-115">Használja a **Backup-AzKeyVaultCertificate** parancsmagot a tanúsítvány titkosított formátumban való visszakereséséhez, majd használja a **Restore-AzKeyVaultCertificate** parancsmagot, és adja meg a második régióban a kulcs boltozatát.</span><span class="sxs-lookup"><span data-stu-id="a37d6-115">Use the **Backup-AzKeyVaultCertificate** cmdlet to retrieve the certificate in encrypted format and then use the **Restore-AzKeyVaultCertificate** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="a37d6-116">Példák</span><span class="sxs-lookup"><span data-stu-id="a37d6-116">EXAMPLES</span></span>

### <span data-ttu-id="a37d6-117">Példa 1: tanúsítvány biztonsági mentése automatikusan létrehozott fájlnévvel</span><span class="sxs-lookup"><span data-stu-id="a37d6-117">Example 1: Back up a certificate with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

<span data-ttu-id="a37d6-118">Ez a parancs beolvassa a MyCert nevű tanúsítványt a MyKeyVault nevű kulcs-tárolóból, és menti az adott tanúsítvány biztonsági másolatát egy automatikusan megnevezett fájlba, és megjeleníti a fájl nevét.</span><span class="sxs-lookup"><span data-stu-id="a37d6-118">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="a37d6-119">2. példa: tanúsítvány biztonsági mentése megadott fájlnévre</span><span class="sxs-lookup"><span data-stu-id="a37d6-119">Example 2: Back up a certificate to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="a37d6-120">Ez a parancs beolvassa a MyCert nevű tanúsítványt a MyKeyVault nevű kulcs-tárolóból, és egy biztonsági másolatot ment a biztonsági másolat. blob nevű fájlra.</span><span class="sxs-lookup"><span data-stu-id="a37d6-120">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file named Backup.blob.</span></span>

### <span data-ttu-id="a37d6-121">3. példa: egy korábban beolvasott tanúsítvány biztonsági mentése egy megadott fájlnévre, a célfájl felülírása a kérés nélkül.</span><span class="sxs-lookup"><span data-stu-id="a37d6-121">Example 3: Back up a previously retrieved certificate to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $cert = Get-AzKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="a37d6-122">Ez a parancs létrehoz egy biztonsági másolatot a $cert nevű tanúsítványról. Nevezze el a $cert nevű boltozatot. VaultName egy backup. blob nevű fájlhoz, a fájl csendes felülírásával, ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="a37d6-122">This command creates a backup of the certificate named $cert.Name in the vault named $cert.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="a37d6-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a37d6-123">PARAMETERS</span></span>

### <span data-ttu-id="a37d6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a37d6-124">-DefaultProfile</span></span>
<span data-ttu-id="a37d6-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a37d6-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a37d6-126">-Force</span><span class="sxs-lookup"><span data-stu-id="a37d6-126">-Force</span></span>
<span data-ttu-id="a37d6-127">A megadott fájl felülírása ha létezik</span><span class="sxs-lookup"><span data-stu-id="a37d6-127">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="a37d6-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a37d6-128">-InputObject</span></span>
<span data-ttu-id="a37d6-129">Titok, hogy biztonsági másolatot készítsen a lekérési hívás kimenetéről.</span><span class="sxs-lookup"><span data-stu-id="a37d6-129">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="a37d6-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a37d6-130">-Name</span></span>
<span data-ttu-id="a37d6-131">Titkos név.</span><span class="sxs-lookup"><span data-stu-id="a37d6-131">Secret name.</span></span>
<span data-ttu-id="a37d6-132">A parancsmag a boltozat nevéből, az aktuálisan kijelölt környezetből és a titkos névvel elkészíti a titkos FQDN-t.</span><span class="sxs-lookup"><span data-stu-id="a37d6-132">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="a37d6-133">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="a37d6-133">-OutputFile</span></span>
<span data-ttu-id="a37d6-134">Kimeneti fájl.</span><span class="sxs-lookup"><span data-stu-id="a37d6-134">Output file.</span></span>
<span data-ttu-id="a37d6-135">A kimeneti fájl a tanúsítvány biztonsági másolatának tárolásához.</span><span class="sxs-lookup"><span data-stu-id="a37d6-135">The output file to store the backup of the certificate.</span></span>
<span data-ttu-id="a37d6-136">Ha nincs megadva, a program egy alapértelmezett fájlnevet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a37d6-136">If not specified, a default filename will be generated.</span></span>

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

### <span data-ttu-id="a37d6-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a37d6-137">-VaultName</span></span>
<span data-ttu-id="a37d6-138">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="a37d6-138">Vault name.</span></span>
<span data-ttu-id="a37d6-139">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="a37d6-139">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="a37d6-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a37d6-140">-Confirm</span></span>
<span data-ttu-id="a37d6-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a37d6-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a37d6-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a37d6-142">-WhatIf</span></span>
<span data-ttu-id="a37d6-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a37d6-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a37d6-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a37d6-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a37d6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a37d6-145">CommonParameters</span></span>
<span data-ttu-id="a37d6-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a37d6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a37d6-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a37d6-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a37d6-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a37d6-148">INPUTS</span></span>

### <span data-ttu-id="a37d6-149">Microsoft. Azure. Command. PSKeyVaultCertificateIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="a37d6-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="a37d6-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a37d6-150">OUTPUTS</span></span>

### <span data-ttu-id="a37d6-151">System. String</span><span class="sxs-lookup"><span data-stu-id="a37d6-151">System.String</span></span>

## <span data-ttu-id="a37d6-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a37d6-152">NOTES</span></span>

## <span data-ttu-id="a37d6-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a37d6-153">RELATED LINKS</span></span>
