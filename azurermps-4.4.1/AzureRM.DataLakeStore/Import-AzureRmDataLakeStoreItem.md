---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: ed10d3ee7c5a35c039a19f44211c7c2fce08aa06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679455"
---
# <span data-ttu-id="bdc0f-101">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bdc0f-101">Import-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="bdc0f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bdc0f-102">SYNOPSIS</span></span>
<span data-ttu-id="bdc0f-103">Helyi fájlt vagy könyvtárat tölt fel egy adattó-áruházba.</span><span class="sxs-lookup"><span data-stu-id="bdc0f-103">Uploads a local file or directory to a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdc0f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bdc0f-104">SYNTAX</span></span>

### <span data-ttu-id="bdc0f-105">Nincs diagnosztikai naplózás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bdc0f-105">No diagnostic logging (Default)</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdc0f-106">Diagnosztikai naplózás befoglalása</span><span class="sxs-lookup"><span data-stu-id="bdc0f-106">Include diagnostic logging</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdc0f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="bdc0f-107">DESCRIPTION</span></span>
<span data-ttu-id="bdc0f-108">Az **import-AzureRmDataLakeStoreItem** parancsmag egy helyi fájlt vagy könyvtárat tölt fel egy adattó-tárolóba.</span><span class="sxs-lookup"><span data-stu-id="bdc0f-108">The **Import-AzureRmDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="bdc0f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="bdc0f-109">EXAMPLES</span></span>

