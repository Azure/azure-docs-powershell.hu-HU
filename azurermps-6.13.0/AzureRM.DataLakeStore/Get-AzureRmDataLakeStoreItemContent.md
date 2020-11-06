---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 15DFF66F-3D78-422B-BA40-71058DE66BA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: 7a757ca4b310176a71a7b2fe7e5c301137998ff9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502956"
---
# <span data-ttu-id="1161c-101">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="1161c-101">Get-AzureRmDataLakeStoreItemContent</span></span>

## <span data-ttu-id="1161c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1161c-102">SYNOPSIS</span></span>
<span data-ttu-id="1161c-103">A fájl tartalmának beolvasása az adattó áruházban.</span><span class="sxs-lookup"><span data-stu-id="1161c-103">Gets the contents of a file in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1161c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1161c-104">SYNTAX</span></span>

### <span data-ttu-id="1161c-105">PreviewFileContent (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1161c-105">PreviewFileContent (Default)</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Offset] <Int64>]
 [[-Length] <Int64>] [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1161c-106">PreviewFileRowsFromHead</span><span class="sxs-lookup"><span data-stu-id="1161c-106">PreviewFileRowsFromHead</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Head] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1161c-107">PreviewFileRowsFromTail</span><span class="sxs-lookup"><span data-stu-id="1161c-107">PreviewFileRowsFromTail</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Tail] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1161c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1161c-108">DESCRIPTION</span></span>
<span data-ttu-id="1161c-109">A **Get-AzureRmDataLakeStoreItemContent** parancsmag a fájl tartalmát az Adattó áruházban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1161c-109">The **Get-AzureRmDataLakeStoreItemContent** cmdlet gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="1161c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1161c-110">EXAMPLES</span></span>

### <span data-ttu-id="1161c-111">1. példa: fájl tartalmának beolvasása</span><span class="sxs-lookup"><span data-stu-id="1161c-111">Example 1: Get the contents of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt"
```

<span data-ttu-id="1161c-112">Ez a parancs beolvassa a fájl tartalmát MyFile.txt a ContosoADL-fiókba.</span><span class="sxs-lookup"><span data-stu-id="1161c-112">This command gets the contents of the file MyFile.txt in the ContosoADL account.</span></span>

### <span data-ttu-id="1161c-113">2. példa: a fájl első két sorának beolvasása</span><span class="sxs-lookup"><span data-stu-id="1161c-113">Example 2: Get the first two rows of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt" -Head 2
```

<span data-ttu-id="1161c-114">Ez a parancs a ContosoADL-fiókban lévő fájl MyFile.txt az első két új sort elválasztó sort kapja.</span><span class="sxs-lookup"><span data-stu-id="1161c-114">This command gets the first two new line separated rows in the file MyFile.txt in the ContosoADL account.</span></span>

## <span data-ttu-id="1161c-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1161c-115">PARAMETERS</span></span>

### <span data-ttu-id="1161c-116">-Fiók</span><span class="sxs-lookup"><span data-stu-id="1161c-116">-Account</span></span>
<span data-ttu-id="1161c-117">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1161c-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="1161c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1161c-118">-DefaultProfile</span></span>
<span data-ttu-id="1161c-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1161c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1161c-120">-Encoding</span><span class="sxs-lookup"><span data-stu-id="1161c-120">-Encoding</span></span>
<span data-ttu-id="1161c-121">A létrehozandó elem kódolását adja meg.</span><span class="sxs-lookup"><span data-stu-id="1161c-121">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="1161c-122">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="1161c-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1161c-123">Ismeretlen</span><span class="sxs-lookup"><span data-stu-id="1161c-123">Unknown</span></span>
- <span data-ttu-id="1161c-124">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="1161c-124">String</span></span>
- <span data-ttu-id="1161c-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="1161c-125">Unicode</span></span>
- <span data-ttu-id="1161c-126">Byte</span><span class="sxs-lookup"><span data-stu-id="1161c-126">Byte</span></span>
- <span data-ttu-id="1161c-127">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="1161c-127">BigEndianUnicode</span></span>
- <span data-ttu-id="1161c-128">UTF8</span><span class="sxs-lookup"><span data-stu-id="1161c-128">UTF8</span></span>
- <span data-ttu-id="1161c-129">UTF7</span><span class="sxs-lookup"><span data-stu-id="1161c-129">UTF7</span></span>
- <span data-ttu-id="1161c-130">ASCII</span><span class="sxs-lookup"><span data-stu-id="1161c-130">Ascii</span></span>
- <span data-ttu-id="1161c-131">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="1161c-131">Default</span></span>
- <span data-ttu-id="1161c-132">OEM</span><span class="sxs-lookup"><span data-stu-id="1161c-132">Oem</span></span>
- <span data-ttu-id="1161c-133">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="1161c-133">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1161c-134">-Force</span><span class="sxs-lookup"><span data-stu-id="1161c-134">-Force</span></span>
<span data-ttu-id="1161c-135">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="1161c-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1161c-136">-Head (Head)</span><span class="sxs-lookup"><span data-stu-id="1161c-136">-Head</span></span>
<span data-ttu-id="1161c-137">Az előnézethez a fájl elejétől számított sorok száma (új sor tagolt).</span><span class="sxs-lookup"><span data-stu-id="1161c-137">The number of rows (new line delimited) from the beginning of the file to preview.</span></span> <span data-ttu-id="1161c-138">Ha a program nem észlelt új sort az első 4MB, akkor csak az adat lesz visszaadott adat.</span><span class="sxs-lookup"><span data-stu-id="1161c-138">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

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

