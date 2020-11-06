---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/export-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 508a7619374b7e245b8df99c929f161ce1966288
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499567"
---
# <span data-ttu-id="ed508-101">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ed508-101">Export-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="ed508-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ed508-102">SYNOPSIS</span></span>
<span data-ttu-id="ed508-103">Az adattó áruházból letölt egy fájlt.</span><span class="sxs-lookup"><span data-stu-id="ed508-103">Downloads a file from Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed508-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ed508-104">SYNTAX</span></span>

### <span data-ttu-id="ed508-105">NoDiagnosticLogging (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ed508-105">NoDiagnosticLogging (Default)</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed508-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="ed508-106">IncludeDiagnosticLogging</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ed508-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ed508-107">DESCRIPTION</span></span>
<span data-ttu-id="ed508-108">Az **export-AzureRmDataLakeStoreItem** parancsmag az Adattó áruházból letölt egy fájlt.</span><span class="sxs-lookup"><span data-stu-id="ed508-108">The **Export-AzureRmDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="ed508-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ed508-109">EXAMPLES</span></span>

### <span data-ttu-id="ed508-110">Példa 1: elem letöltése az adattó áruházból</span><span class="sxs-lookup"><span data-stu-id="ed508-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv" -Concurrency 4
```

<span data-ttu-id="ed508-111">Ez a parancs letölti a fájl TestSource.csv az adattó áruházból C:\Test.csv a 4 egyidejű konverzióval.</span><span class="sxs-lookup"><span data-stu-id="ed508-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="ed508-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ed508-112">PARAMETERS</span></span>

### <span data-ttu-id="ed508-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="ed508-113">-Account</span></span>
<span data-ttu-id="ed508-114">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ed508-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="ed508-115">-Párhuzamosság</span><span class="sxs-lookup"><span data-stu-id="ed508-115">-Concurrency</span></span>
<span data-ttu-id="ed508-116">A párhuzamosan letölthető fájlok vagy adatdarabok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ed508-116">Indicates the number of files or chunks to download in parallel.</span></span> <span data-ttu-id="ed508-117">Az alapértelmezett érték a rendszerspecifikációk alapján kiszámított legjobb munkamennyiség lesz.</span><span class="sxs-lookup"><span data-stu-id="ed508-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="ed508-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed508-118">-DefaultProfile</span></span>
<span data-ttu-id="ed508-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ed508-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed508-120">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="ed508-120">-Destination</span></span>
<span data-ttu-id="ed508-121">Annak a helyi fájlnak az elérési útját adja meg, ahová a fájlt le szeretné tölteni.</span><span class="sxs-lookup"><span data-stu-id="ed508-121">Specifies the local file path to which to download the file.</span></span>

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

### <span data-ttu-id="ed508-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="ed508-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="ed508-123">Tetszés szerint azt jelzi, hogy a diagnosztikai napló szintje az események rögzítéséhez a fájl vagy a mappa importálásakor használható.</span><span class="sxs-lookup"><span data-stu-id="ed508-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="ed508-124">Az alapértelmezett érték a hiba.</span><span class="sxs-lookup"><span data-stu-id="ed508-124">Default is Error.</span></span>

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

### <span data-ttu-id="ed508-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="ed508-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="ed508-126">A diagnosztikai napló elérési útját adja meg, amely a fájlok vagy mappák importálása során eseményeket rögzít.</span><span class="sxs-lookup"><span data-stu-id="ed508-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="ed508-127">-Force</span><span class="sxs-lookup"><span data-stu-id="ed508-127">-Force</span></span>
<span data-ttu-id="ed508-128">Jelzi, hogy az adott művelet felülírja a célfájlba, ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="ed508-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="ed508-129">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="ed508-129">-Path</span></span>
<span data-ttu-id="ed508-130">Annak az elemnek az elérési útvonalát adja meg, amelyet az adattó áruházból szeretne letölteni, kezdve a gyökérkönyvtárból (/).</span><span class="sxs-lookup"><span data-stu-id="ed508-130">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

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

### <span data-ttu-id="ed508-131">-Recurse</span><span class="sxs-lookup"><span data-stu-id="ed508-131">-Recurse</span></span>
<span data-ttu-id="ed508-132">Azt jelzi, hogy egy mappa letöltése rekurzív.</span><span class="sxs-lookup"><span data-stu-id="ed508-132">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="ed508-133">– Önéletrajz</span><span class="sxs-lookup"><span data-stu-id="ed508-133">-Resume</span></span>
<span data-ttu-id="ed508-134">Jelzi, hogy a másolt fájl (ok) az előző Letöltés folytatása.</span><span class="sxs-lookup"><span data-stu-id="ed508-134">Indicates that the file(s) being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="ed508-135">Ennek hatására a rendszer megkísérli az utolsó letöltött fájlból való folytatást.</span><span class="sxs-lookup"><span data-stu-id="ed508-135">This will cause the system to attempt to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="ed508-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ed508-136">-Confirm</span></span>
<span data-ttu-id="ed508-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ed508-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed508-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed508-138">-WhatIf</span></span>
<span data-ttu-id="ed508-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ed508-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed508-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ed508-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed508-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed508-141">CommonParameters</span></span>
<span data-ttu-id="ed508-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ed508-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed508-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed508-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed508-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed508-144">INPUTS</span></span>

### <span data-ttu-id="ed508-145">System. String</span><span class="sxs-lookup"><span data-stu-id="ed508-145">System.String</span></span>

### <span data-ttu-id="ed508-146">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="ed508-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="ed508-147">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ed508-147">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ed508-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ed508-148">System.Int32</span></span>

### <span data-ttu-id="ed508-149">Microsoft. Azure. Command. DataLakeStore. models. LogLevel</span><span class="sxs-lookup"><span data-stu-id="ed508-149">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="ed508-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed508-150">OUTPUTS</span></span>

### <span data-ttu-id="ed508-151">System. String</span><span class="sxs-lookup"><span data-stu-id="ed508-151">System.String</span></span>
<span data-ttu-id="ed508-152">A fájl vagy mappa letöltésének elérési útja.</span><span class="sxs-lookup"><span data-stu-id="ed508-152">The path where the file or folder was downloaded to.</span></span>

## <span data-ttu-id="ed508-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ed508-153">NOTES</span></span>

## <span data-ttu-id="ed508-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed508-154">RELATED LINKS</span></span>

[<span data-ttu-id="ed508-155">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ed508-155">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ed508-156">Importálás – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ed508-156">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ed508-157">Bekapcsolódás a AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ed508-157">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ed508-158">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ed508-158">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ed508-159">Új – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ed508-159">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ed508-160">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ed508-160">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ed508-161">Teszt-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ed508-161">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


