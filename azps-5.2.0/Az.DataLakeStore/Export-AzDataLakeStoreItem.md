---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/export-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
ms.openlocfilehash: e0bac2f22249b27442c75da7879f6a6cf85e7da7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371431"
---
# <span data-ttu-id="bd63b-101">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bd63b-101">Export-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="bd63b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd63b-102">SYNOPSIS</span></span>
<span data-ttu-id="bd63b-103">Letölt egy fájlt a Data Lake Store-ból.</span><span class="sxs-lookup"><span data-stu-id="bd63b-103">Downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="bd63b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bd63b-104">SYNTAX</span></span>

### <span data-ttu-id="bd63b-105">NoDiagnosticLogging (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bd63b-105">NoDiagnosticLogging (Default)</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd63b-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="bd63b-106">IncludeDiagnosticLogging</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bd63b-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bd63b-107">DESCRIPTION</span></span>
<span data-ttu-id="bd63b-108">Az **Export-AzDataLakeStoreItem** parancsmag letölt egy fájlt a Data Lake Store-ból.</span><span class="sxs-lookup"><span data-stu-id="bd63b-108">The **Export-AzDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="bd63b-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bd63b-109">EXAMPLES</span></span>

### <span data-ttu-id="bd63b-110">1. példa: Elem letöltése a Data Lake Store-ból</span><span class="sxs-lookup"><span data-stu-id="bd63b-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv" -Concurrency 4
```

<span data-ttu-id="bd63b-111">Ez a parancs letölti TestSource.csv fájlt a Data Lake Store-ból, C:\Test.csv 4-es egyidejűség mellett letölti a fájlt.</span><span class="sxs-lookup"><span data-stu-id="bd63b-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="bd63b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd63b-112">PARAMETERS</span></span>

### <span data-ttu-id="bd63b-113">-Account</span><span class="sxs-lookup"><span data-stu-id="bd63b-113">-Account</span></span>
<span data-ttu-id="bd63b-114">A Data Lake Store-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bd63b-114">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd63b-115">-Egyidejűség</span><span class="sxs-lookup"><span data-stu-id="bd63b-115">-Concurrency</span></span>
<span data-ttu-id="bd63b-116">A párhuzamos letöltéshez szükséges fájlok vagy adattömbök számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="bd63b-116">Indicates the number of files or chunks to download in parallel.</span></span> <span data-ttu-id="bd63b-117">Az alapértelmezett érték a rendszer specifikációi alapján számítható legjobb munkamennyiségnek.</span><span class="sxs-lookup"><span data-stu-id="bd63b-117">Default will be computed as a best effort based on system specifications.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd63b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd63b-118">-DefaultProfile</span></span>
<span data-ttu-id="bd63b-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bd63b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd63b-120">-Destination</span><span class="sxs-lookup"><span data-stu-id="bd63b-120">-Destination</span></span>
<span data-ttu-id="bd63b-121">Megadja a fájl letöltésének helyi elérési útját.</span><span class="sxs-lookup"><span data-stu-id="bd63b-121">Specifies the local file path to which to download the file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd63b-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="bd63b-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="bd63b-123">Ha szükséges, azt a diagnosztikai naplószintet adja meg, amely a fájl vagy mappa importálása során az események rögzítésére használható.</span><span class="sxs-lookup"><span data-stu-id="bd63b-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="bd63b-124">Az alapértelmezett érték a Hiba.</span><span class="sxs-lookup"><span data-stu-id="bd63b-124">Default is Error.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel
Parameter Sets: IncludeDiagnosticLogging
Aliases:
Accepted values: Debug, Information, Error, None

Required: False
Position: Named
Default value: Error
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd63b-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="bd63b-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="bd63b-126">Megadja a diagnosztikai napló elérési útját, amelybe a fájl vagy mappa importálása közbeni eseményeket rögzíteni kell.</span><span class="sxs-lookup"><span data-stu-id="bd63b-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

```yaml
Type: System.String
Parameter Sets: IncludeDiagnosticLogging
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd63b-127">-Force</span><span class="sxs-lookup"><span data-stu-id="bd63b-127">-Force</span></span>
<span data-ttu-id="bd63b-128">Azt jelzi, hogy ez a művelet felülírhatja a célfájlt, ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="bd63b-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd63b-129">-Path</span><span class="sxs-lookup"><span data-stu-id="bd63b-129">-Path</span></span>
<span data-ttu-id="bd63b-130">A Data Lake Store-ból letölthető elem elérési útját adja meg a gyökérkönyvtártól (/).</span><span class="sxs-lookup"><span data-stu-id="bd63b-130">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd63b-131">-Recurse</span><span class="sxs-lookup"><span data-stu-id="bd63b-131">-Recurse</span></span>
<span data-ttu-id="bd63b-132">Azt jelzi, hogy egy mappa letöltése rekurzív.</span><span class="sxs-lookup"><span data-stu-id="bd63b-132">Indicates that a folder download is recursive.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd63b-133">-Resume</span><span class="sxs-lookup"><span data-stu-id="bd63b-133">-Resume</span></span>
<span data-ttu-id="bd63b-134">Azt jelzi, hogy a másolt fájlok egy korábbi letöltés folytatásai.</span><span class="sxs-lookup"><span data-stu-id="bd63b-134">Indicates that the file(s) being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="bd63b-135">Ennek hatására a rendszer az utolsó olyan fájlból próbál meg folytatódni, amely még nem lett teljesen letöltve.</span><span class="sxs-lookup"><span data-stu-id="bd63b-135">This will cause the system to attempt to resume from the last file that was not fully downloaded.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd63b-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd63b-136">-Confirm</span></span>
<span data-ttu-id="bd63b-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bd63b-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd63b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd63b-138">-WhatIf</span></span>
<span data-ttu-id="bd63b-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bd63b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd63b-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bd63b-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd63b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd63b-141">CommonParameters</span></span>
<span data-ttu-id="bd63b-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd63b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd63b-143">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd63b-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd63b-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd63b-144">INPUTS</span></span>

### <span data-ttu-id="bd63b-145">System.String</span><span class="sxs-lookup"><span data-stu-id="bd63b-145">System.String</span></span>

### <span data-ttu-id="bd63b-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="bd63b-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="bd63b-147">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bd63b-147">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="bd63b-148">System.Int32</span><span class="sxs-lookup"><span data-stu-id="bd63b-148">System.Int32</span></span>

### <span data-ttu-id="bd63b-149">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span><span class="sxs-lookup"><span data-stu-id="bd63b-149">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="bd63b-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd63b-150">OUTPUTS</span></span>

### <span data-ttu-id="bd63b-151">System.String</span><span class="sxs-lookup"><span data-stu-id="bd63b-151">System.String</span></span>

## <span data-ttu-id="bd63b-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bd63b-152">NOTES</span></span>

## <span data-ttu-id="bd63b-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd63b-153">RELATED LINKS</span></span>

[<span data-ttu-id="bd63b-154">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bd63b-154">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="bd63b-155">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bd63b-155">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="bd63b-156">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bd63b-156">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="bd63b-157">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bd63b-157">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="bd63b-158">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bd63b-158">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="bd63b-159">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bd63b-159">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="bd63b-160">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bd63b-160">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