### <span data-ttu-id="bdc0f-110">1. példa: fájl feltöltése</span><span class="sxs-lookup"><span data-stu-id="bdc0f-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv"
```

<span data-ttu-id="bdc0f-111">Ez a parancs feltölti a fájlt SrcFile.csv és felveszi a MyFiles-mappába az adattó áruházban File.csv.</span><span class="sxs-lookup"><span data-stu-id="bdc0f-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv.</span></span>

## <span data-ttu-id="bdc0f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bdc0f-112">PARAMETERS</span></span>

### <span data-ttu-id="bdc0f-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="bdc0f-113">-Account</span></span>
<span data-ttu-id="bdc0f-114">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bdc0f-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="bdc0f-115">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="bdc0f-115">-ConcurrentFileCount</span></span>
<span data-ttu-id="bdc0f-116">Adja meg, hogy a feltöltött fájlok legfeljebb hány fájlt tölthetnek fel párhuzamosan a mappa feltöltésekor.</span><span class="sxs-lookup"><span data-stu-id="bdc0f-116">Specify the maximum number of files to upload in parallel for a folder upload.</span></span>
<span data-ttu-id="bdc0f-117">Az alapértelmezett érték az 5 (5).</span><span class="sxs-lookup"><span data-stu-id="bdc0f-117">The default value is five (5).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdc0f-118">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="bdc0f-118">-Destination</span></span>
<span data-ttu-id="bdc0f-119">Az adattó-tároló elérési útját adja meg, amelybe fájlt vagy mappát szeretne feltölteni, kezdve a root-könyvtárral (/).</span><span class="sxs-lookup"><span data-stu-id="bdc0f-119">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="bdc0f-120">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="bdc0f-120">-DiagnosticLogLevel</span></span>
<span data-ttu-id="bdc0f-121">Tetszés szerint azt jelzi, hogy a diagnosztikai napló szintje az események rögzítéséhez a fájl vagy a mappa importálásakor használható.</span><span class="sxs-lookup"><span data-stu-id="bdc0f-121">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="bdc0f-122">Az alapértelmezett érték a hiba.</span><span class="sxs-lookup"><span data-stu-id="bdc0f-122">Default is Error.</span></span>

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

### <span data-ttu-id="bdc0f-123">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="bdc0f-123">-DiagnosticLogPath</span></span>
<span data-ttu-id="bdc0f-124">A diagnosztikai napló elérési útját adja meg, amely a fájlok vagy mappák importálása során eseményeket rögzít.</span><span class="sxs-lookup"><span data-stu-id="bdc0f-124">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="bdc0f-125">-Force</span><span class="sxs-lookup"><span data-stu-id="bdc0f-125">-Force</span></span>
<span data-ttu-id="bdc0f-126">Jelzi, hogy az adott művelet felülírja a célfájlba, ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="bdc0f-126">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="bdc0f-127">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="bdc0f-127">-ForceBinary</span></span>
<span data-ttu-id="bdc0f-128">Azt jelzi, hogy ez a művelet bináris fájlként tölti fel a fájlt.</span><span class="sxs-lookup"><span data-stu-id="bdc0f-128">Indicates that this operation uploads the file as a binary file.</span></span>

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

### <span data-ttu-id="bdc0f-129">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="bdc0f-129">-Path</span></span>
<span data-ttu-id="bdc0f-130">A feltölteni kívánt fájl vagy mappa helyi elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bdc0f-130">Specifies the local path of the file or folder to upload.</span></span>

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

### <span data-ttu-id="bdc0f-131">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="bdc0f-131">-PerFileThreadCount</span></span>
<span data-ttu-id="bdc0f-132">Megadja, hogy a szálak legfeljebb hány szálat használhatók fájlonként.</span><span class="sxs-lookup"><span data-stu-id="bdc0f-132">Specifies the maximum number of threads to use per file.</span></span>
<span data-ttu-id="bdc0f-133">Az alapértelmezett érték tíz (10).</span><span class="sxs-lookup"><span data-stu-id="bdc0f-133">The default value is ten (10).</span></span>

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

### <span data-ttu-id="bdc0f-134">-Recurse</span><span class="sxs-lookup"><span data-stu-id="bdc0f-134">-Recurse</span></span>
<span data-ttu-id="bdc0f-135">Azt jelzi, hogy ez a művelet minden almappa összes elemét feltölti.</span><span class="sxs-lookup"><span data-stu-id="bdc0f-135">Indicates that this operation should upload all items in all subfolders.</span></span>

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

### <span data-ttu-id="bdc0f-136">– Önéletrajz</span><span class="sxs-lookup"><span data-stu-id="bdc0f-136">-Resume</span></span>
<span data-ttu-id="bdc0f-137">Azt jelzi, hogy ez a művelet a korábban lemondott vagy sikertelen feltöltést folytassa.</span><span class="sxs-lookup"><span data-stu-id="bdc0f-137">Indicates that this operation should resume a previously canceled or failed upload.</span></span>

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

### <span data-ttu-id="bdc0f-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bdc0f-138">-Confirm</span></span>
<span data-ttu-id="bdc0f-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bdc0f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdc0f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdc0f-140">-WhatIf</span></span>
<span data-ttu-id="bdc0f-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bdc0f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdc0f-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bdc0f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdc0f-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdc0f-143">-DefaultProfile</span></span>
<span data-ttu-id="bdc0f-144">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bdc0f-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdc0f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdc0f-145">CommonParameters</span></span>
<span data-ttu-id="bdc0f-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bdc0f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdc0f-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdc0f-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdc0f-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bdc0f-148">INPUTS</span></span>

## <span data-ttu-id="bdc0f-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bdc0f-149">OUTPUTS</span></span>

### <span data-ttu-id="bdc0f-150">karakterlánc</span><span class="sxs-lookup"><span data-stu-id="bdc0f-150">string</span></span>
<span data-ttu-id="bdc0f-151">Az adattó áruházbeli fiók teljes elérési útja a feltöltött fájllal vagy mappával.</span><span class="sxs-lookup"><span data-stu-id="bdc0f-151">The full path in the Data Lake Store account to the uploaded file or folder.</span></span>

## <span data-ttu-id="bdc0f-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bdc0f-152">NOTES</span></span>

## <span data-ttu-id="bdc0f-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bdc0f-153">RELATED LINKS</span></span>

[<span data-ttu-id="bdc0f-154">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bdc0f-154">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="bdc0f-155">Exportálás – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bdc0f-155">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="bdc0f-156">Bekapcsolódás a AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bdc0f-156">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="bdc0f-157">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bdc0f-157">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="bdc0f-158">Új – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bdc0f-158">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="bdc0f-159">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bdc0f-159">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="bdc0f-160">Teszt-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bdc0f-160">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


