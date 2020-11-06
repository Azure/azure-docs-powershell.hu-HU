---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: febcec4d309e849e3b259fc2d80b3129ca7b65f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501907"
---
# <span data-ttu-id="b9e1e-101">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b9e1e-101">Export-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="b9e1e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b9e1e-102">SYNOPSIS</span></span>
<span data-ttu-id="b9e1e-103">Az adattó áruházból letölt egy fájlt.</span><span class="sxs-lookup"><span data-stu-id="b9e1e-103">Downloads a file from Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9e1e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b9e1e-104">SYNTAX</span></span>

### <span data-ttu-id="b9e1e-105">Nincs diagnosztikai naplózás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b9e1e-105">No diagnostic logging (Default)</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9e1e-106">Diagnosztikai naplózás befoglalása</span><span class="sxs-lookup"><span data-stu-id="b9e1e-106">Include diagnostic logging</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9e1e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b9e1e-107">DESCRIPTION</span></span>
<span data-ttu-id="b9e1e-108">Az **export-AzureRmDataLakeStoreItem** parancsmag az Adattó áruházból letölt egy fájlt.</span><span class="sxs-lookup"><span data-stu-id="b9e1e-108">The **Export-AzureRmDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="b9e1e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b9e1e-109">EXAMPLES</span></span>

### <span data-ttu-id="b9e1e-110">Példa 1: elem letöltése az adattó áruházból</span><span class="sxs-lookup"><span data-stu-id="b9e1e-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv"
```

<span data-ttu-id="b9e1e-111">Ez a parancs letölti a fájl TestSource.csv az adattó áruházból a C:\Test.csv-ra.</span><span class="sxs-lookup"><span data-stu-id="b9e1e-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv.</span></span>

## <span data-ttu-id="b9e1e-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b9e1e-112">PARAMETERS</span></span>

### <span data-ttu-id="b9e1e-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="b9e1e-113">-Account</span></span>
<span data-ttu-id="b9e1e-114">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b9e1e-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="b9e1e-115">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="b9e1e-115">-ConcurrentFileCount</span></span>
<span data-ttu-id="b9e1e-116">Itt adhatja meg, hogy a fájlok legfeljebb hány fájlt tölthetnek le párhuzamosan a mappa letöltéséhez.</span><span class="sxs-lookup"><span data-stu-id="b9e1e-116">Specifies the maximum number of files to download in parallel for a folder download.</span></span>
<span data-ttu-id="b9e1e-117">Az alapértelmezett érték az 5 (5).</span><span class="sxs-lookup"><span data-stu-id="b9e1e-117">The default value is five (5).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e1e-118">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="b9e1e-118">-Destination</span></span>
<span data-ttu-id="b9e1e-119">Annak a helyi fájlnak az elérési útját adja meg, ahová a fájlt le szeretné tölteni.</span><span class="sxs-lookup"><span data-stu-id="b9e1e-119">Specifies the local file path to which to download the file.</span></span>

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

### <span data-ttu-id="b9e1e-120">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="b9e1e-120">-DiagnosticLogLevel</span></span>
<span data-ttu-id="b9e1e-121">Tetszés szerint azt jelzi, hogy a diagnosztikai napló szintje az események rögzítéséhez a fájl vagy a mappa importálásakor használható.</span><span class="sxs-lookup"><span data-stu-id="b9e1e-121">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="b9e1e-122">Az alapértelmezett érték a hiba.</span><span class="sxs-lookup"><span data-stu-id="b9e1e-122">Default is Error.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel
Parameter Sets: Include diagnostic logging
Aliases: 
Accepted values: Debug, Information, Error, None

Required: False
Position: Named
Default value: Error
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e1e-123">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="b9e1e-123">-DiagnosticLogPath</span></span>
<span data-ttu-id="b9e1e-124">A diagnosztikai napló elérési útját adja meg, amely a fájlok vagy mappák importálása során eseményeket rögzít.</span><span class="sxs-lookup"><span data-stu-id="b9e1e-124">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

```yaml
Type: System.String
Parameter Sets: Include diagnostic logging
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e1e-125">-Force</span><span class="sxs-lookup"><span data-stu-id="b9e1e-125">-Force</span></span>
<span data-ttu-id="b9e1e-126">Jelzi, hogy az adott művelet felülírja a célfájlba, ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="b9e1e-126">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="b9e1e-127">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="b9e1e-127">-Path</span></span>
<span data-ttu-id="b9e1e-128">Annak az elemnek az elérési útvonalát adja meg, amelyet az adattó áruházból szeretne letölteni, kezdve a gyökérkönyvtárból (/).</span><span class="sxs-lookup"><span data-stu-id="b9e1e-128">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

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

