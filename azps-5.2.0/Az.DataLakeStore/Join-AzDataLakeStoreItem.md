---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/join-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
ms.openlocfilehash: 1d361149109b654cf3e7fa45e133b9daff84c21c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361169"
---
# <span data-ttu-id="6b6fe-101">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6b6fe-101">Join-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="6b6fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b6fe-102">SYNOPSIS</span></span>
<span data-ttu-id="6b6fe-103">Egy vagy több fájlhoz csatlakozva létrehoz egy fájlt a Data Lake Store-ban.</span><span class="sxs-lookup"><span data-stu-id="6b6fe-103">Joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="6b6fe-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6b6fe-104">SYNTAX</span></span>

```
Join-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b6fe-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6b6fe-105">DESCRIPTION</span></span>
<span data-ttu-id="6b6fe-106">A **Join-AzDataLakeStoreItem** parancsmag egy vagy több fájlhoz csatlakozva létrehoz egy fájlt a Data Lake Store-ban.</span><span class="sxs-lookup"><span data-stu-id="6b6fe-106">The **Join-AzDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="6b6fe-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6b6fe-107">EXAMPLES</span></span>

### <span data-ttu-id="6b6fe-108">1. példa: Két elem illesztés</span><span class="sxs-lookup"><span data-stu-id="6b6fe-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="6b6fe-109">Ez a parancs File01.txt és File02.txt hozza létre a CombinedFile.txt.</span><span class="sxs-lookup"><span data-stu-id="6b6fe-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="6b6fe-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b6fe-110">PARAMETERS</span></span>

### <span data-ttu-id="6b6fe-111">-Account</span><span class="sxs-lookup"><span data-stu-id="6b6fe-111">-Account</span></span>
<span data-ttu-id="6b6fe-112">A Data Lake Store-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b6fe-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="6b6fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b6fe-113">-DefaultProfile</span></span>
<span data-ttu-id="6b6fe-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b6fe-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b6fe-115">-Destination</span><span class="sxs-lookup"><span data-stu-id="6b6fe-115">-Destination</span></span>
<span data-ttu-id="6b6fe-116">Az összekapcsolt elem Data Lake Store-beli elérési útját adja meg a gyökérkönyvtártól (/).</span><span class="sxs-lookup"><span data-stu-id="6b6fe-116">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b6fe-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6b6fe-117">-Force</span></span>
<span data-ttu-id="6b6fe-118">Azt jelzi, hogy ez a művelet felülírhatja a célfájlt, ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="6b6fe-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="6b6fe-119">-Paths</span><span class="sxs-lookup"><span data-stu-id="6b6fe-119">-Paths</span></span>
<span data-ttu-id="6b6fe-120">Az egyesítandó fájlok data lake store-beli elérési útvonalának tömbje, a gyökérkönyvtártól (/) kezdve.</span><span class="sxs-lookup"><span data-stu-id="6b6fe-120">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: Path

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b6fe-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b6fe-121">-Confirm</span></span>
<span data-ttu-id="6b6fe-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6b6fe-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b6fe-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b6fe-123">-WhatIf</span></span>
<span data-ttu-id="6b6fe-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6b6fe-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b6fe-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6b6fe-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b6fe-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b6fe-126">CommonParameters</span></span>
<span data-ttu-id="6b6fe-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b6fe-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b6fe-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b6fe-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b6fe-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b6fe-129">INPUTS</span></span>

### <span data-ttu-id="6b6fe-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6b6fe-130">System.String</span></span>

### <span data-ttu-id="6b6fe-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span><span class="sxs-lookup"><span data-stu-id="6b6fe-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="6b6fe-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="6b6fe-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="6b6fe-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6b6fe-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6b6fe-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b6fe-134">OUTPUTS</span></span>

### <span data-ttu-id="6b6fe-135">System.String</span><span class="sxs-lookup"><span data-stu-id="6b6fe-135">System.String</span></span>

## <span data-ttu-id="6b6fe-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6b6fe-136">NOTES</span></span>

## <span data-ttu-id="6b6fe-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b6fe-137">RELATED LINKS</span></span>

[<span data-ttu-id="6b6fe-138">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6b6fe-138">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="6b6fe-139">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6b6fe-139">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="6b6fe-140">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6b6fe-140">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="6b6fe-141">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6b6fe-141">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="6b6fe-142">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6b6fe-142">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="6b6fe-143">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6b6fe-143">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


