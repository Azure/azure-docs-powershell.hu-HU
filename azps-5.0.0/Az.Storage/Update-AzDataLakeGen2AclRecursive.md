---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azdatalakegen2aclrecursive
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2AclRecursive.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2AclRecursive.md
ms.openlocfilehash: 80b1816dff686db7e84bf876fd74f9642389b42f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194170"
---
# <span data-ttu-id="b9203-101">Update-AzDataLakeGen2AclRecursive</span><span class="sxs-lookup"><span data-stu-id="b9203-101">Update-AzDataLakeGen2AclRecursive</span></span>

## <span data-ttu-id="b9203-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b9203-102">SYNOPSIS</span></span>
<span data-ttu-id="b9203-103">A megadott elérési úton rekurzív módon frissítse az ACL-t.</span><span class="sxs-lookup"><span data-stu-id="b9203-103">Update ACL recursively on the specified path.</span></span> 

## <span data-ttu-id="b9203-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b9203-104">SYNTAX</span></span>

```
Update-AzDataLakeGen2AclRecursive [-FileSystem] <String> [[-Path] <String>] [-ContinuationToken <String>]
 -Acl <PSPathAccessControlEntry[]> [-ContinueOnFailure] [-BatchSize <Int32>] [-MaxBatchCount <Int32>] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b9203-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b9203-105">DESCRIPTION</span></span>
<span data-ttu-id="b9203-106">Az **Update-AzDataLakeGen2AclRecursive** parancsmag a megadott elérési útban rekurzívan FRISSÍTI az ACL-t.</span><span class="sxs-lookup"><span data-stu-id="b9203-106">The **Update-AzDataLakeGen2AclRecursive** cmdlet updates ACL recursively on the specified path.</span></span> <span data-ttu-id="b9203-107">A beviteli ACL egyesíti az eredeti ACL-t: Ha az ACL-bejegyzés azonos AccessControlType/EntityId/DefaultScope létezik, akkor a frissítési engedély Máskülönben adjon hozzá új ACL-bejegyzést.</span><span class="sxs-lookup"><span data-stu-id="b9203-107">The input ACL will merge the the original ACL: If ACL entry with same AccessControlType/EntityId/DefaultScope exist, update permission; else add a new ACL entry.</span></span>

## <span data-ttu-id="b9203-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b9203-108">EXAMPLES</span></span>

### <span data-ttu-id="b9203-109">Példa 1: az ACL-t rekurzívan frissítheti a Directiry.</span><span class="sxs-lookup"><span data-stu-id="b9203-109">Example 1: Update ACL recursively on a root directiry of filesystem</span></span>
```
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\> Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Acl $acl -Context $ctx

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 7
TotalFilesSuccessfulCount       : 5
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="b9203-110">Ez a parancs először egy ACL-objektumot hoz létre, amelyben 3 ACL-bejegyzés található, majd rekurzívan frissíti az ACL-t egy fájlrendszer gyökérkönyvtárába.</span><span class="sxs-lookup"><span data-stu-id="b9203-110">This command first creates an ACL object with 3 acl entries, then updates ACL recursively on a root directory of a file system.</span></span>

