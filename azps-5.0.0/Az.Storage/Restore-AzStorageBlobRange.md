---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/restore-azstorageblobrange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
ms.openlocfilehash: ee8a8bd6a12d3f4aa1dc1624d0dc5c11de972b11
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185787"
---
# <span data-ttu-id="a8b68-101">Restore-AzStorageBlobRange</span><span class="sxs-lookup"><span data-stu-id="a8b68-101">Restore-AzStorageBlobRange</span></span>

## <span data-ttu-id="a8b68-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a8b68-102">SYNOPSIS</span></span>
<span data-ttu-id="a8b68-103">Bizonyos blob-tartományokhoz tartozó tárolási fiók visszaállítása.</span><span class="sxs-lookup"><span data-stu-id="a8b68-103">Restores a Storage account for specific blob ranges.</span></span>

## <span data-ttu-id="a8b68-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a8b68-104">SYNTAX</span></span>

### <span data-ttu-id="a8b68-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a8b68-105">AccountName (Default)</span></span>
```
Restore-AzStorageBlobRange [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -TimeToRestore <DateTime> [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8b68-106">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="a8b68-106">AccountResourceId</span></span>
```
Restore-AzStorageBlobRange [-ResourceId] <String> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8b68-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="a8b68-107">AccountObject</span></span>
```
Restore-AzStorageBlobRange -StorageAccount <PSStorageAccount> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8b68-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a8b68-108">DESCRIPTION</span></span>
<span data-ttu-id="a8b68-109">A **Restore-AzStorageBlobRange** parancsmag bizonyos blob-tartományokra visszaállítja a blobokat egy tárterület-fiókban.</span><span class="sxs-lookup"><span data-stu-id="a8b68-109">The **Restore-AzStorageBlobRange** cmdlet restores blobs in a Storage account for specific blob ranges.</span></span>
<span data-ttu-id="a8b68-110">A program a kezdőpontot is tartalmazza, és a végpontot kihagyja a blob-visszaállításban.</span><span class="sxs-lookup"><span data-stu-id="a8b68-110">The start range is included, and the end range is excluded in blob restore.</span></span>

## <span data-ttu-id="a8b68-111">Példák</span><span class="sxs-lookup"><span data-stu-id="a8b68-111">EXAMPLES</span></span>

### <span data-ttu-id="a8b68-112">1. példa: indítsa újra a blobokat egy bizonyos blob-tartományokat tartalmazó tárterület-fiókban.</span><span class="sxs-lookup"><span data-stu-id="a8b68-112">Example 1: Start restores blobs in a Storage account with specific blob ranges</span></span>
```powershell
PS C:\> $range1 = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
PS C:\> $range2 = New-AzStorageBlobRangeToRestore -StartRange container3/blob3 -EndRange container4/blob4
PS C:\> Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -TimeToRestore (Get-Date).AddDays(-1) -BlobRestoreRange $range1,$range2

Status     RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                     
------     ---------                            ------------- ------------------------     ---------------------                     
InProgress 6ca55a8b-fca0-461a-8e4c-13927a9707e6               2020-02-10T13:58:44.6841810Z ["container1/blob1" -> "container2/blob2",...]

PS C:\> (Get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName -IncludeBlobRestoreStatus).BlobRestoreStatus 

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                     
------   ---------                            ------------- ------------------------     ---------------------                     
Complete 6ca55a8b-fca0-461a-8e4c-13927a9707e6               2020-02-10T13:58:44.6841810Z ["container1/blob1" -> "container2/blob2",...]
```

<span data-ttu-id="a8b68-113">Ez a parancs először 2 blob-tartományt hoz létre, majd a blobokat az 1 napja</span><span class="sxs-lookup"><span data-stu-id="a8b68-113">This command first creates 2 blob ranges, then start restores blobs in a Storage account with the 2 blob ranges from 1 day ago.</span></span> <span data-ttu-id="a8b68-114">A felhasználó a Get-AzStorageAccount segítségével később nyomon követheti a visszaállítás állapotát.</span><span class="sxs-lookup"><span data-stu-id="a8b68-114">User can use Get-AzStorageAccount to trace the restore status later.</span></span>

### <span data-ttu-id="a8b68-115">2. példa: az összes blob tárolása a backend-fiókban</span><span class="sxs-lookup"><span data-stu-id="a8b68-115">Example 2: Restores all blobs in a Storage account in the backend</span></span>
```powershell
PS C:\> $job = Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -TimeToRestore (Get-Date).AddMinutes(-30) -WaitForComplete -asjob

PS C:\> $job | Wait-Job

