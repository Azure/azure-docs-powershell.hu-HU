---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: 4ce79044793bbecc76d72fab015166ccc3d8fba6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493525"
---
# <span data-ttu-id="60a5b-101">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="60a5b-101">Add-AzureRmDataLakeStoreItemContent</span></span>

## <span data-ttu-id="60a5b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="60a5b-102">SYNOPSIS</span></span>
<span data-ttu-id="60a5b-103">Tartalmat ad az adattó-tároló elemeihez.</span><span class="sxs-lookup"><span data-stu-id="60a5b-103">Adds content to an item in a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60a5b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="60a5b-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="60a5b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="60a5b-105">DESCRIPTION</span></span>
<span data-ttu-id="60a5b-106">Az **Add-AzureRmDataLakeStoreItemContent** parancsmag tartalmakat ad az Azure Data Lake áruházban található elemekhez.</span><span class="sxs-lookup"><span data-stu-id="60a5b-106">The **Add-AzureRmDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="60a5b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="60a5b-107">EXAMPLES</span></span>

### <span data-ttu-id="60a5b-108">1. példa: tartalom hozzáadása fájlba</span><span class="sxs-lookup"><span data-stu-id="60a5b-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzureRmDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="60a5b-109">Ez a parancs tartalmat ad az myFile.txt fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="60a5b-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="60a5b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="60a5b-110">PARAMETERS</span></span>

### <span data-ttu-id="60a5b-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="60a5b-111">-Account</span></span>
<span data-ttu-id="60a5b-112">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="60a5b-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="60a5b-113">-Encoding</span><span class="sxs-lookup"><span data-stu-id="60a5b-113">-Encoding</span></span>
<span data-ttu-id="60a5b-114">A létrehozandó elem kódolását adja meg.</span><span class="sxs-lookup"><span data-stu-id="60a5b-114">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="60a5b-115">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="60a5b-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="60a5b-116">Ismeretlen</span><span class="sxs-lookup"><span data-stu-id="60a5b-116">Unknown</span></span>
- <span data-ttu-id="60a5b-117">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="60a5b-117">String</span></span>
- <span data-ttu-id="60a5b-118">Unicode</span><span class="sxs-lookup"><span data-stu-id="60a5b-118">Unicode</span></span>
- <span data-ttu-id="60a5b-119">Byte</span><span class="sxs-lookup"><span data-stu-id="60a5b-119">Byte</span></span>
- <span data-ttu-id="60a5b-120">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="60a5b-120">BigEndianUnicode</span></span>
- <span data-ttu-id="60a5b-121">UTF8</span><span class="sxs-lookup"><span data-stu-id="60a5b-121">UTF8</span></span>
- <span data-ttu-id="60a5b-122">UTF7</span><span class="sxs-lookup"><span data-stu-id="60a5b-122">UTF7</span></span>
- <span data-ttu-id="60a5b-123">ASCII</span><span class="sxs-lookup"><span data-stu-id="60a5b-123">Ascii</span></span>
- <span data-ttu-id="60a5b-124">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="60a5b-124">Default</span></span>
- <span data-ttu-id="60a5b-125">OEM</span><span class="sxs-lookup"><span data-stu-id="60a5b-125">Oem</span></span>
- <span data-ttu-id="60a5b-126">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="60a5b-126">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.PowerShell.Commands.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60a5b-127">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="60a5b-127">-Path</span></span>
<span data-ttu-id="60a5b-128">A módosítani kívánt elem az adattó-tároló elérési útját adja meg, kezdve a gyökérkönyvtárral (/).</span><span class="sxs-lookup"><span data-stu-id="60a5b-128">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="60a5b-129">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="60a5b-129">-Value</span></span>
<span data-ttu-id="60a5b-130">Az elemhez hozzáadni kívánt tartalmat adja meg.</span><span class="sxs-lookup"><span data-stu-id="60a5b-130">Specifies the content to add to the item.</span></span>

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

### <span data-ttu-id="60a5b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60a5b-131">-DefaultProfile</span></span>
<span data-ttu-id="60a5b-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="60a5b-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60a5b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60a5b-133">CommonParameters</span></span>
<span data-ttu-id="60a5b-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="60a5b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60a5b-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60a5b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60a5b-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="60a5b-136">INPUTS</span></span>

### <span data-ttu-id="60a5b-137">Objektum</span><span class="sxs-lookup"><span data-stu-id="60a5b-137">Object</span></span>
<span data-ttu-id="60a5b-138">Az ' érték ' paraméter elfogadja az "objektum" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="60a5b-138">Parameter 'Value' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="60a5b-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="60a5b-139">OUTPUTS</span></span>

### <span data-ttu-id="60a5b-140">bool</span><span class="sxs-lookup"><span data-stu-id="60a5b-140">bool</span></span>
<span data-ttu-id="60a5b-141">Siker esetén a True értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="60a5b-141">Returns true on success.</span></span>

## <span data-ttu-id="60a5b-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="60a5b-142">NOTES</span></span>

## <span data-ttu-id="60a5b-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="60a5b-143">RELATED LINKS</span></span>

[<span data-ttu-id="60a5b-144">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="60a5b-144">Get-AzureRmDataLakeStoreItemContent</span></span>](./Get-AzureRmDataLakeStoreItemContent.md)