### <span data-ttu-id="b9203-111">2. példa: az ACL-adatok rekurzív frissítése egy címtárban, és a hiba a ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="b9203-111">Example 2: Update ACL recursively on a directory, and resume from failure with ContinuationToken</span></span>
```
PS C:\> $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -Context $ctx

PS C:\> $result

FailedEntries                   : {dir1/dir2/file4}
TotalDirectoriesSuccessfulCount : 500
TotalFilesSuccessfulCount       : 2500
TotalFailureCount               : 1
ContinuationToken               : VBaHi5TfyO2ai1wYTRhIL2FjbGNibjA2c3RmATAxRDVEN0UzRENFQzZCRTAvYWRsc3Rlc3QyATAxRDY2M0ZCQTZBN0JGQTkvZGlyMC9kaXIxL2ZpbGUzFgAAAA==

PS C:\> $result.FailedEntries

Name            IsDirectory ErrorMessage                                                                   
----            ----------- ------------                                                                   
dir0/dir2/file4       False This request is not authorized to perform this operation using this permission.

# user need fix the failed item , then can resume with ContinuationToken

PS C:\> $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinuationToken $result.ContinuationToken -Context $ctx

PS C:\> $result

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 1000
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="b9203-112">Ez a parancs először frissíti az ACL-t egy címtárba, és sikertelen volt, majd a ContinuationToken után folytatja a telepítést a sikertelen fájl kijavítása után.</span><span class="sxs-lookup"><span data-stu-id="b9203-112">This command first updateds ACL recursively to a directory and failed, then resume with ContinuationToken after user fix the failed file.</span></span>

### <span data-ttu-id="b9203-113">3. példa: a rekurzív rekurzív Többdarabos frissítés frissítése</span><span class="sxs-lookup"><span data-stu-id="b9203-113">Example 3: Update ACL recursively chunk by chunk</span></span>
```
$ContinueOnFailure = $true # Set it to $false if want to terminate the operation quickly on encountering failures
$token = $null
$TotalDirectoriesSuccess = 0
$TotalFilesSuccess = 0
$totalFailure = 0
$FailedEntries = New-Object System.Collections.Generic.List[System.Object]
do
{
    
    if ($ContinueOnFailure)
    {
        $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -BatchSize 100 -MaxBatchCount 50 -ContinuationToken $token -Context $ctx -ContinueOnFailure
    }
    else
    {
        $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -BatchSize 100 -MaxBatchCount 50 -ContinuationToken $token -Context $ctx
    }

    # echo $result
    $TotalFilesSuccess += $result.TotalFilesSuccessfulCount
    $TotalDirectoriesSuccess += $result.TotalDirectoriesSuccessfulCount
    $totalFailure += $result.TotalFailureCount
    $FailedEntries += $result.FailedEntries
    $token = $result.ContinuationToken
}while (($token -ne $null) -and (($ContinueOnFailure) -or ($result.TotalFailureCount -eq 0)))
echo ""
echo "[Result Summary]"
echo "TotalDirectoriesSuccessfulCount: `t$($TotalDirectoriesSuccess)"
echo "TotalFilesSuccessfulCount: `t`t`t$($TotalFilesSuccess)"
echo "TotalFailureCount: `t`t`t`t`t$($totalFailure)"
echo "ContinuationToken: `t`t`t`t`t$($token)"
echo "FailedEntries:"$($FailedEntries | ft)
```

<span data-ttu-id="b9203-114">Ez a parancsfájl az ACL-rescursively a Többdarabos BatchSize \* MaxBatchCount szerint frissíti.</span><span class="sxs-lookup"><span data-stu-id="b9203-114">This script will update ACL rescursively on directory chunk by chunk, with chunk size as BatchSize \* MaxBatchCount.</span></span> <span data-ttu-id="b9203-115">A méret mérete 5000 ebben a parancsfájlban.</span><span class="sxs-lookup"><span data-stu-id="b9203-115">Chunk size is 5000 in this script.</span></span>

### <span data-ttu-id="b9203-116">4. példa: az ACL-t frissíti rekurzív módon egy címtár-és ContinueOnFailure, majd az egyes hibáktól kezdve</span><span class="sxs-lookup"><span data-stu-id="b9203-116">Example 4: Update ACL recursively on a directory and ContinueOnFailure, then resume from failures one by one</span></span>
```
PS C:\> $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinueOnFailure -Context $ctx

PS C:\> $result

FailedEntries                   : {dir0/dir1/file1, dir0/dir2/file4}
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 500
TotalFailureCount               : 2
ContinuationToken               : VBaHi5TfyO2ai1wYTRhIL2FjbGNibjA2c3RmATAxRDVEN0UzRENFQzZCRTAvYWRsc3Rlc3QyATAxRDY2M0ZCQTZBN0JGQTkvZGlyMC9kaXIxL2ZpbGUzFgAAAA==

PS C:\> $result.FailedEntries

Name            IsDirectory ErrorMessage                                                                   
----            ----------- ------------                                                                   
dir0/dir1/file1       False This request is not authorized to perform this operation using this permission.
dir0/dir2/file4       False This request is not authorized to perform this operation using this permission.

# user need fix the failed item , then can resume with ContinuationToken

PS C:\> foreach ($path in $result.FailedEntries.Name)
        {
            # user code to fix failed entry in $path
            
            #set ACL again
            Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path $path -Acl $acl -Context $ctx
        }
