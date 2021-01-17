---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/restore-azstorageblobrange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
ms.openlocfilehash: ee8a8bd6a12d3f4aa1dc1624d0dc5c11de972b11
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348401"
---
# <span data-ttu-id="d9db6-101">Restore-AzStorageBlobRange</span><span class="sxs-lookup"><span data-stu-id="d9db6-101">Restore-AzStorageBlobRange</span></span>

## <span data-ttu-id="d9db6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9db6-102">SYNOPSIS</span></span>
<span data-ttu-id="d9db6-103">Adott blobtartományok tárfiókját visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="d9db6-103">Restores a Storage account for specific blob ranges.</span></span>

## <span data-ttu-id="d9db6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d9db6-104">SYNTAX</span></span>

### <span data-ttu-id="d9db6-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d9db6-105">AccountName (Default)</span></span>
```
Restore-AzStorageBlobRange [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -TimeToRestore <DateTime> [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9db6-106">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="d9db6-106">AccountResourceId</span></span>
```
Restore-AzStorageBlobRange [-ResourceId] <String> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9db6-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="d9db6-107">AccountObject</span></span>
```
Restore-AzStorageBlobRange -StorageAccount <PSStorageAccount> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9db6-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d9db6-108">DESCRIPTION</span></span>
<span data-ttu-id="d9db6-109">A **Restore-AzStorageBlobRange** parancsmag adott blobtartományok blobját visszaállítja egy tárfiókban.</span><span class="sxs-lookup"><span data-stu-id="d9db6-109">The **Restore-AzStorageBlobRange** cmdlet restores blobs in a Storage account for specific blob ranges.</span></span>
<span data-ttu-id="d9db6-110">Az indítási tartományt a rendszer tartalmazza, a végponttartományt pedig kihagyja a blob-visszaállításból.</span><span class="sxs-lookup"><span data-stu-id="d9db6-110">The start range is included, and the end range is excluded in blob restore.</span></span>

## <span data-ttu-id="d9db6-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d9db6-111">EXAMPLES</span></span>

### <span data-ttu-id="d9db6-112">1. példa: Blobok visszaállítása adott blobtartományokkal egy tárfiókban</span><span class="sxs-lookup"><span data-stu-id="d9db6-112">Example 1: Start restores blobs in a Storage account with specific blob ranges</span></span>
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

<span data-ttu-id="d9db6-113">Ez a parancs először 2 blobtartományt hoz létre, majd egy 1 nappal ezelőtti 2 blobtartományt tároló tárfiókban elindítja a blobok visszaállítását.</span><span class="sxs-lookup"><span data-stu-id="d9db6-113">This command first creates 2 blob ranges, then start restores blobs in a Storage account with the 2 blob ranges from 1 day ago.</span></span> <span data-ttu-id="d9db6-114">A felhasználó a Get-AzStorageAccount később nyomon tudja követni a visszaállítás állapotát.</span><span class="sxs-lookup"><span data-stu-id="d9db6-114">User can use Get-AzStorageAccount to trace the restore status later.</span></span>

### <span data-ttu-id="d9db6-115">2. példa: Egy tárfiók összes blobját visszaállítja a háttértárban</span><span class="sxs-lookup"><span data-stu-id="d9db6-115">Example 2: Restores all blobs in a Storage account in the backend</span></span>
```powershell
PS C:\> $job = Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -TimeToRestore (Get-Date).AddMinutes(-30) -WaitForComplete -asjob

PS C:\> $job | Wait-Job

PS C:\> $job.Output

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges
------   ---------                            ------------- ------------------------     ---------------------
Complete 0387953a-bbe6-4602-818d-e661581ee44b               2020-08-28T07:11:33.9843100Z ["" -> ""]
```

<span data-ttu-id="d9db6-116">Ez a parancs visszaállítja egy tárfiók összes blobját 30 perce, és várja meg, amíg a visszaállítás befejeződik.</span><span class="sxs-lookup"><span data-stu-id="d9db6-116">This command restores all blobs in a Storage account from 30 minutes ago, and wait for the restore complete.</span></span> <span data-ttu-id="d9db6-117">Mivel a visszaállítási blobok hosszú ideig is eltelhet, futtassa a backendben -As job paraméterrel, majd várja meg, amíg befejeződik a feladat, és mutassa az eredményt.</span><span class="sxs-lookup"><span data-stu-id="d9db6-117">Since restore blobs might take a long time, run it in the backend with -Asjob parameter, and then wait for the job complete and show the result.</span></span>

### <span data-ttu-id="d9db6-118">3. példa: Blobok visszaállítása bemeneti blobtartományok alapján közvetlenül, és várakozás a teljesre</span><span class="sxs-lookup"><span data-stu-id="d9db6-118">Example 3: Restores blobs by input blob ranges directly, and wait for complete</span></span>
```powershell
PS C:\> Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -WaitForComplete `
    -TimeToRestore (Get-Date).AddSeconds(-1) `
    -BlobRestoreRange @{StartRange="aaa/abc";EndRange="bbb/abc"},@{StartRange="bbb/acc";EndRange=""}
