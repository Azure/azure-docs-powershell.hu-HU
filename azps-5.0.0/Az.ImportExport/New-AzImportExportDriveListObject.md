---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/new-AzImportExportDriveListObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
ms.openlocfilehash: 54252b82ecb32d26cf44b3b6f745856b755d60d9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187370"
---
# <span data-ttu-id="c05ba-101">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="c05ba-101">New-AzImportExportDriveListObject</span></span>

## <span data-ttu-id="c05ba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c05ba-102">SYNOPSIS</span></span>
<span data-ttu-id="c05ba-103">Hozzon létre egy DriverList-objektumot a ImportExport-hoz.</span><span class="sxs-lookup"><span data-stu-id="c05ba-103">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="c05ba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c05ba-104">SYNTAX</span></span>

```
New-AzImportExportDriveListObject [-BitLockerKey <String>] [-BytesSucceeded <Int64>] [-CopyStatus <String>]
 [-DriveHeaderHash <String>] [-DriveId <String>] [-ErrorLogUri <String>] [-ManifestFile <String>]
 [-ManifestHash <String>] [-ManifestUri <String>] [-PercentComplete <Int32>] [-State <DriveState>]
 [-VerboseLogUri <String>] [<CommonParameters>]
```

## <span data-ttu-id="c05ba-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c05ba-105">DESCRIPTION</span></span>
<span data-ttu-id="c05ba-106">Hozzon létre egy DriverList-objektumot a ImportExport-hoz.</span><span class="sxs-lookup"><span data-stu-id="c05ba-106">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="c05ba-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c05ba-107">EXAMPLES</span></span>

### <span data-ttu-id="c05ba-108">Példa 1: új DriveList létrehozása a ImportExport feladatához</span><span class="sxs-lookup"><span data-stu-id="c05ba-108">Example 1: Create a new DriveList for ImportExport job</span></span>
```powershell
PS C:\> New-AzImportExportDriveListObject -DriveId "9CA995BA" -BitLockerKey "238810-662376-448998-450120-652806-203390-606320-483076" -ManifestFile "\\DriveManifest.xml" -ManifestHash "109B21108597EF36D5785F08303F3638"

BitLockerKey                                            BytesSucceeded CopyStatus DriveHeaderHash DriveId  ErrorLogUri ManifestFile        ManifestHash                     ManifestUri PercentComplete State VerboseLogUri  
------------                                            -------------- ---------- --------------- -------  ----------- ------------        ------------                     ----------- --------------- ----- ------- 
238810-662376-448998-450120-652806-203390-606320-483076 0                                         9CA995BA             \\DriveManifest.xml 109B21108597EF36D5785F08303F3638             0
```

<span data-ttu-id="c05ba-109">Ezekkel a parancsmagokkal új DriveList hozhat létre a ImportExport-hoz.</span><span class="sxs-lookup"><span data-stu-id="c05ba-109">These cmdlets create a new DriveList for ImportExport job.</span></span>

## <span data-ttu-id="c05ba-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c05ba-110">PARAMETERS</span></span>

### <span data-ttu-id="c05ba-111">-BitLockerKey</span><span class="sxs-lookup"><span data-stu-id="c05ba-111">-BitLockerKey</span></span>
<span data-ttu-id="c05ba-112">A meghajtó titkosításához használt BitLocker-kulcs.</span><span class="sxs-lookup"><span data-stu-id="c05ba-112">The BitLocker key used to encrypt the drive.</span></span>

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

### <span data-ttu-id="c05ba-113">-BytesSucceeded</span><span class="sxs-lookup"><span data-stu-id="c05ba-113">-BytesSucceeded</span></span>
<span data-ttu-id="c05ba-114">A meghajtóhoz sikeresen átvitt bájtok száma.</span><span class="sxs-lookup"><span data-stu-id="c05ba-114">Bytes successfully transferred for the drive.</span></span>

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

### <span data-ttu-id="c05ba-115">-CopyStatus</span><span class="sxs-lookup"><span data-stu-id="c05ba-115">-CopyStatus</span></span>
<span data-ttu-id="c05ba-116">Az adatátviteli folyamatra vonatkozó részletes állapot</span><span class="sxs-lookup"><span data-stu-id="c05ba-116">Detailed status about the data transfer process.</span></span>
<span data-ttu-id="c05ba-117">Ezt a mezőt addig nem adja vissza a válasz, amíg a meghajtó az átadó államban van.</span><span class="sxs-lookup"><span data-stu-id="c05ba-117">This field is not returned in the response until the drive is in the Transferring state.</span></span>

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

