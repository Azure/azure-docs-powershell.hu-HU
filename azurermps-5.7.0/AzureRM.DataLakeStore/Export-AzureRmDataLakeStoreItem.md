---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/export-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 907e4e92b511349011b27cb8aaf7588b8e495220
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672374"
---
# <span data-ttu-id="b0f62-101">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b0f62-101">Export-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="b0f62-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b0f62-102">SYNOPSIS</span></span>
<span data-ttu-id="b0f62-103">Az adattó áruházból letölt egy fájlt.</span><span class="sxs-lookup"><span data-stu-id="b0f62-103">Downloads a file from Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0f62-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b0f62-104">SYNTAX</span></span>

### <span data-ttu-id="b0f62-105">NoDiagnosticLogging (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b0f62-105">NoDiagnosticLogging (Default)</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0f62-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="b0f62-106">IncludeDiagnosticLogging</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0f62-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b0f62-107">DESCRIPTION</span></span>
<span data-ttu-id="b0f62-108">Az **export-AzureRmDataLakeStoreItem** parancsmag az Adattó áruházból letölt egy fájlt.</span><span class="sxs-lookup"><span data-stu-id="b0f62-108">The **Export-AzureRmDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="b0f62-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b0f62-109">EXAMPLES</span></span>

### <span data-ttu-id="b0f62-110">Példa 1: elem letöltése az adattó áruházból</span><span class="sxs-lookup"><span data-stu-id="b0f62-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv" -Concurrency 4
```

<span data-ttu-id="b0f62-111">Ez a parancs letölti a fájl TestSource.csv az adattó áruházból C:\Test.csv a 4 egyidejű konverzióval.</span><span class="sxs-lookup"><span data-stu-id="b0f62-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="b0f62-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b0f62-112">PARAMETERS</span></span>

### <span data-ttu-id="b0f62-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="b0f62-113">-Account</span></span>
<span data-ttu-id="b0f62-114">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b0f62-114">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0f62-115">-Párhuzamosság</span><span class="sxs-lookup"><span data-stu-id="b0f62-115">-Concurrency</span></span>
<span data-ttu-id="b0f62-116">A párhuzamosan letölthető fájlok vagy adatdarabok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b0f62-116">Indicates the number of files or chunks to download in parallel.</span></span> <span data-ttu-id="b0f62-117">Az alapértelmezett érték a rendszerspecifikációk alapján kiszámított legjobb munkamennyiség lesz.</span><span class="sxs-lookup"><span data-stu-id="b0f62-117">Default will be computed as a best effort based on system specifications.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0f62-118">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="b0f62-118">-ConcurrentFileCount</span></span>
<span data-ttu-id="b0f62-119">Azt jelzi, hogy a fájlok legfeljebb hány fájlt tölthetnek le párhuzamosan a mappa letöltéséhez.</span><span class="sxs-lookup"><span data-stu-id="b0f62-119">Indicates the maximum number of files to download in parallel for a folder download.</span></span>  <span data-ttu-id="b0f62-120">Az alapértelmezett értéket a program a mappa és a fájlméret alapján számítja ki legjobban.</span><span class="sxs-lookup"><span data-stu-id="b0f62-120">Default will be computed as a best effort based on folder and file size</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0f62-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0f62-121">-DefaultProfile</span></span>
<span data-ttu-id="b0f62-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b0f62-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0f62-123">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="b0f62-123">-Destination</span></span>
<span data-ttu-id="b0f62-124">Annak a helyi fájlnak az elérési útját adja meg, ahová a fájlt le szeretné tölteni.</span><span class="sxs-lookup"><span data-stu-id="b0f62-124">Specifies the local file path to which to download the file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0f62-125">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="b0f62-125">-DiagnosticLogLevel</span></span>
<span data-ttu-id="b0f62-126">Tetszés szerint azt jelzi, hogy a diagnosztikai napló szintje az események rögzítéséhez a fájl vagy a mappa importálásakor használható.</span><span class="sxs-lookup"><span data-stu-id="b0f62-126">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="b0f62-127">Az alapértelmezett érték a hiba.</span><span class="sxs-lookup"><span data-stu-id="b0f62-127">Default is Error.</span></span>

```yaml
Type: LogLevel
Parameter Sets: IncludeDiagnosticLogging
Aliases: 
Accepted values: Debug, Information, Error, None

