---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/new-AzImportExportDriveListObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
ms.openlocfilehash: 4b3907e71dd8d457b1ab38ecd5cdc82b38d7b772
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928026"
---
# <span data-ttu-id="a3fff-101">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="a3fff-101">New-AzImportExportDriveListObject</span></span>

## <span data-ttu-id="a3fff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3fff-102">SYNOPSIS</span></span>
<span data-ttu-id="a3fff-103">Hozzon létre egy DriverList-objektumot az ImportExporthoz.</span><span class="sxs-lookup"><span data-stu-id="a3fff-103">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="a3fff-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a3fff-104">SYNTAX</span></span>

```
New-AzImportExportDriveListObject [-BitLockerKey <String>] [-BytesSucceeded <Int64>] [-CopyStatus <String>]
 [-DriveHeaderHash <String>] [-DriveId <String>] [-ErrorLogUri <String>] [-ManifestFile <String>]
 [-ManifestHash <String>] [-ManifestUri <String>] [-PercentComplete <Int32>] [-State <DriveState>]
 [-VerboseLogUri <String>] [<CommonParameters>]
```

## <span data-ttu-id="a3fff-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a3fff-105">DESCRIPTION</span></span>
<span data-ttu-id="a3fff-106">Hozzon létre egy DriverList-objektumot az ImportExporthoz.</span><span class="sxs-lookup"><span data-stu-id="a3fff-106">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="a3fff-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a3fff-107">EXAMPLES</span></span>

### <span data-ttu-id="a3fff-108">1. példa: Új DriveList létrehozása az ImportExport feladathoz</span><span class="sxs-lookup"><span data-stu-id="a3fff-108">Example 1: Create a new DriveList for ImportExport job</span></span>
```powershell
PS C:\> New-AzImportExportDriveListObject -DriveId "9CA995BA" -BitLockerKey "238810-662376-448998-450120-652806-203390-606320-483076" -ManifestFile "\\DriveManifest.xml" -ManifestHash "109B21108597EF36D5785F08303F3638"

BitLockerKey                                            BytesSucceeded CopyStatus DriveHeaderHash DriveId  ErrorLogUri ManifestFile        ManifestHash                     ManifestUri PercentComplete State VerboseLogUri  
------------                                            -------------- ---------- --------------- -------  ----------- ------------        ------------                     ----------- --------------- ----- ------- 
238810-662376-448998-450120-652806-203390-606320-483076 0                                         9CA995BA             \\DriveManifest.xml 109B21108597EF36D5785F08303F3638             0
```

<span data-ttu-id="a3fff-109">Ezek a parancsmagok új DriveList-et hoznak létre az ImportExport feladathoz.</span><span class="sxs-lookup"><span data-stu-id="a3fff-109">These cmdlets create a new DriveList for ImportExport job.</span></span>

## <span data-ttu-id="a3fff-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3fff-110">PARAMETERS</span></span>

### <span data-ttu-id="a3fff-111">-BitLockerKey</span><span class="sxs-lookup"><span data-stu-id="a3fff-111">-BitLockerKey</span></span>
<span data-ttu-id="a3fff-112">A meghajtó titkosításához használt BitLocker kulcs.</span><span class="sxs-lookup"><span data-stu-id="a3fff-112">The BitLocker key used to encrypt the drive.</span></span>

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

### <span data-ttu-id="a3fff-113">-BytesSucceed</span><span class="sxs-lookup"><span data-stu-id="a3fff-113">-BytesSucceeded</span></span>
<span data-ttu-id="a3fff-114">A meghajtóhoz bájtok átvitele sikerült.</span><span class="sxs-lookup"><span data-stu-id="a3fff-114">Bytes successfully transferred for the drive.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3fff-115">-CopyStatus</span><span class="sxs-lookup"><span data-stu-id="a3fff-115">-CopyStatus</span></span>
<span data-ttu-id="a3fff-116">Az adatátviteli folyamat részletes állapota.</span><span class="sxs-lookup"><span data-stu-id="a3fff-116">Detailed status about the data transfer process.</span></span>
<span data-ttu-id="a3fff-117">Ez a mező mindaddig nem ad vissza a válaszban, amíg a meghajtó átvitt állapotba nem áll.</span><span class="sxs-lookup"><span data-stu-id="a3fff-117">This field is not returned in the response until the drive is in the Transferring state.</span></span>

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

