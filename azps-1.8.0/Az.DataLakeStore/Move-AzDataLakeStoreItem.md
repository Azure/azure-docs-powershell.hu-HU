---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/move-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
ms.openlocfilehash: 8a8cc4d60bfba73b9cbcc9d323b063bff87f8a2a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836286"
---
# <span data-ttu-id="c28d4-101">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c28d4-101">Move-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="c28d4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c28d4-102">SYNOPSIS</span></span>
<span data-ttu-id="c28d4-103">Egy fájl vagy mappa áthelyezése vagy átnevezése az adattó áruházban.</span><span class="sxs-lookup"><span data-stu-id="c28d4-103">Moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c28d4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c28d4-104">SYNTAX</span></span>

```
Move-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c28d4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c28d4-105">DESCRIPTION</span></span>
<span data-ttu-id="c28d4-106">Az **Move-AzDataLakeStoreItem** parancsmag az Adattó áruházban lévő fájlok vagy mappák áthelyezésére vagy átnevezésére.</span><span class="sxs-lookup"><span data-stu-id="c28d4-106">The **Move-AzDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c28d4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c28d4-107">EXAMPLES</span></span>

### <span data-ttu-id="c28d4-108">1. példa: elem áthelyezése és átnevezése</span><span class="sxs-lookup"><span data-stu-id="c28d4-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="c28d4-109">Ez a parancs átnevezi az elemet File.txt RenamedFile.txt és egy másik mappába helyezi át.</span><span class="sxs-lookup"><span data-stu-id="c28d4-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="c28d4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c28d4-110">PARAMETERS</span></span>

### <span data-ttu-id="c28d4-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="c28d4-111">-Account</span></span>
<span data-ttu-id="c28d4-112">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c28d4-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="c28d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c28d4-113">-DefaultProfile</span></span>
<span data-ttu-id="c28d4-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c28d4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c28d4-115">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="c28d4-115">-Destination</span></span>
<span data-ttu-id="c28d4-116">Az az adattó-tároló elérési útját adja meg, amelybe az elemet át szeretné helyezni, kezdve a legfelső szintű könyvtárral (/).</span><span class="sxs-lookup"><span data-stu-id="c28d4-116">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="c28d4-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c28d4-117">-Force</span></span>
<span data-ttu-id="c28d4-118">Jelzi, hogy az adott művelet felülírja a célfájlba, ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="c28d4-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="c28d4-119">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="c28d4-119">-Path</span></span>
<span data-ttu-id="c28d4-120">Az áthelyezni vagy átnevezni kívánt elem az adattó-tároló elérési útját adja meg, kezdve a gyökérkönyvtárral (/).</span><span class="sxs-lookup"><span data-stu-id="c28d4-120">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="c28d4-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c28d4-121">-Confirm</span></span>
<span data-ttu-id="c28d4-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c28d4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c28d4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c28d4-123">-WhatIf</span></span>
<span data-ttu-id="c28d4-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c28d4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c28d4-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c28d4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c28d4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c28d4-126">CommonParameters</span></span>
<span data-ttu-id="c28d4-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c28d4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c28d4-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c28d4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c28d4-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c28d4-129">INPUTS</span></span>

### <span data-ttu-id="c28d4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c28d4-130">System.String</span></span>

### <span data-ttu-id="c28d4-131">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="c28d4-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="c28d4-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c28d4-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c28d4-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c28d4-133">OUTPUTS</span></span>

### <span data-ttu-id="c28d4-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c28d4-134">System.String</span></span>

## <span data-ttu-id="c28d4-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c28d4-135">NOTES</span></span>

## <span data-ttu-id="c28d4-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c28d4-136">RELATED LINKS</span></span>

[<span data-ttu-id="c28d4-137">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c28d4-137">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="c28d4-138">Exportálás – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c28d4-138">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="c28d4-139">Importálás – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c28d4-139">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="c28d4-140">Új – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c28d4-140">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="c28d4-141">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c28d4-141">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="c28d4-142">Teszt-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c28d4-142">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