Required: False
Position: Named
Default value: Error
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0f62-128">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="b0f62-128">-DiagnosticLogPath</span></span>
<span data-ttu-id="b0f62-129">A diagnosztikai napló elérési útját adja meg, amely a fájlok vagy mappák importálása során eseményeket rögzít.</span><span class="sxs-lookup"><span data-stu-id="b0f62-129">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

```yaml
Type: String
Parameter Sets: IncludeDiagnosticLogging
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0f62-130">-Force</span><span class="sxs-lookup"><span data-stu-id="b0f62-130">-Force</span></span>
<span data-ttu-id="b0f62-131">Jelzi, hogy az adott művelet felülírja a célfájlba, ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="b0f62-131">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0f62-132">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="b0f62-132">-Path</span></span>
<span data-ttu-id="b0f62-133">Annak az elemnek az elérési útvonalát adja meg, amelyet az adattó áruházból szeretne letölteni, kezdve a gyökérkönyvtárból (/).</span><span class="sxs-lookup"><span data-stu-id="b0f62-133">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0f62-134">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="b0f62-134">-PerFileThreadCount</span></span>
<span data-ttu-id="b0f62-135">Azt jelzi, hogy a szálak maximális száma fájlonként használható.</span><span class="sxs-lookup"><span data-stu-id="b0f62-135">Indicates the maximum number of threads to use per file.</span></span>  <span data-ttu-id="b0f62-136">Az alapértelmezett értéket a program a mappa és a fájlméret alapján számítja ki legjobban.</span><span class="sxs-lookup"><span data-stu-id="b0f62-136">Default will be computed as a best effort based on folder and file size</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0f62-137">-Recurse</span><span class="sxs-lookup"><span data-stu-id="b0f62-137">-Recurse</span></span>
<span data-ttu-id="b0f62-138">Azt jelzi, hogy egy mappa letöltése rekurzív.</span><span class="sxs-lookup"><span data-stu-id="b0f62-138">Indicates that a folder download is recursive.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0f62-139">– Önéletrajz</span><span class="sxs-lookup"><span data-stu-id="b0f62-139">-Resume</span></span>
<span data-ttu-id="b0f62-140">Jelzi, hogy a másolt fájl (ok) az előző Letöltés folytatása.</span><span class="sxs-lookup"><span data-stu-id="b0f62-140">Indicates that the file(s) being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="b0f62-141">Ennek hatására a rendszer megkísérli az utolsó letöltött fájlból való folytatást.</span><span class="sxs-lookup"><span data-stu-id="b0f62-141">This will cause the system to attempt to resume from the last file that was not fully downloaded.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0f62-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b0f62-142">-Confirm</span></span>
<span data-ttu-id="b0f62-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b0f62-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0f62-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0f62-144">-WhatIf</span></span>
<span data-ttu-id="b0f62-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b0f62-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0f62-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b0f62-146">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0f62-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0f62-147">CommonParameters</span></span>
<span data-ttu-id="b0f62-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b0f62-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0f62-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0f62-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0f62-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0f62-150">INPUTS</span></span>

### <span data-ttu-id="b0f62-151">Nincs</span><span class="sxs-lookup"><span data-stu-id="b0f62-151">None</span></span>
<span data-ttu-id="b0f62-152">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="b0f62-152">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b0f62-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0f62-153">OUTPUTS</span></span>

### <span data-ttu-id="b0f62-154">karakterlánc</span><span class="sxs-lookup"><span data-stu-id="b0f62-154">string</span></span>
<span data-ttu-id="b0f62-155">A fájl vagy mappa letöltésének elérési útja.</span><span class="sxs-lookup"><span data-stu-id="b0f62-155">The path where the file or folder was downloaded to.</span></span>

## <span data-ttu-id="b0f62-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b0f62-156">NOTES</span></span>

## <span data-ttu-id="b0f62-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b0f62-157">RELATED LINKS</span></span>

[<span data-ttu-id="b0f62-158">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b0f62-158">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b0f62-159">Importálás – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b0f62-159">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b0f62-160">Bekapcsolódás a AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b0f62-160">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b0f62-161">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b0f62-161">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b0f62-162">Új – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b0f62-162">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b0f62-163">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b0f62-163">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b0f62-164">Teszt-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b0f62-164">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


