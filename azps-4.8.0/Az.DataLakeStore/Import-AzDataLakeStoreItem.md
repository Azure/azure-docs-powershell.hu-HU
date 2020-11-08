---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/import-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
ms.openlocfilehash: bdad54f8d5615fe0e8c3a1a7d75077e9e6f34f80
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184163"
---
# <span data-ttu-id="9c7cc-101">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9c7cc-101">Import-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="9c7cc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9c7cc-102">SYNOPSIS</span></span>
<span data-ttu-id="9c7cc-103">Helyi fájlt vagy könyvtárat tölt fel egy adattó-áruházba.</span><span class="sxs-lookup"><span data-stu-id="9c7cc-103">Uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="9c7cc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9c7cc-104">SYNTAX</span></span>

### <span data-ttu-id="9c7cc-105">NoDiagnosticLogging (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9c7cc-105">NoDiagnosticLogging (Default)</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c7cc-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="9c7cc-106">IncludeDiagnosticLogging</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9c7cc-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9c7cc-107">DESCRIPTION</span></span>
<span data-ttu-id="9c7cc-108">Az **import-AzDataLakeStoreItem** parancsmag egy helyi fájlt vagy könyvtárat tölt fel egy adattó-tárolóba.</span><span class="sxs-lookup"><span data-stu-id="9c7cc-108">The **Import-AzDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="9c7cc-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9c7cc-109">EXAMPLES</span></span>

### <span data-ttu-id="9c7cc-110">1. példa: fájl feltöltése</span><span class="sxs-lookup"><span data-stu-id="9c7cc-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

<span data-ttu-id="9c7cc-111">Ez a parancs feltölti a fájlt SrcFile.csv és felveszi a MyFiles-mappába az adattó-tárolóban, mint a 4 egyidejű File.csv.</span><span class="sxs-lookup"><span data-stu-id="9c7cc-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="9c7cc-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9c7cc-112">PARAMETERS</span></span>

### <span data-ttu-id="9c7cc-113">-Fiók</span><span class="sxs-lookup"><span data-stu-id="9c7cc-113">-Account</span></span>
<span data-ttu-id="9c7cc-114">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9c7cc-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="9c7cc-115">-Párhuzamosság</span><span class="sxs-lookup"><span data-stu-id="9c7cc-115">-Concurrency</span></span>
<span data-ttu-id="9c7cc-116">A párhuzamosan feltöltött fájlok vagy adatdarabok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9c7cc-116">Indicates the number of files or chunks to upload in parallel.</span></span> <span data-ttu-id="9c7cc-117">Az alapértelmezett érték a rendszerspecifikációk alapján kiszámított legjobb munkamennyiség lesz.</span><span class="sxs-lookup"><span data-stu-id="9c7cc-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="9c7cc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c7cc-118">-DefaultProfile</span></span>
<span data-ttu-id="9c7cc-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9c7cc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c7cc-120">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="9c7cc-120">-Destination</span></span>
<span data-ttu-id="9c7cc-121">Az adattó-tároló elérési útját adja meg, amelybe fájlt vagy mappát szeretne feltölteni, kezdve a root-könyvtárral (/).</span><span class="sxs-lookup"><span data-stu-id="9c7cc-121">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="9c7cc-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="9c7cc-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="9c7cc-123">Tetszés szerint azt jelzi, hogy a diagnosztikai napló szintje az események rögzítéséhez a fájl vagy a mappa importálásakor használható.</span><span class="sxs-lookup"><span data-stu-id="9c7cc-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="9c7cc-124">Az alapértelmezett érték a hiba.</span><span class="sxs-lookup"><span data-stu-id="9c7cc-124">Default is Error.</span></span>

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

