---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/new-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 2dc2d18fc0bc09fd7e9477115f4212aeb2452bbb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493140"
---
# <span data-ttu-id="11002-101">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="11002-101">New-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="11002-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="11002-102">SYNOPSIS</span></span>
<span data-ttu-id="11002-103">Új fájlt vagy mappát hoz létre az adattó áruházban.</span><span class="sxs-lookup"><span data-stu-id="11002-103">Creates a new file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11002-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="11002-104">SYNTAX</span></span>

```
New-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11002-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="11002-105">DESCRIPTION</span></span>
<span data-ttu-id="11002-106">A **New-AzureRmDataLakeStoreItem** parancsmag új fájlt vagy mappát hoz létre a Data Lake Store áruházban.</span><span class="sxs-lookup"><span data-stu-id="11002-106">The **New-AzureRmDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="11002-107">Példák</span><span class="sxs-lookup"><span data-stu-id="11002-107">EXAMPLES</span></span>

### <span data-ttu-id="11002-108">Példa 1: új fájl és új mappa létrehozása</span><span class="sxs-lookup"><span data-stu-id="11002-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="11002-109">Az első parancs létrehozza a megadott fiókhoz tartozó fájlt NewFile.txt.</span><span class="sxs-lookup"><span data-stu-id="11002-109">The first command creates the file NewFile.txt for the specified account.</span></span>

<span data-ttu-id="11002-110">A második parancs létrehozza a mappa NewFolder a root mappából.</span><span class="sxs-lookup"><span data-stu-id="11002-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="11002-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="11002-111">PARAMETERS</span></span>

### <span data-ttu-id="11002-112">-Fiók</span><span class="sxs-lookup"><span data-stu-id="11002-112">-Account</span></span>
<span data-ttu-id="11002-113">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="11002-113">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11002-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11002-114">-DefaultProfile</span></span>
<span data-ttu-id="11002-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="11002-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11002-116">-Encoding</span><span class="sxs-lookup"><span data-stu-id="11002-116">-Encoding</span></span>
<span data-ttu-id="11002-117">A létrehozandó elem kódolását adja meg.</span><span class="sxs-lookup"><span data-stu-id="11002-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="11002-118">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="11002-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="11002-119">Ismeretlen</span><span class="sxs-lookup"><span data-stu-id="11002-119">Unknown</span></span>
- <span data-ttu-id="11002-120">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="11002-120">String</span></span>
- <span data-ttu-id="11002-121">Unicode</span><span class="sxs-lookup"><span data-stu-id="11002-121">Unicode</span></span>
- <span data-ttu-id="11002-122">Byte</span><span class="sxs-lookup"><span data-stu-id="11002-122">Byte</span></span>
- <span data-ttu-id="11002-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="11002-123">BigEndianUnicode</span></span>
- <span data-ttu-id="11002-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="11002-124">UTF8</span></span>
- <span data-ttu-id="11002-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="11002-125">UTF7</span></span>
- <span data-ttu-id="11002-126">ASCII</span><span class="sxs-lookup"><span data-stu-id="11002-126">Ascii</span></span>
- <span data-ttu-id="11002-127">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="11002-127">Default</span></span>
- <span data-ttu-id="11002-128">OEM</span><span class="sxs-lookup"><span data-stu-id="11002-128">Oem</span></span>
- <span data-ttu-id="11002-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="11002-129">BigEndianUTF32</span></span>

```yaml
Type: FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11002-130">-Mappa</span><span class="sxs-lookup"><span data-stu-id="11002-130">-Folder</span></span>
<span data-ttu-id="11002-131">Jelzi, hogy a művelet létrehoz egy mappát.</span><span class="sxs-lookup"><span data-stu-id="11002-131">Indicates that this operation creates a folder.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11002-132">-Force</span><span class="sxs-lookup"><span data-stu-id="11002-132">-Force</span></span>
<span data-ttu-id="11002-133">Jelzi, hogy az adott művelet felülírja a cél elemét, ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="11002-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11002-134">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="11002-134">-Path</span></span>
<span data-ttu-id="11002-135">A létrehozandó elem Data Lake Store elérési útját adja meg, a gyökérkönyvtárral kezdve (/).</span><span class="sxs-lookup"><span data-stu-id="11002-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11002-136">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="11002-136">-Value</span></span>
<span data-ttu-id="11002-137">A létrehozott elemhez hozzáadni kívánt tartalmat adja meg.</span><span class="sxs-lookup"><span data-stu-id="11002-137">Specifies the content to add to the item you create.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11002-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="11002-138">-Confirm</span></span>
<span data-ttu-id="11002-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="11002-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11002-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11002-140">-WhatIf</span></span>
<span data-ttu-id="11002-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="11002-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11002-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="11002-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11002-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11002-143">CommonParameters</span></span>
<span data-ttu-id="11002-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="11002-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11002-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11002-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11002-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="11002-146">INPUTS</span></span>

### <span data-ttu-id="11002-147">Objektum</span><span class="sxs-lookup"><span data-stu-id="11002-147">Object</span></span>
<span data-ttu-id="11002-148">Az ' érték ' paraméter elfogadja az "objektum" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="11002-148">Parameter 'Value' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="11002-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11002-149">OUTPUTS</span></span>

### <span data-ttu-id="11002-150">karakterlánc</span><span class="sxs-lookup"><span data-stu-id="11002-150">string</span></span>
<span data-ttu-id="11002-151">A létrehozott fájl vagy mappa teljes elérési útja.</span><span class="sxs-lookup"><span data-stu-id="11002-151">The full path to the created file or folder.</span></span>

## <span data-ttu-id="11002-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="11002-152">NOTES</span></span>

## <span data-ttu-id="11002-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11002-153">RELATED LINKS</span></span>

[<span data-ttu-id="11002-154">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="11002-154">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="11002-155">Exportálás – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="11002-155">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="11002-156">Importálás – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="11002-156">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="11002-157">Új – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="11002-157">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="11002-158">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="11002-158">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="11002-159">Teszt-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="11002-159">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


