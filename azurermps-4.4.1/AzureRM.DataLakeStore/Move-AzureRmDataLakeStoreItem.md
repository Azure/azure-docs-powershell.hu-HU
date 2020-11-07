---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Move-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Move-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 5d975e70423e03e3ab17bbfc8631ff8e1f892cc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679454"
---
# <span data-ttu-id="35063-101">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="35063-101">Move-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="35063-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="35063-102">SYNOPSIS</span></span>
<span data-ttu-id="35063-103">Egy fájl vagy mappa áthelyezése vagy átnevezése az adattó áruházban.</span><span class="sxs-lookup"><span data-stu-id="35063-103">Moves or renames a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35063-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="35063-104">SYNTAX</span></span>

```
Move-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35063-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="35063-105">DESCRIPTION</span></span>
<span data-ttu-id="35063-106">Az **Move-AzureRmDataLakeStoreItem** parancsmag az Adattó áruházban lévő fájlok vagy mappák áthelyezésére vagy átnevezésére.</span><span class="sxs-lookup"><span data-stu-id="35063-106">The **Move-AzureRmDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="35063-107">Példák</span><span class="sxs-lookup"><span data-stu-id="35063-107">EXAMPLES</span></span>

### <span data-ttu-id="35063-108">1. példa: elem áthelyezése és átnevezése</span><span class="sxs-lookup"><span data-stu-id="35063-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="35063-109">Ez a parancs átnevezi az elemet File.txt RenamedFile.txt és egy másik mappába helyezi át.</span><span class="sxs-lookup"><span data-stu-id="35063-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="35063-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="35063-110">PARAMETERS</span></span>

### <span data-ttu-id="35063-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="35063-111">-Account</span></span>
<span data-ttu-id="35063-112">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="35063-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="35063-113">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="35063-113">-Destination</span></span>
<span data-ttu-id="35063-114">Az az adattó-tároló elérési útját adja meg, amelybe az elemet át szeretné helyezni, kezdve a legfelső szintű könyvtárral (/).</span><span class="sxs-lookup"><span data-stu-id="35063-114">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="35063-115">-Force</span><span class="sxs-lookup"><span data-stu-id="35063-115">-Force</span></span>
<span data-ttu-id="35063-116">Jelzi, hogy az adott művelet felülírja a célfájlba, ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="35063-116">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="35063-117">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="35063-117">-Path</span></span>
<span data-ttu-id="35063-118">Az áthelyezni vagy átnevezni kívánt elem az adattó-tároló elérési útját adja meg, kezdve a gyökérkönyvtárral (/).</span><span class="sxs-lookup"><span data-stu-id="35063-118">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="35063-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="35063-119">-Confirm</span></span>
<span data-ttu-id="35063-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="35063-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35063-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35063-121">-WhatIf</span></span>
<span data-ttu-id="35063-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="35063-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35063-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="35063-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35063-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35063-124">-DefaultProfile</span></span>
<span data-ttu-id="35063-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="35063-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35063-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35063-126">CommonParameters</span></span>
<span data-ttu-id="35063-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="35063-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35063-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35063-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35063-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="35063-129">INPUTS</span></span>

## <span data-ttu-id="35063-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="35063-130">OUTPUTS</span></span>

### <span data-ttu-id="35063-131">karakterlánc</span><span class="sxs-lookup"><span data-stu-id="35063-131">string</span></span>
<span data-ttu-id="35063-132">Az áthelyezett fájl vagy mappa teljes elérési útja.</span><span class="sxs-lookup"><span data-stu-id="35063-132">The full path to the moved file or folder.</span></span>

## <span data-ttu-id="35063-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="35063-133">NOTES</span></span>

## <span data-ttu-id="35063-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="35063-134">RELATED LINKS</span></span>

[<span data-ttu-id="35063-135">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="35063-135">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="35063-136">Exportálás – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="35063-136">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="35063-137">Importálás – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="35063-137">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="35063-138">Új – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="35063-138">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="35063-139">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="35063-139">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="35063-140">Teszt-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="35063-140">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


