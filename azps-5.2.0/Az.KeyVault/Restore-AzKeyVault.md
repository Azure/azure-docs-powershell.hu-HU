---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
ms.openlocfilehash: 8be76f6eb5cf56e5f4612a175c067a7647576a4c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354941"
---
# <span data-ttu-id="ef0fe-101">Restore-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="ef0fe-101">Restore-AzKeyVault</span></span>

## <span data-ttu-id="ef0fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef0fe-102">SYNOPSIS</span></span>
<span data-ttu-id="ef0fe-103">A felügyelt HSM teljes visszaállítása biztonsági másolatból.</span><span class="sxs-lookup"><span data-stu-id="ef0fe-103">Fully restores a managed HSM from backup.</span></span>

## <span data-ttu-id="ef0fe-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ef0fe-104">SYNTAX</span></span>

### <span data-ttu-id="ef0fe-105">InteractiveStorageName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ef0fe-105">InteractiveStorageName (Default)</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-PassThru] [-HsmName] <String> -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef0fe-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="ef0fe-106">InteractiveStorageUri</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-PassThru] [-HsmName] <String> -StorageContainerUri <Uri>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef0fe-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="ef0fe-107">InputObjectStorageUri</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-PassThru] -StorageContainerUri <Uri> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef0fe-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="ef0fe-108">InputObjectStorageName</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-PassThru] -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef0fe-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ef0fe-109">DESCRIPTION</span></span>
<span data-ttu-id="ef0fe-110">Egy tárfiókban tárolt biztonsági másolatból teljesen visszaállítja a felügyelt HSM-et.</span><span class="sxs-lookup"><span data-stu-id="ef0fe-110">Fully restores a managed HSM from a backup stored in a storage account.</span></span>
<span data-ttu-id="ef0fe-111">Biztonsági `Backup-AzKeyVault` másolat készítése.</span><span class="sxs-lookup"><span data-stu-id="ef0fe-111">Use `Backup-AzKeyVault` to backup.</span></span>

## <span data-ttu-id="ef0fe-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ef0fe-112">EXAMPLES</span></span>

### <span data-ttu-id="ef0fe-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="ef0fe-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"
PS C:\> Restore-AzKeyVault -HsmName myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -BackupFolder "mhsm-myHsm-2020101308504935" -SasToken $sasToken
```

<span data-ttu-id="ef0fe-114">A példa visszaállítja a "https://{accountName}.blob.core.windows.net/{containerName}" tároló "mhsm-myHsm-2020101308504935" nevű mappájában tárolt biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="ef0fe-114">The example restores a backup stored in a folder named "mhsm-myHsm-2020101308504935" of a storage container "https://{accountName}.blob.core.windows.net/{containerName}".</span></span>

## <span data-ttu-id="ef0fe-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef0fe-115">PARAMETERS</span></span>

### <span data-ttu-id="ef0fe-116">-BackupFolder</span><span class="sxs-lookup"><span data-stu-id="ef0fe-116">-BackupFolder</span></span>
<span data-ttu-id="ef0fe-117">A biztonsági másolat mappaneve, például "mhsm-*-2020101309020403". Beágyazható például a "backups/mhsm-*-2020101309020403" is.</span><span class="sxs-lookup"><span data-stu-id="ef0fe-117">Folder name of the backup, e.g. 'mhsm-*-2020101309020403'. It can also be nested such as 'backups/mhsm-*-2020101309020403'.</span></span>

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

### <span data-ttu-id="ef0fe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef0fe-118">-DefaultProfile</span></span>
<span data-ttu-id="ef0fe-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef0fe-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef0fe-120">-HsmName</span><span class="sxs-lookup"><span data-stu-id="ef0fe-120">-HsmName</span></span>
<span data-ttu-id="ef0fe-121">A HSM neve.</span><span class="sxs-lookup"><span data-stu-id="ef0fe-121">Name of the HSM.</span></span>

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

### <span data-ttu-id="ef0fe-122">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="ef0fe-122">-HsmObject</span></span>
<span data-ttu-id="ef0fe-123">Felügyelt HSM-objektum</span><span class="sxs-lookup"><span data-stu-id="ef0fe-123">Managed HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: InputObjectStorageUri, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef0fe-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef0fe-124">-PassThru</span></span>
<span data-ttu-id="ef0fe-125">A HSM visszaállításakor a visszatérési érték igaz.</span><span class="sxs-lookup"><span data-stu-id="ef0fe-125">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="ef0fe-126">-SasToken</span><span class="sxs-lookup"><span data-stu-id="ef0fe-126">-SasToken</span></span>
<span data-ttu-id="ef0fe-127">A tárfiók hitelesítéséhez használt MEGOSZTOTT hozzáférés-aláírás (SAS) jogkivonat.</span><span class="sxs-lookup"><span data-stu-id="ef0fe-127">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="ef0fe-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ef0fe-128">-StorageAccountName</span></span>
<span data-ttu-id="ef0fe-129">Annak a tárfióknak a neve, amelyben a biztonsági mentést tárolni fogja.</span><span class="sxs-lookup"><span data-stu-id="ef0fe-129">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="ef0fe-130">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="ef0fe-130">-StorageContainerName</span></span>
<span data-ttu-id="ef0fe-131">Annak a blobtárolónak a neve, amelyben a biztonsági mentést tárolni fogja.</span><span class="sxs-lookup"><span data-stu-id="ef0fe-131">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="ef0fe-132">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="ef0fe-132">-StorageContainerUri</span></span>
<span data-ttu-id="ef0fe-133">Annak a tárolónak az URI-ja, amely a biztonsági mentést fogja tárolni.</span><span class="sxs-lookup"><span data-stu-id="ef0fe-133">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="ef0fe-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef0fe-134">-Confirm</span></span>
<span data-ttu-id="ef0fe-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ef0fe-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef0fe-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef0fe-136">-WhatIf</span></span>
<span data-ttu-id="ef0fe-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ef0fe-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef0fe-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ef0fe-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef0fe-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef0fe-139">CommonParameters</span></span>
<span data-ttu-id="ef0fe-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef0fe-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef0fe-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef0fe-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef0fe-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef0fe-142">INPUTS</span></span>

### <span data-ttu-id="ef0fe-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="ef0fe-143">None</span></span>

## <span data-ttu-id="ef0fe-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef0fe-144">OUTPUTS</span></span>

### <span data-ttu-id="ef0fe-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ef0fe-145">System.Boolean</span></span>

## <span data-ttu-id="ef0fe-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ef0fe-146">NOTES</span></span>

## <span data-ttu-id="ef0fe-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef0fe-147">RELATED LINKS</span></span>