### <span data-ttu-id="a3fff-118">-DriveHeaderHash</span><span class="sxs-lookup"><span data-stu-id="a3fff-118">-DriveHeaderHash</span></span>
<span data-ttu-id="a3fff-119">A meghajtófejléc kivonatának értéke.</span><span class="sxs-lookup"><span data-stu-id="a3fff-119">The drive header hash value.</span></span>

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

### <span data-ttu-id="a3fff-120">-DriveId</span><span class="sxs-lookup"><span data-stu-id="a3fff-120">-DriveId</span></span>
<span data-ttu-id="a3fff-121">A meghajtó hardveres sorozatszáma szóközök nélkül.</span><span class="sxs-lookup"><span data-stu-id="a3fff-121">The drive's hardware serial number, without spaces.</span></span>

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

### <span data-ttu-id="a3fff-122">-ErrorLogUri</span><span class="sxs-lookup"><span data-stu-id="a3fff-122">-ErrorLogUri</span></span>
<span data-ttu-id="a3fff-123">Egy URI, amely az adatátviteli művelet hibanaplóját tartalmazó blobra mutat.</span><span class="sxs-lookup"><span data-stu-id="a3fff-123">A URI that points to the blob containing the error log for the data transfer operation.</span></span>

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

### <span data-ttu-id="a3fff-124">-ManifestFile</span><span class="sxs-lookup"><span data-stu-id="a3fff-124">-ManifestFile</span></span>
<span data-ttu-id="a3fff-125">A jegyzékfájl relatív elérési útja a meghajtón.</span><span class="sxs-lookup"><span data-stu-id="a3fff-125">The relative path of the manifest file on the drive.</span></span>

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

### <span data-ttu-id="a3fff-126">-ManifestHash</span><span class="sxs-lookup"><span data-stu-id="a3fff-126">-ManifestHash</span></span>
<span data-ttu-id="a3fff-127">A meghajtón található jegyzékfájl Base16 kódolású MD5-kivonata.</span><span class="sxs-lookup"><span data-stu-id="a3fff-127">The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>

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

### <span data-ttu-id="a3fff-128">-ManifestUri</span><span class="sxs-lookup"><span data-stu-id="a3fff-128">-ManifestUri</span></span>
<span data-ttu-id="a3fff-129">Egy URI, amely a meghajtó jegyzékfájlját tartalmazó blobra mutat.</span><span class="sxs-lookup"><span data-stu-id="a3fff-129">A URI that points to the blob containing the drive manifest file.</span></span>

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

### <span data-ttu-id="a3fff-130">-PercentComplete</span><span class="sxs-lookup"><span data-stu-id="a3fff-130">-PercentComplete</span></span>
<span data-ttu-id="a3fff-131">A meghajtóra vonatkozó százalékos érték.</span><span class="sxs-lookup"><span data-stu-id="a3fff-131">Percentage completed for the drive.</span></span>

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

### <span data-ttu-id="a3fff-132">-State</span><span class="sxs-lookup"><span data-stu-id="a3fff-132">-State</span></span>
<span data-ttu-id="a3fff-133">A meghajtó aktuális állapota.</span><span class="sxs-lookup"><span data-stu-id="a3fff-133">The drive's current state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Support.DriveState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3fff-134">-VerboseLogUri</span><span class="sxs-lookup"><span data-stu-id="a3fff-134">-VerboseLogUri</span></span>
<span data-ttu-id="a3fff-135">Egy URI, amely az adatátviteli művelet részletes naplóját tartalmazó blobra mutat.</span><span class="sxs-lookup"><span data-stu-id="a3fff-135">A URI that points to the blob containing the verbose log for the data transfer operation.</span></span>

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

### <span data-ttu-id="a3fff-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3fff-136">CommonParameters</span></span>
<span data-ttu-id="a3fff-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3fff-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3fff-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3fff-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3fff-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a3fff-139">INPUTS</span></span>

## <span data-ttu-id="a3fff-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3fff-140">OUTPUTS</span></span>

### <span data-ttu-id="a3fff-141">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus</span><span class="sxs-lookup"><span data-stu-id="a3fff-141">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus</span></span>

## <span data-ttu-id="a3fff-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a3fff-142">NOTES</span></span>

<span data-ttu-id="a3fff-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a3fff-143">ALIASES</span></span>

## <span data-ttu-id="a3fff-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a3fff-144">RELATED LINKS</span></span>

