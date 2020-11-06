---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/import-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 91e7969600f387a95f46cad02f87cf6466f2c642
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494059"
---
# <span data-ttu-id="94d82-101">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="94d82-101">Import-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="94d82-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="94d82-102">SYNOPSIS</span></span>
<span data-ttu-id="94d82-103">Helyi fájlt vagy könyvtárat tölt fel egy adattó-áruházba.</span><span class="sxs-lookup"><span data-stu-id="94d82-103">Uploads a local file or directory to a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94d82-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="94d82-104">SYNTAX</span></span>

### <span data-ttu-id="94d82-105">NoDiagnosticLogging (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="94d82-105">NoDiagnosticLogging (Default)</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94d82-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="94d82-106">IncludeDiagnosticLogging</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94d82-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="94d82-107">DESCRIPTION</span></span>
<span data-ttu-id="94d82-108">Az **import-AzureRmDataLakeStoreItem** parancsmag egy helyi fájlt vagy könyvtárat tölt fel egy adattó-tárolóba.</span><span class="sxs-lookup"><span data-stu-id="94d82-108">The **Import-AzureRmDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="94d82-109">Példák</span><span class="sxs-lookup"><span data-stu-id="94d82-109">EXAMPLES</span></span>

### <span data-ttu-id="94d82-110">1. példa: fájl feltöltése</span><span class="sxs-lookup"><span data-stu-id="94d82-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

<span data-ttu-id="94d82-111">Ez a parancs feltölti a fájlt SrcFile.csv és felveszi a MyFiles-mappába az adattó-tárolóban, mint a 4 egyidejű File.csv.</span><span class="sxs-lookup"><span data-stu-id="94d82-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="94d82-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="94d82-112">PARAMETERS</span></span>

### <span data-ttu-id="94d82-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="94d82-113">-Account</span></span>
<span data-ttu-id="94d82-114">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="94d82-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="94d82-115">-Párhuzamosság</span><span class="sxs-lookup"><span data-stu-id="94d82-115">-Concurrency</span></span>
<span data-ttu-id="94d82-116">A párhuzamosan feltöltött fájlok vagy adatdarabok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="94d82-116">Indicates the number of files or chunks to upload in parallel.</span></span> <span data-ttu-id="94d82-117">Az alapértelmezett érték a rendszerspecifikációk alapján kiszámított legjobb munkamennyiség lesz.</span><span class="sxs-lookup"><span data-stu-id="94d82-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="94d82-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94d82-118">-DefaultProfile</span></span>
<span data-ttu-id="94d82-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94d82-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94d82-120">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="94d82-120">-Destination</span></span>
<span data-ttu-id="94d82-121">Az adattó-tároló elérési útját adja meg, amelybe fájlt vagy mappát szeretne feltölteni, kezdve a root-könyvtárral (/).</span><span class="sxs-lookup"><span data-stu-id="94d82-121">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94d82-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="94d82-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="94d82-123">Tetszés szerint azt jelzi, hogy a diagnosztikai napló szintje az események rögzítéséhez a fájl vagy a mappa importálásakor használható.</span><span class="sxs-lookup"><span data-stu-id="94d82-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="94d82-124">Az alapértelmezett érték a hiba.</span><span class="sxs-lookup"><span data-stu-id="94d82-124">Default is Error.</span></span>

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

### <span data-ttu-id="94d82-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="94d82-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="94d82-126">A diagnosztikai napló elérési útját adja meg, amely a fájlok vagy mappák importálása során eseményeket rögzít.</span><span class="sxs-lookup"><span data-stu-id="94d82-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="94d82-127">-Force</span><span class="sxs-lookup"><span data-stu-id="94d82-127">-Force</span></span>
<span data-ttu-id="94d82-128">Jelzi, hogy az adott művelet felülírja a célfájlba, ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="94d82-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94d82-129">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="94d82-129">-ForceBinary</span></span>
<span data-ttu-id="94d82-130">Azt jelzi, hogy a másolt fájl (oka) t a program nem érinti az új, hozzáfűzéssel való megőrzést.</span><span class="sxs-lookup"><span data-stu-id="94d82-130">Indicates that the file(s) being copied should be copied with no concern for new line preservation across appends.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94d82-131">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="94d82-131">-Path</span></span>
<span data-ttu-id="94d82-132">A feltölteni kívánt fájl vagy mappa helyi elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="94d82-132">Specifies the local path of the file or folder to upload.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94d82-133">-Recurse</span><span class="sxs-lookup"><span data-stu-id="94d82-133">-Recurse</span></span>
<span data-ttu-id="94d82-134">Azt jelzi, hogy ez a művelet minden almappa összes elemét feltölti.</span><span class="sxs-lookup"><span data-stu-id="94d82-134">Indicates that this operation should upload all items in all subfolders.</span></span>

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

### <span data-ttu-id="94d82-135">– Önéletrajz</span><span class="sxs-lookup"><span data-stu-id="94d82-135">-Resume</span></span>
<span data-ttu-id="94d82-136">Jelzi, hogy a másolt fájl (ok) az előző feltöltés folytatása.</span><span class="sxs-lookup"><span data-stu-id="94d82-136">Indicates that the file(s) being copied are a continuation of a previous upload.</span></span> <span data-ttu-id="94d82-137">Ennek hatására a rendszer megkísérli folytatni az utolsó olyan fájlból való visszatérést, amely nem lett teljesen feltöltve.</span><span class="sxs-lookup"><span data-stu-id="94d82-137">This will cause the system to attempt to resume from the last file that was not fully uploaded.</span></span>

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

### <span data-ttu-id="94d82-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="94d82-138">-Confirm</span></span>
<span data-ttu-id="94d82-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="94d82-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94d82-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94d82-140">-WhatIf</span></span>
<span data-ttu-id="94d82-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="94d82-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94d82-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="94d82-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94d82-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94d82-143">CommonParameters</span></span>
<span data-ttu-id="94d82-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="94d82-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94d82-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94d82-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94d82-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="94d82-146">INPUTS</span></span>

### <span data-ttu-id="94d82-147">System. String</span><span class="sxs-lookup"><span data-stu-id="94d82-147">System.String</span></span>

### <span data-ttu-id="94d82-148">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="94d82-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="94d82-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="94d82-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="94d82-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="94d82-150">System.Int32</span></span>

### <span data-ttu-id="94d82-151">Microsoft. Azure. Command. DataLakeStore. models. LogLevel</span><span class="sxs-lookup"><span data-stu-id="94d82-151">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="94d82-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94d82-152">OUTPUTS</span></span>

### <span data-ttu-id="94d82-153">System. String</span><span class="sxs-lookup"><span data-stu-id="94d82-153">System.String</span></span>
<span data-ttu-id="94d82-154">Az adattó áruházbeli fiók teljes elérési útja a feltöltött fájllal vagy mappával.</span><span class="sxs-lookup"><span data-stu-id="94d82-154">The full path in the Data Lake Store account to the uploaded file or folder.</span></span>

## <span data-ttu-id="94d82-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="94d82-155">NOTES</span></span>

## <span data-ttu-id="94d82-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94d82-156">RELATED LINKS</span></span>

[<span data-ttu-id="94d82-157">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="94d82-157">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="94d82-158">Exportálás – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="94d82-158">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="94d82-159">Bekapcsolódás a AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="94d82-159">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="94d82-160">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="94d82-160">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="94d82-161">Új – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="94d82-161">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="94d82-162">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="94d82-162">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="94d82-163">Teszt-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="94d82-163">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


