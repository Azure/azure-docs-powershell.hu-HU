---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-azstorageblobqueryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
ms.openlocfilehash: ec1b3b7ab7cd0ddbbdb0b938149f03755563a742
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349494"
---
# <span data-ttu-id="14ed1-101">New-AzStorageBlobQueryConfig</span><span class="sxs-lookup"><span data-stu-id="14ed1-101">New-AzStorageBlobQueryConfig</span></span>

## <span data-ttu-id="14ed1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14ed1-102">SYNOPSIS</span></span>
<span data-ttu-id="14ed1-103">Bloblekérdezés konfigurációs objektum létrehozása, amely használható a Get-AzStorageBlobQueryResult eszközben.</span><span class="sxs-lookup"><span data-stu-id="14ed1-103">Creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="14ed1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="14ed1-104">SYNTAX</span></span>

### <span data-ttu-id="14ed1-105">Csv (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="14ed1-105">Csv (Default)</span></span>
```
New-AzStorageBlobQueryConfig [-AsCsv] [-RecordSeparator <String>] [-ColumnSeparator <String>]
 [-QuotationCharacter <Char>] [-EscapeCharacter <Char>] [-HasHeader] [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="14ed1-106">Json</span><span class="sxs-lookup"><span data-stu-id="14ed1-106">Json</span></span>
```
New-AzStorageBlobQueryConfig [-AsJson] [-RecordSeparator <String>] [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="14ed1-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="14ed1-107">DESCRIPTION</span></span>
<span data-ttu-id="14ed1-108">A **New-AzStorageBlobQueryConfig** parancsmag létrehoz egy bloblekérdezés konfigurációs objektumot, amely használható a Get-AzStorageBlobQueryResult eszközben.</span><span class="sxs-lookup"><span data-stu-id="14ed1-108">The **New-AzStorageBlobQueryConfig** cmdlet creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="14ed1-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="14ed1-109">EXAMPLES</span></span>

### <span data-ttu-id="14ed1-110">1. példa: Bloblekérdezés konfigurálása és bloblekérdezés létrehozása</span><span class="sxs-lookup"><span data-stu-id="14ed1-110">Example 1: Create blob query configures , and query a blob</span></span>
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

<span data-ttu-id="14ed1-111">Ez a parancs először hozza létre a bemeneti konfigurációs objektumot CSV-ként, a kimeneti konfigurációs objektumot pedig jsonként, majd a 2 konfigurációt használva lekérdezési blobot.</span><span class="sxs-lookup"><span data-stu-id="14ed1-111">This command first create input configuration object as csv, and output configuration object as json, then use the 2 configurations to query blob.</span></span>

## <span data-ttu-id="14ed1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14ed1-112">PARAMETERS</span></span>

### <span data-ttu-id="14ed1-113">-AsCsv</span><span class="sxs-lookup"><span data-stu-id="14ed1-113">-AsCsv</span></span>
<span data-ttu-id="14ed1-114">Azt jelzi, hogy bloblekérdezés-konfigurációt hoz létre a CSV-hez.</span><span class="sxs-lookup"><span data-stu-id="14ed1-114">Indicate to create a Blob Query Configuration for CSV.</span></span>

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

### <span data-ttu-id="14ed1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14ed1-115">-AsJob</span></span>
<span data-ttu-id="14ed1-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="14ed1-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14ed1-117">-AsJson</span><span class="sxs-lookup"><span data-stu-id="14ed1-117">-AsJson</span></span>
<span data-ttu-id="14ed1-118">Azt jelzi, hogy a Jsonhoz bloblekérdezés-konfigurációt kell létrehoznia.</span><span class="sxs-lookup"><span data-stu-id="14ed1-118">Indicate to create a Blob Query Configuration for Json.</span></span>

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

### <span data-ttu-id="14ed1-119">-ColumnSeparator</span><span class="sxs-lookup"><span data-stu-id="14ed1-119">-ColumnSeparator</span></span>
<span data-ttu-id="14ed1-120">Nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="14ed1-120">Optional.</span></span>
<span data-ttu-id="14ed1-121">Az oszlopok elválasztása.</span><span class="sxs-lookup"><span data-stu-id="14ed1-121">The string used to separate columns.</span></span>

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

### <span data-ttu-id="14ed1-122">-EscapeCharacter</span><span class="sxs-lookup"><span data-stu-id="14ed1-122">-EscapeCharacter</span></span>
<span data-ttu-id="14ed1-123">Nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="14ed1-123">Optional.</span></span>
<span data-ttu-id="14ed1-124">Az escape-karakterként használt karakter.</span><span class="sxs-lookup"><span data-stu-id="14ed1-124">The char used as an escape character.</span></span>

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

### <span data-ttu-id="14ed1-125">-HasHeader</span><span class="sxs-lookup"><span data-stu-id="14ed1-125">-HasHeader</span></span>
<span data-ttu-id="14ed1-126">Nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="14ed1-126">Optional.</span></span>
<span data-ttu-id="14ed1-127">Azt jelzi, hogy az adatok fejlécet tartalmaznak.</span><span class="sxs-lookup"><span data-stu-id="14ed1-127">Indicate it represent the data has headers.</span></span>

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

### <span data-ttu-id="14ed1-128">-QuotationCharacter</span><span class="sxs-lookup"><span data-stu-id="14ed1-128">-QuotationCharacter</span></span>
<span data-ttu-id="14ed1-129">Nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="14ed1-129">Optional.</span></span>
<span data-ttu-id="14ed1-130">Az a karakter, amely egy adott mező idézi.</span><span class="sxs-lookup"><span data-stu-id="14ed1-130">The char used to quote a specific field.</span></span>

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

### <span data-ttu-id="14ed1-131">-RecordSeparator</span><span class="sxs-lookup"><span data-stu-id="14ed1-131">-RecordSeparator</span></span>
<span data-ttu-id="14ed1-132">Nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="14ed1-132">Optional.</span></span>
<span data-ttu-id="14ed1-133">A rekordok elválasztó karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="14ed1-133">The string used to separate records.</span></span>

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

### <span data-ttu-id="14ed1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14ed1-134">CommonParameters</span></span>
<span data-ttu-id="14ed1-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14ed1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14ed1-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14ed1-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14ed1-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="14ed1-137">INPUTS</span></span>

### <span data-ttu-id="14ed1-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="14ed1-138">None</span></span>

## <span data-ttu-id="14ed1-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="14ed1-139">OUTPUTS</span></span>

### <span data-ttu-id="14ed1-140">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="14ed1-140">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration</span></span>

## <span data-ttu-id="14ed1-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="14ed1-141">NOTES</span></span>

## <span data-ttu-id="14ed1-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="14ed1-142">RELATED LINKS</span></span>