### <span data-ttu-id="b9e1e-129">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="b9e1e-129">-PerFileThreadCount</span></span>
<span data-ttu-id="b9e1e-130">Megadja, hogy a szálak legfeljebb hány szálat használhatók fájlonként.</span><span class="sxs-lookup"><span data-stu-id="b9e1e-130">Specifies the maximum number of threads to use per file.</span></span>
<span data-ttu-id="b9e1e-131">Az alapértelmezett érték tíz (10).</span><span class="sxs-lookup"><span data-stu-id="b9e1e-131">The default value is ten (10).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e1e-132">-Recurse</span><span class="sxs-lookup"><span data-stu-id="b9e1e-132">-Recurse</span></span>
<span data-ttu-id="b9e1e-133">Azt jelzi, hogy egy mappa letöltése rekurzív.</span><span class="sxs-lookup"><span data-stu-id="b9e1e-133">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="b9e1e-134">– Önéletrajz</span><span class="sxs-lookup"><span data-stu-id="b9e1e-134">-Resume</span></span>
<span data-ttu-id="b9e1e-135">Jelzi, hogy a másolt fájl vagy fájlok az előző Letöltés folytatását jelentik.</span><span class="sxs-lookup"><span data-stu-id="b9e1e-135">Indicates that the file or files being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="b9e1e-136">A letöltés a legutóbb letöltött fájlból kísérli meg az önéletrajzot.</span><span class="sxs-lookup"><span data-stu-id="b9e1e-136">The download attempts to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="b9e1e-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b9e1e-137">-Confirm</span></span>
<span data-ttu-id="b9e1e-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b9e1e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9e1e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9e1e-139">-WhatIf</span></span>
<span data-ttu-id="b9e1e-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b9e1e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9e1e-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b9e1e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9e1e-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9e1e-142">-DefaultProfile</span></span>
<span data-ttu-id="b9e1e-143">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b9e1e-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e1e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9e1e-144">CommonParameters</span></span>
<span data-ttu-id="b9e1e-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b9e1e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9e1e-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9e1e-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9e1e-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9e1e-147">INPUTS</span></span>

## <span data-ttu-id="b9e1e-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9e1e-148">OUTPUTS</span></span>

### <span data-ttu-id="b9e1e-149">karakterlánc</span><span class="sxs-lookup"><span data-stu-id="b9e1e-149">string</span></span>
<span data-ttu-id="b9e1e-150">A fájl vagy mappa letöltésének elérési útja.</span><span class="sxs-lookup"><span data-stu-id="b9e1e-150">The path where the file or folder was downloaded to.</span></span>

## <span data-ttu-id="b9e1e-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b9e1e-151">NOTES</span></span>

## <span data-ttu-id="b9e1e-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9e1e-152">RELATED LINKS</span></span>

[<span data-ttu-id="b9e1e-153">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b9e1e-153">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b9e1e-154">Importálás – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b9e1e-154">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b9e1e-155">Bekapcsolódás a AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b9e1e-155">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b9e1e-156">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b9e1e-156">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b9e1e-157">Új – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b9e1e-157">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b9e1e-158">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b9e1e-158">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b9e1e-159">Teszt-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b9e1e-159">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


