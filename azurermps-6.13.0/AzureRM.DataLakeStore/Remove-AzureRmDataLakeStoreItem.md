---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 03e43530a044bad5f3ea7509fa649da9f26a93f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491945"
---
# <span data-ttu-id="89809-101">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="89809-101">Remove-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="89809-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="89809-102">SYNOPSIS</span></span>
<span data-ttu-id="89809-103">Töröl egy fájlt vagy mappát az adattó áruházból.</span><span class="sxs-lookup"><span data-stu-id="89809-103">Deletes a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89809-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="89809-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89809-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="89809-105">DESCRIPTION</span></span>
<span data-ttu-id="89809-106">A **Remove-AzureRmDataLakeStoreItem** parancsmag töröl egy fájlt vagy mappát az adattó-áruházban.</span><span class="sxs-lookup"><span data-stu-id="89809-106">The **Remove-AzureRmDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="89809-107">Példák</span><span class="sxs-lookup"><span data-stu-id="89809-107">EXAMPLES</span></span>

### <span data-ttu-id="89809-108">Példa 1: több elem eltávolítása</span><span class="sxs-lookup"><span data-stu-id="89809-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="89809-109">Ez a parancs eltávolítja a fájlokat File01.txt és File.csv az adattó áruházból.</span><span class="sxs-lookup"><span data-stu-id="89809-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="89809-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="89809-110">PARAMETERS</span></span>

### <span data-ttu-id="89809-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="89809-111">-Account</span></span>
<span data-ttu-id="89809-112">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="89809-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="89809-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89809-113">-DefaultProfile</span></span>
<span data-ttu-id="89809-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="89809-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89809-115">-Force</span><span class="sxs-lookup"><span data-stu-id="89809-115">-Force</span></span>
<span data-ttu-id="89809-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="89809-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="89809-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89809-117">-PassThru</span></span>
<span data-ttu-id="89809-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="89809-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="89809-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="89809-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89809-120">-Paths</span><span class="sxs-lookup"><span data-stu-id="89809-120">-Paths</span></span>
<span data-ttu-id="89809-121">Az eltávolítandó fájlok elérési útjának tömbjét adja meg, kezdve a gyökérkönyvtárral (/).</span><span class="sxs-lookup"><span data-stu-id="89809-121">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89809-122">-Recurse</span><span class="sxs-lookup"><span data-stu-id="89809-122">-Recurse</span></span>
<span data-ttu-id="89809-123">Jelzi, hogy ez a művelet törli a célmappa összes elemét, az almappákat is.</span><span class="sxs-lookup"><span data-stu-id="89809-123">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89809-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="89809-124">-Confirm</span></span>
<span data-ttu-id="89809-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="89809-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89809-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89809-126">-WhatIf</span></span>
<span data-ttu-id="89809-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="89809-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89809-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="89809-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89809-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89809-129">CommonParameters</span></span>
<span data-ttu-id="89809-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="89809-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89809-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89809-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89809-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="89809-132">INPUTS</span></span>

### <span data-ttu-id="89809-133">System. String</span><span class="sxs-lookup"><span data-stu-id="89809-133">System.String</span></span>

### <span data-ttu-id="89809-134">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance []</span><span class="sxs-lookup"><span data-stu-id="89809-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="89809-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="89809-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="89809-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89809-136">OUTPUTS</span></span>

### <span data-ttu-id="89809-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="89809-137">System.Boolean</span></span>

## <span data-ttu-id="89809-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="89809-138">NOTES</span></span>

## <span data-ttu-id="89809-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89809-139">RELATED LINKS</span></span>

[<span data-ttu-id="89809-140">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="89809-140">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="89809-141">Exportálás – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="89809-141">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="89809-142">Importálás – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="89809-142">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="89809-143">Bekapcsolódás a AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="89809-143">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="89809-144">Új – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="89809-144">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="89809-145">Teszt-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="89809-145">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


