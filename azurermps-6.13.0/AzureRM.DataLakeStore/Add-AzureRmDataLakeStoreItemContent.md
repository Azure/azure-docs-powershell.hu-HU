---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/add-azurermdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: ed931444940b86c04e027eb88da9266c7af20206
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499580"
---
# <span data-ttu-id="fb4e3-101">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="fb4e3-101">Add-AzureRmDataLakeStoreItemContent</span></span>

## <span data-ttu-id="fb4e3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb4e3-102">SYNOPSIS</span></span>
<span data-ttu-id="fb4e3-103">Tartalmat ad az adattó-tároló elemeihez.</span><span class="sxs-lookup"><span data-stu-id="fb4e3-103">Adds content to an item in a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb4e3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb4e3-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb4e3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb4e3-105">DESCRIPTION</span></span>
<span data-ttu-id="fb4e3-106">Az **Add-AzureRmDataLakeStoreItemContent** parancsmag tartalmakat ad az Azure Data Lake áruházban található elemekhez.</span><span class="sxs-lookup"><span data-stu-id="fb4e3-106">The **Add-AzureRmDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="fb4e3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fb4e3-107">EXAMPLES</span></span>

### <span data-ttu-id="fb4e3-108">1. példa: tartalom hozzáadása fájlba</span><span class="sxs-lookup"><span data-stu-id="fb4e3-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzureRmDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="fb4e3-109">Ez a parancs tartalmat ad az myFile.txt fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="fb4e3-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="fb4e3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb4e3-110">PARAMETERS</span></span>

### <span data-ttu-id="fb4e3-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="fb4e3-111">-Account</span></span>
<span data-ttu-id="fb4e3-112">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb4e3-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="fb4e3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb4e3-113">-DefaultProfile</span></span>
<span data-ttu-id="fb4e3-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fb4e3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb4e3-115">-Encoding</span><span class="sxs-lookup"><span data-stu-id="fb4e3-115">-Encoding</span></span>
<span data-ttu-id="fb4e3-116">A létrehozandó elem kódolását adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb4e3-116">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="fb4e3-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="fb4e3-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fb4e3-118">Ismeretlen</span><span class="sxs-lookup"><span data-stu-id="fb4e3-118">Unknown</span></span>
- <span data-ttu-id="fb4e3-119">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="fb4e3-119">String</span></span>
- <span data-ttu-id="fb4e3-120">Unicode</span><span class="sxs-lookup"><span data-stu-id="fb4e3-120">Unicode</span></span>
- <span data-ttu-id="fb4e3-121">Byte</span><span class="sxs-lookup"><span data-stu-id="fb4e3-121">Byte</span></span>
- <span data-ttu-id="fb4e3-122">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="fb4e3-122">BigEndianUnicode</span></span>
- <span data-ttu-id="fb4e3-123">UTF8</span><span class="sxs-lookup"><span data-stu-id="fb4e3-123">UTF8</span></span>
- <span data-ttu-id="fb4e3-124">UTF7</span><span class="sxs-lookup"><span data-stu-id="fb4e3-124">UTF7</span></span>
- <span data-ttu-id="fb4e3-125">ASCII</span><span class="sxs-lookup"><span data-stu-id="fb4e3-125">Ascii</span></span>
- <span data-ttu-id="fb4e3-126">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="fb4e3-126">Default</span></span>
- <span data-ttu-id="fb4e3-127">OEM</span><span class="sxs-lookup"><span data-stu-id="fb4e3-127">Oem</span></span>
- <span data-ttu-id="fb4e3-128">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="fb4e3-128">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb4e3-129">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="fb4e3-129">-Path</span></span>
<span data-ttu-id="fb4e3-130">A módosítani kívánt elem az adattó-tároló elérési útját adja meg, kezdve a gyökérkönyvtárral (/).</span><span class="sxs-lookup"><span data-stu-id="fb4e3-130">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="fb4e3-131">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="fb4e3-131">-Value</span></span>
<span data-ttu-id="fb4e3-132">Az elemhez hozzáadni kívánt tartalmat adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb4e3-132">Specifies the content to add to the item.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb4e3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb4e3-133">CommonParameters</span></span>
<span data-ttu-id="fb4e3-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb4e3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb4e3-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb4e3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb4e3-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb4e3-136">INPUTS</span></span>

### <span data-ttu-id="fb4e3-137">System. String</span><span class="sxs-lookup"><span data-stu-id="fb4e3-137">System.String</span></span>

### <span data-ttu-id="fb4e3-138">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="fb4e3-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="fb4e3-139">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="fb4e3-139">System.Object</span></span>

### <span data-ttu-id="fb4e3-140">Microsoft. Azure. Command. DataLakeStore. models. FileSystemCmdletProviderEncoding</span><span class="sxs-lookup"><span data-stu-id="fb4e3-140">Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding</span></span>

## <span data-ttu-id="fb4e3-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb4e3-141">OUTPUTS</span></span>

### <span data-ttu-id="fb4e3-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fb4e3-142">System.Boolean</span></span>

## <span data-ttu-id="fb4e3-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb4e3-143">NOTES</span></span>

## <span data-ttu-id="fb4e3-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb4e3-144">RELATED LINKS</span></span>

[<span data-ttu-id="fb4e3-145">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="fb4e3-145">Get-AzureRmDataLakeStoreItemContent</span></span>](./Get-AzureRmDataLakeStoreItemContent.md)


