---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azdatalakegen2aclrecursive
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2AclRecursive.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2AclRecursive.md
ms.openlocfilehash: cb2c409ae2bbe7734c433de74ef4a21c368221e1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479402"
---
# <span data-ttu-id="21843-101">Remove-AzDataLakeGen2AclRecursive</span><span class="sxs-lookup"><span data-stu-id="21843-101">Remove-AzDataLakeGen2AclRecursive</span></span>

## <span data-ttu-id="21843-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21843-102">SYNOPSIS</span></span>
<span data-ttu-id="21843-103">Távolítsa el az ACL-t rekurzívan a megadott útvonalon.</span><span class="sxs-lookup"><span data-stu-id="21843-103">Remove ACL recursively on the specified path.</span></span> 

## <span data-ttu-id="21843-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="21843-104">SYNTAX</span></span>

```
Remove-AzDataLakeGen2AclRecursive [-FileSystem] <String> [[-Path] <String>] [-ContinuationToken <String>]
 -Acl <PSPathAccessControlEntry[]> [-ContinueOnFailure] [-BatchSize <Int32>] [-MaxBatchCount <Int32>] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="21843-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="21843-105">DESCRIPTION</span></span>
<span data-ttu-id="21843-106">A **Remove-AzDataLakeGen2AclRecursive** parancsmag eltávolítja az ACL-rekurzív adatokat a megadott útvonalon.</span><span class="sxs-lookup"><span data-stu-id="21843-106">The **Remove-AzDataLakeGen2AclRecursive** cmdlet removes ACL recursively on the specified path.</span></span> <span data-ttu-id="21843-107">Az eredeti ACL-bejegyzések, amelyek azonos AccessControlType, DefaultScope és EntityId típusú bemeneti ACL-bejegyzésekkel (akár eltérő engedélyekkel is) el vannak távolítva.</span><span class="sxs-lookup"><span data-stu-id="21843-107">The ACL entries in original ACL, which has same AccessControlType, DefaultScope and EntityId with input ACL entries (even with different permission) wil lbe removed.</span></span>

## <span data-ttu-id="21843-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="21843-108">EXAMPLES</span></span>

### <span data-ttu-id="21843-109">1. példa: Az ACL rekurzív eltávolítása a fájlrendszer gyökér directiry-ján</span><span class="sxs-lookup"><span data-stu-id="21843-109">Example 1: Remove ACL recursively on a root directiry of filesystem</span></span>
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission r-x -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission r-x -InputObject $acl
PS C:\> Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Acl $acl -Context $ctx
WARNING: To find the ACL Entry to remove, will only compare AccessControlType, DefaultScope and EntityId, will omit Permission.

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 7
TotalFilesSuccessfulCount       : 5
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="21843-110">Ez a parancs először létrehoz egy 2 acl bejegyzéssel egy ACL-objektumot, majd a fájlrendszer gyökérkönyvtárában eltávolítja az ACL-t rekurzív módon.</span><span class="sxs-lookup"><span data-stu-id="21843-110">This command first creates an ACL object with 2 acl entries, then removes ACL recursively on a root directory of a file system.</span></span>

### <span data-ttu-id="21843-111">2. példa: Címtár ACL-rekurzív eltávolítása</span><span class="sxs-lookup"><span data-stu-id="21843-111">Example 2: Remove ACL recursively on a directory</span></span>
```
PS C:\> $result = Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -Context $ctx
WARNING: To find the ACL Entry to remove, will only compare AccessControlType, DefaultScope and EntityId, will omit Permission.

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

PS C:\> $result = Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinuationToken $result.ContinuationToken -Context $ctx
WARNING: To find the ACL Entry to remove, will only compare AccessControlType, DefaultScope and EntityId, will omit Permission.

PS C:\> $result

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 1000
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="21843-112">Ez a parancs először eltávolítja az ACL-t rekurzívan egy címtárból, és nem sikerült, majd a sikertelen fájl kijavítása után folytatja a folytatást a ContinuationToken paranccsal.</span><span class="sxs-lookup"><span data-stu-id="21843-112">This command first removes ACL recursively on a directory and failed, then resume with ContinuationToken after user fix the failed file.</span></span>

