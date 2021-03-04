---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestorechilditemsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItemSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItemSummary.md
ms.openlocfilehash: d83e07e207c2b0e3a03c745abc874814378e5ee4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921258"
---
# <span data-ttu-id="81044-101">Get-AzDataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="81044-101">Get-AzDataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="81044-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81044-102">SYNOPSIS</span></span>
<span data-ttu-id="81044-103">A megadott elérési útban szereplő összes méret, fájl és könyvtár összesítését adja vissza.</span><span class="sxs-lookup"><span data-stu-id="81044-103">Gets the summary of total size, files and directories contained in the path specified</span></span>

## <span data-ttu-id="81044-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="81044-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreChildItemSummary [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81044-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="81044-105">DESCRIPTION</span></span>
<span data-ttu-id="81044-106">A **Get-AzDataLakeStoreDataItemSummary** egy adott elérési úthoz olvassa be a tartalom összefoglalását.</span><span class="sxs-lookup"><span data-stu-id="81044-106">The **Get-AzDataLakeStoreChildItemSummary** retrieves the content summary for a given path.</span></span> <span data-ttu-id="81044-107">Rekurzív módon kiszámítja a fájlok, könyvtárak és az adott elérési út alatt lévő összes fájl teljes méretét.</span><span class="sxs-lookup"><span data-stu-id="81044-107">It recursively computes total number of files, directories and total size of all the files under the given path.</span></span>

## <span data-ttu-id="81044-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="81044-108">EXAMPLES</span></span>

### <span data-ttu-id="81044-109">1. példa: Mappa tartalom-összesítésének lekérte</span><span class="sxs-lookup"><span data-stu-id="81044-109">Example 1: Get the content summary of a folder</span></span>
```
PS C:\> Get-AzDataLakeStoreChildItemSummary -Account ContosoADL -Path /a -Concurrency 128
```

<span data-ttu-id="81044-110">Felsorolja a /a alatt található összes könyvtárat, fájlt és azok méretét.</span><span class="sxs-lookup"><span data-stu-id="81044-110">It lists number of total directories, files and their size contained under /a.</span></span>

## <span data-ttu-id="81044-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81044-111">PARAMETERS</span></span>

### <span data-ttu-id="81044-112">-Account</span><span class="sxs-lookup"><span data-stu-id="81044-112">-Account</span></span>
<span data-ttu-id="81044-113">The Data Lake Store account to execute the filesystem operation in</span><span class="sxs-lookup"><span data-stu-id="81044-113">The Data Lake Store account to execute the filesystem operation in</span></span>

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

### <span data-ttu-id="81044-114">-Egyidejűség</span><span class="sxs-lookup"><span data-stu-id="81044-114">-Concurrency</span></span>
<span data-ttu-id="81044-115">A párhuzamosan feldolgozott fájlok/könyvtárak számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="81044-115">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="81044-116">Az alapértelmezett érték a rendszer specifikációja alapján számítható legjobb munkamennyiségként.</span><span class="sxs-lookup"><span data-stu-id="81044-116">Default will be computed as a best effort based on system specification.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81044-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81044-117">-DefaultProfile</span></span>
<span data-ttu-id="81044-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="81044-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81044-119">-Path</span><span class="sxs-lookup"><span data-stu-id="81044-119">-Path</span></span>
<span data-ttu-id="81044-120">A megadott Data Lake-fiókban lekérni szükséges elérési út.</span><span class="sxs-lookup"><span data-stu-id="81044-120">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="81044-121">Fájl vagy mappa lehet "/folder/file.txt" formátumban, ahol a DNS utáni első "/" a fájlrendszer gyökerét jelzi.</span><span class="sxs-lookup"><span data-stu-id="81044-121">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81044-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81044-122">-Confirm</span></span>
<span data-ttu-id="81044-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="81044-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81044-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81044-124">-WhatIf</span></span>
<span data-ttu-id="81044-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="81044-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81044-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="81044-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81044-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81044-127">CommonParameters</span></span>
<span data-ttu-id="81044-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81044-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81044-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81044-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81044-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="81044-130">INPUTS</span></span>

### <span data-ttu-id="81044-131">System.String</span><span class="sxs-lookup"><span data-stu-id="81044-131">System.String</span></span>

### <span data-ttu-id="81044-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="81044-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="81044-133">System.Int32</span><span class="sxs-lookup"><span data-stu-id="81044-133">System.Int32</span></span>

## <span data-ttu-id="81044-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81044-134">OUTPUTS</span></span>

### <span data-ttu-id="81044-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreSummary</span><span class="sxs-lookup"><span data-stu-id="81044-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="81044-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="81044-136">NOTES</span></span>

## <span data-ttu-id="81044-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81044-137">RELATED LINKS</span></span>
