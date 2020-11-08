---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
ms.openlocfilehash: 3cf411e75e2a3ec430f13354015d5b6e271c840c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010521"
---
# <span data-ttu-id="d7066-101">Add-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="d7066-101">Add-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="d7066-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d7066-102">SYNOPSIS</span></span>
<span data-ttu-id="d7066-103">Tartalmat ad az adattó-tároló elemeihez.</span><span class="sxs-lookup"><span data-stu-id="d7066-103">Adds content to an item in a Data Lake Store.</span></span>

## <span data-ttu-id="d7066-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d7066-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7066-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d7066-105">DESCRIPTION</span></span>
<span data-ttu-id="d7066-106">Az **Add-AzDataLakeStoreItemContent** parancsmag tartalmakat ad az Azure Data Lake áruházban található elemekhez.</span><span class="sxs-lookup"><span data-stu-id="d7066-106">The **Add-AzDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="d7066-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d7066-107">EXAMPLES</span></span>

### <span data-ttu-id="d7066-108">1. példa: tartalom hozzáadása fájlba</span><span class="sxs-lookup"><span data-stu-id="d7066-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="d7066-109">Ez a parancs tartalmat ad az myFile.txt fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="d7066-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="d7066-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d7066-110">PARAMETERS</span></span>

### <span data-ttu-id="d7066-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="d7066-111">-Account</span></span>
<span data-ttu-id="d7066-112">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7066-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="d7066-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7066-113">-DefaultProfile</span></span>
<span data-ttu-id="d7066-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d7066-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7066-115">-Encoding</span><span class="sxs-lookup"><span data-stu-id="d7066-115">-Encoding</span></span>
<span data-ttu-id="d7066-116">A létrehozandó elem kódolását adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7066-116">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="d7066-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d7066-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d7066-118">Ismeretlen</span><span class="sxs-lookup"><span data-stu-id="d7066-118">Unknown</span></span>
- <span data-ttu-id="d7066-119">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="d7066-119">String</span></span>
- <span data-ttu-id="d7066-120">Unicode</span><span class="sxs-lookup"><span data-stu-id="d7066-120">Unicode</span></span>
- <span data-ttu-id="d7066-121">Byte</span><span class="sxs-lookup"><span data-stu-id="d7066-121">Byte</span></span>
- <span data-ttu-id="d7066-122">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="d7066-122">BigEndianUnicode</span></span>
- <span data-ttu-id="d7066-123">UTF8</span><span class="sxs-lookup"><span data-stu-id="d7066-123">UTF8</span></span>
- <span data-ttu-id="d7066-124">UTF7</span><span class="sxs-lookup"><span data-stu-id="d7066-124">UTF7</span></span>
- <span data-ttu-id="d7066-125">ASCII</span><span class="sxs-lookup"><span data-stu-id="d7066-125">Ascii</span></span>
- <span data-ttu-id="d7066-126">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="d7066-126">Default</span></span>
- <span data-ttu-id="d7066-127">OEM</span><span class="sxs-lookup"><span data-stu-id="d7066-127">Oem</span></span>
- <span data-ttu-id="d7066-128">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="d7066-128">BigEndianUTF32</span></span>

```yaml
Type: System.Text.Encoding
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7066-129">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="d7066-129">-Path</span></span>
<span data-ttu-id="d7066-130">A módosítani kívánt elem az adattó-tároló elérési útját adja meg, kezdve a gyökérkönyvtárral (/).</span><span class="sxs-lookup"><span data-stu-id="d7066-130">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="d7066-131">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="d7066-131">-Value</span></span>
<span data-ttu-id="d7066-132">Az elemhez hozzáadni kívánt tartalmat adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7066-132">Specifies the content to add to the item.</span></span>

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

### <span data-ttu-id="d7066-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7066-133">CommonParameters</span></span>
<span data-ttu-id="d7066-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d7066-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7066-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7066-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7066-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7066-136">INPUTS</span></span>

### <span data-ttu-id="d7066-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d7066-137">System.String</span></span>

### <span data-ttu-id="d7066-138">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="d7066-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="d7066-139">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="d7066-139">System.Object</span></span>

### <span data-ttu-id="d7066-140">System. Text. Encoding</span><span class="sxs-lookup"><span data-stu-id="d7066-140">System.Text.Encoding</span></span>

## <span data-ttu-id="d7066-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7066-141">OUTPUTS</span></span>

### <span data-ttu-id="d7066-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d7066-142">System.Boolean</span></span>

## <span data-ttu-id="d7066-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d7066-143">NOTES</span></span>

## <span data-ttu-id="d7066-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7066-144">RELATED LINKS</span></span>

[<span data-ttu-id="d7066-145">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="d7066-145">Get-AzDataLakeStoreItemContent</span></span>](./Get-AzDataLakeStoreItemContent.md)


