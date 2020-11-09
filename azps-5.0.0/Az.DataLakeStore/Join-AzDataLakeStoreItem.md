---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/join-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
ms.openlocfilehash: 1d361149109b654cf3e7fa45e133b9daff84c21c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297815"
---
# <span data-ttu-id="b15c1-101">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b15c1-101">Join-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="b15c1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b15c1-102">SYNOPSIS</span></span>
<span data-ttu-id="b15c1-103">Csatlakozik egy vagy több fájlhoz egy fájl létrehozásához az adattó áruházban.</span><span class="sxs-lookup"><span data-stu-id="b15c1-103">Joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="b15c1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b15c1-104">SYNTAX</span></span>

```
Join-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b15c1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b15c1-105">DESCRIPTION</span></span>
<span data-ttu-id="b15c1-106">A **JOIN-AzDataLakeStoreItem** parancsmag egy vagy több fájlhoz csatlakozik egy fájl létrehozásához az Adattó áruházban.</span><span class="sxs-lookup"><span data-stu-id="b15c1-106">The **Join-AzDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="b15c1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b15c1-107">EXAMPLES</span></span>

### <span data-ttu-id="b15c1-108">1. példa: csatlakozás két elemhez</span><span class="sxs-lookup"><span data-stu-id="b15c1-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="b15c1-109">Ez a parancs csatlakozik File01.txthez, és File02.txt hozza létre a fájlt a CombinedFile.txt.</span><span class="sxs-lookup"><span data-stu-id="b15c1-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="b15c1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b15c1-110">PARAMETERS</span></span>

### <span data-ttu-id="b15c1-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="b15c1-111">-Account</span></span>
<span data-ttu-id="b15c1-112">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b15c1-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="b15c1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b15c1-113">-DefaultProfile</span></span>
<span data-ttu-id="b15c1-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b15c1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b15c1-115">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="b15c1-115">-Destination</span></span>
<span data-ttu-id="b15c1-116">Az illesztett elem Data Lake Store elérési útját adja meg, kezdve a legfelső szintű könyvtárral (/).</span><span class="sxs-lookup"><span data-stu-id="b15c1-116">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="b15c1-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b15c1-117">-Force</span></span>
<span data-ttu-id="b15c1-118">Jelzi, hogy az adott művelet felülírja a célfájlba, ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="b15c1-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="b15c1-119">-Paths</span><span class="sxs-lookup"><span data-stu-id="b15c1-119">-Paths</span></span>
<span data-ttu-id="b15c1-120">Az egyesíteni kívánt fájlok elérési útjának sorát adja meg, a gyökérkönyvtárral kezdve (/).</span><span class="sxs-lookup"><span data-stu-id="b15c1-120">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="b15c1-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b15c1-121">-Confirm</span></span>
<span data-ttu-id="b15c1-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b15c1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b15c1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b15c1-123">-WhatIf</span></span>
<span data-ttu-id="b15c1-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b15c1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b15c1-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b15c1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b15c1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b15c1-126">CommonParameters</span></span>
<span data-ttu-id="b15c1-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b15c1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b15c1-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b15c1-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b15c1-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b15c1-129">INPUTS</span></span>

### <span data-ttu-id="b15c1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b15c1-130">System.String</span></span>

### <span data-ttu-id="b15c1-131">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance []</span><span class="sxs-lookup"><span data-stu-id="b15c1-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="b15c1-132">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="b15c1-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="b15c1-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b15c1-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b15c1-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b15c1-134">OUTPUTS</span></span>

### <span data-ttu-id="b15c1-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b15c1-135">System.String</span></span>

## <span data-ttu-id="b15c1-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b15c1-136">NOTES</span></span>

## <span data-ttu-id="b15c1-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b15c1-137">RELATED LINKS</span></span>

[<span data-ttu-id="b15c1-138">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b15c1-138">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="b15c1-139">Exportálás – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b15c1-139">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="b15c1-140">Importálás – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b15c1-140">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="b15c1-141">Új – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b15c1-141">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="b15c1-142">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b15c1-142">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="b15c1-143">Teszt-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b15c1-143">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


