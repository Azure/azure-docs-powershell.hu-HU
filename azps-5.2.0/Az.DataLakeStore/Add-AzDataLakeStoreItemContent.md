---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
ms.openlocfilehash: 3cf411e75e2a3ec430f13354015d5b6e271c840c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339557"
---
# <span data-ttu-id="25aef-101">Add-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="25aef-101">Add-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="25aef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25aef-102">SYNOPSIS</span></span>
<span data-ttu-id="25aef-103">Tartalmat ad hozzá egy adattavatárban található elemhez.</span><span class="sxs-lookup"><span data-stu-id="25aef-103">Adds content to an item in a Data Lake Store.</span></span>

## <span data-ttu-id="25aef-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="25aef-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25aef-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="25aef-105">DESCRIPTION</span></span>
<span data-ttu-id="25aef-106">Az **Add-AzDataLakeStoreItemContent** parancsmag tartalmat ad hozzá egy Azure Data Lake Store-beli elemhez.</span><span class="sxs-lookup"><span data-stu-id="25aef-106">The **Add-AzDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="25aef-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="25aef-107">EXAMPLES</span></span>

### <span data-ttu-id="25aef-108">1. példa: Tartalom hozzáadása fájlhoz</span><span class="sxs-lookup"><span data-stu-id="25aef-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="25aef-109">Ez a parancs tartalmat ad a fájlhoz myFile.txt.</span><span class="sxs-lookup"><span data-stu-id="25aef-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="25aef-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25aef-110">PARAMETERS</span></span>

### <span data-ttu-id="25aef-111">-Account</span><span class="sxs-lookup"><span data-stu-id="25aef-111">-Account</span></span>
<span data-ttu-id="25aef-112">A Data Lake Store-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="25aef-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="25aef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25aef-113">-DefaultProfile</span></span>
<span data-ttu-id="25aef-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="25aef-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25aef-115">-Kódolás</span><span class="sxs-lookup"><span data-stu-id="25aef-115">-Encoding</span></span>
<span data-ttu-id="25aef-116">A létrehozni kívánt elem kódolását határozza meg.</span><span class="sxs-lookup"><span data-stu-id="25aef-116">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="25aef-117">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="25aef-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="25aef-118">Ismeretlen</span><span class="sxs-lookup"><span data-stu-id="25aef-118">Unknown</span></span>
- <span data-ttu-id="25aef-119">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="25aef-119">String</span></span>
- <span data-ttu-id="25aef-120">Unicode</span><span class="sxs-lookup"><span data-stu-id="25aef-120">Unicode</span></span>
- <span data-ttu-id="25aef-121">Bájt</span><span class="sxs-lookup"><span data-stu-id="25aef-121">Byte</span></span>
- <span data-ttu-id="25aef-122">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="25aef-122">BigEndianUnicode</span></span>
- <span data-ttu-id="25aef-123">UTF8</span><span class="sxs-lookup"><span data-stu-id="25aef-123">UTF8</span></span>
- <span data-ttu-id="25aef-124">UTF7</span><span class="sxs-lookup"><span data-stu-id="25aef-124">UTF7</span></span>
- <span data-ttu-id="25aef-125">Ascii</span><span class="sxs-lookup"><span data-stu-id="25aef-125">Ascii</span></span>
- <span data-ttu-id="25aef-126">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="25aef-126">Default</span></span>
- <span data-ttu-id="25aef-127">Oem</span><span class="sxs-lookup"><span data-stu-id="25aef-127">Oem</span></span>
- <span data-ttu-id="25aef-128">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="25aef-128">BigEndianUTF32</span></span>

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

### <span data-ttu-id="25aef-129">-Path</span><span class="sxs-lookup"><span data-stu-id="25aef-129">-Path</span></span>
<span data-ttu-id="25aef-130">A módosítani kívánt elem Data Lake Store-beli elérési útját adja meg a gyökérkönyvtártól (/).</span><span class="sxs-lookup"><span data-stu-id="25aef-130">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="25aef-131">-Érték</span><span class="sxs-lookup"><span data-stu-id="25aef-131">-Value</span></span>
<span data-ttu-id="25aef-132">Az elemhez hozzáadni kívánt tartalom.</span><span class="sxs-lookup"><span data-stu-id="25aef-132">Specifies the content to add to the item.</span></span>

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

### <span data-ttu-id="25aef-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25aef-133">CommonParameters</span></span>
<span data-ttu-id="25aef-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25aef-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25aef-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25aef-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25aef-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="25aef-136">INPUTS</span></span>

### <span data-ttu-id="25aef-137">System.String</span><span class="sxs-lookup"><span data-stu-id="25aef-137">System.String</span></span>

### <span data-ttu-id="25aef-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="25aef-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="25aef-139">System.Object</span><span class="sxs-lookup"><span data-stu-id="25aef-139">System.Object</span></span>

### <span data-ttu-id="25aef-140">System.Text.Encoding</span><span class="sxs-lookup"><span data-stu-id="25aef-140">System.Text.Encoding</span></span>

## <span data-ttu-id="25aef-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25aef-141">OUTPUTS</span></span>

### <span data-ttu-id="25aef-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="25aef-142">System.Boolean</span></span>

## <span data-ttu-id="25aef-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="25aef-143">NOTES</span></span>

## <span data-ttu-id="25aef-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25aef-144">RELATED LINKS</span></span>

[<span data-ttu-id="25aef-145">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="25aef-145">Get-AzDataLakeStoreItemContent</span></span>](./Get-AzDataLakeStoreItemContent.md)


