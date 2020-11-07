---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/new-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
ms.openlocfilehash: ab752ec2201c9b64a9656153f29a947b7a722819
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846102"
---
# <span data-ttu-id="451f1-101">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="451f1-101">New-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="451f1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="451f1-102">SYNOPSIS</span></span>
<span data-ttu-id="451f1-103">Új fájlt vagy mappát hoz létre az adattó áruházban.</span><span class="sxs-lookup"><span data-stu-id="451f1-103">Creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="451f1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="451f1-104">SYNTAX</span></span>

```
New-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <Encoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="451f1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="451f1-105">DESCRIPTION</span></span>
<span data-ttu-id="451f1-106">A **New-AzDataLakeStoreItem** parancsmag új fájlt vagy mappát hoz létre a Data Lake Store áruházban.</span><span class="sxs-lookup"><span data-stu-id="451f1-106">The **New-AzDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="451f1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="451f1-107">EXAMPLES</span></span>

### <span data-ttu-id="451f1-108">Példa 1: új fájl és új mappa létrehozása</span><span class="sxs-lookup"><span data-stu-id="451f1-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="451f1-109">Az első parancs létrehozza a megadott fiókhoz tartozó fájlt NewFile.txt.</span><span class="sxs-lookup"><span data-stu-id="451f1-109">The first command creates the file NewFile.txt for the specified account.</span></span>
<span data-ttu-id="451f1-110">A második parancs létrehozza a mappa NewFolder a root mappából.</span><span class="sxs-lookup"><span data-stu-id="451f1-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="451f1-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="451f1-111">PARAMETERS</span></span>

### <span data-ttu-id="451f1-112">-Fiók</span><span class="sxs-lookup"><span data-stu-id="451f1-112">-Account</span></span>
<span data-ttu-id="451f1-113">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="451f1-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="451f1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="451f1-114">-DefaultProfile</span></span>
<span data-ttu-id="451f1-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="451f1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="451f1-116">-Encoding</span><span class="sxs-lookup"><span data-stu-id="451f1-116">-Encoding</span></span>
<span data-ttu-id="451f1-117">A létrehozandó elem kódolását adja meg.</span><span class="sxs-lookup"><span data-stu-id="451f1-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="451f1-118">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="451f1-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="451f1-119">Ismeretlen</span><span class="sxs-lookup"><span data-stu-id="451f1-119">Unknown</span></span>
- <span data-ttu-id="451f1-120">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="451f1-120">String</span></span>
- <span data-ttu-id="451f1-121">Unicode</span><span class="sxs-lookup"><span data-stu-id="451f1-121">Unicode</span></span>
- <span data-ttu-id="451f1-122">Byte</span><span class="sxs-lookup"><span data-stu-id="451f1-122">Byte</span></span>
- <span data-ttu-id="451f1-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="451f1-123">BigEndianUnicode</span></span>
- <span data-ttu-id="451f1-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="451f1-124">UTF8</span></span>
- <span data-ttu-id="451f1-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="451f1-125">UTF7</span></span>
- <span data-ttu-id="451f1-126">ASCII</span><span class="sxs-lookup"><span data-stu-id="451f1-126">Ascii</span></span>
- <span data-ttu-id="451f1-127">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="451f1-127">Default</span></span>
- <span data-ttu-id="451f1-128">OEM</span><span class="sxs-lookup"><span data-stu-id="451f1-128">Oem</span></span>
- <span data-ttu-id="451f1-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="451f1-129">BigEndianUTF32</span></span>

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

### <span data-ttu-id="451f1-130">-Mappa</span><span class="sxs-lookup"><span data-stu-id="451f1-130">-Folder</span></span>
<span data-ttu-id="451f1-131">Jelzi, hogy a művelet létrehoz egy mappát.</span><span class="sxs-lookup"><span data-stu-id="451f1-131">Indicates that this operation creates a folder.</span></span>

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

### <span data-ttu-id="451f1-132">-Force</span><span class="sxs-lookup"><span data-stu-id="451f1-132">-Force</span></span>
<span data-ttu-id="451f1-133">Jelzi, hogy az adott művelet felülírja a cél elemét, ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="451f1-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

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

### <span data-ttu-id="451f1-134">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="451f1-134">-Path</span></span>
<span data-ttu-id="451f1-135">A létrehozandó elem Data Lake Store elérési útját adja meg, a gyökérkönyvtárral kezdve (/).</span><span class="sxs-lookup"><span data-stu-id="451f1-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="451f1-136">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="451f1-136">-Value</span></span>
<span data-ttu-id="451f1-137">A létrehozott elemhez hozzáadni kívánt tartalmat adja meg.</span><span class="sxs-lookup"><span data-stu-id="451f1-137">Specifies the content to add to the item you create.</span></span>

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

### <span data-ttu-id="451f1-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="451f1-138">-Confirm</span></span>
<span data-ttu-id="451f1-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="451f1-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="451f1-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="451f1-140">-WhatIf</span></span>
<span data-ttu-id="451f1-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="451f1-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="451f1-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="451f1-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="451f1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="451f1-143">CommonParameters</span></span>
<span data-ttu-id="451f1-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="451f1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="451f1-145">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="451f1-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="451f1-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="451f1-146">INPUTS</span></span>

### <span data-ttu-id="451f1-147">System. String</span><span class="sxs-lookup"><span data-stu-id="451f1-147">System.String</span></span>

### <span data-ttu-id="451f1-148">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="451f1-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="451f1-149">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="451f1-149">System.Object</span></span>

### <span data-ttu-id="451f1-150">System. Text. Encoding</span><span class="sxs-lookup"><span data-stu-id="451f1-150">System.Text.Encoding</span></span>

### <span data-ttu-id="451f1-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="451f1-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="451f1-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="451f1-152">OUTPUTS</span></span>

### <span data-ttu-id="451f1-153">System. String</span><span class="sxs-lookup"><span data-stu-id="451f1-153">System.String</span></span>

## <span data-ttu-id="451f1-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="451f1-154">NOTES</span></span>

## <span data-ttu-id="451f1-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="451f1-155">RELATED LINKS</span></span>

[<span data-ttu-id="451f1-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="451f1-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="451f1-157">Exportálás – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="451f1-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="451f1-158">Importálás – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="451f1-158">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="451f1-159">Új – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="451f1-159">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="451f1-160">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="451f1-160">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="451f1-161">Teszt-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="451f1-161">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


