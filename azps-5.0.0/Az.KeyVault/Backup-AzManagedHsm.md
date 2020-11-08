---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsm.md
ms.openlocfilehash: 5353adade342b7f73cf60ff6b0befa88f4a3da73
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185320"
---
# <span data-ttu-id="a86a1-101">Backup-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="a86a1-101">Backup-AzManagedHsm</span></span>

## <span data-ttu-id="a86a1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a86a1-102">SYNOPSIS</span></span>
<span data-ttu-id="a86a1-103">Teljes biztonsági másolat a felügyelt HSM-ról</span><span class="sxs-lookup"><span data-stu-id="a86a1-103">Fully backup a managed HSM.</span></span>

## <span data-ttu-id="a86a1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a86a1-104">SYNTAX</span></span>

### <span data-ttu-id="a86a1-105">InteractiveStorageName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a86a1-105">InteractiveStorageName (Default)</span></span>
```
Backup-AzManagedHsm [-Name] <String> -StorageAccountName <String> -StorageContainerName <String>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a86a1-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="a86a1-106">InteractiveStorageUri</span></span>
```
Backup-AzManagedHsm [-Name] <String> -StorageContainerUri <Uri> -SasToken <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a86a1-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="a86a1-107">InputObjectStorageUri</span></span>
```
Backup-AzManagedHsm -StorageContainerUri <Uri> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a86a1-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="a86a1-108">InputObjectStorageName</span></span>
```
Backup-AzManagedHsm -StorageAccountName <String> -StorageContainerName <String> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a86a1-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="a86a1-109">DESCRIPTION</span></span>
<span data-ttu-id="a86a1-110">Teljes mértékben biztonsági másolat készítése a felügyelt HSM-ról a tárolási fiókra.</span><span class="sxs-lookup"><span data-stu-id="a86a1-110">Fully backup a managed HSM to a storage account.</span></span>
<span data-ttu-id="a86a1-111">Segítségével `Restore-AzManagedHsm` visszaállíthatja a biztonsági mentést.</span><span class="sxs-lookup"><span data-stu-id="a86a1-111">Use `Restore-AzManagedHsm` to restore the backup.</span></span>

## <span data-ttu-id="a86a1-112">Példák</span><span class="sxs-lookup"><span data-stu-id="a86a1-112">EXAMPLES</span></span>

### <span data-ttu-id="a86a1-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a86a1-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"

PS C:\> Backup-AzManagedHsm -Name myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -SasToken $sasToken

https://{accountName}.blob.core.windows.net/{containerName}/{backupFolder}
```

<span data-ttu-id="a86a1-114">A parancsmag létrehoz egy mappát (általában elnevezett `mhsm-{name}-{timestamp}` ) a tároló tárolóban, tárolja a biztonsági másolatot abban a mappában, és megjeleníti a mappa URI-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="a86a1-114">The cmdlet will create a folder (typically named `mhsm-{name}-{timestamp}`) in the storage container, store the backup in that folder and output the folder URI.</span></span>

## <span data-ttu-id="a86a1-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a86a1-115">PARAMETERS</span></span>

### <span data-ttu-id="a86a1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a86a1-116">-DefaultProfile</span></span>
<span data-ttu-id="a86a1-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a86a1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a86a1-118">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="a86a1-118">-HsmObject</span></span>
<span data-ttu-id="a86a1-119">Felügyelt HSM objektum</span><span class="sxs-lookup"><span data-stu-id="a86a1-119">Managed HSM object</span></span>

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

### <span data-ttu-id="a86a1-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a86a1-120">-Name</span></span>
<span data-ttu-id="a86a1-121">A HSM neve.</span><span class="sxs-lookup"><span data-stu-id="a86a1-121">Name of the HSM.</span></span>

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

### <span data-ttu-id="a86a1-122">-SasToken</span><span class="sxs-lookup"><span data-stu-id="a86a1-122">-SasToken</span></span>
<span data-ttu-id="a86a1-123">A megosztott hozzáférés-aláírási (SA) jogkivonat hitelesíti a tárolási fiókot.</span><span class="sxs-lookup"><span data-stu-id="a86a1-123">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="a86a1-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a86a1-124">-StorageAccountName</span></span>
<span data-ttu-id="a86a1-125">Annak a tárolási fióknak a neve, amelybe a biztonsági másolatot menteni fogják.</span><span class="sxs-lookup"><span data-stu-id="a86a1-125">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="a86a1-126">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="a86a1-126">-StorageContainerName</span></span>
<span data-ttu-id="a86a1-127">Annak a blob-tárolónak a neve, amelybe a biztonsági másolatot menteni fogják.</span><span class="sxs-lookup"><span data-stu-id="a86a1-127">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="a86a1-128">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="a86a1-128">-StorageContainerUri</span></span>
<span data-ttu-id="a86a1-129">Annak a tárolónak az URI-ja, amelyben a biztonsági másolat tárolása történik.</span><span class="sxs-lookup"><span data-stu-id="a86a1-129">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="a86a1-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a86a1-130">-Confirm</span></span>
<span data-ttu-id="a86a1-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a86a1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a86a1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a86a1-132">-WhatIf</span></span>
<span data-ttu-id="a86a1-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a86a1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a86a1-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a86a1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a86a1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a86a1-135">CommonParameters</span></span>
<span data-ttu-id="a86a1-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a86a1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a86a1-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a86a1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a86a1-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a86a1-138">INPUTS</span></span>

### <span data-ttu-id="a86a1-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="a86a1-139">None</span></span>

## <span data-ttu-id="a86a1-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a86a1-140">OUTPUTS</span></span>

### <span data-ttu-id="a86a1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a86a1-141">System.String</span></span>

## <span data-ttu-id="a86a1-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a86a1-142">NOTES</span></span>

## <span data-ttu-id="a86a1-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a86a1-143">RELATED LINKS</span></span>
