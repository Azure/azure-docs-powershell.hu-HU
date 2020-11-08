---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobrecurrence
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobRecurrence.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobRecurrence.md
ms.openlocfilehash: d571eb887069aa5c28029dfa98ab022c1d82fc88
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025408"
---
# <span data-ttu-id="4b5dd-101">Get-AzDataLakeAnalyticsJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="4b5dd-101">Get-AzDataLakeAnalyticsJobRecurrence</span></span>

## <span data-ttu-id="4b5dd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4b5dd-102">SYNOPSIS</span></span>
<span data-ttu-id="4b5dd-103">Beolvassa az adat-tó Analytics-feladatát, vagy ismétlődést kap.</span><span class="sxs-lookup"><span data-stu-id="4b5dd-103">Gets a Data Lake Analytics Job recurrence or recurrences.</span></span>

## <span data-ttu-id="4b5dd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4b5dd-104">SYNTAX</span></span>

### <span data-ttu-id="4b5dd-105">GetAllInAccount (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4b5dd-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobRecurrence [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b5dd-106">GetBySpecificJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="4b5dd-106">GetBySpecificJobRecurrence</span></span>
```
Get-AzDataLakeAnalyticsJobRecurrence [-Account] <String> [-RecurrenceId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b5dd-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4b5dd-107">DESCRIPTION</span></span>
<span data-ttu-id="4b5dd-108">A **Get-AzDataLakeAnalyticsJobRecurrence** megkapja a megadott Azure Data Lake Analytics feladat ismétlődését vagy az ismétlődések listáját.</span><span class="sxs-lookup"><span data-stu-id="4b5dd-108">The **Get-AzDataLakeAnalyticsJobRecurrence** gets a specified Azure Data Lake Analytics Job recurrence or a list of recurrence.</span></span>

## <span data-ttu-id="4b5dd-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4b5dd-109">EXAMPLES</span></span>

### <span data-ttu-id="4b5dd-110">Példa 1: megadott ismétlődés beszerzése</span><span class="sxs-lookup"><span data-stu-id="4b5dd-110">Example 1: Get a specified recurrence</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobRecurrence -Account "contosoadla" -RecurrenceId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="4b5dd-111">Ez a parancs a "83cb7ad2-3523-4b82-b909-d478b0d8aea3" azonosítójú "contosoadla" fiókban a megadott feladat ismétlődését kapja.</span><span class="sxs-lookup"><span data-stu-id="4b5dd-111">This command gets the specified job recurrence with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="4b5dd-112">2. példa: a fiók összes ismétlődésének beszerzése</span><span class="sxs-lookup"><span data-stu-id="4b5dd-112">Example 2: Get a list of all recurrences in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobRecurrence -AccountName "contosoadla"
```

<span data-ttu-id="4b5dd-113">Ez a parancs a "contosoadla" fiók minden ismétlődési listáját beolvassa.</span><span class="sxs-lookup"><span data-stu-id="4b5dd-113">This command gets a list of all recurrences in the account "contosoadla"</span></span>

## <span data-ttu-id="4b5dd-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4b5dd-114">PARAMETERS</span></span>

### <span data-ttu-id="4b5dd-115">-Fiók</span><span class="sxs-lookup"><span data-stu-id="4b5dd-115">-Account</span></span>
<span data-ttu-id="4b5dd-116">Annak az adattó-fióknak a neve, amely alatt a feladat ismétlődését be szeretné olvasni.</span><span class="sxs-lookup"><span data-stu-id="4b5dd-116">Name of the Data Lake Analytics account name under which want to retrieve the job recurrence.</span></span>

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

### <span data-ttu-id="4b5dd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b5dd-117">-DefaultProfile</span></span>
<span data-ttu-id="4b5dd-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4b5dd-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b5dd-119">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="4b5dd-119">-RecurrenceId</span></span>
<span data-ttu-id="4b5dd-120">Az adott feladat ismétlődésének azonosítója az adatok visszaadásához.</span><span class="sxs-lookup"><span data-stu-id="4b5dd-120">ID of the specific job recurrence to return information for.</span></span>

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobRecurrence
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b5dd-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="4b5dd-121">-SubmittedAfter</span></span>
<span data-ttu-id="4b5dd-122">Egy opcionális szűrő, amely visszaadja a feladat ismétlődését (ka) t, és csak a megadott időpont után küldi el.</span><span class="sxs-lookup"><span data-stu-id="4b5dd-122">An optional filter which returns job recurrence(s) only submitted after the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b5dd-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="4b5dd-123">-SubmittedBefore</span></span>
<span data-ttu-id="4b5dd-124">Egy opcionális szűrő, amely csak a megadott idő előtt küldi el a feladat ismétlődését (ka) t.</span><span class="sxs-lookup"><span data-stu-id="4b5dd-124">An optional filter which returns job recurrence(s) only submitted before the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b5dd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b5dd-125">CommonParameters</span></span>
<span data-ttu-id="4b5dd-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4b5dd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b5dd-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b5dd-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b5dd-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b5dd-128">INPUTS</span></span>

### <span data-ttu-id="4b5dd-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4b5dd-129">System.String</span></span>

### <span data-ttu-id="4b5dd-130">System. GUID</span><span class="sxs-lookup"><span data-stu-id="4b5dd-130">System.Guid</span></span>

### <span data-ttu-id="4b5dd-131">System. null ' 1 [[System. DateTimeOffset, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4b5dd-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4b5dd-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b5dd-132">OUTPUTS</span></span>

### <span data-ttu-id="4b5dd-133">Microsoft. Azure. Command. DataLakeAnalytics. models. PSJobRecurrenceInformation</span><span class="sxs-lookup"><span data-stu-id="4b5dd-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobRecurrenceInformation</span></span>

## <span data-ttu-id="4b5dd-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4b5dd-134">NOTES</span></span>

## <span data-ttu-id="4b5dd-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4b5dd-135">RELATED LINKS</span></span>
