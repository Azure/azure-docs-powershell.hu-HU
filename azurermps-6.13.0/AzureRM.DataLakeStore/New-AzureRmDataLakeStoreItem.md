---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/new-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 2e50135762826661e82f499f2aec48c67d00c648
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491951"
---
# <span data-ttu-id="5914a-101">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5914a-101">New-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="5914a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5914a-102">SYNOPSIS</span></span>
<span data-ttu-id="5914a-103">Új fájlt vagy mappát hoz létre az adattó áruházban.</span><span class="sxs-lookup"><span data-stu-id="5914a-103">Creates a new file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5914a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5914a-104">SYNTAX</span></span>

```
New-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5914a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5914a-105">DESCRIPTION</span></span>
<span data-ttu-id="5914a-106">A **New-AzureRmDataLakeStoreItem** parancsmag új fájlt vagy mappát hoz létre a Data Lake Store áruházban.</span><span class="sxs-lookup"><span data-stu-id="5914a-106">The **New-AzureRmDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="5914a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5914a-107">EXAMPLES</span></span>

### <span data-ttu-id="5914a-108">Példa 1: új fájl és új mappa létrehozása</span><span class="sxs-lookup"><span data-stu-id="5914a-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="5914a-109">Az első parancs létrehozza a megadott fiókhoz tartozó fájlt NewFile.txt.</span><span class="sxs-lookup"><span data-stu-id="5914a-109">The first command creates the file NewFile.txt for the specified account.</span></span>
<span data-ttu-id="5914a-110">A második parancs létrehozza a mappa NewFolder a root mappából.</span><span class="sxs-lookup"><span data-stu-id="5914a-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="5914a-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5914a-111">PARAMETERS</span></span>

### <span data-ttu-id="5914a-112">-Fiók</span><span class="sxs-lookup"><span data-stu-id="5914a-112">-Account</span></span>
<span data-ttu-id="5914a-113">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5914a-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="5914a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5914a-114">-DefaultProfile</span></span>
<span data-ttu-id="5914a-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5914a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5914a-116">-Encoding</span><span class="sxs-lookup"><span data-stu-id="5914a-116">-Encoding</span></span>
<span data-ttu-id="5914a-117">A létrehozandó elem kódolását adja meg.</span><span class="sxs-lookup"><span data-stu-id="5914a-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="5914a-118">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="5914a-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5914a-119">Ismeretlen</span><span class="sxs-lookup"><span data-stu-id="5914a-119">Unknown</span></span>
- <span data-ttu-id="5914a-120">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="5914a-120">String</span></span>
- <span data-ttu-id="5914a-121">Unicode</span><span class="sxs-lookup"><span data-stu-id="5914a-121">Unicode</span></span>
- <span data-ttu-id="5914a-122">Byte</span><span class="sxs-lookup"><span data-stu-id="5914a-122">Byte</span></span>
- <span data-ttu-id="5914a-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="5914a-123">BigEndianUnicode</span></span>
- <span data-ttu-id="5914a-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="5914a-124">UTF8</span></span>
- <span data-ttu-id="5914a-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="5914a-125">UTF7</span></span>
- <span data-ttu-id="5914a-126">ASCII</span><span class="sxs-lookup"><span data-stu-id="5914a-126">Ascii</span></span>
- <span data-ttu-id="5914a-127">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="5914a-127">Default</span></span>
- <span data-ttu-id="5914a-128">OEM</span><span class="sxs-lookup"><span data-stu-id="5914a-128">Oem</span></span>
- <span data-ttu-id="5914a-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="5914a-129">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5914a-130">-Mappa</span><span class="sxs-lookup"><span data-stu-id="5914a-130">-Folder</span></span>
<span data-ttu-id="5914a-131">Jelzi, hogy a művelet létrehoz egy mappát.</span><span class="sxs-lookup"><span data-stu-id="5914a-131">Indicates that this operation creates a folder.</span></span>

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

### <span data-ttu-id="5914a-132">-Force</span><span class="sxs-lookup"><span data-stu-id="5914a-132">-Force</span></span>
<span data-ttu-id="5914a-133">Jelzi, hogy az adott művelet felülírja a cél elemét, ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="5914a-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

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

### <span data-ttu-id="5914a-134">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="5914a-134">-Path</span></span>
<span data-ttu-id="5914a-135">A létrehozandó elem Data Lake Store elérési útját adja meg, a gyökérkönyvtárral kezdve (/).</span><span class="sxs-lookup"><span data-stu-id="5914a-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="5914a-136">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="5914a-136">-Value</span></span>
<span data-ttu-id="5914a-137">A létrehozott elemhez hozzáadni kívánt tartalmat adja meg.</span><span class="sxs-lookup"><span data-stu-id="5914a-137">Specifies the content to add to the item you create.</span></span>

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

### <span data-ttu-id="5914a-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5914a-138">-Confirm</span></span>
<span data-ttu-id="5914a-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5914a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5914a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5914a-140">-WhatIf</span></span>
<span data-ttu-id="5914a-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5914a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5914a-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5914a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5914a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5914a-143">CommonParameters</span></span>
<span data-ttu-id="5914a-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5914a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5914a-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5914a-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5914a-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5914a-146">INPUTS</span></span>

### <span data-ttu-id="5914a-147">System. String</span><span class="sxs-lookup"><span data-stu-id="5914a-147">System.String</span></span>

### <span data-ttu-id="5914a-148">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="5914a-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="5914a-149">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="5914a-149">System.Object</span></span>

### <span data-ttu-id="5914a-150">Microsoft. Azure. Command. DataLakeStore. models. FileSystemCmdletProviderEncoding</span><span class="sxs-lookup"><span data-stu-id="5914a-150">Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding</span></span>

### <span data-ttu-id="5914a-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5914a-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5914a-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5914a-152">OUTPUTS</span></span>

### <span data-ttu-id="5914a-153">System. String</span><span class="sxs-lookup"><span data-stu-id="5914a-153">System.String</span></span>
<span data-ttu-id="5914a-154">A létrehozott fájl vagy mappa teljes elérési útja.</span><span class="sxs-lookup"><span data-stu-id="5914a-154">The full path to the created file or folder.</span></span>

## <span data-ttu-id="5914a-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5914a-155">NOTES</span></span>

## <span data-ttu-id="5914a-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5914a-156">RELATED LINKS</span></span>

[<span data-ttu-id="5914a-157">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5914a-157">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5914a-158">Exportálás – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5914a-158">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5914a-159">Importálás – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5914a-159">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5914a-160">Új – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5914a-160">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5914a-161">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5914a-161">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5914a-162">Teszt-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5914a-162">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


