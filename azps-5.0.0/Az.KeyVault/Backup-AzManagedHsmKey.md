---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmKey.md
ms.openlocfilehash: 9e75b6de483f0103103434518d31b472660f4a70
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296873"
---
# <span data-ttu-id="65638-101">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="65638-101">Backup-AzManagedHsmKey</span></span>

## <span data-ttu-id="65638-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="65638-102">SYNOPSIS</span></span>
<span data-ttu-id="65638-103">Egy felügyelt HSM-kulcs biztonsági mentése</span><span class="sxs-lookup"><span data-stu-id="65638-103">Backs up a key in a managed HSM.</span></span>

## <span data-ttu-id="65638-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="65638-104">SYNTAX</span></span>

### <span data-ttu-id="65638-105">ByKeyName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="65638-105">ByKeyName (Default)</span></span>
```
Backup-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65638-106">ByKey</span><span class="sxs-lookup"><span data-stu-id="65638-106">ByKey</span></span>
```
Backup-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65638-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="65638-107">DESCRIPTION</span></span>
<span data-ttu-id="65638-108">A **biztonsági másolat-AzManagedHsmKey** parancsmag a felügyelt HSM megadott kulcsát biztonsági másolatot készíti egy fájlban történő letöltéssel.</span><span class="sxs-lookup"><span data-stu-id="65638-108">The **Backup-AzManagedHsmKey** cmdlet backs up a specified key in a managed HSM by downloading it and storing it in a file.</span></span>
<span data-ttu-id="65638-109">Ha a kulcs több verziója is létezik, az összes verzió megtalálható a biztonsági másolatban.</span><span class="sxs-lookup"><span data-stu-id="65638-109">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="65638-110">Mivel a letöltött tartalom titkosítva van, nem használható az Azure Managed HSM alkalmazáson kívül.</span><span class="sxs-lookup"><span data-stu-id="65638-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Managed HSM.</span></span>
<span data-ttu-id="65638-111">A mentett kulcsokat visszaállíthatja az előfizetésben lévő felügyelt HSM-ra.</span><span class="sxs-lookup"><span data-stu-id="65638-111">You can restore a backed-up key to any managed HSM in the subscription that it was backed up from.</span></span>
<span data-ttu-id="65638-112">A parancsmag használatának tipikus okai a következők:</span><span class="sxs-lookup"><span data-stu-id="65638-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="65638-113">Szeretne a kulcs egy példányát letétbe helyezni, hogy legyen kapcsolat nélküli példánya, ha véletlenül törli a kulcsot a felügyelt HSM-ben.</span><span class="sxs-lookup"><span data-stu-id="65638-113">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your managed HSM.</span></span>
 
- <span data-ttu-id="65638-114">A felügyelt HSM segítségével létrehozta a kulcsot, és most egy másik Azure-területre szeretné használni a kulcsot, így a kiosztott alkalmazás minden példányában használhatja azt.</span><span class="sxs-lookup"><span data-stu-id="65638-114">You created a key using Managed HSM and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="65638-115">Használja a **Backup-AzManagedHsmKey** parancsmagot a kulcs titkosított formátumban való visszakereséséhez, majd használja az Restore-AzManagedHsmKey parancsmagot, és adja meg a kezelt HSM-t a második régióban.</span><span class="sxs-lookup"><span data-stu-id="65638-115">Use the **Backup-AzManagedHsmKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzManagedHsmKey cmdlet and specify a managed HSM in the second region.</span></span>

## <span data-ttu-id="65638-116">Példák</span><span class="sxs-lookup"><span data-stu-id="65638-116">EXAMPLES</span></span>

### <span data-ttu-id="65638-117">1. példa: kulcs biztonsági mentése automatikusan generált fájlnévvel</span><span class="sxs-lookup"><span data-stu-id="65638-117">Example 1: Back up a key with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzManagedHsmKey -HsmName testmhsm -Name testkey

