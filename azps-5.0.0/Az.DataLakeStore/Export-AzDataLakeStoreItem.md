---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/export-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
ms.openlocfilehash: e0bac2f22249b27442c75da7879f6a6cf85e7da7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297902"
---
# <span data-ttu-id="d4bda-101">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d4bda-101">Export-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="d4bda-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d4bda-102">SYNOPSIS</span></span>
<span data-ttu-id="d4bda-103">Az adattó áruházból letölt egy fájlt.</span><span class="sxs-lookup"><span data-stu-id="d4bda-103">Downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="d4bda-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d4bda-104">SYNTAX</span></span>

### <span data-ttu-id="d4bda-105">NoDiagnosticLogging (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d4bda-105">NoDiagnosticLogging (Default)</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4bda-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="d4bda-106">IncludeDiagnosticLogging</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d4bda-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d4bda-107">DESCRIPTION</span></span>
<span data-ttu-id="d4bda-108">Az **export-AzDataLakeStoreItem** parancsmag az Adattó áruházból letölt egy fájlt.</span><span class="sxs-lookup"><span data-stu-id="d4bda-108">The **Export-AzDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="d4bda-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d4bda-109">EXAMPLES</span></span>

### <span data-ttu-id="d4bda-110">Példa 1: elem letöltése az adattó áruházból</span><span class="sxs-lookup"><span data-stu-id="d4bda-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv" -Concurrency 4
```

<span data-ttu-id="d4bda-111">Ez a parancs letölti a fájl TestSource.csv az adattó áruházból C:\Test.csv a 4 egyidejű konverzióval.</span><span class="sxs-lookup"><span data-stu-id="d4bda-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="d4bda-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d4bda-112">PARAMETERS</span></span>

### <span data-ttu-id="d4bda-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="d4bda-113">-Account</span></span>
<span data-ttu-id="d4bda-114">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4bda-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="d4bda-115">-Párhuzamosság</span><span class="sxs-lookup"><span data-stu-id="d4bda-115">-Concurrency</span></span>
<span data-ttu-id="d4bda-116">A párhuzamosan letölthető fájlok vagy adatdarabok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4bda-116">Indicates the number of files or chunks to download in parallel.</span></span> <span data-ttu-id="d4bda-117">Az alapértelmezett érték a rendszerspecifikációk alapján kiszámított legjobb munkamennyiség lesz.</span><span class="sxs-lookup"><span data-stu-id="d4bda-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="d4bda-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4bda-118">-DefaultProfile</span></span>
<span data-ttu-id="d4bda-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d4bda-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4bda-120">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="d4bda-120">-Destination</span></span>
<span data-ttu-id="d4bda-121">Annak a helyi fájlnak az elérési útját adja meg, ahová a fájlt le szeretné tölteni.</span><span class="sxs-lookup"><span data-stu-id="d4bda-121">Specifies the local file path to which to download the file.</span></span>

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

### <span data-ttu-id="d4bda-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="d4bda-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="d4bda-123">Tetszés szerint azt jelzi, hogy a diagnosztikai napló szintje az események rögzítéséhez a fájl vagy a mappa importálásakor használható.</span><span class="sxs-lookup"><span data-stu-id="d4bda-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="d4bda-124">Az alapértelmezett érték a hiba.</span><span class="sxs-lookup"><span data-stu-id="d4bda-124">Default is Error.</span></span>

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

### <span data-ttu-id="d4bda-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="d4bda-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="d4bda-126">A diagnosztikai napló elérési útját adja meg, amely a fájlok vagy mappák importálása során eseményeket rögzít.</span><span class="sxs-lookup"><span data-stu-id="d4bda-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="d4bda-127">-Force</span><span class="sxs-lookup"><span data-stu-id="d4bda-127">-Force</span></span>
<span data-ttu-id="d4bda-128">Jelzi, hogy az adott művelet felülírja a célfájlba, ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="d4bda-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="d4bda-129">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="d4bda-129">-Path</span></span>
<span data-ttu-id="d4bda-130">Annak az elemnek az elérési útvonalát adja meg, amelyet az adattó áruházból szeretne letölteni, kezdve a gyökérkönyvtárból (/).</span><span class="sxs-lookup"><span data-stu-id="d4bda-130">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

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

### <span data-ttu-id="d4bda-131">-Recurse</span><span class="sxs-lookup"><span data-stu-id="d4bda-131">-Recurse</span></span>
<span data-ttu-id="d4bda-132">Azt jelzi, hogy egy mappa letöltése rekurzív.</span><span class="sxs-lookup"><span data-stu-id="d4bda-132">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="d4bda-133">– Önéletrajz</span><span class="sxs-lookup"><span data-stu-id="d4bda-133">-Resume</span></span>
<span data-ttu-id="d4bda-134">Jelzi, hogy a másolt fájl (ok) az előző Letöltés folytatása.</span><span class="sxs-lookup"><span data-stu-id="d4bda-134">Indicates that the file(s) being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="d4bda-135">Ennek hatására a rendszer megkísérli az utolsó letöltött fájlból való folytatást.</span><span class="sxs-lookup"><span data-stu-id="d4bda-135">This will cause the system to attempt to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="d4bda-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d4bda-136">-Confirm</span></span>
<span data-ttu-id="d4bda-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d4bda-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4bda-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4bda-138">-WhatIf</span></span>
<span data-ttu-id="d4bda-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d4bda-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4bda-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d4bda-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4bda-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4bda-141">CommonParameters</span></span>
<span data-ttu-id="d4bda-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d4bda-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4bda-143">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4bda-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4bda-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4bda-144">INPUTS</span></span>

### <span data-ttu-id="d4bda-145">System. String</span><span class="sxs-lookup"><span data-stu-id="d4bda-145">System.String</span></span>

### <span data-ttu-id="d4bda-146">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="d4bda-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="d4bda-147">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d4bda-147">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="d4bda-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d4bda-148">System.Int32</span></span>

### <span data-ttu-id="d4bda-149">Microsoft. Azure. Command. DataLakeStore. models. LogLevel</span><span class="sxs-lookup"><span data-stu-id="d4bda-149">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="d4bda-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4bda-150">OUTPUTS</span></span>

### <span data-ttu-id="d4bda-151">System. String</span><span class="sxs-lookup"><span data-stu-id="d4bda-151">System.String</span></span>

## <span data-ttu-id="d4bda-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d4bda-152">NOTES</span></span>

## <span data-ttu-id="d4bda-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4bda-153">RELATED LINKS</span></span>

[<span data-ttu-id="d4bda-154">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d4bda-154">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="d4bda-155">Importálás – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d4bda-155">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="d4bda-156">Bekapcsolódás a AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d4bda-156">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="d4bda-157">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d4bda-157">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="d4bda-158">Új – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d4bda-158">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="d4bda-159">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d4bda-159">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="d4bda-160">Teszt-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d4bda-160">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


