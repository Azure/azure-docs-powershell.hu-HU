---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVault.md
ms.openlocfilehash: 7e5aa5091376b8c80d71bdeb2bbad7bd8d22c3a2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357221"
---
# <span data-ttu-id="39e25-101">Backup-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="39e25-101">Backup-AzKeyVault</span></span>

## <span data-ttu-id="39e25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39e25-102">SYNOPSIS</span></span>
<span data-ttu-id="39e25-103">Teljes biztonsági mentés felügyelt HSM-ről.</span><span class="sxs-lookup"><span data-stu-id="39e25-103">Fully backup a managed HSM.</span></span>

## <span data-ttu-id="39e25-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="39e25-104">SYNTAX</span></span>

### <span data-ttu-id="39e25-105">InteractiveStorageName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="39e25-105">InteractiveStorageName (Default)</span></span>
```
Backup-AzKeyVault [-HsmName] <String> -StorageAccountName <String> -StorageContainerName <String>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39e25-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="39e25-106">InteractiveStorageUri</span></span>
```
Backup-AzKeyVault [-HsmName] <String> -StorageContainerUri <Uri> -SasToken <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39e25-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="39e25-107">InputObjectStorageUri</span></span>
```
Backup-AzKeyVault -StorageContainerUri <Uri> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39e25-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="39e25-108">InputObjectStorageName</span></span>
```
Backup-AzKeyVault -StorageAccountName <String> -StorageContainerName <String> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39e25-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="39e25-109">DESCRIPTION</span></span>
<span data-ttu-id="39e25-110">A felügyelt HSM-ről teljes biztonsági mentést kell készítenie egy tárfiókba.</span><span class="sxs-lookup"><span data-stu-id="39e25-110">Fully backup a managed HSM to a storage account.</span></span>
<span data-ttu-id="39e25-111">Segítségével `Restore-AzKeyVault` visszaállíthatja a biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="39e25-111">Use `Restore-AzKeyVault` to restore the backup.</span></span>

## <span data-ttu-id="39e25-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="39e25-112">EXAMPLES</span></span>

### <span data-ttu-id="39e25-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="39e25-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"

PS C:\> Backup-AzKeyVault -HsmName myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -SasToken $sasToken

https://{accountName}.blob.core.windows.net/{containerName}/{backupFolder}
```

<span data-ttu-id="39e25-114">A parancsmag létrehoz egy mappát (általában névvel) a tárolóban, a biztonsági másolatot abban a mappában tárolja, és kimenetként hozza létre a mappa `mhsm-{name}-{timestamp}` URI-ját.</span><span class="sxs-lookup"><span data-stu-id="39e25-114">The cmdlet will create a folder (typically named `mhsm-{name}-{timestamp}`) in the storage container, store the backup in that folder and output the folder URI.</span></span>

## <span data-ttu-id="39e25-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39e25-115">PARAMETERS</span></span>

### <span data-ttu-id="39e25-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39e25-116">-DefaultProfile</span></span>
<span data-ttu-id="39e25-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="39e25-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39e25-118">-HsmName</span><span class="sxs-lookup"><span data-stu-id="39e25-118">-HsmName</span></span>
<span data-ttu-id="39e25-119">A HSM neve.</span><span class="sxs-lookup"><span data-stu-id="39e25-119">Name of the HSM.</span></span>

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

### <span data-ttu-id="39e25-120">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="39e25-120">-HsmObject</span></span>
<span data-ttu-id="39e25-121">Felügyelt HSM-objektum</span><span class="sxs-lookup"><span data-stu-id="39e25-121">Managed HSM object</span></span>

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

### <span data-ttu-id="39e25-122">-SasToken</span><span class="sxs-lookup"><span data-stu-id="39e25-122">-SasToken</span></span>
<span data-ttu-id="39e25-123">A tárfiók hitelesítéséhez használt MEGOSZTOTT hozzáférés-aláírás (SAS) jogkivonat.</span><span class="sxs-lookup"><span data-stu-id="39e25-123">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="39e25-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="39e25-124">-StorageAccountName</span></span>
<span data-ttu-id="39e25-125">Annak a tárfióknak a neve, amelyben a biztonsági mentést tárolni fogja.</span><span class="sxs-lookup"><span data-stu-id="39e25-125">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="39e25-126">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="39e25-126">-StorageContainerName</span></span>
<span data-ttu-id="39e25-127">Annak a blobtárolónak a neve, amelyben a biztonsági mentést tárolni fogja.</span><span class="sxs-lookup"><span data-stu-id="39e25-127">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="39e25-128">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="39e25-128">-StorageContainerUri</span></span>
<span data-ttu-id="39e25-129">Annak a tárolónak az URI-ja, amely a biztonsági mentést fogja tárolni.</span><span class="sxs-lookup"><span data-stu-id="39e25-129">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="39e25-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39e25-130">-Confirm</span></span>
<span data-ttu-id="39e25-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="39e25-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39e25-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39e25-132">-WhatIf</span></span>
<span data-ttu-id="39e25-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="39e25-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39e25-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="39e25-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39e25-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39e25-135">CommonParameters</span></span>
<span data-ttu-id="39e25-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39e25-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39e25-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39e25-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39e25-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39e25-138">INPUTS</span></span>

### <span data-ttu-id="39e25-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="39e25-139">None</span></span>

## <span data-ttu-id="39e25-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39e25-140">OUTPUTS</span></span>

### <span data-ttu-id="39e25-141">System.String</span><span class="sxs-lookup"><span data-stu-id="39e25-141">System.String</span></span>

## <span data-ttu-id="39e25-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="39e25-142">NOTES</span></span>

## <span data-ttu-id="39e25-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39e25-143">RELATED LINKS</span></span>