### <span data-ttu-id="c05ba-118">-DriveHeaderHash</span><span class="sxs-lookup"><span data-stu-id="c05ba-118">-DriveHeaderHash</span></span>
<span data-ttu-id="c05ba-119">A meghajtó fejlécének hash értéke.</span><span class="sxs-lookup"><span data-stu-id="c05ba-119">The drive header hash value.</span></span>

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

### <span data-ttu-id="c05ba-120">-DriveId</span><span class="sxs-lookup"><span data-stu-id="c05ba-120">-DriveId</span></span>
<span data-ttu-id="c05ba-121">A meghajtó hardveres sorozatszáma szóközök nélkül.</span><span class="sxs-lookup"><span data-stu-id="c05ba-121">The drive's hardware serial number, without spaces.</span></span>

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

### <span data-ttu-id="c05ba-122">-ErrorLogUri</span><span class="sxs-lookup"><span data-stu-id="c05ba-122">-ErrorLogUri</span></span>
<span data-ttu-id="c05ba-123">Az adatátviteli művelethez tartozó, a blobot tartalmazó URI-azonosító.</span><span class="sxs-lookup"><span data-stu-id="c05ba-123">A URI that points to the blob containing the error log for the data transfer operation.</span></span>

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

### <span data-ttu-id="c05ba-124">-ManifestFile</span><span class="sxs-lookup"><span data-stu-id="c05ba-124">-ManifestFile</span></span>
<span data-ttu-id="c05ba-125">A manifest-fájl relatív elérési útja a meghajtón.</span><span class="sxs-lookup"><span data-stu-id="c05ba-125">The relative path of the manifest file on the drive.</span></span>

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

### <span data-ttu-id="c05ba-126">-ManifestHash</span><span class="sxs-lookup"><span data-stu-id="c05ba-126">-ManifestHash</span></span>
<span data-ttu-id="c05ba-127">A manifest-fájl Base16 kódolt MD5 hash-je a meghajtón.</span><span class="sxs-lookup"><span data-stu-id="c05ba-127">The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>

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

### <span data-ttu-id="c05ba-128">-ManifestUri</span><span class="sxs-lookup"><span data-stu-id="c05ba-128">-ManifestUri</span></span>
<span data-ttu-id="c05ba-129">Egy URI, amely a Drive manifest-fájlt tartalmazó blobra mutat.</span><span class="sxs-lookup"><span data-stu-id="c05ba-129">A URI that points to the blob containing the drive manifest file.</span></span>

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

### <span data-ttu-id="c05ba-130">-KészültségiSzint paraméter értéke</span><span class="sxs-lookup"><span data-stu-id="c05ba-130">-PercentComplete</span></span>
<span data-ttu-id="c05ba-131">A meghajtóhoz befejezett százalékos készültségi érték</span><span class="sxs-lookup"><span data-stu-id="c05ba-131">Percentage completed for the drive.</span></span>

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

### <span data-ttu-id="c05ba-132">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="c05ba-132">-State</span></span>
<span data-ttu-id="c05ba-133">A meghajtó aktuális állapota.</span><span class="sxs-lookup"><span data-stu-id="c05ba-133">The drive's current state.</span></span>

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

### <span data-ttu-id="c05ba-134">-VerboseLogUri</span><span class="sxs-lookup"><span data-stu-id="c05ba-134">-VerboseLogUri</span></span>
<span data-ttu-id="c05ba-135">Egy URI, amely rámutat az adatátviteli művelet részletes naplóját tartalmazó blobra.</span><span class="sxs-lookup"><span data-stu-id="c05ba-135">A URI that points to the blob containing the verbose log for the data transfer operation.</span></span>

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

### <span data-ttu-id="c05ba-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c05ba-136">CommonParameters</span></span>
<span data-ttu-id="c05ba-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c05ba-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c05ba-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c05ba-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c05ba-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c05ba-139">INPUTS</span></span>

## <span data-ttu-id="c05ba-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c05ba-140">OUTPUTS</span></span>

### <span data-ttu-id="c05ba-141">Microsoft. Azure. PowerShell. parancsmagok. ImportExport. modellek. Api20161101. IDriveStatus</span><span class="sxs-lookup"><span data-stu-id="c05ba-141">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus</span></span>

## <span data-ttu-id="c05ba-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c05ba-142">NOTES</span></span>

<span data-ttu-id="c05ba-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c05ba-143">ALIASES</span></span>

## <span data-ttu-id="c05ba-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c05ba-144">RELATED LINKS</span></span>