WARNING: Restore blob rang with Id 'd66d1d02-6e48-47ef-b516-0155dd8319c6' started. Restore blob ranges time to complete is dependent on the size of the restore.

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges   
------   ---------                            ------------- ------------------------     ---------------------   
Complete d66d1d02-6e48-47ef-b516-0155dd8319c6               2020-02-10T14:17:46.8189116Z ["aaa/abc" -> "bbb/abc",...]
```

<span data-ttu-id="d9db6-119">Ez a parancs 1 napja visszaállítja egy tárfiók blobját úgy, hogy 2 blobtartományt ad meg közvetlenül a Restore-AzStorageBlobRange parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="d9db6-119">This command restores blobs in a Storage account from 1 day ago, by input 2 blob ranges directly to the Restore-AzStorageBlobRange cmdlet.</span></span> <span data-ttu-id="d9db6-120">Ez a parancs a visszaállítás befejeződik.</span><span class="sxs-lookup"><span data-stu-id="d9db6-120">This command will wait for the restore complete.</span></span>

## <span data-ttu-id="d9db6-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9db6-121">PARAMETERS</span></span>

### <span data-ttu-id="d9db6-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9db6-122">-AsJob</span></span>
<span data-ttu-id="d9db6-123">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d9db6-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d9db6-124">-BlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="d9db6-124">-BlobRestoreRange</span></span>
<span data-ttu-id="d9db6-125">A visszaállítható blobtartomány.</span><span class="sxs-lookup"><span data-stu-id="d9db6-125">The blob range to Restore.</span></span>
<span data-ttu-id="d9db6-126">Ha nem adja meg ezt a paramétert, az összes blobot visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="d9db6-126">If not specify this parameter, will restore all blobs.</span></span>

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

### <span data-ttu-id="d9db6-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9db6-127">-DefaultProfile</span></span>
<span data-ttu-id="d9db6-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d9db6-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9db6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9db6-129">-ResourceGroupName</span></span>
<span data-ttu-id="d9db6-130">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d9db6-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="d9db6-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9db6-131">-ResourceId</span></span>
<span data-ttu-id="d9db6-132">Tárfiók erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d9db6-132">Storage Account Resource Id.</span></span>

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

### <span data-ttu-id="d9db6-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d9db6-133">-StorageAccount</span></span>
<span data-ttu-id="d9db6-134">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="d9db6-134">Storage account object</span></span>

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

### <span data-ttu-id="d9db6-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d9db6-135">-StorageAccountName</span></span>
<span data-ttu-id="d9db6-136">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="d9db6-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="d9db6-137">-TimeToRestore</span><span class="sxs-lookup"><span data-stu-id="d9db6-137">-TimeToRestore</span></span>
<span data-ttu-id="d9db6-138">A blob visszaállításának ideje.</span><span class="sxs-lookup"><span data-stu-id="d9db6-138">The Time to Restore Blob.</span></span>

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

### <span data-ttu-id="d9db6-139">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="d9db6-139">-WaitForComplete</span></span>
<span data-ttu-id="d9db6-140">Várakozás a visszaállítási feladat befejezésére</span><span class="sxs-lookup"><span data-stu-id="d9db6-140">Wait for Restore task complete</span></span>

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

### <span data-ttu-id="d9db6-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9db6-141">-Confirm</span></span>
<span data-ttu-id="d9db6-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d9db6-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9db6-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9db6-143">-WhatIf</span></span>
<span data-ttu-id="d9db6-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d9db6-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d9db6-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d9db6-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9db6-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9db6-146">CommonParameters</span></span>
<span data-ttu-id="d9db6-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9db6-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9db6-148">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9db6-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9db6-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d9db6-149">INPUTS</span></span>

### <span data-ttu-id="d9db6-150">System.String</span><span class="sxs-lookup"><span data-stu-id="d9db6-150">System.String</span></span>

### <span data-ttu-id="d9db6-151">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d9db6-151">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="d9db6-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9db6-152">OUTPUTS</span></span>

### <span data-ttu-id="d9db6-153">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="d9db6-153">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreStatus</span></span>

## <span data-ttu-id="d9db6-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d9db6-154">NOTES</span></span>

## <span data-ttu-id="d9db6-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d9db6-155">RELATED LINKS</span></span>