PS C:\> $job.Output

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges
------   ---------                            ------------- ------------------------     ---------------------
Complete 0387953a-bbe6-4602-818d-e661581ee44b               2020-08-28T07:11:33.9843100Z ["" -> ""]
```

<span data-ttu-id="a8b68-116">A parancs a tárterület-fiók minden blobját visszaállítja 30 perccel ezelőtt, és megvárja a visszaállítás befejeződését.</span><span class="sxs-lookup"><span data-stu-id="a8b68-116">This command restores all blobs in a Storage account from 30 minutes ago, and wait for the restore complete.</span></span> <span data-ttu-id="a8b68-117">Mivel a módosítások visszaállítása hosszú időt vesz igénybe, a backend with-Asjob paraméterrel futtatja azt, majd megvárja a feladat befejezését és a találatok megjelenítését.</span><span class="sxs-lookup"><span data-stu-id="a8b68-117">Since restore blobs might take a long time, run it in the backend with -Asjob parameter, and then wait for the job complete and show the result.</span></span>

### <span data-ttu-id="a8b68-118">3. példa: a Blobs-adatok közvetlen beírásával visszaállítja a blob-tartományokat, és várja meg, amíg kész</span><span class="sxs-lookup"><span data-stu-id="a8b68-118">Example 3: Restores blobs by input blob ranges directly, and wait for complete</span></span>
```powershell
PS C:\> Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -WaitForComplete `
    -TimeToRestore (Get-Date).AddSeconds(-1) `
    -BlobRestoreRange @{StartRange="aaa/abc";EndRange="bbb/abc"},@{StartRange="bbb/acc";EndRange=""}
WARNING: Restore blob rang with Id 'd66d1d02-6e48-47ef-b516-0155dd8319c6' started. Restore blob ranges time to complete is dependent on the size of the restore.

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges   
------   ---------                            ------------- ------------------------     ---------------------   
Complete d66d1d02-6e48-47ef-b516-0155dd8319c6               2020-02-10T14:17:46.8189116Z ["aaa/abc" -> "bbb/abc",...]
```

<span data-ttu-id="a8b68-119">A parancs visszaállítja a blobokat egy tárolási fiókból 1 nappal korábban, a 2 blob-tartomány közvetlen beírásával az Restore-AzStorageBlobRange parancsmagba.</span><span class="sxs-lookup"><span data-stu-id="a8b68-119">This command restores blobs in a Storage account from 1 day ago, by input 2 blob ranges directly to the Restore-AzStorageBlobRange cmdlet.</span></span> <span data-ttu-id="a8b68-120">Ez a parancs a visszaállítás befejeződésére fog várni.</span><span class="sxs-lookup"><span data-stu-id="a8b68-120">This command will wait for the restore complete.</span></span>

## <span data-ttu-id="a8b68-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a8b68-121">PARAMETERS</span></span>

### <span data-ttu-id="a8b68-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8b68-122">-AsJob</span></span>
<span data-ttu-id="a8b68-123">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a8b68-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a8b68-124">-BlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="a8b68-124">-BlobRestoreRange</span></span>
<span data-ttu-id="a8b68-125">A visszaállítandó blob-tartománnyal.</span><span class="sxs-lookup"><span data-stu-id="a8b68-125">The blob range to Restore.</span></span>
<span data-ttu-id="a8b68-126">Ha nem adja meg ezt a paramétert, a program visszaállítja az összes blobot.</span><span class="sxs-lookup"><span data-stu-id="a8b68-126">If not specify this parameter, will restore all blobs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8b68-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8b68-127">-DefaultProfile</span></span>
<span data-ttu-id="a8b68-128">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a8b68-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8b68-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8b68-129">-ResourceGroupName</span></span>
<span data-ttu-id="a8b68-130">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="a8b68-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="a8b68-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8b68-131">-ResourceId</span></span>
<span data-ttu-id="a8b68-132">Tárolási fiók erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="a8b68-132">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8b68-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="a8b68-133">-StorageAccount</span></span>
<span data-ttu-id="a8b68-134">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="a8b68-134">Storage account object</span></span>

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

### <span data-ttu-id="a8b68-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a8b68-135">-StorageAccountName</span></span>
<span data-ttu-id="a8b68-136">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="a8b68-136">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8b68-137">-TimeToRestore</span><span class="sxs-lookup"><span data-stu-id="a8b68-137">-TimeToRestore</span></span>
<span data-ttu-id="a8b68-138">A blob visszaállításának ideje.</span><span class="sxs-lookup"><span data-stu-id="a8b68-138">The Time to Restore Blob.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8b68-139">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="a8b68-139">-WaitForComplete</span></span>
<span data-ttu-id="a8b68-140">Várakozás a tevékenység visszaállítása befejezésre</span><span class="sxs-lookup"><span data-stu-id="a8b68-140">Wait for Restore task complete</span></span>

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

### <span data-ttu-id="a8b68-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a8b68-141">-Confirm</span></span>
<span data-ttu-id="a8b68-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a8b68-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8b68-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8b68-143">-WhatIf</span></span>
<span data-ttu-id="a8b68-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a8b68-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8b68-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a8b68-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8b68-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8b68-146">CommonParameters</span></span>
<span data-ttu-id="a8b68-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a8b68-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8b68-148">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8b68-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8b68-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8b68-149">INPUTS</span></span>

### <span data-ttu-id="a8b68-150">System. String</span><span class="sxs-lookup"><span data-stu-id="a8b68-150">System.String</span></span>

### <span data-ttu-id="a8b68-151">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a8b68-151">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="a8b68-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8b68-152">OUTPUTS</span></span>

### <span data-ttu-id="a8b68-153">Microsoft. Azure. Command. Management. Storage. models. PSBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="a8b68-153">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreStatus</span></span>

## <span data-ttu-id="a8b68-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a8b68-154">NOTES</span></span>

## <span data-ttu-id="a8b68-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8b68-155">RELATED LINKS</span></span>
