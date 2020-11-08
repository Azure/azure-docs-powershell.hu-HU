---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: a5b5b1c761bb6e3c23a5dd5f0525d2d6627b3ab2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025903"
---
# <span data-ttu-id="b9c07-101">Enable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="b9c07-101">Enable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="b9c07-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b9c07-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c07-103">Lehetővé teszi a blob-visszaállítási házirendet egy tárterület-fiókban.</span><span class="sxs-lookup"><span data-stu-id="b9c07-103">Enables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="b9c07-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b9c07-104">SYNTAX</span></span>

### <span data-ttu-id="b9c07-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b9c07-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RestoreDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b9c07-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="b9c07-106">AccountObject</span></span>
```
Enable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9c07-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="b9c07-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceId] <String> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9c07-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b9c07-108">DESCRIPTION</span></span>
<span data-ttu-id="b9c07-109">Az **enable-AzStorageBlobRestorePolicy** parancsmag lehetővé teszi a blob-visszaállítási házirendet az Azure Storage blob szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="b9c07-109">The **Enable-AzStorageBlobRestorePolicy** cmdlet enables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="b9c07-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b9c07-110">EXAMPLES</span></span>

### <span data-ttu-id="b9c07-111">1. példa: a blob-visszaállítási házirend engedélyezése az Azure Storage blob szolgáltatásához a tárolási fiókban</span><span class="sxs-lookup"><span data-stu-id="b9c07-111">Example 1: Enables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
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

<span data-ttu-id="b9c07-112">Ez a parancs először engedélyezi a blob-softdelete és a changefeed, majd engedélyezi a blob-visszaállítási házirendet, végül ellenőrizze a beállítást a blob-szolgáltatás tulajdonságaiban.</span><span class="sxs-lookup"><span data-stu-id="b9c07-112">This command first enable Blob softdelete and changefeed, then enables Blob Restore Policy, finally check the setting in Blob service properties.</span></span>
<span data-ttu-id="b9c07-113">A blob-szolgáltatás RestorePolicy. Days argumentumának kisebbnek kell lennie, mint a DeleteRetentionPolicy. Days.</span><span class="sxs-lookup"><span data-stu-id="b9c07-113">The Blob service RestorePolicy.Days must be smaller than DeleteRetentionPolicy.Days.</span></span>
<span data-ttu-id="b9c07-114">A blob-visszaállítási házirend engedélyezése előtt engedélyezni kell a blob-softdelete és a ChangeFeed.</span><span class="sxs-lookup"><span data-stu-id="b9c07-114">Blob softdelete and ChangeFeed must be enabled before enable blob Restore Policy.</span></span>
<span data-ttu-id="b9c07-115">Ha a softdelete és a Changefeed csak engedélyezve vannak, előfordulhat, hogy várnia kell egy ideig a kiszolgáló számára a beállítás kezeléséhez, a blob-visszaállítási házirend engedélyezése előtt.</span><span class="sxs-lookup"><span data-stu-id="b9c07-115">If softdelete and Changefeed are just enabled, might need wait for some time for server to handle the setting, before enable Blob restore policy.</span></span>

## <span data-ttu-id="b9c07-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b9c07-116">PARAMETERS</span></span>

### <span data-ttu-id="b9c07-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c07-117">-DefaultProfile</span></span>
<span data-ttu-id="b9c07-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b9c07-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9c07-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9c07-119">-PassThru</span></span>
<span data-ttu-id="b9c07-120">ServiceProperties megjelenítése</span><span class="sxs-lookup"><span data-stu-id="b9c07-120">Display ServiceProperties</span></span>

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

### <span data-ttu-id="b9c07-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9c07-121">-ResourceGroupName</span></span>
<span data-ttu-id="b9c07-122">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="b9c07-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="b9c07-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9c07-123">-ResourceId</span></span>
<span data-ttu-id="b9c07-124">Adja meg a tárolási fiók erőforrás-azonosítóját vagy a blob-szolgáltatás tulajdonságainak erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="b9c07-124">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="b9c07-125">-RestoreDays</span><span class="sxs-lookup"><span data-stu-id="b9c07-125">-RestoreDays</span></span>
<span data-ttu-id="b9c07-126">Itt adhatja meg, hogy a blob hány napig állítható vissza.</span><span class="sxs-lookup"><span data-stu-id="b9c07-126">Sets the number of days for the blob can be restored..</span></span>

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

### <span data-ttu-id="b9c07-127">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="b9c07-127">-StorageAccount</span></span>
<span data-ttu-id="b9c07-128">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="b9c07-128">Storage account object</span></span>

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

### <span data-ttu-id="b9c07-129">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b9c07-129">-StorageAccountName</span></span>
<span data-ttu-id="b9c07-130">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="b9c07-130">Storage Account Name.</span></span>

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

### <span data-ttu-id="b9c07-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b9c07-131">-Confirm</span></span>
<span data-ttu-id="b9c07-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b9c07-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9c07-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9c07-133">-WhatIf</span></span>
<span data-ttu-id="b9c07-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b9c07-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9c07-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b9c07-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9c07-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c07-136">CommonParameters</span></span>
<span data-ttu-id="b9c07-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b9c07-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c07-138">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9c07-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c07-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9c07-139">INPUTS</span></span>

### <span data-ttu-id="b9c07-140">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b9c07-140">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="b9c07-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b9c07-141">System.String</span></span>

## <span data-ttu-id="b9c07-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9c07-142">OUTPUTS</span></span>

### <span data-ttu-id="b9c07-143">Microsoft. Azure. Command. Management. Storage. models. PSRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="b9c07-143">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="b9c07-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b9c07-144">NOTES</span></span>

## <span data-ttu-id="b9c07-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9c07-145">RELATED LINKS</span></span>