### <span data-ttu-id="1161c-139">-Hosszúság</span><span class="sxs-lookup"><span data-stu-id="1161c-139">-Length</span></span>
<span data-ttu-id="1161c-140">A beolvasott tartalom hosszát adja meg bájtban.</span><span class="sxs-lookup"><span data-stu-id="1161c-140">Specifies the length, in bytes, of the content to get.</span></span>

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

### <span data-ttu-id="1161c-141">-Eltolás</span><span class="sxs-lookup"><span data-stu-id="1161c-141">-Offset</span></span>
<span data-ttu-id="1161c-142">Azt adja meg, hogy hány bájtot szeretne kihagyni egy fájlban a tartalom beszerzése előtt.</span><span class="sxs-lookup"><span data-stu-id="1161c-142">Specifies the number of bytes to skip in a file before getting content.</span></span>

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

### <span data-ttu-id="1161c-143">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="1161c-143">-Path</span></span>
<span data-ttu-id="1161c-144">Az adattó-tároló elérési útját adja meg a gyökérkönyvtártól (/) kezdve.</span><span class="sxs-lookup"><span data-stu-id="1161c-144">Specifies the Data Lake Store path of a file, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="1161c-145">-Farok</span><span class="sxs-lookup"><span data-stu-id="1161c-145">-Tail</span></span>
<span data-ttu-id="1161c-146">A fájl végéről az előnézethez tartozó sorok száma (az új sor tagolt).</span><span class="sxs-lookup"><span data-stu-id="1161c-146">The number of rows (new line delimited) from the end of the file to preview.</span></span> <span data-ttu-id="1161c-147">Ha a program nem észlelt új sort az első 4MB, akkor csak az adat lesz visszaadott adat.</span><span class="sxs-lookup"><span data-stu-id="1161c-147">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

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

### <span data-ttu-id="1161c-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1161c-148">-Confirm</span></span>
<span data-ttu-id="1161c-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1161c-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1161c-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1161c-150">-WhatIf</span></span>
<span data-ttu-id="1161c-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1161c-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1161c-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1161c-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1161c-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1161c-153">CommonParameters</span></span>
<span data-ttu-id="1161c-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1161c-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1161c-155">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1161c-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1161c-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1161c-156">INPUTS</span></span>

### <span data-ttu-id="1161c-157">System. String</span><span class="sxs-lookup"><span data-stu-id="1161c-157">System.String</span></span>

### <span data-ttu-id="1161c-158">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="1161c-158">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="1161c-159">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1161c-159">System.Int32</span></span>

### <span data-ttu-id="1161c-160">System. Int64</span><span class="sxs-lookup"><span data-stu-id="1161c-160">System.Int64</span></span>

### <span data-ttu-id="1161c-161">Microsoft. Azure. Command. DataLakeStore. models. FileSystemCmdletProviderEncoding</span><span class="sxs-lookup"><span data-stu-id="1161c-161">Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding</span></span>

### <span data-ttu-id="1161c-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1161c-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1161c-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1161c-163">OUTPUTS</span></span>

### <span data-ttu-id="1161c-164">System. byte</span><span class="sxs-lookup"><span data-stu-id="1161c-164">System.Byte</span></span>
<span data-ttu-id="1161c-165">A lekérdezett fájl tartalmát tartalmazó adatfolyamot ábrázoló bájtos adatfolyam.</span><span class="sxs-lookup"><span data-stu-id="1161c-165">The byte stream representation of the file contents retrieved.</span></span>

### <span data-ttu-id="1161c-166">System. String</span><span class="sxs-lookup"><span data-stu-id="1161c-166">System.String</span></span>
<span data-ttu-id="1161c-167">A beolvasott fájl tartalma (a megadott kódolásban) karakterlánc-ábrázolása.</span><span class="sxs-lookup"><span data-stu-id="1161c-167">The string representation (in the specified encoding) of the file contents retrieved.</span></span>

## <span data-ttu-id="1161c-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1161c-168">NOTES</span></span>

## <span data-ttu-id="1161c-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1161c-169">RELATED LINKS</span></span>