### <span data-ttu-id="21843-113">3. példa: Acl rekurzív adattömb eltávolítása egy adattömbből</span><span class="sxs-lookup"><span data-stu-id="21843-113">Example 3: Remove ACL recursively chunk by chunk</span></span>
```
$token = $null
$TotalDirectoriesSuccess = 0
$TotalFilesSuccess = 0
$totalFailure = 0
$FailedEntries = New-Object System.Collections.Generic.List[System.Object]
do
{
    $result = Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -BatchSize 1000 -MaxBatchCount 50 -ContinuationToken $token -Context $ctx

    # echo $result
    $TotalFilesSuccess += $result.TotalFilesSuccessfulCount
    $TotalDirectoriesSuccess += $result.TotalDirectoriesSuccessfulCount
    $totalFailure += $result.TotalFailureCount
    $FailedEntries += $result.FailedEntries
    $token = $result.ContinuationToken
}while (($token -ne $null) -and ($result.TotalFailureCount -eq 0))
echo ""
echo "[Result Summary]"
echo "TotalDirectoriesSuccessfulCount: `t$($TotalDirectoriesSuccess)"
echo "TotalFilesSuccessfulCount: `t`t`t$($TotalFilesSuccess)"
echo "TotalFailureCount: `t`t`t`t`t$($totalFailure)"
echo "ContinuationToken: `t`t`t`t`t$($token)"
echo "FailedEntries:"$($FailedEntries | ft)
```

<span data-ttu-id="21843-114">Ez a parancsprogram a címtár-adattömbök ACL-rescursively-ét eltávolítja, és a batchSize \* MaxBatchCount fájlmérettel együtt a címtárban reskurzívan eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="21843-114">This script will remove ACL rescursively on directory chunk by chunk, with chunk size as BatchSize \* MaxBatchCount.</span></span> <span data-ttu-id="21843-115">A parancsprogramban 50000 darabos adattömb van.</span><span class="sxs-lookup"><span data-stu-id="21843-115">Chunk size is 50000 in this script.</span></span>

### <span data-ttu-id="21843-116">4. példa: Az ACL-rekurzív eltávolítása egy címtárban és a ContinueOnFailure szolgáltatásban, majd a hibákból való egyesének újraindítása</span><span class="sxs-lookup"><span data-stu-id="21843-116">Example 4: Remove ACL recursively on a directory and ContinueOnFailure, then resume from failures one by one</span></span>
```
PS C:\> $result = Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinueOnFailure -Context $ctx

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
            Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path $path -Acl $acl -Context $ctx
        }
