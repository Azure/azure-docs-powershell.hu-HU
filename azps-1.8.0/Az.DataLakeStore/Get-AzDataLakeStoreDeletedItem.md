---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BF0A5D64-AC93-48F5-AED2-C21CC8829053
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: 750203e954ef96619e32b63ffd6eae333bb852f2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836314"
---
# <span data-ttu-id="1736b-101">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="1736b-101">Get-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="1736b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1736b-102">SYNOPSIS</span></span>
<span data-ttu-id="1736b-103">Megkeresi azokat a törölt bejegyzéseket a kukában, amelyek megegyeznek a szűrővel.</span><span class="sxs-lookup"><span data-stu-id="1736b-103">Searches for deleted entries in trash which match the filter.</span></span>

## <span data-ttu-id="1736b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1736b-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreDeletedItem [-Account] <String> [-Filter] <String> [-Count <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1736b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1736b-105">DESCRIPTION</span></span>
<span data-ttu-id="1736b-106">A **Get-AzDataLakeStoreDeletedItem** parancsmag azokat a törölt fájlokat vagy mappákat keresi meg az Adattó áruházban, amelyek megegyeznek az adott szűrővel.</span><span class="sxs-lookup"><span data-stu-id="1736b-106">The **Get-AzDataLakeStoreDeletedItem** cmdlet searches the deleted files or folders in Data Lake Store which match the given filter.</span></span>
<span data-ttu-id="1736b-107">A törölt elemek következő attribútumait jeleníti meg:-OriginalPath, TrashDirPath, típus, CreationTime.</span><span class="sxs-lookup"><span data-stu-id="1736b-107">It displays the following attributes of the deleted items - OriginalPath, TrashDirPath, Type, CreationTime.</span></span>
<span data-ttu-id="1736b-108">Ez hosszú futási művelet lehet, mivel előfordulhat, hogy a kukában a fájlok millióit kell keresnie, és a feladatot munkavégzésként lehet futtatni.</span><span class="sxs-lookup"><span data-stu-id="1736b-108">This could be a long running operation as it may have to search through millions of files in trash and could be run as a job.</span></span>

## <span data-ttu-id="1736b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1736b-109">EXAMPLES</span></span>

### <span data-ttu-id="1736b-110">Példa: az adattó áruházból származó fájlok adatainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="1736b-110">Example: Get details of a file from the Data Lake Store</span></span>
```
PS> Get-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Filter test0/file_123

TrashDirPath                         OriginalPath                                          Type CreationTime
------------                         ------------                                          ---- ------------
cd6ad5ce-792b-4812-8a33-8f9ed19eb532 adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 FILE 2/8/2019 8:12:18 AM
356cfd42-39c7-451e-96cb-9f47883d91e2 adl://ml1ptrashtest.azuredatalake.com/test0/file_1232 FILE 2/8/2019 8:12:18 AM
e7b30ac8-2dbc-43a3-8ca6-2d420ac0c488 adl://ml1ptrashtest.azuredatalake.com/test0/file_1237 FILE 2/8/2019 8:12:18 AM
```

## <span data-ttu-id="1736b-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1736b-111">PARAMETERS</span></span>

### <span data-ttu-id="1736b-112">-Fiók</span><span class="sxs-lookup"><span data-stu-id="1736b-112">-Account</span></span>
<span data-ttu-id="1736b-113">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1736b-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="1736b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1736b-114">-AsJob</span></span>
<span data-ttu-id="1736b-115">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="1736b-115">Run cmdlet in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1736b-116">-Count</span><span class="sxs-lookup"><span data-stu-id="1736b-116">-Count</span></span>
<span data-ttu-id="1736b-117">Itt adhatja meg, hogy a felhasználó hány találatot szeretne keresni.</span><span class="sxs-lookup"><span data-stu-id="1736b-117">Specifies the number of results the user wants to find.</span></span> <span data-ttu-id="1736b-118">A lekérdezés addig fut, amíg meg nem találja a találatok számát, vagy ha a teljes kukában keres, amelyik előbb történik.</span><span class="sxs-lookup"><span data-stu-id="1736b-118">The query runs until it finds Count results or it searches through entire trash, whichever happens first.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1736b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1736b-119">-DefaultProfile</span></span>
<span data-ttu-id="1736b-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1736b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1736b-121">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="1736b-121">-Filter</span></span>
<span data-ttu-id="1736b-122">A keresési lekérdezést adja meg.</span><span class="sxs-lookup"><span data-stu-id="1736b-122">Specifies the search query.</span></span> <span data-ttu-id="1736b-123">Egy specifikusabb érték további releváns eredményeket ad.</span><span class="sxs-lookup"><span data-stu-id="1736b-123">A more specific value gives more relevant results.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1736b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1736b-124">CommonParameters</span></span>
<span data-ttu-id="1736b-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1736b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1736b-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1736b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1736b-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1736b-127">INPUTS</span></span>

### <span data-ttu-id="1736b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1736b-128">System.String</span></span>

## <span data-ttu-id="1736b-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1736b-129">OUTPUTS</span></span>

### <span data-ttu-id="1736b-130">System. Collections. Generic. list<Microsoft. Azure. Command. DataLakeStore. modellek. DataLakeStoreDeletedItem></span><span class="sxs-lookup"><span data-stu-id="1736b-130">System.Collections.Generic.List<Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem></span></span>

## <span data-ttu-id="1736b-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1736b-131">NOTES</span></span>

## <span data-ttu-id="1736b-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1736b-132">RELATED LINKS</span></span>

[<span data-ttu-id="1736b-133">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="1736b-133">Restore-AzDataLakeStoreDeletedItem</span></span>](./Restore-AzDataLakeStoreDeletedItem.md)