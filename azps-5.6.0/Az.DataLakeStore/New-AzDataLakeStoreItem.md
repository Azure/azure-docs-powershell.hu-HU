---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/new-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
ms.openlocfilehash: 46495d5a057de6c7cff21cdc09fe68d80e0c4da7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938833"
---
# <span data-ttu-id="f0a07-101">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f0a07-101">New-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="f0a07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0a07-102">SYNOPSIS</span></span>
<span data-ttu-id="f0a07-103">Új fájlt vagy mappát hoz létre a Data Lake Store-ban.</span><span class="sxs-lookup"><span data-stu-id="f0a07-103">Creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="f0a07-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f0a07-104">SYNTAX</span></span>

```
New-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <Encoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f0a07-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f0a07-105">DESCRIPTION</span></span>
<span data-ttu-id="f0a07-106">A **New-AzDataLakeStoreItem** parancsmag létrehoz egy új fájlt vagy mappát a Data Lake Store-ban.</span><span class="sxs-lookup"><span data-stu-id="f0a07-106">The **New-AzDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="f0a07-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f0a07-107">EXAMPLES</span></span>

### <span data-ttu-id="f0a07-108">1. példa: Új fájl és új mappa létrehozása</span><span class="sxs-lookup"><span data-stu-id="f0a07-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="f0a07-109">Az első parancs létrehozza a NewFile.txt a megadott fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="f0a07-109">The first command creates the file NewFile.txt for the specified account.</span></span>
<span data-ttu-id="f0a07-110">A második parancs létrehozza a NewFolder mappát a gyökérmappában.</span><span class="sxs-lookup"><span data-stu-id="f0a07-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="f0a07-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0a07-111">PARAMETERS</span></span>

### <span data-ttu-id="f0a07-112">-Account</span><span class="sxs-lookup"><span data-stu-id="f0a07-112">-Account</span></span>
<span data-ttu-id="f0a07-113">A Data Lake Store-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f0a07-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="f0a07-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0a07-114">-DefaultProfile</span></span>
<span data-ttu-id="f0a07-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f0a07-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0a07-116">-Kódolás</span><span class="sxs-lookup"><span data-stu-id="f0a07-116">-Encoding</span></span>
<span data-ttu-id="f0a07-117">A létrehozni kívánt elem kódolását határozza meg.</span><span class="sxs-lookup"><span data-stu-id="f0a07-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="f0a07-118">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="f0a07-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f0a07-119">Ismeretlen</span><span class="sxs-lookup"><span data-stu-id="f0a07-119">Unknown</span></span>
- <span data-ttu-id="f0a07-120">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="f0a07-120">String</span></span>
- <span data-ttu-id="f0a07-121">Unicode</span><span class="sxs-lookup"><span data-stu-id="f0a07-121">Unicode</span></span>
- <span data-ttu-id="f0a07-122">Bájt</span><span class="sxs-lookup"><span data-stu-id="f0a07-122">Byte</span></span>
- <span data-ttu-id="f0a07-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="f0a07-123">BigEndianUnicode</span></span>
- <span data-ttu-id="f0a07-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="f0a07-124">UTF8</span></span>
- <span data-ttu-id="f0a07-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="f0a07-125">UTF7</span></span>
- <span data-ttu-id="f0a07-126">Ascii</span><span class="sxs-lookup"><span data-stu-id="f0a07-126">Ascii</span></span>
- <span data-ttu-id="f0a07-127">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="f0a07-127">Default</span></span>
- <span data-ttu-id="f0a07-128">Oem</span><span class="sxs-lookup"><span data-stu-id="f0a07-128">Oem</span></span>
- <span data-ttu-id="f0a07-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="f0a07-129">BigEndianUTF32</span></span>

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

### <span data-ttu-id="f0a07-130">-Mappa</span><span class="sxs-lookup"><span data-stu-id="f0a07-130">-Folder</span></span>
<span data-ttu-id="f0a07-131">Azt jelzi, hogy ez a művelet mappát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f0a07-131">Indicates that this operation creates a folder.</span></span>

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

### <span data-ttu-id="f0a07-132">-Force</span><span class="sxs-lookup"><span data-stu-id="f0a07-132">-Force</span></span>
<span data-ttu-id="f0a07-133">Azt jelzi, hogy ez a művelet felülírhatja a célelemet, ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="f0a07-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

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

### <span data-ttu-id="f0a07-134">-Path</span><span class="sxs-lookup"><span data-stu-id="f0a07-134">-Path</span></span>
<span data-ttu-id="f0a07-135">A létrehozni kívánt elem Data Lake Store-beli elérési útját adja meg a gyökérkönyvtártól (/).</span><span class="sxs-lookup"><span data-stu-id="f0a07-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="f0a07-136">-Érték</span><span class="sxs-lookup"><span data-stu-id="f0a07-136">-Value</span></span>
<span data-ttu-id="f0a07-137">A létrehozott elemhez hozzáadni kívánt tartalom.</span><span class="sxs-lookup"><span data-stu-id="f0a07-137">Specifies the content to add to the item you create.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0a07-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0a07-138">-Confirm</span></span>
<span data-ttu-id="f0a07-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f0a07-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0a07-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0a07-140">-WhatIf</span></span>
<span data-ttu-id="f0a07-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f0a07-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0a07-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f0a07-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0a07-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0a07-143">CommonParameters</span></span>
<span data-ttu-id="f0a07-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0a07-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0a07-145">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0a07-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0a07-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f0a07-146">INPUTS</span></span>

### <span data-ttu-id="f0a07-147">System.String</span><span class="sxs-lookup"><span data-stu-id="f0a07-147">System.String</span></span>

### <span data-ttu-id="f0a07-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="f0a07-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="f0a07-149">System.Object</span><span class="sxs-lookup"><span data-stu-id="f0a07-149">System.Object</span></span>

### <span data-ttu-id="f0a07-150">System.Text.Encoding</span><span class="sxs-lookup"><span data-stu-id="f0a07-150">System.Text.Encoding</span></span>

### <span data-ttu-id="f0a07-151">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f0a07-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f0a07-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0a07-152">OUTPUTS</span></span>

### <span data-ttu-id="f0a07-153">System.String</span><span class="sxs-lookup"><span data-stu-id="f0a07-153">System.String</span></span>

## <span data-ttu-id="f0a07-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f0a07-154">NOTES</span></span>

## <span data-ttu-id="f0a07-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f0a07-155">RELATED LINKS</span></span>

[<span data-ttu-id="f0a07-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f0a07-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="f0a07-157">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f0a07-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="f0a07-158">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f0a07-158">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="f0a07-159">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f0a07-159">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="f0a07-160">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f0a07-160">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="f0a07-161">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f0a07-161">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


