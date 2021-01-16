---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/new-AzImportExportDriveListObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
ms.openlocfilehash: 54252b82ecb32d26cf44b3b6f745856b755d60d9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364488"
---
# <span data-ttu-id="6ea26-101">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="6ea26-101">New-AzImportExportDriveListObject</span></span>

## <span data-ttu-id="6ea26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ea26-102">SYNOPSIS</span></span>
<span data-ttu-id="6ea26-103">Hozzon létre egy DriverList-objektumot az ImportExporthoz.</span><span class="sxs-lookup"><span data-stu-id="6ea26-103">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="6ea26-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6ea26-104">SYNTAX</span></span>

```
New-AzImportExportDriveListObject [-BitLockerKey <String>] [-BytesSucceeded <Int64>] [-CopyStatus <String>]
 [-DriveHeaderHash <String>] [-DriveId <String>] [-ErrorLogUri <String>] [-ManifestFile <String>]
 [-ManifestHash <String>] [-ManifestUri <String>] [-PercentComplete <Int32>] [-State <DriveState>]
 [-VerboseLogUri <String>] [<CommonParameters>]
```

## <span data-ttu-id="6ea26-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6ea26-105">DESCRIPTION</span></span>
<span data-ttu-id="6ea26-106">Hozzon létre egy DriverList-objektumot az ImportExporthoz.</span><span class="sxs-lookup"><span data-stu-id="6ea26-106">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="6ea26-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6ea26-107">EXAMPLES</span></span>

### <span data-ttu-id="6ea26-108">1. példa: Új DriveList létrehozása az ImportExport feladathoz</span><span class="sxs-lookup"><span data-stu-id="6ea26-108">Example 1: Create a new DriveList for ImportExport job</span></span>
```powershell
PS C:\> New-AzImportExportDriveListObject -DriveId "9CA995BA" -BitLockerKey "238810-662376-448998-450120-652806-203390-606320-483076" -ManifestFile "\\DriveManifest.xml" -ManifestHash "109B21108597EF36D5785F08303F3638"

BitLockerKey                                            BytesSucceeded CopyStatus DriveHeaderHash DriveId  ErrorLogUri ManifestFile        ManifestHash                     ManifestUri PercentComplete State VerboseLogUri  
------------                                            -------------- ---------- --------------- -------  ----------- ------------        ------------                     ----------- --------------- ----- ------- 
238810-662376-448998-450120-652806-203390-606320-483076 0                                         9CA995BA             \\DriveManifest.xml 109B21108597EF36D5785F08303F3638             0
```

<span data-ttu-id="6ea26-109">Ezek a parancsmagok új DriveList-et hoznak létre az ImportExport feladathoz.</span><span class="sxs-lookup"><span data-stu-id="6ea26-109">These cmdlets create a new DriveList for ImportExport job.</span></span>

## <span data-ttu-id="6ea26-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ea26-110">PARAMETERS</span></span>

### <span data-ttu-id="6ea26-111">-BitLockerKey</span><span class="sxs-lookup"><span data-stu-id="6ea26-111">-BitLockerKey</span></span>
<span data-ttu-id="6ea26-112">A meghajtó titkosításához használt BitLocker kulcs.</span><span class="sxs-lookup"><span data-stu-id="6ea26-112">The BitLocker key used to encrypt the drive.</span></span>

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

### <span data-ttu-id="6ea26-113">-BytesSucceed</span><span class="sxs-lookup"><span data-stu-id="6ea26-113">-BytesSucceeded</span></span>
<span data-ttu-id="6ea26-114">A meghajtóhoz bájtok átvitele sikerült.</span><span class="sxs-lookup"><span data-stu-id="6ea26-114">Bytes successfully transferred for the drive.</span></span>

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

### <span data-ttu-id="6ea26-115">-CopyStatus</span><span class="sxs-lookup"><span data-stu-id="6ea26-115">-CopyStatus</span></span>
<span data-ttu-id="6ea26-116">Az adatátviteli folyamat részletes állapota.</span><span class="sxs-lookup"><span data-stu-id="6ea26-116">Detailed status about the data transfer process.</span></span>
<span data-ttu-id="6ea26-117">Ez a mező mindaddig nem ad vissza a válaszban, amíg a meghajtó átvitt állapotba nem áll.</span><span class="sxs-lookup"><span data-stu-id="6ea26-117">This field is not returned in the response until the drive is in the Transferring state.</span></span>

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

