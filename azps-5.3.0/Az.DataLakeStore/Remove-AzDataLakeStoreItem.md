---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
ms.openlocfilehash: 5f927bd9ef64cc22eda7669e9b0d60127cf503ac
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465807"
---
# <span data-ttu-id="869cf-101">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="869cf-101">Remove-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="869cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="869cf-102">SYNOPSIS</span></span>
<span data-ttu-id="869cf-103">Töröl egy fájlt vagy mappát a Data Lake Store-ban.</span><span class="sxs-lookup"><span data-stu-id="869cf-103">Deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="869cf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="869cf-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="869cf-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="869cf-105">DESCRIPTION</span></span>
<span data-ttu-id="869cf-106">A **Remove-AzDataLakeStoreItem** parancsmag töröl egy fájlt vagy mappát a Data Lake Store-ban.</span><span class="sxs-lookup"><span data-stu-id="869cf-106">The **Remove-AzDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="869cf-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="869cf-107">EXAMPLES</span></span>

### <span data-ttu-id="869cf-108">1. példa: Több elem eltávolítása</span><span class="sxs-lookup"><span data-stu-id="869cf-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="869cf-109">Ez a parancs eltávolítja a fájlokat File01.txt és File.csv a Data Lake Store-ból.</span><span class="sxs-lookup"><span data-stu-id="869cf-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="869cf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="869cf-110">PARAMETERS</span></span>

### <span data-ttu-id="869cf-111">-Account</span><span class="sxs-lookup"><span data-stu-id="869cf-111">-Account</span></span>
<span data-ttu-id="869cf-112">A Data Lake Store-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="869cf-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="869cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="869cf-113">-DefaultProfile</span></span>
<span data-ttu-id="869cf-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="869cf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="869cf-115">-Force</span><span class="sxs-lookup"><span data-stu-id="869cf-115">-Force</span></span>
<span data-ttu-id="869cf-116">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="869cf-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="869cf-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="869cf-117">-PassThru</span></span>
<span data-ttu-id="869cf-118">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="869cf-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="869cf-119">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="869cf-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="869cf-120">-Paths</span><span class="sxs-lookup"><span data-stu-id="869cf-120">-Paths</span></span>
<span data-ttu-id="869cf-121">A Data Lake Store-ban eltávolítandó fájlok elérési útvonalának tömbje, a gyökérkönyvtártól (/) kezdve.</span><span class="sxs-lookup"><span data-stu-id="869cf-121">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="869cf-122">-Recurse</span><span class="sxs-lookup"><span data-stu-id="869cf-122">-Recurse</span></span>
<span data-ttu-id="869cf-123">Azt jelzi, hogy ez a művelet a célmappa összes elemét törli, az almappákat is beleértve.</span><span class="sxs-lookup"><span data-stu-id="869cf-123">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>

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

### <span data-ttu-id="869cf-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="869cf-124">-Confirm</span></span>
<span data-ttu-id="869cf-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="869cf-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="869cf-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="869cf-126">-WhatIf</span></span>
<span data-ttu-id="869cf-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="869cf-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="869cf-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="869cf-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="869cf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="869cf-129">CommonParameters</span></span>
<span data-ttu-id="869cf-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="869cf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="869cf-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="869cf-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="869cf-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="869cf-132">INPUTS</span></span>

### <span data-ttu-id="869cf-133">System.String</span><span class="sxs-lookup"><span data-stu-id="869cf-133">System.String</span></span>

### <span data-ttu-id="869cf-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span><span class="sxs-lookup"><span data-stu-id="869cf-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="869cf-135">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="869cf-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="869cf-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="869cf-136">OUTPUTS</span></span>

### <span data-ttu-id="869cf-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="869cf-137">System.Boolean</span></span>

## <span data-ttu-id="869cf-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="869cf-138">NOTES</span></span>

## <span data-ttu-id="869cf-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="869cf-139">RELATED LINKS</span></span>

[<span data-ttu-id="869cf-140">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="869cf-140">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="869cf-141">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="869cf-141">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="869cf-142">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="869cf-142">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="869cf-143">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="869cf-143">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="869cf-144">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="869cf-144">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="869cf-145">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="869cf-145">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


