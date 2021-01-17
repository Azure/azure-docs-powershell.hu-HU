---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobrecurrence
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobRecurrence.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobRecurrence.md
ms.openlocfilehash: d571eb887069aa5c28029dfa98ab022c1d82fc88
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353213"
---
# <span data-ttu-id="e3ecf-101">Get-AzDataLakeAnalyticsJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="e3ecf-101">Get-AzDataLakeAnalyticsJobRecurrence</span></span>

## <span data-ttu-id="e3ecf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3ecf-102">SYNOPSIS</span></span>
<span data-ttu-id="e3ecf-103">A Data Lake Analytics-feladat ismétlődési vagy ismétlődési feladatot kap.</span><span class="sxs-lookup"><span data-stu-id="e3ecf-103">Gets a Data Lake Analytics Job recurrence or recurrences.</span></span>

## <span data-ttu-id="e3ecf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e3ecf-104">SYNTAX</span></span>

### <span data-ttu-id="e3ecf-105">GetAllInAccount (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e3ecf-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobRecurrence [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3ecf-106">GetBySpecificJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="e3ecf-106">GetBySpecificJobRecurrence</span></span>
```
Get-AzDataLakeAnalyticsJobRecurrence [-Account] <String> [-RecurrenceId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3ecf-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e3ecf-107">DESCRIPTION</span></span>
<span data-ttu-id="e3ecf-108">A **Get-AzDataLakeAnalytics JobRecurrerence** egy megadott Azure Data Lake Analytics Job ismétlődési feladatot vagy az ismétlődés listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="e3ecf-108">The **Get-AzDataLakeAnalyticsJobRecurrence** gets a specified Azure Data Lake Analytics Job recurrence or a list of recurrence.</span></span>

## <span data-ttu-id="e3ecf-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e3ecf-109">EXAMPLES</span></span>

### <span data-ttu-id="e3ecf-110">1. példa: Megadott ismétlődés</span><span class="sxs-lookup"><span data-stu-id="e3ecf-110">Example 1: Get a specified recurrence</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobRecurrence -Account "contosoadla" -RecurrenceId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="e3ecf-111">Ez a parancs a megadott feladat ismétlődését kapja a "contosoadla" fiókban a következő azonosítóval: '83cb7ad2-3523-4b82-b909-d478b0d8aea3'.</span><span class="sxs-lookup"><span data-stu-id="e3ecf-111">This command gets the specified job recurrence with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="e3ecf-112">2. példa: A fiókban ismétlődéseket felsoroló lista</span><span class="sxs-lookup"><span data-stu-id="e3ecf-112">Example 2: Get a list of all recurrences in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobRecurrence -AccountName "contosoadla"
```

<span data-ttu-id="e3ecf-113">Ez a parancs az összes ismétlődés listáját lekérte a "contosoadla" fiókban</span><span class="sxs-lookup"><span data-stu-id="e3ecf-113">This command gets a list of all recurrences in the account "contosoadla"</span></span>

## <span data-ttu-id="e3ecf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3ecf-114">PARAMETERS</span></span>

### <span data-ttu-id="e3ecf-115">-Account</span><span class="sxs-lookup"><span data-stu-id="e3ecf-115">-Account</span></span>
<span data-ttu-id="e3ecf-116">Annak a Data Lake Analytics-fióknak a neve, amely alatt be szeretné olvasni a feladat ismétlődését.</span><span class="sxs-lookup"><span data-stu-id="e3ecf-116">Name of the Data Lake Analytics account name under which want to retrieve the job recurrence.</span></span>

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

### <span data-ttu-id="e3ecf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3ecf-117">-DefaultProfile</span></span>
<span data-ttu-id="e3ecf-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e3ecf-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3ecf-119">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="e3ecf-119">-RecurrenceId</span></span>
<span data-ttu-id="e3ecf-120">A feladat ismétlődésének azonosítója, amelyről információt ad vissza.</span><span class="sxs-lookup"><span data-stu-id="e3ecf-120">ID of the specific job recurrence to return information for.</span></span>

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

### <span data-ttu-id="e3ecf-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="e3ecf-121">-SubmittedAfter</span></span>
<span data-ttu-id="e3ecf-122">Egy választható szűrő, amely csak a megadott idő után elküldve adja vissza a feladat ismétlődését.</span><span class="sxs-lookup"><span data-stu-id="e3ecf-122">An optional filter which returns job recurrence(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="e3ecf-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="e3ecf-123">-SubmittedBefore</span></span>
<span data-ttu-id="e3ecf-124">Egy választható szűrő, amely csak a megadott időpont előtt elküldve adja vissza a feladat ismétlődését.</span><span class="sxs-lookup"><span data-stu-id="e3ecf-124">An optional filter which returns job recurrence(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="e3ecf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3ecf-125">CommonParameters</span></span>
<span data-ttu-id="e3ecf-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3ecf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3ecf-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3ecf-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3ecf-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e3ecf-128">INPUTS</span></span>

### <span data-ttu-id="e3ecf-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e3ecf-129">System.String</span></span>

### <span data-ttu-id="e3ecf-130">System.Guid</span><span class="sxs-lookup"><span data-stu-id="e3ecf-130">System.Guid</span></span>

### <span data-ttu-id="e3ecf-131">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e3ecf-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e3ecf-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3ecf-132">OUTPUTS</span></span>

### <span data-ttu-id="e3ecf-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSCurRecurrenceInformation</span><span class="sxs-lookup"><span data-stu-id="e3ecf-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobRecurrenceInformation</span></span>

## <span data-ttu-id="e3ecf-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e3ecf-134">NOTES</span></span>

## <span data-ttu-id="e3ecf-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3ecf-135">RELATED LINKS</span></span>
