---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsm.md
ms.openlocfilehash: 97e5c836d7d6b209d31851264047c6df894d77a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195916"
---
# <span data-ttu-id="cb798-101">Restore-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="cb798-101">Restore-AzManagedHsm</span></span>

## <span data-ttu-id="cb798-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cb798-102">SYNOPSIS</span></span>
<span data-ttu-id="cb798-103">Teljes mértékben visszaállítja a felügyelt HSM biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="cb798-103">Fully restores a managed HSM from backup.</span></span>

## <span data-ttu-id="cb798-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cb798-104">SYNTAX</span></span>

### <span data-ttu-id="cb798-105">InteractiveStorageName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cb798-105">InteractiveStorageName (Default)</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] [-Name] <String> -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb798-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="cb798-106">InteractiveStorageUri</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] [-Name] <String> -StorageContainerUri <Uri>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb798-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="cb798-107">InputObjectStorageUri</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] -StorageContainerUri <Uri> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb798-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="cb798-108">InputObjectStorageName</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb798-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="cb798-109">DESCRIPTION</span></span>
<span data-ttu-id="cb798-110">Teljes mértékben visszaállítja a felügyelt HSM-t egy tároló fiókban tárolt biztonsági másolatból.</span><span class="sxs-lookup"><span data-stu-id="cb798-110">Fully restores a managed HSM from a backup stored in a storage account.</span></span>
<span data-ttu-id="cb798-111">Használható `Backup-AzManagedHsm` a biztonsági mentéshez.</span><span class="sxs-lookup"><span data-stu-id="cb798-111">Use `Backup-AzManagedHsm` to backup.</span></span>

## <span data-ttu-id="cb798-112">Példák</span><span class="sxs-lookup"><span data-stu-id="cb798-112">EXAMPLES</span></span>

### <span data-ttu-id="cb798-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cb798-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"
PS C:\> Restore-AzManagedHsm -Name myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -BackupFolder "mhsm-myHsm-2020101308504935" -SasToken $sasToken
```

<span data-ttu-id="cb798-114">A példa visszaállít egy "mhsm-myHsm-2020101308504935" nevű mappában lévő biztonsági másolatot a "https://{accountName}. blob. Core. Windows. net/{containerName}" nevű mappából.</span><span class="sxs-lookup"><span data-stu-id="cb798-114">The example restores a backup stored in a folder named "mhsm-myHsm-2020101308504935" of a storage container "https://{accountName}.blob.core.windows.net/{containerName}".</span></span>

## <span data-ttu-id="cb798-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cb798-115">PARAMETERS</span></span>

### <span data-ttu-id="cb798-116">-BackupFolder</span><span class="sxs-lookup"><span data-stu-id="cb798-116">-BackupFolder</span></span>
<span data-ttu-id="cb798-117">A biztonsági másolat mappájának neve (például "mhsm – *2020101309020403"). Az is beágyazható, mint például a "biztonsági másolatok/mhsm –* 2020101309020403".</span><span class="sxs-lookup"><span data-stu-id="cb798-117">Folder name of the backup, e.g. 'mhsm- *-2020101309020403'. It can also be nested such as 'backups/mhsm-* -2020101309020403'.</span></span>

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

### <span data-ttu-id="cb798-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb798-118">-DefaultProfile</span></span>
<span data-ttu-id="cb798-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cb798-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb798-120">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="cb798-120">-HsmObject</span></span>
<span data-ttu-id="cb798-121">Felügyelt HSM objektum</span><span class="sxs-lookup"><span data-stu-id="cb798-121">Managed HSM object</span></span>

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

### <span data-ttu-id="cb798-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cb798-122">-Name</span></span>
<span data-ttu-id="cb798-123">A HSM neve.</span><span class="sxs-lookup"><span data-stu-id="cb798-123">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InteractiveStorageUri
Aliases: HsmName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb798-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb798-124">-PassThru</span></span>
<span data-ttu-id="cb798-125">Igaz érték visszaadása a HSM visszaállításakor</span><span class="sxs-lookup"><span data-stu-id="cb798-125">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="cb798-126">-SasToken</span><span class="sxs-lookup"><span data-stu-id="cb798-126">-SasToken</span></span>
<span data-ttu-id="cb798-127">A megosztott hozzáférés-aláírási (SA) jogkivonat hitelesíti a tárolási fiókot.</span><span class="sxs-lookup"><span data-stu-id="cb798-127">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="cb798-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cb798-128">-StorageAccountName</span></span>
<span data-ttu-id="cb798-129">Annak a tárolási fióknak a neve, amelybe a biztonsági másolatot menteni fogják.</span><span class="sxs-lookup"><span data-stu-id="cb798-129">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="cb798-130">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="cb798-130">-StorageContainerName</span></span>
<span data-ttu-id="cb798-131">Annak a blob-tárolónak a neve, amelybe a biztonsági másolatot menteni fogják.</span><span class="sxs-lookup"><span data-stu-id="cb798-131">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="cb798-132">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="cb798-132">-StorageContainerUri</span></span>
<span data-ttu-id="cb798-133">Annak a tárolónak az URI-ja, amelyben a biztonsági másolat tárolása történik.</span><span class="sxs-lookup"><span data-stu-id="cb798-133">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="cb798-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cb798-134">-Confirm</span></span>
<span data-ttu-id="cb798-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cb798-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb798-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb798-136">-WhatIf</span></span>
<span data-ttu-id="cb798-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cb798-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb798-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cb798-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb798-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb798-139">CommonParameters</span></span>
<span data-ttu-id="cb798-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cb798-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb798-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cb798-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb798-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb798-142">INPUTS</span></span>

### <span data-ttu-id="cb798-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="cb798-143">None</span></span>

## <span data-ttu-id="cb798-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb798-144">OUTPUTS</span></span>

### <span data-ttu-id="cb798-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cb798-145">System.Boolean</span></span>

## <span data-ttu-id="cb798-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cb798-146">NOTES</span></span>

## <span data-ttu-id="cb798-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb798-147">RELATED LINKS</span></span>
