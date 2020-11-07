---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/move-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
ms.openlocfilehash: e8e90b6cca2808bbf2caee69ebef5582ed0f8c5b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846118"
---
# <span data-ttu-id="20368-101">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="20368-101">Move-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="20368-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="20368-102">SYNOPSIS</span></span>
<span data-ttu-id="20368-103">Egy fájl vagy mappa áthelyezése vagy átnevezése az adattó áruházban.</span><span class="sxs-lookup"><span data-stu-id="20368-103">Moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="20368-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="20368-104">SYNTAX</span></span>

```
Move-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20368-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="20368-105">DESCRIPTION</span></span>
<span data-ttu-id="20368-106">Az **Move-AzDataLakeStoreItem** parancsmag az Adattó áruházban lévő fájlok vagy mappák áthelyezésére vagy átnevezésére.</span><span class="sxs-lookup"><span data-stu-id="20368-106">The **Move-AzDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="20368-107">Példák</span><span class="sxs-lookup"><span data-stu-id="20368-107">EXAMPLES</span></span>

### <span data-ttu-id="20368-108">1. példa: elem áthelyezése és átnevezése</span><span class="sxs-lookup"><span data-stu-id="20368-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="20368-109">Ez a parancs átnevezi az elemet File.txt RenamedFile.txt és egy másik mappába helyezi át.</span><span class="sxs-lookup"><span data-stu-id="20368-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="20368-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="20368-110">PARAMETERS</span></span>

### <span data-ttu-id="20368-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="20368-111">-Account</span></span>
<span data-ttu-id="20368-112">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="20368-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="20368-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20368-113">-DefaultProfile</span></span>
<span data-ttu-id="20368-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="20368-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20368-115">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="20368-115">-Destination</span></span>
<span data-ttu-id="20368-116">Az az adattó-tároló elérési útját adja meg, amelybe az elemet át szeretné helyezni, kezdve a legfelső szintű könyvtárral (/).</span><span class="sxs-lookup"><span data-stu-id="20368-116">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="20368-117">-Force</span><span class="sxs-lookup"><span data-stu-id="20368-117">-Force</span></span>
<span data-ttu-id="20368-118">Jelzi, hogy az adott művelet felülírja a célfájlba, ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="20368-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="20368-119">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="20368-119">-Path</span></span>
<span data-ttu-id="20368-120">Az áthelyezni vagy átnevezni kívánt elem az adattó-tároló elérési útját adja meg, kezdve a gyökérkönyvtárral (/).</span><span class="sxs-lookup"><span data-stu-id="20368-120">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="20368-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="20368-121">-Confirm</span></span>
<span data-ttu-id="20368-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="20368-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20368-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20368-123">-WhatIf</span></span>
<span data-ttu-id="20368-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="20368-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20368-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="20368-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20368-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20368-126">CommonParameters</span></span>
<span data-ttu-id="20368-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="20368-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20368-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20368-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20368-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="20368-129">INPUTS</span></span>

### <span data-ttu-id="20368-130">System. String</span><span class="sxs-lookup"><span data-stu-id="20368-130">System.String</span></span>

### <span data-ttu-id="20368-131">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="20368-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="20368-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="20368-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="20368-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20368-133">OUTPUTS</span></span>

### <span data-ttu-id="20368-134">System. String</span><span class="sxs-lookup"><span data-stu-id="20368-134">System.String</span></span>

## <span data-ttu-id="20368-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="20368-135">NOTES</span></span>

## <span data-ttu-id="20368-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20368-136">RELATED LINKS</span></span>

[<span data-ttu-id="20368-137">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="20368-137">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="20368-138">Exportálás – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="20368-138">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="20368-139">Importálás – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="20368-139">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="20368-140">Új – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="20368-140">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="20368-141">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="20368-141">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="20368-142">Teszt-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="20368-142">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


