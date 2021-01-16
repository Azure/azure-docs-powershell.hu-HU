---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: a5b5b1c761bb6e3c23a5dd5f0525d2d6627b3ab2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349782"
---
# <span data-ttu-id="8799c-101">Enable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="8799c-101">Enable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="8799c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8799c-102">SYNOPSIS</span></span>
<span data-ttu-id="8799c-103">Engedélyezi a Blob-visszaállítási házirendet egy tárfiókon.</span><span class="sxs-lookup"><span data-stu-id="8799c-103">Enables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="8799c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8799c-104">SYNTAX</span></span>

### <span data-ttu-id="8799c-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8799c-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RestoreDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8799c-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="8799c-106">AccountObject</span></span>
```
Enable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8799c-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="8799c-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceId] <String> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8799c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8799c-108">DESCRIPTION</span></span>
<span data-ttu-id="8799c-109">Az **Enable-AzStorageBlobRestorePolicy parancsmag** lehetővé teszi a blob-visszaállítási házirendet az Azure Storage Blob szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="8799c-109">The **Enable-AzStorageBlobRestorePolicy** cmdlet enables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="8799c-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8799c-110">EXAMPLES</span></span>

### <span data-ttu-id="8799c-111">1. példa: Blob-visszaállítási házirendet tesz lehetővé az Azure Storage Blob szolgáltatáshoz egy tárfiókon</span><span class="sxs-lookup"><span data-stu-id="8799c-111">Example 1: Enables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
```powershell
PS C:\> Enable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" $accountName -RetentionDays 5

PS C:\> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -EnableChangeFeed $true

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegoup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : True
DeleteRetentionPolicy.Days    : 5
RestorePolicy.Enabled         : False
RestorePolicy.Days            : 
RestorePolicy.MinRestoreTime  : 
ChangeFeed                    : True
IsVersioningEnabled           : True

PS C:\> Enable-AzStorageBlobRestorePolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -RestoreDays 4

PS C:\> Get-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount"

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegoup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : True
DeleteRetentionPolicy.Days    : 5
RestorePolicy.Enabled         : True
RestorePolicy.Days            : 4
RestorePolicy.MinRestoreTime  : 8/28/2020 6:00:59 AM
ChangeFeed                    : True
IsVersioningEnabled           : True
```

<span data-ttu-id="8799c-112">Ez a parancs először engedélyezi a Blob softdelete és changefeed beállítását, majd engedélyezi a Blob-visszaállítási házirendet, végül pedig ellenőrzi a beállítást a Blob szolgáltatás tulajdonságai között.</span><span class="sxs-lookup"><span data-stu-id="8799c-112">This command first enable Blob softdelete and changefeed, then enables Blob Restore Policy, finally check the setting in Blob service properties.</span></span>
<span data-ttu-id="8799c-113">A RestorePolicy.Days blobszolgáltatásnak kisebbnek kell lennie, mint a DeleteRetentionPolicy.Days.</span><span class="sxs-lookup"><span data-stu-id="8799c-113">The Blob service RestorePolicy.Days must be smaller than DeleteRetentionPolicy.Days.</span></span>
<span data-ttu-id="8799c-114">A blob-visszaállítási házirend engedélyezése előtt engedélyezni kell a blob softdelete és a ChangeFeed funkciót.</span><span class="sxs-lookup"><span data-stu-id="8799c-114">Blob softdelete and ChangeFeed must be enabled before enable blob Restore Policy.</span></span>
<span data-ttu-id="8799c-115">Ha a softdelete és a Changefeed csak engedélyezve van, lehet, hogy várnia kell egy kis ideig, amíg a kiszolgáló kezeli a beállítást, mielőtt engedélyezné a Blob-visszaállítási házirendet.</span><span class="sxs-lookup"><span data-stu-id="8799c-115">If softdelete and Changefeed are just enabled, might need wait for some time for server to handle the setting, before enable Blob restore policy.</span></span>

## <span data-ttu-id="8799c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8799c-116">PARAMETERS</span></span>

### <span data-ttu-id="8799c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8799c-117">-DefaultProfile</span></span>
<span data-ttu-id="8799c-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8799c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8799c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8799c-119">-PassThru</span></span>
<span data-ttu-id="8799c-120">Display ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="8799c-120">Display ServiceProperties</span></span>

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

### <span data-ttu-id="8799c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8799c-121">-ResourceGroupName</span></span>
<span data-ttu-id="8799c-122">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8799c-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8799c-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8799c-123">-ResourceId</span></span>
<span data-ttu-id="8799c-124">Adja meg a tárfiók erőforrás-azonosítóját vagy blobszolgáltatás erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="8799c-124">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8799c-125">-RestoreDays</span><span class="sxs-lookup"><span data-stu-id="8799c-125">-RestoreDays</span></span>
<span data-ttu-id="8799c-126">Beállítja, hogy a blob hány napig állítható vissza.</span><span class="sxs-lookup"><span data-stu-id="8799c-126">Sets the number of days for the blob can be restored..</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8799c-127">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="8799c-127">-StorageAccount</span></span>
<span data-ttu-id="8799c-128">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="8799c-128">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8799c-129">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8799c-129">-StorageAccountName</span></span>
<span data-ttu-id="8799c-130">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="8799c-130">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8799c-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8799c-131">-Confirm</span></span>
<span data-ttu-id="8799c-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8799c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8799c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8799c-133">-WhatIf</span></span>
<span data-ttu-id="8799c-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8799c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8799c-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8799c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8799c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8799c-136">CommonParameters</span></span>
<span data-ttu-id="8799c-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8799c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8799c-138">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8799c-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8799c-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8799c-139">INPUTS</span></span>

### <span data-ttu-id="8799c-140">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8799c-140">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="8799c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="8799c-141">System.String</span></span>

## <span data-ttu-id="8799c-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8799c-142">OUTPUTS</span></span>

### <span data-ttu-id="8799c-143">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="8799c-143">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="8799c-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8799c-144">NOTES</span></span>

## <span data-ttu-id="8799c-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8799c-145">RELATED LINKS</span></span>
