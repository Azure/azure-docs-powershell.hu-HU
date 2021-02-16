---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobpipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
ms.openlocfilehash: 1d13d1b6e55831c972457c5a6a5aadc427ecb3a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148162"
---
# <span data-ttu-id="5110c-101">Get-AzDataLakeAnalyticsJobPipeline</span><span class="sxs-lookup"><span data-stu-id="5110c-101">Get-AzDataLakeAnalyticsJobPipeline</span></span>

## <span data-ttu-id="5110c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5110c-102">SYNOPSIS</span></span>
<span data-ttu-id="5110c-103">Data Lake Analytics Job-folyamatot vagy -prognózist kap.</span><span class="sxs-lookup"><span data-stu-id="5110c-103">Gets a Data Lake Analytics Job pipeline or pipelines.</span></span>

## <span data-ttu-id="5110c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5110c-104">SYNTAX</span></span>

### <span data-ttu-id="5110c-105">GetAllInAccount (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5110c-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5110c-106">GetBySpecificAdvaPipeline</span><span class="sxs-lookup"><span data-stu-id="5110c-106">GetBySpecificJobPipeline</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-PipelineId] <Guid> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5110c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5110c-107">DESCRIPTION</span></span>
<span data-ttu-id="5110c-108">A **Get-AzDataLakeAnalytics JobPipeline** egy megadott Azure Data Lake Analytics Job-folyamathoz vagy a folyamatok listájához jut.</span><span class="sxs-lookup"><span data-stu-id="5110c-108">The **Get-AzDataLakeAnalyticsJobPipeline** gets a specified Azure Data Lake Analytics Job pipeline or a list of pipelines.</span></span>

## <span data-ttu-id="5110c-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5110c-109">EXAMPLES</span></span>

### <span data-ttu-id="5110c-110">1. példa: Adott folyamat lekérte</span><span class="sxs-lookup"><span data-stu-id="5110c-110">Example 1: Get a specified pipeline</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -Account "contosoadla" -PipelineId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="5110c-111">Ez a parancs a megadott, '83cb7ad2-3523-4b82-b909-d478b0d8aea3' azonosítójú prognózist kapja a "contosoadla" fiókban.</span><span class="sxs-lookup"><span data-stu-id="5110c-111">This command gets the specified pipeline with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="5110c-112">2. példa: A fiókban található összes folyamat listájának lekérte</span><span class="sxs-lookup"><span data-stu-id="5110c-112">Example 2: Get a list of all pipelines in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -AccountName "contosoadla"
```

<span data-ttu-id="5110c-113">Ez a parancs a "contosoadla" fiók összes folyamatának listáját lekérte.</span><span class="sxs-lookup"><span data-stu-id="5110c-113">This command gets a list of all pipelines in the account "contosoadla"</span></span>

## <span data-ttu-id="5110c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5110c-114">PARAMETERS</span></span>

### <span data-ttu-id="5110c-115">-Account</span><span class="sxs-lookup"><span data-stu-id="5110c-115">-Account</span></span>
<span data-ttu-id="5110c-116">Annak a Data Lake Analytics-fióknak a neve, amely alatt be szeretné olvasni a feladat prognózisát.</span><span class="sxs-lookup"><span data-stu-id="5110c-116">Name of the Data Lake Analytics account name under which want to retrieve the job pipeline.</span></span>

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

### <span data-ttu-id="5110c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5110c-117">-DefaultProfile</span></span>
<span data-ttu-id="5110c-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5110c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5110c-119">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="5110c-119">-PipelineId</span></span>
<span data-ttu-id="5110c-120">Annak az adott folyamatnak az azonosítója, amely adatait vissza kell adni.</span><span class="sxs-lookup"><span data-stu-id="5110c-120">ID of the specific job pipeline to return information for.</span></span>

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobPipeline
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5110c-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="5110c-121">-SubmittedAfter</span></span>
<span data-ttu-id="5110c-122">Egy választható szűrő, amely csak a megadott idő után adja vissza a feladat prognózisát.</span><span class="sxs-lookup"><span data-stu-id="5110c-122">An optional filter which returns job pipeline(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="5110c-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="5110c-123">-SubmittedBefore</span></span>
<span data-ttu-id="5110c-124">Egy választható szűrő, amely csak a megadott időpont előtt elküldve adja vissza a feladat prognózisát.</span><span class="sxs-lookup"><span data-stu-id="5110c-124">An optional filter which returns job pipeline(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="5110c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5110c-125">CommonParameters</span></span>
<span data-ttu-id="5110c-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5110c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5110c-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5110c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5110c-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5110c-128">INPUTS</span></span>

### <span data-ttu-id="5110c-129">System.String</span><span class="sxs-lookup"><span data-stu-id="5110c-129">System.String</span></span>

### <span data-ttu-id="5110c-130">System.Guid</span><span class="sxs-lookup"><span data-stu-id="5110c-130">System.Guid</span></span>

### <span data-ttu-id="5110c-131">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5110c-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5110c-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5110c-132">OUTPUTS</span></span>

### <span data-ttu-id="5110c-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSVpPipelineInformation</span><span class="sxs-lookup"><span data-stu-id="5110c-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span></span>

## <span data-ttu-id="5110c-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5110c-134">NOTES</span></span>

## <span data-ttu-id="5110c-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5110c-135">RELATED LINKS</span></span>