```

<span data-ttu-id="21843-117">Ez a parancs először eltávolítja az ACL-t rekurzív módon a ContinueOnFailure címtárból, és egyes elemek nem sikerültek, majd egyes esetekben folytassa a sikertelen elemeket.</span><span class="sxs-lookup"><span data-stu-id="21843-117">This command first removes ACL recursively to a directory with ContinueOnFailure, and some items failed, then resume the failed items one by one.</span></span>

## <span data-ttu-id="21843-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21843-118">PARAMETERS</span></span>

### <span data-ttu-id="21843-119">-Acl</span><span class="sxs-lookup"><span data-stu-id="21843-119">-Acl</span></span>
<span data-ttu-id="21843-120">A POSIX hozzáférés-vezérlési listája a fájl vagy a címtár rekurzív beállításához.</span><span class="sxs-lookup"><span data-stu-id="21843-120">The POSIX access control list to set recursively for the file or directory.</span></span>

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

### <span data-ttu-id="21843-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21843-121">-AsJob</span></span>
<span data-ttu-id="21843-122">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="21843-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="21843-123">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="21843-123">-BatchSize</span></span>
<span data-ttu-id="21843-124">Ha az adatkészlet mérete meghaladja a köteg méretét, a művelet több kérésre lesz felosztva, hogy nyomon követhető legyen az előrehaladás.</span><span class="sxs-lookup"><span data-stu-id="21843-124">If data set size exceeds batch size then operation will be split into multiple requests so that progress can be tracked.</span></span>
<span data-ttu-id="21843-125">A kötegek mérete 1 és 2000 között lehet.</span><span class="sxs-lookup"><span data-stu-id="21843-125">Batch size should be between 1 and 2000.</span></span>
<span data-ttu-id="21843-126">Az alapértelmezett érték 2000.</span><span class="sxs-lookup"><span data-stu-id="21843-126">Default is 2000.</span></span>

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

### <span data-ttu-id="21843-127">-Környezet</span><span class="sxs-lookup"><span data-stu-id="21843-127">-Context</span></span>
<span data-ttu-id="21843-128">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="21843-128">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="21843-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="21843-129">-ContinuationToken</span></span>
<span data-ttu-id="21843-130">Folytatási jogkivonat.</span><span class="sxs-lookup"><span data-stu-id="21843-130">Continuation Token.</span></span>

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

### <span data-ttu-id="21843-131">-ContinueOnFailure</span><span class="sxs-lookup"><span data-stu-id="21843-131">-ContinueOnFailure</span></span>
<span data-ttu-id="21843-132">A paraméter beállításával figyelmen kívül hagyhatja a hibákat, és folytathatja a műveletet a címtár más al entitásainál.</span><span class="sxs-lookup"><span data-stu-id="21843-132">Set this parameter to ignore failures and continue proceeing with the operation on other sub-entities of the directory.</span></span> <span data-ttu-id="21843-133">Alapértelmezés szerint a művelet gyorsan megszűnik hibák esetén.</span><span class="sxs-lookup"><span data-stu-id="21843-133">Default the operation will terminate quickly on encountering failures.</span></span>

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

### <span data-ttu-id="21843-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21843-134">-DefaultProfile</span></span>
<span data-ttu-id="21843-135">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="21843-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21843-136">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="21843-136">-FileSystem</span></span>
<span data-ttu-id="21843-137">FileSystem name</span><span class="sxs-lookup"><span data-stu-id="21843-137">FileSystem name</span></span>

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

### <span data-ttu-id="21843-138">-MaxBatchCount</span><span class="sxs-lookup"><span data-stu-id="21843-138">-MaxBatchCount</span></span>
<span data-ttu-id="21843-139">Azon kötegek maximális száma, amelyek végrehajthatók egy módosításon áteső Hozzáférés-vezérlési művelettel.</span><span class="sxs-lookup"><span data-stu-id="21843-139">Maximum number of batches that single change Access Control operation can execute.</span></span> <span data-ttu-id="21843-140">Ha az adatkészlet mérete meghaladja a MaxBatchCount batchSize szorzását, a folytatási jogkivonatot adja vissza a rendszer.</span><span class="sxs-lookup"><span data-stu-id="21843-140">If data set size exceeds MaxBatchCount multiply BatchSize, continuation token will be return.</span></span>

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

### <span data-ttu-id="21843-141">-Path</span><span class="sxs-lookup"><span data-stu-id="21843-141">-Path</span></span>
<span data-ttu-id="21843-142">Az Acl rekurzív módosítására használt elérési út a megadott FileSystemben.</span><span class="sxs-lookup"><span data-stu-id="21843-142">The path in the specified FileSystem that to change Acl recursively.</span></span>
<span data-ttu-id="21843-143">Fájl vagy címtár lehet.</span><span class="sxs-lookup"><span data-stu-id="21843-143">Can be a file or directory.</span></span>
<span data-ttu-id="21843-144">"directory/file.txt" vagy "directory1/directory2/" formátumban.</span><span class="sxs-lookup"><span data-stu-id="21843-144">In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="21843-145">Skip set this parameter to change Acl recursively from root directory of the Filesystem.</span><span class="sxs-lookup"><span data-stu-id="21843-145">Skip set this parameter to change Acl recursively from root directory of the Filesystem.</span></span>

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

### <span data-ttu-id="21843-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21843-146">-Confirm</span></span>
<span data-ttu-id="21843-147">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="21843-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21843-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21843-148">-WhatIf</span></span>
<span data-ttu-id="21843-149">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="21843-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21843-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="21843-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21843-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21843-151">CommonParameters</span></span>
<span data-ttu-id="21843-152">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21843-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21843-153">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21843-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21843-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="21843-154">INPUTS</span></span>

### <span data-ttu-id="21843-155">System.String</span><span class="sxs-lookup"><span data-stu-id="21843-155">System.String</span></span>

### <span data-ttu-id="21843-156">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="21843-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="21843-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="21843-157">OUTPUTS</span></span>

### <span data-ttu-id="21843-158">System.String</span><span class="sxs-lookup"><span data-stu-id="21843-158">System.String</span></span>

## <span data-ttu-id="21843-159">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="21843-159">NOTES</span></span>

## <span data-ttu-id="21843-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="21843-160">RELATED LINKS</span></span>