### <span data-ttu-id="9c7cc-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="9c7cc-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="9c7cc-126">A diagnosztikai napló elérési útját adja meg, amely a fájlok vagy mappák importálása során eseményeket rögzít.</span><span class="sxs-lookup"><span data-stu-id="9c7cc-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="9c7cc-127">-Force</span><span class="sxs-lookup"><span data-stu-id="9c7cc-127">-Force</span></span>
<span data-ttu-id="9c7cc-128">Jelzi, hogy az adott művelet felülírja a célfájlba, ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="9c7cc-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="9c7cc-129">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="9c7cc-129">-ForceBinary</span></span>
<span data-ttu-id="9c7cc-130">Azt jelzi, hogy a másolt fájl (oka) t a program nem érinti az új, hozzáfűzéssel való megőrzést.</span><span class="sxs-lookup"><span data-stu-id="9c7cc-130">Indicates that the file(s) being copied should be copied with no concern for new line preservation across appends.</span></span>

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

### <span data-ttu-id="9c7cc-131">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="9c7cc-131">-Path</span></span>
<span data-ttu-id="9c7cc-132">A feltölteni kívánt fájl vagy mappa helyi elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9c7cc-132">Specifies the local path of the file or folder to upload.</span></span>

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

### <span data-ttu-id="9c7cc-133">-Recurse</span><span class="sxs-lookup"><span data-stu-id="9c7cc-133">-Recurse</span></span>
<span data-ttu-id="9c7cc-134">Azt jelzi, hogy ez a művelet minden almappa összes elemét feltölti.</span><span class="sxs-lookup"><span data-stu-id="9c7cc-134">Indicates that this operation should upload all items in all subfolders.</span></span>

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

### <span data-ttu-id="9c7cc-135">– Önéletrajz</span><span class="sxs-lookup"><span data-stu-id="9c7cc-135">-Resume</span></span>
<span data-ttu-id="9c7cc-136">Jelzi, hogy a másolt fájl (ok) az előző feltöltés folytatása.</span><span class="sxs-lookup"><span data-stu-id="9c7cc-136">Indicates that the file(s) being copied are a continuation of a previous upload.</span></span> <span data-ttu-id="9c7cc-137">Ennek hatására a rendszer megkísérli folytatni az utolsó olyan fájlból való visszatérést, amely nem lett teljesen feltöltve.</span><span class="sxs-lookup"><span data-stu-id="9c7cc-137">This will cause the system to attempt to resume from the last file that was not fully uploaded.</span></span>

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

### <span data-ttu-id="9c7cc-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9c7cc-138">-Confirm</span></span>
<span data-ttu-id="9c7cc-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9c7cc-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c7cc-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c7cc-140">-WhatIf</span></span>
<span data-ttu-id="9c7cc-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9c7cc-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c7cc-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9c7cc-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c7cc-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c7cc-143">CommonParameters</span></span>
<span data-ttu-id="9c7cc-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9c7cc-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c7cc-145">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c7cc-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c7cc-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c7cc-146">INPUTS</span></span>

### <span data-ttu-id="9c7cc-147">System. String</span><span class="sxs-lookup"><span data-stu-id="9c7cc-147">System.String</span></span>

### <span data-ttu-id="9c7cc-148">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="9c7cc-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="9c7cc-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9c7cc-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="9c7cc-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="9c7cc-150">System.Int32</span></span>

### <span data-ttu-id="9c7cc-151">Microsoft. Azure. Command. DataLakeStore. models. LogLevel</span><span class="sxs-lookup"><span data-stu-id="9c7cc-151">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="9c7cc-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c7cc-152">OUTPUTS</span></span>

### <span data-ttu-id="9c7cc-153">System. String</span><span class="sxs-lookup"><span data-stu-id="9c7cc-153">System.String</span></span>

## <span data-ttu-id="9c7cc-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9c7cc-154">NOTES</span></span>

## <span data-ttu-id="9c7cc-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9c7cc-155">RELATED LINKS</span></span>

[<span data-ttu-id="9c7cc-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9c7cc-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="9c7cc-157">Exportálás – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9c7cc-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="9c7cc-158">Bekapcsolódás a AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9c7cc-158">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="9c7cc-159">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9c7cc-159">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="9c7cc-160">Új – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9c7cc-160">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="9c7cc-161">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9c7cc-161">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="9c7cc-162">Teszt-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9c7cc-162">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


