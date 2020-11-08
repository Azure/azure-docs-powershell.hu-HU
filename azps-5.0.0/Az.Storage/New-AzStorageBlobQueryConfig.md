---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-azstorageblobqueryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
ms.openlocfilehash: ec1b3b7ab7cd0ddbbdb0b938149f03755563a742
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187178"
---
# <span data-ttu-id="dc18b-101">New-AzStorageBlobQueryConfig</span><span class="sxs-lookup"><span data-stu-id="dc18b-101">New-AzStorageBlobQueryConfig</span></span>

## <span data-ttu-id="dc18b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dc18b-102">SYNOPSIS</span></span>
<span data-ttu-id="dc18b-103">BLOB-lekérdezési konfigurációs objektumot hoz létre, amelyet a Get-AzStorageBlobQueryResult használhat.</span><span class="sxs-lookup"><span data-stu-id="dc18b-103">Creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="dc18b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dc18b-104">SYNTAX</span></span>

### <span data-ttu-id="dc18b-105">CSV (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dc18b-105">Csv (Default)</span></span>
```
New-AzStorageBlobQueryConfig [-AsCsv] [-RecordSeparator <String>] [-ColumnSeparator <String>]
 [-QuotationCharacter <Char>] [-EscapeCharacter <Char>] [-HasHeader] [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="dc18b-106">JSON</span><span class="sxs-lookup"><span data-stu-id="dc18b-106">Json</span></span>
```
New-AzStorageBlobQueryConfig [-AsJson] [-RecordSeparator <String>] [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="dc18b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="dc18b-107">DESCRIPTION</span></span>
<span data-ttu-id="dc18b-108">A **New-AzStorageBlobQueryConfig** parancsmag létrehoz egy blob lekérdezési konfigurációs objektumot, amelyet a Get-AzStorageBlobQueryResult-ban használhat.</span><span class="sxs-lookup"><span data-stu-id="dc18b-108">The **New-AzStorageBlobQueryConfig** cmdlet creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="dc18b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="dc18b-109">EXAMPLES</span></span>

### <span data-ttu-id="dc18b-110">1. példa: blob-lekérdezés beállítása és a blob lekérdezése</span><span class="sxs-lookup"><span data-stu-id="dc18b-110">Example 1: Create blob query configures , and query a blob</span></span>
```powershell
PS C:\> $inputconfig = New-AzStorageBlobQueryConfig -AsCsv -ColumnSeparator "," -QuotationCharacter """" -EscapeCharacter "\" -RecordSeparator "`n" -HasHeader

PS C:\> $outputconfig = New-AzStorageBlobQueryConfig -AsJson -RecordSeparator "`n" 

PS C:\> $queryString = "SELECT * FROM BlobStorage WHERE Name = 'a'"

PS C:\> $result = Get-AzStorageBlobQueryResult -Container $containerName -Blob $blobName -QueryString $queryString -ResultFile "c:\resultfile.json" -InputTextConfiguration $inputconfig -OutputTextConfiguration $outputconfig -Context $ctx

PS C:\> $result

BytesScanned FailureCount BlobQueryError
------------ ------------ --------------
         449            0
```

<span data-ttu-id="dc18b-111">Ebben a parancsban először létre kell hoznia a bemeneti konfigurációs objektumot CSV-fájlként és kimeneti konfigurációs objektumként JSON-ként, majd a 2 konfiguráció segítségével lekérdezheti a blobot.</span><span class="sxs-lookup"><span data-stu-id="dc18b-111">This command first create input configuration object as csv, and output configuration object as json, then use the 2 configurations to query blob.</span></span>

## <span data-ttu-id="dc18b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dc18b-112">PARAMETERS</span></span>

### <span data-ttu-id="dc18b-113">-AsCsv</span><span class="sxs-lookup"><span data-stu-id="dc18b-113">-AsCsv</span></span>
<span data-ttu-id="dc18b-114">Adja meg, hogy miként hozhat létre blob-lekérdezési konfigurációt a CSV-hez.</span><span class="sxs-lookup"><span data-stu-id="dc18b-114">Indicate to create a Blob Query Configuration for CSV.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Csv
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc18b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc18b-115">-AsJob</span></span>
<span data-ttu-id="dc18b-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="dc18b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dc18b-117">-AsJson</span><span class="sxs-lookup"><span data-stu-id="dc18b-117">-AsJson</span></span>
<span data-ttu-id="dc18b-118">Adja meg, hogy miként hozhat létre blob-lekérdezési konfigurációt a JSON-hoz.</span><span class="sxs-lookup"><span data-stu-id="dc18b-118">Indicate to create a Blob Query Configuration for Json.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Json
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc18b-119">-ColumnSeparator</span><span class="sxs-lookup"><span data-stu-id="dc18b-119">-ColumnSeparator</span></span>
<span data-ttu-id="dc18b-120">Nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="dc18b-120">Optional.</span></span>
<span data-ttu-id="dc18b-121">Az oszlopok elkülönítéséhez használt karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="dc18b-121">The string used to separate columns.</span></span>

```yaml
Type: System.String
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc18b-122">-EscapeCharacter</span><span class="sxs-lookup"><span data-stu-id="dc18b-122">-EscapeCharacter</span></span>
<span data-ttu-id="dc18b-123">Nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="dc18b-123">Optional.</span></span>
<span data-ttu-id="dc18b-124">A karakter Escape-karakterként használható.</span><span class="sxs-lookup"><span data-stu-id="dc18b-124">The char used as an escape character.</span></span>

```yaml
Type: System.Nullable`1[System.Char]
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc18b-125">-HasHeader</span><span class="sxs-lookup"><span data-stu-id="dc18b-125">-HasHeader</span></span>
<span data-ttu-id="dc18b-126">Nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="dc18b-126">Optional.</span></span>
<span data-ttu-id="dc18b-127">Annak jelzése, hogy az adatot fejlécekkel jelöli.</span><span class="sxs-lookup"><span data-stu-id="dc18b-127">Indicate it represent the data has headers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc18b-128">-QuotationCharacter</span><span class="sxs-lookup"><span data-stu-id="dc18b-128">-QuotationCharacter</span></span>
<span data-ttu-id="dc18b-129">Nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="dc18b-129">Optional.</span></span>
<span data-ttu-id="dc18b-130">Az adott mező idézéséhez használt karakter.</span><span class="sxs-lookup"><span data-stu-id="dc18b-130">The char used to quote a specific field.</span></span>

```yaml
Type: System.Char
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc18b-131">-RecordSeparator</span><span class="sxs-lookup"><span data-stu-id="dc18b-131">-RecordSeparator</span></span>
<span data-ttu-id="dc18b-132">Nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="dc18b-132">Optional.</span></span>
<span data-ttu-id="dc18b-133">A rekordok elkülönítéséhez használt karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="dc18b-133">The string used to separate records.</span></span>

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

### <span data-ttu-id="dc18b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc18b-134">CommonParameters</span></span>
<span data-ttu-id="dc18b-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dc18b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc18b-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc18b-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc18b-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc18b-137">INPUTS</span></span>

### <span data-ttu-id="dc18b-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="dc18b-138">None</span></span>

## <span data-ttu-id="dc18b-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc18b-139">OUTPUTS</span></span>

### <span data-ttu-id="dc18b-140">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. PSBlobQueryTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc18b-140">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration</span></span>

## <span data-ttu-id="dc18b-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dc18b-141">NOTES</span></span>

## <span data-ttu-id="dc18b-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dc18b-142">RELATED LINKS</span></span>
