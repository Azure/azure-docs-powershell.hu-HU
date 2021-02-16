---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 15DFF66F-3D78-422B-BA40-71058DE66BA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemContent.md
ms.openlocfilehash: e5aaff4f915143e2e7695c9f650aed6fb01ba389
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163802"
---
# <span data-ttu-id="4efc6-101">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="4efc6-101">Get-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="4efc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4efc6-102">SYNOPSIS</span></span>
<span data-ttu-id="4efc6-103">A Data Lake Store-ban tárolt fájl tartalmának be- és lekérte.</span><span class="sxs-lookup"><span data-stu-id="4efc6-103">Gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="4efc6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4efc6-104">SYNTAX</span></span>

### <span data-ttu-id="4efc6-105">PreviewFileContent (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4efc6-105">PreviewFileContent (Default)</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Offset] <Int64>]
 [[-Length] <Int64>] [[-Encoding] <Encoding>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4efc6-106">PreviewFileRowsFromHead</span><span class="sxs-lookup"><span data-stu-id="4efc6-106">PreviewFileRowsFromHead</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Head] <Int32>]
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4efc6-107">PreviewFileRowsFromTail</span><span class="sxs-lookup"><span data-stu-id="4efc6-107">PreviewFileRowsFromTail</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Tail] <Int32>]
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4efc6-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4efc6-108">DESCRIPTION</span></span>
<span data-ttu-id="4efc6-109">A **Get-AzDataLakeStoreItemContent** parancsmag egy fájl tartalmát a Data Lake Store-ban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4efc6-109">The **Get-AzDataLakeStoreItemContent** cmdlet gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="4efc6-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4efc6-110">EXAMPLES</span></span>

### <span data-ttu-id="4efc6-111">1. példa: Fájl tartalmának lekérte</span><span class="sxs-lookup"><span data-stu-id="4efc6-111">Example 1: Get the contents of a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt"
```

<span data-ttu-id="4efc6-112">Ez a parancs begyakorlja a fájl tartalmát MyFile.txt ContosoADL-fiókban.</span><span class="sxs-lookup"><span data-stu-id="4efc6-112">This command gets the contents of the file MyFile.txt in the ContosoADL account.</span></span>

### <span data-ttu-id="4efc6-113">2. példa: Fájl első két sorának be szereznie</span><span class="sxs-lookup"><span data-stu-id="4efc6-113">Example 2: Get the first two rows of a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt" -Head 2
```

<span data-ttu-id="4efc6-114">Ez a parancs a fájl első két új sorát választja el, MyFile.txt ContosoADL-fiókban.</span><span class="sxs-lookup"><span data-stu-id="4efc6-114">This command gets the first two new line separated rows in the file MyFile.txt in the ContosoADL account.</span></span>

## <span data-ttu-id="4efc6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4efc6-115">PARAMETERS</span></span>

### <span data-ttu-id="4efc6-116">-Account</span><span class="sxs-lookup"><span data-stu-id="4efc6-116">-Account</span></span>
<span data-ttu-id="4efc6-117">Az Adattavatár-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4efc6-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="4efc6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4efc6-118">-DefaultProfile</span></span>
<span data-ttu-id="4efc6-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4efc6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4efc6-120">-Kódolás</span><span class="sxs-lookup"><span data-stu-id="4efc6-120">-Encoding</span></span>
<span data-ttu-id="4efc6-121">A létrehozni kívánt elem kódolását határozza meg.</span><span class="sxs-lookup"><span data-stu-id="4efc6-121">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="4efc6-122">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="4efc6-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4efc6-123">Ismeretlen</span><span class="sxs-lookup"><span data-stu-id="4efc6-123">Unknown</span></span>
- <span data-ttu-id="4efc6-124">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="4efc6-124">String</span></span>
- <span data-ttu-id="4efc6-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="4efc6-125">Unicode</span></span>
- <span data-ttu-id="4efc6-126">Bájt</span><span class="sxs-lookup"><span data-stu-id="4efc6-126">Byte</span></span>
- <span data-ttu-id="4efc6-127">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="4efc6-127">BigEndianUnicode</span></span>
- <span data-ttu-id="4efc6-128">UTF8</span><span class="sxs-lookup"><span data-stu-id="4efc6-128">UTF8</span></span>
- <span data-ttu-id="4efc6-129">UTF7</span><span class="sxs-lookup"><span data-stu-id="4efc6-129">UTF7</span></span>
- <span data-ttu-id="4efc6-130">Ascii</span><span class="sxs-lookup"><span data-stu-id="4efc6-130">Ascii</span></span>
- <span data-ttu-id="4efc6-131">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="4efc6-131">Default</span></span>
- <span data-ttu-id="4efc6-132">Oem</span><span class="sxs-lookup"><span data-stu-id="4efc6-132">Oem</span></span>
- <span data-ttu-id="4efc6-133">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="4efc6-133">BigEndianUTF32</span></span>

```yaml
Type: System.Text.Encoding
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4efc6-134">-Force</span><span class="sxs-lookup"><span data-stu-id="4efc6-134">-Force</span></span>
<span data-ttu-id="4efc6-135">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="4efc6-135">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PreviewFileContent
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4efc6-136">-Head</span><span class="sxs-lookup"><span data-stu-id="4efc6-136">-Head</span></span>
<span data-ttu-id="4efc6-137">A fájl elejétől az előnézetig (új sorokkal tagolt) sorok száma.</span><span class="sxs-lookup"><span data-stu-id="4efc6-137">The number of rows (new line delimited) from the beginning of the file to preview.</span></span> <span data-ttu-id="4efc6-138">Ha az adatok első 4 MB-ában nem történik új sor, a visszaadott érték csak az adott adatot fogja visszaadni.</span><span class="sxs-lookup"><span data-stu-id="4efc6-138">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: PreviewFileRowsFromHead
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4efc6-139">-Length</span><span class="sxs-lookup"><span data-stu-id="4efc6-139">-Length</span></span>
<span data-ttu-id="4efc6-140">A behozni megfelelő tartalom hossza bájtban.</span><span class="sxs-lookup"><span data-stu-id="4efc6-140">Specifies the length, in bytes, of the content to get.</span></span>

```yaml
Type: System.Int64
Parameter Sets: PreviewFileContent
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4efc6-141">-Eltolás</span><span class="sxs-lookup"><span data-stu-id="4efc6-141">-Offset</span></span>
<span data-ttu-id="4efc6-142">Azt adja meg, hogy hány bájtot kell kihagyni egy fájlba a tartalom beszerzése előtt.</span><span class="sxs-lookup"><span data-stu-id="4efc6-142">Specifies the number of bytes to skip in a file before getting content.</span></span>

```yaml
Type: System.Int64
Parameter Sets: PreviewFileContent
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4efc6-143">-Path</span><span class="sxs-lookup"><span data-stu-id="4efc6-143">-Path</span></span>
<span data-ttu-id="4efc6-144">Egy fájl Data Lake Store-beli elérési útját adja meg a gyökérkönyvtártól (/).</span><span class="sxs-lookup"><span data-stu-id="4efc6-144">Specifies the Data Lake Store path of a file, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="4efc6-145">-Tail</span><span class="sxs-lookup"><span data-stu-id="4efc6-145">-Tail</span></span>
<span data-ttu-id="4efc6-146">A fájl végtől az előnézetig (új sorokkal tagolt) sorok száma.</span><span class="sxs-lookup"><span data-stu-id="4efc6-146">The number of rows (new line delimited) from the end of the file to preview.</span></span> <span data-ttu-id="4efc6-147">Ha az adatok első 4 MB-ában nem történik új sor, a visszaadott érték csak az adott adatot fogja visszaadni.</span><span class="sxs-lookup"><span data-stu-id="4efc6-147">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: PreviewFileRowsFromTail
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4efc6-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4efc6-148">-Confirm</span></span>
<span data-ttu-id="4efc6-149">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4efc6-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4efc6-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4efc6-150">-WhatIf</span></span>
<span data-ttu-id="4efc6-151">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4efc6-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4efc6-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4efc6-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4efc6-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4efc6-153">CommonParameters</span></span>
<span data-ttu-id="4efc6-154">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4efc6-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4efc6-155">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4efc6-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4efc6-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4efc6-156">INPUTS</span></span>

### <span data-ttu-id="4efc6-157">System.String</span><span class="sxs-lookup"><span data-stu-id="4efc6-157">System.String</span></span>

### <span data-ttu-id="4efc6-158">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="4efc6-158">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="4efc6-159">System.Int32</span><span class="sxs-lookup"><span data-stu-id="4efc6-159">System.Int32</span></span>

### <span data-ttu-id="4efc6-160">System.Int64</span><span class="sxs-lookup"><span data-stu-id="4efc6-160">System.Int64</span></span>

### <span data-ttu-id="4efc6-161">System.Text.Encoding</span><span class="sxs-lookup"><span data-stu-id="4efc6-161">System.Text.Encoding</span></span>

### <span data-ttu-id="4efc6-162">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4efc6-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4efc6-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4efc6-163">OUTPUTS</span></span>

### <span data-ttu-id="4efc6-164">System.Byte</span><span class="sxs-lookup"><span data-stu-id="4efc6-164">System.Byte</span></span>

### <span data-ttu-id="4efc6-165">System.String</span><span class="sxs-lookup"><span data-stu-id="4efc6-165">System.String</span></span>

## <span data-ttu-id="4efc6-166">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4efc6-166">NOTES</span></span>

## <span data-ttu-id="4efc6-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4efc6-167">RELATED LINKS</span></span>
