---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/import-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
ms.openlocfilehash: bdad54f8d5615fe0e8c3a1a7d75077e9e6f34f80
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357670"
---
# <span data-ttu-id="37567-101">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="37567-101">Import-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="37567-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37567-102">SYNOPSIS</span></span>
<span data-ttu-id="37567-103">Feltölt egy helyi fájlt vagy címtárat egy Data Lake Store-beli tárolóba.</span><span class="sxs-lookup"><span data-stu-id="37567-103">Uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="37567-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="37567-104">SYNTAX</span></span>

### <span data-ttu-id="37567-105">NoDiagnosticLogging (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="37567-105">NoDiagnosticLogging (Default)</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37567-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="37567-106">IncludeDiagnosticLogging</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="37567-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="37567-107">DESCRIPTION</span></span>
<span data-ttu-id="37567-108">Az **Import-AzDataLakeStoreItem** parancsmag feltölt egy helyi fájlt vagy címtárat a Data Lake Store-ból.</span><span class="sxs-lookup"><span data-stu-id="37567-108">The **Import-AzDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="37567-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="37567-109">EXAMPLES</span></span>

### <span data-ttu-id="37567-110">1. példa: Fájl feltöltése</span><span class="sxs-lookup"><span data-stu-id="37567-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

<span data-ttu-id="37567-111">Ez a parancs feltölti SrcFile.csv fájlt, és hozzáadja a Data Lake Store MyFiles mappájába, File.csv 4-es egyidejűség mellett.</span><span class="sxs-lookup"><span data-stu-id="37567-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="37567-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37567-112">PARAMETERS</span></span>

### <span data-ttu-id="37567-113">-Account</span><span class="sxs-lookup"><span data-stu-id="37567-113">-Account</span></span>
<span data-ttu-id="37567-114">A Data Lake Store-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="37567-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="37567-115">-Egyidejűség</span><span class="sxs-lookup"><span data-stu-id="37567-115">-Concurrency</span></span>
<span data-ttu-id="37567-116">A párhuzamos feltöltéshez szükséges fájlok vagy adattömbök számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="37567-116">Indicates the number of files or chunks to upload in parallel.</span></span> <span data-ttu-id="37567-117">Az alapértelmezett érték a rendszer specifikációi alapján számítható legjobb munkamennyiségnek.</span><span class="sxs-lookup"><span data-stu-id="37567-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="37567-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37567-118">-DefaultProfile</span></span>
<span data-ttu-id="37567-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="37567-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37567-120">-Destination</span><span class="sxs-lookup"><span data-stu-id="37567-120">-Destination</span></span>
<span data-ttu-id="37567-121">Megadja azt a Data Lake Store-beli elérési utat, amelybe fel kell töltenie egy fájlt vagy mappát, a gyökérkönyvtártól (/).</span><span class="sxs-lookup"><span data-stu-id="37567-121">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="37567-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="37567-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="37567-123">Ha szükséges, azt a diagnosztikai naplószintet adja meg, amely a fájl vagy mappa importálása során az események rögzítésére használható.</span><span class="sxs-lookup"><span data-stu-id="37567-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="37567-124">Az alapértelmezett érték a Hiba.</span><span class="sxs-lookup"><span data-stu-id="37567-124">Default is Error.</span></span>

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

### <span data-ttu-id="37567-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="37567-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="37567-126">Megadja a diagnosztikai naplónak azt az elérési útját, amelybe a fájl vagy mappa importálása közbeni eseményeket rögzíteni kell.</span><span class="sxs-lookup"><span data-stu-id="37567-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="37567-127">-Force</span><span class="sxs-lookup"><span data-stu-id="37567-127">-Force</span></span>
<span data-ttu-id="37567-128">Azt jelzi, hogy ez a művelet felülírhatja a célfájlt, ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="37567-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="37567-129">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="37567-129">-ForceBinary</span></span>
<span data-ttu-id="37567-130">Azt jelzi, hogy a másolt fájlokat úgy kell másolni, hogy ne okoz gondot az új sorok megőrzése a hozzáfűzésben.</span><span class="sxs-lookup"><span data-stu-id="37567-130">Indicates that the file(s) being copied should be copied with no concern for new line preservation across appends.</span></span>

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

### <span data-ttu-id="37567-131">-Path</span><span class="sxs-lookup"><span data-stu-id="37567-131">-Path</span></span>
<span data-ttu-id="37567-132">A feltölteni kívánt fájl vagy mappa helyi elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="37567-132">Specifies the local path of the file or folder to upload.</span></span>

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

### <span data-ttu-id="37567-133">-Recurse</span><span class="sxs-lookup"><span data-stu-id="37567-133">-Recurse</span></span>
<span data-ttu-id="37567-134">Azt jelzi, hogy a műveletnek az összes almappában fel kell töltenie az összes elemet.</span><span class="sxs-lookup"><span data-stu-id="37567-134">Indicates that this operation should upload all items in all subfolders.</span></span>

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

### <span data-ttu-id="37567-135">-Resume</span><span class="sxs-lookup"><span data-stu-id="37567-135">-Resume</span></span>
<span data-ttu-id="37567-136">Azt jelzi, hogy a másolt fájlok egy korábbi feltöltés folytatásai.</span><span class="sxs-lookup"><span data-stu-id="37567-136">Indicates that the file(s) being copied are a continuation of a previous upload.</span></span> <span data-ttu-id="37567-137">Ennek hatására a rendszer az utolsó olyan fájlból próbál meg folytatódni, amely még nem lett teljesen feltöltve.</span><span class="sxs-lookup"><span data-stu-id="37567-137">This will cause the system to attempt to resume from the last file that was not fully uploaded.</span></span>

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

### <span data-ttu-id="37567-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37567-138">-Confirm</span></span>
<span data-ttu-id="37567-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="37567-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37567-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37567-140">-WhatIf</span></span>
<span data-ttu-id="37567-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="37567-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37567-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="37567-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37567-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37567-143">CommonParameters</span></span>
<span data-ttu-id="37567-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37567-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37567-145">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37567-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37567-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="37567-146">INPUTS</span></span>

### <span data-ttu-id="37567-147">System.String</span><span class="sxs-lookup"><span data-stu-id="37567-147">System.String</span></span>

### <span data-ttu-id="37567-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="37567-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="37567-149">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="37567-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="37567-150">System.Int32</span><span class="sxs-lookup"><span data-stu-id="37567-150">System.Int32</span></span>

### <span data-ttu-id="37567-151">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span><span class="sxs-lookup"><span data-stu-id="37567-151">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="37567-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="37567-152">OUTPUTS</span></span>

### <span data-ttu-id="37567-153">System.String</span><span class="sxs-lookup"><span data-stu-id="37567-153">System.String</span></span>

## <span data-ttu-id="37567-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="37567-154">NOTES</span></span>

## <span data-ttu-id="37567-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="37567-155">RELATED LINKS</span></span>

[<span data-ttu-id="37567-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="37567-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="37567-157">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="37567-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="37567-158">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="37567-158">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="37567-159">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="37567-159">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="37567-160">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="37567-160">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="37567-161">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="37567-161">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="37567-162">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="37567-162">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