```

<span data-ttu-id="b9203-117">Ez a parancs először frissítette az ACL-t egy ContinueOnFailure-ra, és néhány elem sikertelen volt, majd a sikertelen elemek mindegyike egyenként folytatódik.</span><span class="sxs-lookup"><span data-stu-id="b9203-117">This command first updateds ACL recursively to a directory with ContinueOnFailure, and some items failed, then resume the failed items one by one.</span></span>

## <span data-ttu-id="b9203-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b9203-118">PARAMETERS</span></span>

### <span data-ttu-id="b9203-119">-ACL</span><span class="sxs-lookup"><span data-stu-id="b9203-119">-Acl</span></span>
<span data-ttu-id="b9203-120">A POSIX-alapú hozzáférés-vezérlési lista a fájl vagy a könyvtár rekurzív beállításához.</span><span class="sxs-lookup"><span data-stu-id="b9203-120">The POSIX access control list to set recursively for the file or directory.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9203-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9203-121">-AsJob</span></span>
<span data-ttu-id="b9203-122">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b9203-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b9203-123">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="b9203-123">-BatchSize</span></span>
<span data-ttu-id="b9203-124">Ha az adathalmaz mérete túllépi a köteg méretét, akkor a művelet több kérésre oszlik, így a folyamat nyomon követhető lesz.</span><span class="sxs-lookup"><span data-stu-id="b9203-124">If data set size exceeds batch size then operation will be split into multiple requests so that progress can be tracked.</span></span>
<span data-ttu-id="b9203-125">A köteg méretének 1 és 2000 között kell lennie.</span><span class="sxs-lookup"><span data-stu-id="b9203-125">Batch size should be between 1 and 2000.</span></span>
<span data-ttu-id="b9203-126">Az alapértelmezett érték a 2000.</span><span class="sxs-lookup"><span data-stu-id="b9203-126">Default is 2000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9203-127">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b9203-127">-Context</span></span>
<span data-ttu-id="b9203-128">Azure Storage Context objektum</span><span class="sxs-lookup"><span data-stu-id="b9203-128">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9203-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="b9203-129">-ContinuationToken</span></span>
<span data-ttu-id="b9203-130">Folytatólagos jogkivonat.</span><span class="sxs-lookup"><span data-stu-id="b9203-130">Continuation Token.</span></span>

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

### <span data-ttu-id="b9203-131">-ContinueOnFailure</span><span class="sxs-lookup"><span data-stu-id="b9203-131">-ContinueOnFailure</span></span>
<span data-ttu-id="b9203-132">Ezt a paramétert beállíthatja a hibák mellőzése érdekében, és folytathatja a proceeing a címtár más alszervezetein végzett művelettel.</span><span class="sxs-lookup"><span data-stu-id="b9203-132">Set this parameter to ignore failures and continue proceeing with the operation on other sub-entities of the directory.</span></span> <span data-ttu-id="b9203-133">Alapértelmezés szerint a művelet gyorsan leáll a hibák elhárításakor.</span><span class="sxs-lookup"><span data-stu-id="b9203-133">Default the operation will terminate quickly on encountering failures.</span></span>

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

### <span data-ttu-id="b9203-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9203-134">-DefaultProfile</span></span>
<span data-ttu-id="b9203-135">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b9203-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9203-136">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="b9203-136">-FileSystem</span></span>
<span data-ttu-id="b9203-137">FileSystem neve</span><span class="sxs-lookup"><span data-stu-id="b9203-137">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9203-138">-MaxBatchCount</span><span class="sxs-lookup"><span data-stu-id="b9203-138">-MaxBatchCount</span></span>
<span data-ttu-id="b9203-139">A hozzáférés-vezérlési művelet módosítására használható kötegek maximális száma.</span><span class="sxs-lookup"><span data-stu-id="b9203-139">Maximum number of batches that single change Access Control operation can execute.</span></span> <span data-ttu-id="b9203-140">Ha az adathalmaz mérete túllépi a MaxBatchCount szorzás BatchSize, a folytatási token visszaadásra kerül.</span><span class="sxs-lookup"><span data-stu-id="b9203-140">If data set size exceeds MaxBatchCount multiply BatchSize, continuation token will be return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9203-141">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="b9203-141">-Path</span></span>
<span data-ttu-id="b9203-142">A megadott fájlrendszerben az ACL rekurzív módosítására szolgáló elérési út.</span><span class="sxs-lookup"><span data-stu-id="b9203-142">The path in the specified FileSystem that to change Acl recursively.</span></span>
<span data-ttu-id="b9203-143">Lehet fájl vagy címtár.</span><span class="sxs-lookup"><span data-stu-id="b9203-143">Can be a file or directory.</span></span>
<span data-ttu-id="b9203-144">A "címtár/file.txt" vagy a "directory1/directory2/" formátumban.</span><span class="sxs-lookup"><span data-stu-id="b9203-144">In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="b9203-145">Ha kihagyja ezt a paramétert, az ACL-t a fájlrendszer gyökérkönyvtárába rekurzív módon változtathatja meg.</span><span class="sxs-lookup"><span data-stu-id="b9203-145">Skip set this parameter to change Acl recursively from root directory of the Filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9203-146">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b9203-146">-Confirm</span></span>
<span data-ttu-id="b9203-147">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b9203-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9203-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9203-148">-WhatIf</span></span>
<span data-ttu-id="b9203-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b9203-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9203-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b9203-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9203-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9203-151">CommonParameters</span></span>
<span data-ttu-id="b9203-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b9203-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9203-153">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9203-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9203-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9203-154">INPUTS</span></span>

### <span data-ttu-id="b9203-155">System. String</span><span class="sxs-lookup"><span data-stu-id="b9203-155">System.String</span></span>

### <span data-ttu-id="b9203-156">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b9203-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b9203-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9203-157">OUTPUTS</span></span>

### <span data-ttu-id="b9203-158">System. String</span><span class="sxs-lookup"><span data-stu-id="b9203-158">System.String</span></span>

## <span data-ttu-id="b9203-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b9203-159">NOTES</span></span>

## <span data-ttu-id="b9203-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9203-160">RELATED LINKS</span></span>
