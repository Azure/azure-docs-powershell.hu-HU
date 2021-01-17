---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/move-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
ms.openlocfilehash: e8e90b6cca2808bbf2caee69ebef5582ed0f8c5b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465821"
---
# <span data-ttu-id="4cac5-101">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4cac5-101">Move-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="4cac5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cac5-102">SYNOPSIS</span></span>
<span data-ttu-id="4cac5-103">Áthelyez vagy átnevez egy fájlt vagy mappát a Data Lake Store-ban.</span><span class="sxs-lookup"><span data-stu-id="4cac5-103">Moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="4cac5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4cac5-104">SYNTAX</span></span>

```
Move-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cac5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4cac5-105">DESCRIPTION</span></span>
<span data-ttu-id="4cac5-106">A **Move-AzDataLakeStoreItem** parancsmag áthelyez vagy átnevez egy fájlt vagy mappát a Data Lake Store-ban.</span><span class="sxs-lookup"><span data-stu-id="4cac5-106">The **Move-AzDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="4cac5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4cac5-107">EXAMPLES</span></span>

### <span data-ttu-id="4cac5-108">1. példa: Elem áthelyezése és átnevezése</span><span class="sxs-lookup"><span data-stu-id="4cac5-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="4cac5-109">Ez a parancs átnevezi az File.txt, RenamedFile.txt áthelyezi egy másik mappába.</span><span class="sxs-lookup"><span data-stu-id="4cac5-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="4cac5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4cac5-110">PARAMETERS</span></span>

### <span data-ttu-id="4cac5-111">-Account</span><span class="sxs-lookup"><span data-stu-id="4cac5-111">-Account</span></span>
<span data-ttu-id="4cac5-112">A Data Lake Store-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4cac5-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="4cac5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cac5-113">-DefaultProfile</span></span>
<span data-ttu-id="4cac5-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4cac5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cac5-115">-Destination</span><span class="sxs-lookup"><span data-stu-id="4cac5-115">-Destination</span></span>
<span data-ttu-id="4cac5-116">Azt az elérési utat adja meg a Data Lake Store-ban, amelybe át kell áthelyezni az elemet, a gyökérkönyvtártól (/).</span><span class="sxs-lookup"><span data-stu-id="4cac5-116">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="4cac5-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4cac5-117">-Force</span></span>
<span data-ttu-id="4cac5-118">Azt jelzi, hogy ez a művelet felülírhatja a célfájlt, ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="4cac5-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="4cac5-119">-Path</span><span class="sxs-lookup"><span data-stu-id="4cac5-119">-Path</span></span>
<span data-ttu-id="4cac5-120">Az áthelyezni vagy átnevezni kívánt elem Data Lake Store-beli elérési útját adja meg a gyökérkönyvtártól (/).</span><span class="sxs-lookup"><span data-stu-id="4cac5-120">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="4cac5-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4cac5-121">-Confirm</span></span>
<span data-ttu-id="4cac5-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4cac5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cac5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cac5-123">-WhatIf</span></span>
<span data-ttu-id="4cac5-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4cac5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cac5-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4cac5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cac5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cac5-126">CommonParameters</span></span>
<span data-ttu-id="4cac5-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cac5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cac5-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cac5-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cac5-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4cac5-129">INPUTS</span></span>

### <span data-ttu-id="4cac5-130">System.String</span><span class="sxs-lookup"><span data-stu-id="4cac5-130">System.String</span></span>

### <span data-ttu-id="4cac5-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="4cac5-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="4cac5-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4cac5-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4cac5-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4cac5-133">OUTPUTS</span></span>

### <span data-ttu-id="4cac5-134">System.String</span><span class="sxs-lookup"><span data-stu-id="4cac5-134">System.String</span></span>

## <span data-ttu-id="4cac5-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4cac5-135">NOTES</span></span>

## <span data-ttu-id="4cac5-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4cac5-136">RELATED LINKS</span></span>

[<span data-ttu-id="4cac5-137">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4cac5-137">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="4cac5-138">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4cac5-138">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="4cac5-139">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4cac5-139">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="4cac5-140">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4cac5-140">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="4cac5-141">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4cac5-141">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="4cac5-142">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4cac5-142">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


