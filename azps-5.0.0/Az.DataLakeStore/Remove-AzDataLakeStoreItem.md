---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
ms.openlocfilehash: 5f927bd9ef64cc22eda7669e9b0d60127cf503ac
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297779"
---
# <span data-ttu-id="82ece-101">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="82ece-101">Remove-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="82ece-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="82ece-102">SYNOPSIS</span></span>
<span data-ttu-id="82ece-103">Töröl egy fájlt vagy mappát az adattó áruházból.</span><span class="sxs-lookup"><span data-stu-id="82ece-103">Deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="82ece-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="82ece-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82ece-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="82ece-105">DESCRIPTION</span></span>
<span data-ttu-id="82ece-106">A **Remove-AzDataLakeStoreItem** parancsmag töröl egy fájlt vagy mappát az adattó-áruházban.</span><span class="sxs-lookup"><span data-stu-id="82ece-106">The **Remove-AzDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="82ece-107">Példák</span><span class="sxs-lookup"><span data-stu-id="82ece-107">EXAMPLES</span></span>

### <span data-ttu-id="82ece-108">Példa 1: több elem eltávolítása</span><span class="sxs-lookup"><span data-stu-id="82ece-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="82ece-109">Ez a parancs eltávolítja a fájlokat File01.txt és File.csv az adattó áruházból.</span><span class="sxs-lookup"><span data-stu-id="82ece-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="82ece-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="82ece-110">PARAMETERS</span></span>

### <span data-ttu-id="82ece-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="82ece-111">-Account</span></span>
<span data-ttu-id="82ece-112">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="82ece-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="82ece-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82ece-113">-DefaultProfile</span></span>
<span data-ttu-id="82ece-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="82ece-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82ece-115">-Force</span><span class="sxs-lookup"><span data-stu-id="82ece-115">-Force</span></span>
<span data-ttu-id="82ece-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="82ece-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="82ece-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82ece-117">-PassThru</span></span>
<span data-ttu-id="82ece-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="82ece-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="82ece-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="82ece-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="82ece-120">-Paths</span><span class="sxs-lookup"><span data-stu-id="82ece-120">-Paths</span></span>
<span data-ttu-id="82ece-121">Az eltávolítandó fájlok elérési útjának tömbjét adja meg, kezdve a gyökérkönyvtárral (/).</span><span class="sxs-lookup"><span data-stu-id="82ece-121">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="82ece-122">-Recurse</span><span class="sxs-lookup"><span data-stu-id="82ece-122">-Recurse</span></span>
<span data-ttu-id="82ece-123">Jelzi, hogy ez a művelet törli a célmappa összes elemét, az almappákat is.</span><span class="sxs-lookup"><span data-stu-id="82ece-123">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>

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

### <span data-ttu-id="82ece-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="82ece-124">-Confirm</span></span>
<span data-ttu-id="82ece-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="82ece-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82ece-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82ece-126">-WhatIf</span></span>
<span data-ttu-id="82ece-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="82ece-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82ece-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="82ece-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82ece-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82ece-129">CommonParameters</span></span>
<span data-ttu-id="82ece-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="82ece-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82ece-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82ece-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82ece-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="82ece-132">INPUTS</span></span>

### <span data-ttu-id="82ece-133">System. String</span><span class="sxs-lookup"><span data-stu-id="82ece-133">System.String</span></span>

### <span data-ttu-id="82ece-134">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance []</span><span class="sxs-lookup"><span data-stu-id="82ece-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="82ece-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="82ece-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="82ece-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="82ece-136">OUTPUTS</span></span>

### <span data-ttu-id="82ece-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="82ece-137">System.Boolean</span></span>

## <span data-ttu-id="82ece-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="82ece-138">NOTES</span></span>

## <span data-ttu-id="82ece-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="82ece-139">RELATED LINKS</span></span>

[<span data-ttu-id="82ece-140">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="82ece-140">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="82ece-141">Exportálás – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="82ece-141">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="82ece-142">Importálás – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="82ece-142">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="82ece-143">Bekapcsolódás a AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="82ece-143">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="82ece-144">Új – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="82ece-144">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="82ece-145">Teszt-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="82ece-145">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