### <span data-ttu-id="6ea26-118">-DriveHeaderHash</span><span class="sxs-lookup"><span data-stu-id="6ea26-118">-DriveHeaderHash</span></span>
<span data-ttu-id="6ea26-119">A meghajtófejléc kivonatának értéke.</span><span class="sxs-lookup"><span data-stu-id="6ea26-119">The drive header hash value.</span></span>

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

### <span data-ttu-id="6ea26-120">-DriveId</span><span class="sxs-lookup"><span data-stu-id="6ea26-120">-DriveId</span></span>
<span data-ttu-id="6ea26-121">A meghajtó hardveres sorozatszáma szóközök nélkül.</span><span class="sxs-lookup"><span data-stu-id="6ea26-121">The drive's hardware serial number, without spaces.</span></span>

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

### <span data-ttu-id="6ea26-122">-ErrorLogUri</span><span class="sxs-lookup"><span data-stu-id="6ea26-122">-ErrorLogUri</span></span>
<span data-ttu-id="6ea26-123">Egy URI, amely az adatátviteli művelet hibanaplóját tartalmazó blobra mutat.</span><span class="sxs-lookup"><span data-stu-id="6ea26-123">A URI that points to the blob containing the error log for the data transfer operation.</span></span>

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

### <span data-ttu-id="6ea26-124">-ManifestFile</span><span class="sxs-lookup"><span data-stu-id="6ea26-124">-ManifestFile</span></span>
<span data-ttu-id="6ea26-125">A jegyzékfájl relatív elérési útja a meghajtón.</span><span class="sxs-lookup"><span data-stu-id="6ea26-125">The relative path of the manifest file on the drive.</span></span>

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

### <span data-ttu-id="6ea26-126">-ManifestHash</span><span class="sxs-lookup"><span data-stu-id="6ea26-126">-ManifestHash</span></span>
<span data-ttu-id="6ea26-127">A meghajtón található jegyzékfájl Base16 kódolású MD5-kivonata.</span><span class="sxs-lookup"><span data-stu-id="6ea26-127">The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>

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

### <span data-ttu-id="6ea26-128">-ManifestUri</span><span class="sxs-lookup"><span data-stu-id="6ea26-128">-ManifestUri</span></span>
<span data-ttu-id="6ea26-129">Egy URI, amely a meghajtó jegyzékfájlját tartalmazó blobra mutat.</span><span class="sxs-lookup"><span data-stu-id="6ea26-129">A URI that points to the blob containing the drive manifest file.</span></span>

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

### <span data-ttu-id="6ea26-130">-PercentComplete</span><span class="sxs-lookup"><span data-stu-id="6ea26-130">-PercentComplete</span></span>
<span data-ttu-id="6ea26-131">A meghajtóra vonatkozó százalékos érték.</span><span class="sxs-lookup"><span data-stu-id="6ea26-131">Percentage completed for the drive.</span></span>

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

### <span data-ttu-id="6ea26-132">-State</span><span class="sxs-lookup"><span data-stu-id="6ea26-132">-State</span></span>
<span data-ttu-id="6ea26-133">A meghajtó aktuális állapota.</span><span class="sxs-lookup"><span data-stu-id="6ea26-133">The drive's current state.</span></span>

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

### <span data-ttu-id="6ea26-134">-VerboseLogUri</span><span class="sxs-lookup"><span data-stu-id="6ea26-134">-VerboseLogUri</span></span>
<span data-ttu-id="6ea26-135">Egy URI, amely az adatátviteli művelet részletes naplóját tartalmazó blobra mutat.</span><span class="sxs-lookup"><span data-stu-id="6ea26-135">A URI that points to the blob containing the verbose log for the data transfer operation.</span></span>

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

### <span data-ttu-id="6ea26-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ea26-136">CommonParameters</span></span>
<span data-ttu-id="6ea26-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ea26-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ea26-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ea26-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ea26-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6ea26-139">INPUTS</span></span>

## <span data-ttu-id="6ea26-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ea26-140">OUTPUTS</span></span>

### <span data-ttu-id="6ea26-141">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus</span><span class="sxs-lookup"><span data-stu-id="6ea26-141">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus</span></span>

## <span data-ttu-id="6ea26-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6ea26-142">NOTES</span></span>

<span data-ttu-id="6ea26-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6ea26-143">ALIASES</span></span>

## <span data-ttu-id="6ea26-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6ea26-144">RELATED LINKS</span></span>

