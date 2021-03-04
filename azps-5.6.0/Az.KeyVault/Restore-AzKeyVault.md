---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/restore-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
ms.openlocfilehash: 36dfd9e5b4e1ddddadb745b2c44ab65b97833baa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931842"
---
# <span data-ttu-id="d7929-101">Restore-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="d7929-101">Restore-AzKeyVault</span></span>

## <span data-ttu-id="d7929-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7929-102">SYNOPSIS</span></span>
<span data-ttu-id="d7929-103">A felügyelt HSM teljes visszaállítása biztonsági másolatból.</span><span class="sxs-lookup"><span data-stu-id="d7929-103">Fully restores a managed HSM from backup.</span></span>

## <span data-ttu-id="d7929-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d7929-104">SYNTAX</span></span>

### <span data-ttu-id="d7929-105">InteractiveStorageName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d7929-105">InteractiveStorageName (Default)</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] [-HsmName] <String>
 -StorageAccountName <String> -StorageContainerName <String> -SasToken <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7929-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="d7929-106">InteractiveStorageUri</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] [-HsmName] <String>
 -StorageContainerUri <Uri> -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7929-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="d7929-107">InputObjectStorageUri</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] -StorageContainerUri <Uri>
 -SasToken <SecureString> -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7929-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="d7929-108">InputObjectStorageName</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7929-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d7929-109">DESCRIPTION</span></span>
<span data-ttu-id="d7929-110">Egy tárfiókban tárolt biztonsági másolatból teljesen visszaállítja a felügyelt HSM-et.</span><span class="sxs-lookup"><span data-stu-id="d7929-110">Fully restores a managed HSM from a backup stored in a storage account.</span></span>
<span data-ttu-id="d7929-111">Biztonsági `Backup-AzKeyVault` másolat készítése.</span><span class="sxs-lookup"><span data-stu-id="d7929-111">Use `Backup-AzKeyVault` to backup.</span></span>

## <span data-ttu-id="d7929-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d7929-112">EXAMPLES</span></span>

### <span data-ttu-id="d7929-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="d7929-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"
PS C:\> Restore-AzKeyVault -HsmName myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -BackupFolder "mhsm-myHsm-2020101308504935" -SasToken $sasToken
```

<span data-ttu-id="d7929-114">A példa visszaállítja a "https://{accountName}.blob.core.windows.net/{containerName}" tároló "mhsm-myHsm-2020101308504935" nevű mappájában tárolt biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="d7929-114">The example restores a backup stored in a folder named "mhsm-myHsm-2020101308504935" of a storage container "https://{accountName}.blob.core.windows.net/{containerName}".</span></span>

## <span data-ttu-id="d7929-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7929-115">PARAMETERS</span></span>

### <span data-ttu-id="d7929-116">-BackupFolder</span><span class="sxs-lookup"><span data-stu-id="d7929-116">-BackupFolder</span></span>
<span data-ttu-id="d7929-117">A biztonsági másolat mappaneve, például "mhsm-*-2020101309020403". Beágyazható például a "backups/mhsm-*-2020101309020403" is.</span><span class="sxs-lookup"><span data-stu-id="d7929-117">Folder name of the backup, e.g. 'mhsm-*-2020101309020403'. It can also be nested such as 'backups/mhsm-*-2020101309020403'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7929-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7929-118">-DefaultProfile</span></span>
<span data-ttu-id="d7929-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d7929-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7929-120">-HsmName</span><span class="sxs-lookup"><span data-stu-id="d7929-120">-HsmName</span></span>
<span data-ttu-id="d7929-121">A HSM neve.</span><span class="sxs-lookup"><span data-stu-id="d7929-121">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InteractiveStorageUri
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7929-122">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="d7929-122">-HsmObject</span></span>
<span data-ttu-id="d7929-123">Felügyelt HSM-objektum</span><span class="sxs-lookup"><span data-stu-id="d7929-123">Managed HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: InputObjectStorageUri, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7929-124">-KeyName</span><span class="sxs-lookup"><span data-stu-id="d7929-124">-KeyName</span></span>
<span data-ttu-id="d7929-125">Visszaállítható kulcsnév.</span><span class="sxs-lookup"><span data-stu-id="d7929-125">Key name to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7929-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7929-126">-PassThru</span></span>
<span data-ttu-id="d7929-127">A HSM visszaállításakor a visszatérési érték igaz.</span><span class="sxs-lookup"><span data-stu-id="d7929-127">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="d7929-128">-SasToken</span><span class="sxs-lookup"><span data-stu-id="d7929-128">-SasToken</span></span>
<span data-ttu-id="d7929-129">A tárfiók hitelesítéséhez használt MEGOSZTOTT hozzáférés-aláírás (SAS) jogkivonat.</span><span class="sxs-lookup"><span data-stu-id="d7929-129">The shared access signature (SAS) token to authenticate the storage account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7929-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d7929-130">-StorageAccountName</span></span>
<span data-ttu-id="d7929-131">Annak a tárfióknak a neve, amelyben a biztonsági mentést tárolni fogja.</span><span class="sxs-lookup"><span data-stu-id="d7929-131">Name of the storage account where the backup is going to be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7929-132">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="d7929-132">-StorageContainerName</span></span>
<span data-ttu-id="d7929-133">Annak a blobtárolónak a neve, amelyben a biztonsági mentést tárolni fogja.</span><span class="sxs-lookup"><span data-stu-id="d7929-133">Name of the blob container where the backup is going to be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7929-134">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="d7929-134">-StorageContainerUri</span></span>
<span data-ttu-id="d7929-135">Annak a tárolónak az URI-ja, amely a biztonsági mentést fogja tárolni.</span><span class="sxs-lookup"><span data-stu-id="d7929-135">URI of the storage container where the backup is going to be stored.</span></span>

```yaml
Type: System.Uri
Parameter Sets: InteractiveStorageUri, InputObjectStorageUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7929-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7929-136">-Confirm</span></span>
<span data-ttu-id="d7929-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d7929-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7929-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7929-138">-WhatIf</span></span>
<span data-ttu-id="d7929-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d7929-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7929-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d7929-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7929-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7929-141">CommonParameters</span></span>
<span data-ttu-id="d7929-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7929-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7929-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7929-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7929-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d7929-144">INPUTS</span></span>

### <span data-ttu-id="d7929-145">Nincs</span><span class="sxs-lookup"><span data-stu-id="d7929-145">None</span></span>

## <span data-ttu-id="d7929-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7929-146">OUTPUTS</span></span>

### <span data-ttu-id="d7929-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d7929-147">System.Boolean</span></span>

## <span data-ttu-id="d7929-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d7929-148">NOTES</span></span>

## <span data-ttu-id="d7929-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7929-149">RELATED LINKS</span></span>
