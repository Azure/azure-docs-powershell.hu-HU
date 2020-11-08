---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BF0A5D64-AC93-48F5-AED2-C21CC8829053
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: cfcdf8accb5de467c5b243df2c973074fe9ae31a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017854"
---
# <span data-ttu-id="88fdc-101">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="88fdc-101">Get-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="88fdc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="88fdc-102">SYNOPSIS</span></span>
<span data-ttu-id="88fdc-103">Megkeresi azokat a törölt bejegyzéseket a kukában, amelyek megegyeznek a szűrővel.</span><span class="sxs-lookup"><span data-stu-id="88fdc-103">Searches for deleted entries in trash which match the filter.</span></span>

## <span data-ttu-id="88fdc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="88fdc-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreDeletedItem [-Account] <String> [-Filter] <String> [-Count <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88fdc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="88fdc-105">DESCRIPTION</span></span>
<span data-ttu-id="88fdc-106">A **Get-AzDataLakeStoreDeletedItem** parancsmag azokat a törölt fájlokat vagy mappákat keresi meg az Adattó áruházban, amelyek megegyeznek az adott szűrővel.</span><span class="sxs-lookup"><span data-stu-id="88fdc-106">The **Get-AzDataLakeStoreDeletedItem** cmdlet searches the deleted files or folders in Data Lake Store which match the given filter.</span></span>
<span data-ttu-id="88fdc-107">A törölt elemek következő attribútumait jeleníti meg:-OriginalPath, TrashDirPath, típus, CreationTime.</span><span class="sxs-lookup"><span data-stu-id="88fdc-107">It displays the following attributes of the deleted items - OriginalPath, TrashDirPath, Type, CreationTime.</span></span>
<span data-ttu-id="88fdc-108">Ez hosszú futási művelet lehet, mivel előfordulhat, hogy a kukában a fájlok millióit kell keresnie, és a feladatot munkavégzésként lehet futtatni.</span><span class="sxs-lookup"><span data-stu-id="88fdc-108">This could be a long running operation as it may have to search through millions of files in trash and could be run as a job.</span></span>
<span data-ttu-id="88fdc-109">Figyelmeztetés: a törlés visszavonása ajánlott művelet.</span><span class="sxs-lookup"><span data-stu-id="88fdc-109">Caution: Undeleting files is a best effort operation.</span></span> <span data-ttu-id="88fdc-110">Nincs garancia arra, hogy a fájl törlés után visszaállíthatók.</span><span class="sxs-lookup"><span data-stu-id="88fdc-110">There are no guarantees that a file can be restored once it is deleted.</span></span> <span data-ttu-id="88fdc-111">Az API használatát a whitelisten keresztül engedélyezheti.</span><span class="sxs-lookup"><span data-stu-id="88fdc-111">The use of this API is enabled via whitelisting.</span></span> <span data-ttu-id="88fdc-112">Ha az ADL-fiókja nem whitelist, akkor ezzel az API-val nem fog bevezetni a kivételt.</span><span class="sxs-lookup"><span data-stu-id="88fdc-112">If your ADL account is not whitelisted, then using this api will throw Not implemented exception.</span></span> <span data-ttu-id="88fdc-113">További információért és segítségért forduljon a Microsoft ügyfélszolgálatához.</span><span class="sxs-lookup"><span data-stu-id="88fdc-113">For further information and assistance please contact Microsoft support.</span></span>

## <span data-ttu-id="88fdc-114">Példák</span><span class="sxs-lookup"><span data-stu-id="88fdc-114">EXAMPLES</span></span>

### <span data-ttu-id="88fdc-115">Példa: az adattó áruházból származó fájlok adatainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="88fdc-115">Example: Get details of a file from the Data Lake Store</span></span>
```
PS> Get-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Filter test0/file_123

TrashDirPath                         OriginalPath                                          Type CreationTime
------------                         ------------                                          ---- ------------
cd6ad5ce-792b-4812-8a33-8f9ed19eb532 adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 FILE 2/8/2019 8:12:18 AM
356cfd42-39c7-451e-96cb-9f47883d91e2 adl://ml1ptrashtest.azuredatalake.com/test0/file_1232 FILE 2/8/2019 8:12:18 AM
e7b30ac8-2dbc-43a3-8ca6-2d420ac0c488 adl://ml1ptrashtest.azuredatalake.com/test0/file_1237 FILE 2/8/2019 8:12:18 AM
```

## <span data-ttu-id="88fdc-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="88fdc-116">PARAMETERS</span></span>

### <span data-ttu-id="88fdc-117">-Fiók</span><span class="sxs-lookup"><span data-stu-id="88fdc-117">-Account</span></span>
<span data-ttu-id="88fdc-118">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="88fdc-118">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="88fdc-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88fdc-119">-AsJob</span></span>
<span data-ttu-id="88fdc-120">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="88fdc-120">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="88fdc-121">-Count</span><span class="sxs-lookup"><span data-stu-id="88fdc-121">-Count</span></span>
<span data-ttu-id="88fdc-122">Itt adhatja meg, hogy a felhasználó hány találatot szeretne keresni.</span><span class="sxs-lookup"><span data-stu-id="88fdc-122">Specifies the number of results the user wants to find.</span></span> <span data-ttu-id="88fdc-123">A lekérdezés addig fut, amíg meg nem találja a találatok számát, vagy ha a teljes kukában keres, amelyik előbb történik.</span><span class="sxs-lookup"><span data-stu-id="88fdc-123">The query runs until it finds Count results or it searches through entire trash, whichever happens first.</span></span>

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

### <span data-ttu-id="88fdc-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88fdc-124">-DefaultProfile</span></span>
<span data-ttu-id="88fdc-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="88fdc-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88fdc-126">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="88fdc-126">-Filter</span></span>
<span data-ttu-id="88fdc-127">A keresési lekérdezést adja meg.</span><span class="sxs-lookup"><span data-stu-id="88fdc-127">Specifies the search query.</span></span> <span data-ttu-id="88fdc-128">Egy specifikusabb érték további releváns eredményeket ad.</span><span class="sxs-lookup"><span data-stu-id="88fdc-128">A more specific value gives more relevant results.</span></span>

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

### <span data-ttu-id="88fdc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88fdc-129">CommonParameters</span></span>
<span data-ttu-id="88fdc-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="88fdc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88fdc-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88fdc-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88fdc-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="88fdc-132">INPUTS</span></span>

### <span data-ttu-id="88fdc-133">System. String</span><span class="sxs-lookup"><span data-stu-id="88fdc-133">System.String</span></span>

## <span data-ttu-id="88fdc-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="88fdc-134">OUTPUTS</span></span>

### <span data-ttu-id="88fdc-135">System. Collections. Generic. list<Microsoft. Azure. Command. DataLakeStore. modellek. DataLakeStoreDeletedItem></span><span class="sxs-lookup"><span data-stu-id="88fdc-135">System.Collections.Generic.List<Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem></span></span>

## <span data-ttu-id="88fdc-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="88fdc-136">NOTES</span></span>

## <span data-ttu-id="88fdc-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="88fdc-137">RELATED LINKS</span></span>

[<span data-ttu-id="88fdc-138">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="88fdc-138">Restore-AzDataLakeStoreDeletedItem</span></span>](./Restore-AzDataLakeStoreDeletedItem.md)