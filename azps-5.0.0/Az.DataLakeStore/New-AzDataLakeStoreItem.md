---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/new-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
ms.openlocfilehash: ab752ec2201c9b64a9656153f29a947b7a722819
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303950"
---
# <span data-ttu-id="8c6cd-101">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8c6cd-101">New-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="8c6cd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8c6cd-102">SYNOPSIS</span></span>
<span data-ttu-id="8c6cd-103">Új fájlt vagy mappát hoz létre az adattó áruházban.</span><span class="sxs-lookup"><span data-stu-id="8c6cd-103">Creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="8c6cd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8c6cd-104">SYNTAX</span></span>

```
New-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <Encoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8c6cd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8c6cd-105">DESCRIPTION</span></span>
<span data-ttu-id="8c6cd-106">A **New-AzDataLakeStoreItem** parancsmag új fájlt vagy mappát hoz létre a Data Lake Store áruházban.</span><span class="sxs-lookup"><span data-stu-id="8c6cd-106">The **New-AzDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="8c6cd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8c6cd-107">EXAMPLES</span></span>

### <span data-ttu-id="8c6cd-108">Példa 1: új fájl és új mappa létrehozása</span><span class="sxs-lookup"><span data-stu-id="8c6cd-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="8c6cd-109">Az első parancs létrehozza a megadott fiókhoz tartozó fájlt NewFile.txt.</span><span class="sxs-lookup"><span data-stu-id="8c6cd-109">The first command creates the file NewFile.txt for the specified account.</span></span>
<span data-ttu-id="8c6cd-110">A második parancs létrehozza a mappa NewFolder a root mappából.</span><span class="sxs-lookup"><span data-stu-id="8c6cd-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="8c6cd-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8c6cd-111">PARAMETERS</span></span>

### <span data-ttu-id="8c6cd-112">-Fiók</span><span class="sxs-lookup"><span data-stu-id="8c6cd-112">-Account</span></span>
<span data-ttu-id="8c6cd-113">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c6cd-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="8c6cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c6cd-114">-DefaultProfile</span></span>
<span data-ttu-id="8c6cd-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8c6cd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c6cd-116">-Encoding</span><span class="sxs-lookup"><span data-stu-id="8c6cd-116">-Encoding</span></span>
<span data-ttu-id="8c6cd-117">A létrehozandó elem kódolását adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c6cd-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="8c6cd-118">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8c6cd-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8c6cd-119">Ismeretlen</span><span class="sxs-lookup"><span data-stu-id="8c6cd-119">Unknown</span></span>
- <span data-ttu-id="8c6cd-120">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="8c6cd-120">String</span></span>
- <span data-ttu-id="8c6cd-121">Unicode</span><span class="sxs-lookup"><span data-stu-id="8c6cd-121">Unicode</span></span>
- <span data-ttu-id="8c6cd-122">Byte</span><span class="sxs-lookup"><span data-stu-id="8c6cd-122">Byte</span></span>
- <span data-ttu-id="8c6cd-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="8c6cd-123">BigEndianUnicode</span></span>
- <span data-ttu-id="8c6cd-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="8c6cd-124">UTF8</span></span>
- <span data-ttu-id="8c6cd-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="8c6cd-125">UTF7</span></span>
- <span data-ttu-id="8c6cd-126">ASCII</span><span class="sxs-lookup"><span data-stu-id="8c6cd-126">Ascii</span></span>
- <span data-ttu-id="8c6cd-127">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="8c6cd-127">Default</span></span>
- <span data-ttu-id="8c6cd-128">OEM</span><span class="sxs-lookup"><span data-stu-id="8c6cd-128">Oem</span></span>
- <span data-ttu-id="8c6cd-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="8c6cd-129">BigEndianUTF32</span></span>

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

### <span data-ttu-id="8c6cd-130">-Mappa</span><span class="sxs-lookup"><span data-stu-id="8c6cd-130">-Folder</span></span>
<span data-ttu-id="8c6cd-131">Jelzi, hogy a művelet létrehoz egy mappát.</span><span class="sxs-lookup"><span data-stu-id="8c6cd-131">Indicates that this operation creates a folder.</span></span>

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

### <span data-ttu-id="8c6cd-132">-Force</span><span class="sxs-lookup"><span data-stu-id="8c6cd-132">-Force</span></span>
<span data-ttu-id="8c6cd-133">Jelzi, hogy az adott művelet felülírja a cél elemét, ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="8c6cd-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

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

### <span data-ttu-id="8c6cd-134">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="8c6cd-134">-Path</span></span>
<span data-ttu-id="8c6cd-135">A létrehozandó elem Data Lake Store elérési útját adja meg, a gyökérkönyvtárral kezdve (/).</span><span class="sxs-lookup"><span data-stu-id="8c6cd-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="8c6cd-136">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="8c6cd-136">-Value</span></span>
<span data-ttu-id="8c6cd-137">A létrehozott elemhez hozzáadni kívánt tartalmat adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c6cd-137">Specifies the content to add to the item you create.</span></span>

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

### <span data-ttu-id="8c6cd-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8c6cd-138">-Confirm</span></span>
<span data-ttu-id="8c6cd-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8c6cd-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c6cd-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c6cd-140">-WhatIf</span></span>
<span data-ttu-id="8c6cd-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8c6cd-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c6cd-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8c6cd-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c6cd-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c6cd-143">CommonParameters</span></span>
<span data-ttu-id="8c6cd-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8c6cd-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c6cd-145">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c6cd-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c6cd-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c6cd-146">INPUTS</span></span>

### <span data-ttu-id="8c6cd-147">System. String</span><span class="sxs-lookup"><span data-stu-id="8c6cd-147">System.String</span></span>

### <span data-ttu-id="8c6cd-148">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="8c6cd-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="8c6cd-149">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="8c6cd-149">System.Object</span></span>

### <span data-ttu-id="8c6cd-150">System. Text. Encoding</span><span class="sxs-lookup"><span data-stu-id="8c6cd-150">System.Text.Encoding</span></span>

### <span data-ttu-id="8c6cd-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8c6cd-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8c6cd-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c6cd-152">OUTPUTS</span></span>

### <span data-ttu-id="8c6cd-153">System. String</span><span class="sxs-lookup"><span data-stu-id="8c6cd-153">System.String</span></span>

## <span data-ttu-id="8c6cd-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8c6cd-154">NOTES</span></span>

## <span data-ttu-id="8c6cd-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c6cd-155">RELATED LINKS</span></span>

[<span data-ttu-id="8c6cd-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8c6cd-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="8c6cd-157">Exportálás – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8c6cd-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="8c6cd-158">Importálás – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8c6cd-158">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="8c6cd-159">Új – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8c6cd-159">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="8c6cd-160">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8c6cd-160">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="8c6cd-161">Teszt-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8c6cd-161">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


