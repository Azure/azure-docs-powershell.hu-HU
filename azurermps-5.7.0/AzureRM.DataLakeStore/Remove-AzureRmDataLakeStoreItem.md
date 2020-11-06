---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 40477ad0635f1b832e7d95e459b27102dc68f8db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492288"
---
# <span data-ttu-id="0ddcc-101">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0ddcc-101">Remove-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="0ddcc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0ddcc-102">SYNOPSIS</span></span>
<span data-ttu-id="0ddcc-103">Töröl egy fájlt vagy mappát az adattó áruházból.</span><span class="sxs-lookup"><span data-stu-id="0ddcc-103">Deletes a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ddcc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0ddcc-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Clean]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ddcc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0ddcc-105">DESCRIPTION</span></span>
<span data-ttu-id="0ddcc-106">A **Remove-AzureRmDataLakeStoreItem** parancsmag töröl egy fájlt vagy mappát az adattó-áruházban.</span><span class="sxs-lookup"><span data-stu-id="0ddcc-106">The **Remove-AzureRmDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="0ddcc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0ddcc-107">EXAMPLES</span></span>

### <span data-ttu-id="0ddcc-108">Példa 1: több elem eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0ddcc-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="0ddcc-109">Ez a parancs eltávolítja a fájlokat File01.txt és File.csv az adattó áruházból.</span><span class="sxs-lookup"><span data-stu-id="0ddcc-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="0ddcc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0ddcc-110">PARAMETERS</span></span>

### <span data-ttu-id="0ddcc-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="0ddcc-111">-Account</span></span>
<span data-ttu-id="0ddcc-112">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0ddcc-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="0ddcc-113">-Clean</span><span class="sxs-lookup"><span data-stu-id="0ddcc-113">-Clean</span></span>
<span data-ttu-id="0ddcc-114">Jelzi, hogy a felhasználó törölni szeretné a mappa teljes tartalmát, a mappát azonban nem.</span><span class="sxs-lookup"><span data-stu-id="0ddcc-114">Indicates the user wants to remove all of the contents of the folder, but not the folder itself</span></span>

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

### <span data-ttu-id="0ddcc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ddcc-115">-DefaultProfile</span></span>
<span data-ttu-id="0ddcc-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0ddcc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ddcc-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0ddcc-117">-Force</span></span>
<span data-ttu-id="0ddcc-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="0ddcc-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0ddcc-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ddcc-119">-PassThru</span></span>
<span data-ttu-id="0ddcc-120">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="0ddcc-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0ddcc-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="0ddcc-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ddcc-122">-Paths</span><span class="sxs-lookup"><span data-stu-id="0ddcc-122">-Paths</span></span>
<span data-ttu-id="0ddcc-123">Az eltávolítandó fájlok elérési útjának tömbjét adja meg, kezdve a gyökérkönyvtárral (/).</span><span class="sxs-lookup"><span data-stu-id="0ddcc-123">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ddcc-124">-Recurse</span><span class="sxs-lookup"><span data-stu-id="0ddcc-124">-Recurse</span></span>
<span data-ttu-id="0ddcc-125">Jelzi, hogy ez a művelet törli a célmappa összes elemét, az almappákat is.</span><span class="sxs-lookup"><span data-stu-id="0ddcc-125">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>
<span data-ttu-id="0ddcc-126">Ha nem adja meg a *Clean* paramétert, a célmappát is törli.</span><span class="sxs-lookup"><span data-stu-id="0ddcc-126">Unless you specify the *Clean* parameter, the target folder is also deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ddcc-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0ddcc-127">-Confirm</span></span>
<span data-ttu-id="0ddcc-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0ddcc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ddcc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ddcc-129">-WhatIf</span></span>
<span data-ttu-id="0ddcc-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0ddcc-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ddcc-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0ddcc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ddcc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ddcc-132">CommonParameters</span></span>
<span data-ttu-id="0ddcc-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0ddcc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ddcc-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ddcc-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ddcc-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ddcc-135">INPUTS</span></span>

### <span data-ttu-id="0ddcc-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="0ddcc-136">None</span></span>
<span data-ttu-id="0ddcc-137">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="0ddcc-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0ddcc-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ddcc-138">OUTPUTS</span></span>

### <span data-ttu-id="0ddcc-139">bool</span><span class="sxs-lookup"><span data-stu-id="0ddcc-139">bool</span></span>
<span data-ttu-id="0ddcc-140">Ha a PassThru meg van adva, a művelet eredményét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="0ddcc-140">If PassThru is specified, returns the result of the operation.</span></span>

## <span data-ttu-id="0ddcc-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0ddcc-141">NOTES</span></span>

## <span data-ttu-id="0ddcc-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ddcc-142">RELATED LINKS</span></span>

[<span data-ttu-id="0ddcc-143">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0ddcc-143">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="0ddcc-144">Exportálás – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0ddcc-144">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="0ddcc-145">Importálás – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0ddcc-145">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="0ddcc-146">Bekapcsolódás a AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0ddcc-146">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="0ddcc-147">Új – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0ddcc-147">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="0ddcc-148">Teszt-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0ddcc-148">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


