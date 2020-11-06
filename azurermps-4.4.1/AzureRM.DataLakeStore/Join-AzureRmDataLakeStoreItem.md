---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Join-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Join-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 1f09d1da5ab4ad88ff16be56affaa582ad1e24d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500860"
---
# <span data-ttu-id="6c9c3-101">Join-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6c9c3-101">Join-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="6c9c3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6c9c3-102">SYNOPSIS</span></span>
<span data-ttu-id="6c9c3-103">Csatlakozik egy vagy több fájlhoz egy fájl létrehozásához az adattó áruházban.</span><span class="sxs-lookup"><span data-stu-id="6c9c3-103">Joins one or more files to create one file in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c9c3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6c9c3-104">SYNTAX</span></span>

```
Join-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c9c3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6c9c3-105">DESCRIPTION</span></span>
<span data-ttu-id="6c9c3-106">A **JOIN-AzureRmDataLakeStoreItem** parancsmag egy vagy több fájlhoz csatlakozik egy fájl létrehozásához az Adattó áruházban.</span><span class="sxs-lookup"><span data-stu-id="6c9c3-106">The **Join-AzureRmDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="6c9c3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6c9c3-107">EXAMPLES</span></span>

### <span data-ttu-id="6c9c3-108">1. példa: csatlakozás két elemhez</span><span class="sxs-lookup"><span data-stu-id="6c9c3-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="6c9c3-109">Ez a parancs csatlakozik File01.txthez, és File02.txt hozza létre a fájlt a CombinedFile.txt.</span><span class="sxs-lookup"><span data-stu-id="6c9c3-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="6c9c3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6c9c3-110">PARAMETERS</span></span>

### <span data-ttu-id="6c9c3-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="6c9c3-111">-Account</span></span>
<span data-ttu-id="6c9c3-112">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c9c3-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="6c9c3-113">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="6c9c3-113">-Destination</span></span>
<span data-ttu-id="6c9c3-114">Az illesztett elem Data Lake Store elérési útját adja meg, kezdve a legfelső szintű könyvtárral (/).</span><span class="sxs-lookup"><span data-stu-id="6c9c3-114">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="6c9c3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6c9c3-115">-Force</span></span>
<span data-ttu-id="6c9c3-116">Jelzi, hogy az adott művelet felülírja a célfájlba, ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="6c9c3-116">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="6c9c3-117">-Paths</span><span class="sxs-lookup"><span data-stu-id="6c9c3-117">-Paths</span></span>
<span data-ttu-id="6c9c3-118">Az egyesíteni kívánt fájlok elérési útjának sorát adja meg, a gyökérkönyvtárral kezdve (/).</span><span class="sxs-lookup"><span data-stu-id="6c9c3-118">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="6c9c3-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6c9c3-119">-Confirm</span></span>
<span data-ttu-id="6c9c3-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6c9c3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c9c3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c9c3-121">-WhatIf</span></span>
<span data-ttu-id="6c9c3-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6c9c3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c9c3-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6c9c3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c9c3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c9c3-124">-DefaultProfile</span></span>
<span data-ttu-id="6c9c3-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6c9c3-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c9c3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c9c3-126">CommonParameters</span></span>
<span data-ttu-id="6c9c3-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6c9c3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c9c3-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c9c3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c9c3-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c9c3-129">INPUTS</span></span>

## <span data-ttu-id="6c9c3-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c9c3-130">OUTPUTS</span></span>

### <span data-ttu-id="6c9c3-131">karakterlánc</span><span class="sxs-lookup"><span data-stu-id="6c9c3-131">string</span></span>
<span data-ttu-id="6c9c3-132">Az így létrehozott fájl teljes elérési útja az illesztett fájlokból.</span><span class="sxs-lookup"><span data-stu-id="6c9c3-132">The full path to the resulting file from the joined files.</span></span>

## <span data-ttu-id="6c9c3-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6c9c3-133">NOTES</span></span>

## <span data-ttu-id="6c9c3-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6c9c3-134">RELATED LINKS</span></span>

[<span data-ttu-id="6c9c3-135">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6c9c3-135">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6c9c3-136">Exportálás – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6c9c3-136">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6c9c3-137">Importálás – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6c9c3-137">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6c9c3-138">Új – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6c9c3-138">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6c9c3-139">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6c9c3-139">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6c9c3-140">Teszt-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6c9c3-140">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