C:\Users\username\testmhsm-testkey-1602664728.7106073
```

<span data-ttu-id="65638-118">Ez a parancs beolvassa a testkey nevű kulcsot a testmhsm nevű felügyelt HSM szolgáltatásból, és menti az adott kulcs biztonsági másolatát egy automatikusan elnevezett fájlba, és megjeleníti a fájl nevét.</span><span class="sxs-lookup"><span data-stu-id="65638-118">This command retrieves the key named testkey from the managed HSM named testmhsm and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

## <span data-ttu-id="65638-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="65638-119">PARAMETERS</span></span>

### <span data-ttu-id="65638-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65638-120">-DefaultProfile</span></span>
<span data-ttu-id="65638-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="65638-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65638-122">-Force</span><span class="sxs-lookup"><span data-stu-id="65638-122">-Force</span></span>
<span data-ttu-id="65638-123">A megadott fájl felülírása ha létezik</span><span class="sxs-lookup"><span data-stu-id="65638-123">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="65638-124">-HsmName</span><span class="sxs-lookup"><span data-stu-id="65638-124">-HsmName</span></span>
<span data-ttu-id="65638-125">HSM-név.</span><span class="sxs-lookup"><span data-stu-id="65638-125">HSM name.</span></span> <span data-ttu-id="65638-126">A parancsmag a felügyelt HSM teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="65638-126">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="65638-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65638-127">-InputObject</span></span>
<span data-ttu-id="65638-128">Fontos köteg a lekérési hívás kimenetéről való biztonsági mentéshez.</span><span class="sxs-lookup"><span data-stu-id="65638-128">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="65638-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="65638-129">-Name</span></span>
<span data-ttu-id="65638-130">Fontos név.</span><span class="sxs-lookup"><span data-stu-id="65638-130">Key name.</span></span>
<span data-ttu-id="65638-131">Parancsmag: a felügyelt HSM-név, az aktuálisan kijelölt környezet és a kulcsnév alapján egy kulcs teljes tartománynevét építi fel.</span><span class="sxs-lookup"><span data-stu-id="65638-131">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="65638-132">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="65638-132">-OutputFile</span></span>
<span data-ttu-id="65638-133">Kimeneti fájl.</span><span class="sxs-lookup"><span data-stu-id="65638-133">Output file.</span></span>
<span data-ttu-id="65638-134">A kimeneti fájl a mentett kulcs blobjának tárolásához.</span><span class="sxs-lookup"><span data-stu-id="65638-134">The output file to store the backed up key blob in.</span></span>
<span data-ttu-id="65638-135">Ha nem jelenik meg, az alapértelmezett fájlnév van kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="65638-135">If not present, a default filename is chosen.</span></span>

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

### <span data-ttu-id="65638-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="65638-136">-Confirm</span></span>
<span data-ttu-id="65638-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="65638-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65638-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65638-138">-WhatIf</span></span>
<span data-ttu-id="65638-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="65638-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65638-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="65638-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65638-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65638-141">CommonParameters</span></span>
<span data-ttu-id="65638-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="65638-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65638-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="65638-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65638-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="65638-144">INPUTS</span></span>

### <span data-ttu-id="65638-145">Microsoft. Azure. Command. PSKeyVaultKeyIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="65638-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="65638-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65638-146">OUTPUTS</span></span>

### <span data-ttu-id="65638-147">System. String</span><span class="sxs-lookup"><span data-stu-id="65638-147">System.String</span></span>

## <span data-ttu-id="65638-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="65638-148">NOTES</span></span>

## <span data-ttu-id="65638-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65638-149">RELATED LINKS</span></span>

[<span data-ttu-id="65638-150">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="65638-150">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="65638-151">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="65638-151">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="65638-152">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="65638-152">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="65638-153">Visszavonás – AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="65638-153">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="65638-154">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="65638-154">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="65638-155">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="65638-155">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)