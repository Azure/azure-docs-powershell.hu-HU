---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BF0A5D64-AC93-48F5-AED2-C21CC8829053
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: cfcdf8accb5de467c5b243df2c973074fe9ae31a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351521"
---
# <span data-ttu-id="275bd-101">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="275bd-101">Get-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="275bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="275bd-102">SYNOPSIS</span></span>
<span data-ttu-id="275bd-103">Olyan törölt bejegyzéseket keres a kukában, amelyek megfelelnek a szűrőnek.</span><span class="sxs-lookup"><span data-stu-id="275bd-103">Searches for deleted entries in trash which match the filter.</span></span>

## <span data-ttu-id="275bd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="275bd-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreDeletedItem [-Account] <String> [-Filter] <String> [-Count <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="275bd-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="275bd-105">DESCRIPTION</span></span>
<span data-ttu-id="275bd-106">A **Get-AzDataLakeStoreDeletedItem** parancsmag a Data Lake Store-ban a megadott szűrőnek megfelelő törölt fájlokban vagy mappákban keres.</span><span class="sxs-lookup"><span data-stu-id="275bd-106">The **Get-AzDataLakeStoreDeletedItem** cmdlet searches the deleted files or folders in Data Lake Store which match the given filter.</span></span>
<span data-ttu-id="275bd-107">A törölt elemek alábbi attribútumait jeleníti meg: OriginalPath, TrashDirPath, Type, CreationTime.</span><span class="sxs-lookup"><span data-stu-id="275bd-107">It displays the following attributes of the deleted items - OriginalPath, TrashDirPath, Type, CreationTime.</span></span>
<span data-ttu-id="275bd-108">Ez hosszú ideig futó művelet lehet, mivel előfordulhat, hogy több millió fájlban kell keresnie a kukában, és feladatként is futtatható.</span><span class="sxs-lookup"><span data-stu-id="275bd-108">This could be a long running operation as it may have to search through millions of files in trash and could be run as a job.</span></span>
<span data-ttu-id="275bd-109">Figyelem: A fájlok törlése a legjobb munkamennyiség-művelet.</span><span class="sxs-lookup"><span data-stu-id="275bd-109">Caution: Undeleting files is a best effort operation.</span></span> <span data-ttu-id="275bd-110">Nincs garancia arra, hogy a fájlok a törlés után visszaállíthatóak.</span><span class="sxs-lookup"><span data-stu-id="275bd-110">There are no guarantees that a file can be restored once it is deleted.</span></span> <span data-ttu-id="275bd-111">Az API használata az engedélyezési listán keresztül engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="275bd-111">The use of this API is enabled via whitelisting.</span></span> <span data-ttu-id="275bd-112">Ha az ADL-fiókja nincs whitelisted listán, akkor az api használata kivételt képez a Nem megvalósított kivételtől.</span><span class="sxs-lookup"><span data-stu-id="275bd-112">If your ADL account is not whitelisted, then using this api will throw Not implemented exception.</span></span> <span data-ttu-id="275bd-113">További információért és segítségért forduljon a Microsoft ügyfélszolgálatához.</span><span class="sxs-lookup"><span data-stu-id="275bd-113">For further information and assistance please contact Microsoft support.</span></span>

## <span data-ttu-id="275bd-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="275bd-114">EXAMPLES</span></span>

### <span data-ttu-id="275bd-115">Példa: Fájl részleteinek lekérte a Data Lake Store-ból</span><span class="sxs-lookup"><span data-stu-id="275bd-115">Example: Get details of a file from the Data Lake Store</span></span>
```
PS> Get-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Filter test0/file_123

TrashDirPath                         OriginalPath                                          Type CreationTime
------------                         ------------                                          ---- ------------
cd6ad5ce-792b-4812-8a33-8f9ed19eb532 adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 FILE 2/8/2019 8:12:18 AM
356cfd42-39c7-451e-96cb-9f47883d91e2 adl://ml1ptrashtest.azuredatalake.com/test0/file_1232 FILE 2/8/2019 8:12:18 AM
e7b30ac8-2dbc-43a3-8ca6-2d420ac0c488 adl://ml1ptrashtest.azuredatalake.com/test0/file_1237 FILE 2/8/2019 8:12:18 AM
```

## <span data-ttu-id="275bd-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="275bd-116">PARAMETERS</span></span>

### <span data-ttu-id="275bd-117">-Account</span><span class="sxs-lookup"><span data-stu-id="275bd-117">-Account</span></span>
<span data-ttu-id="275bd-118">A Data Lake Store-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="275bd-118">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="275bd-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="275bd-119">-AsJob</span></span>
<span data-ttu-id="275bd-120">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="275bd-120">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="275bd-121">-Count</span><span class="sxs-lookup"><span data-stu-id="275bd-121">-Count</span></span>
<span data-ttu-id="275bd-122">Azt adja meg, hogy a felhasználó hány találatot szeretne megtalálni.</span><span class="sxs-lookup"><span data-stu-id="275bd-122">Specifies the number of results the user wants to find.</span></span> <span data-ttu-id="275bd-123">A lekérdezés addig fut, amíg meg nem találja a Count találatokat, vagy a teljes kukában keres (amelyik előbb megtörténik).</span><span class="sxs-lookup"><span data-stu-id="275bd-123">The query runs until it finds Count results or it searches through entire trash, whichever happens first.</span></span>

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

### <span data-ttu-id="275bd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="275bd-124">-DefaultProfile</span></span>
<span data-ttu-id="275bd-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="275bd-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="275bd-126">-Filter</span><span class="sxs-lookup"><span data-stu-id="275bd-126">-Filter</span></span>
<span data-ttu-id="275bd-127">A keresési lekérdezést adja meg.</span><span class="sxs-lookup"><span data-stu-id="275bd-127">Specifies the search query.</span></span> <span data-ttu-id="275bd-128">Egy konkrétabb érték relevánsabb eredményt ad.</span><span class="sxs-lookup"><span data-stu-id="275bd-128">A more specific value gives more relevant results.</span></span>

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

### <span data-ttu-id="275bd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="275bd-129">CommonParameters</span></span>
<span data-ttu-id="275bd-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="275bd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="275bd-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="275bd-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="275bd-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="275bd-132">INPUTS</span></span>

### <span data-ttu-id="275bd-133">System.String</span><span class="sxs-lookup"><span data-stu-id="275bd-133">System.String</span></span>

## <span data-ttu-id="275bd-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="275bd-134">OUTPUTS</span></span>

### <span data-ttu-id="275bd-135">System.Collections.Generic.List<Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem></span><span class="sxs-lookup"><span data-stu-id="275bd-135">System.Collections.Generic.List<Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem></span></span>

## <span data-ttu-id="275bd-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="275bd-136">NOTES</span></span>

## <span data-ttu-id="275bd-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="275bd-137">RELATED LINKS</span></span>

[<span data-ttu-id="275bd-138">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="275bd-138">Restore-AzDataLakeStoreDeletedItem</span></span>](./Restore-AzDataLakeStoreDeletedItem.md)