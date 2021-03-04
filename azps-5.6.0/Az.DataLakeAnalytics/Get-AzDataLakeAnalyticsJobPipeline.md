---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobpipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
ms.openlocfilehash: 9e925e1bd118a9ac5f676ee666cb945f22d1ffac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937033"
---
# <span data-ttu-id="cb9dd-101">Get-AzDataLakeAnalyticsJobPipeline</span><span class="sxs-lookup"><span data-stu-id="cb9dd-101">Get-AzDataLakeAnalyticsJobPipeline</span></span>

## <span data-ttu-id="cb9dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb9dd-102">SYNOPSIS</span></span>
<span data-ttu-id="cb9dd-103">Data Lake Analytics Job-folyamatot vagy -prognózist kap.</span><span class="sxs-lookup"><span data-stu-id="cb9dd-103">Gets a Data Lake Analytics Job pipeline or pipelines.</span></span>

## <span data-ttu-id="cb9dd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cb9dd-104">SYNTAX</span></span>

### <span data-ttu-id="cb9dd-105">GetAllInAccount (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cb9dd-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb9dd-106">GetBySpecificAdvaPipeline</span><span class="sxs-lookup"><span data-stu-id="cb9dd-106">GetBySpecificJobPipeline</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-PipelineId] <Guid> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb9dd-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cb9dd-107">DESCRIPTION</span></span>
<span data-ttu-id="cb9dd-108">A **Get-AzDataLakeAnalytics JobPipeline** egy megadott Azure Data Lake Analytics Job-folyamathoz vagy a folyamatok listájához jut.</span><span class="sxs-lookup"><span data-stu-id="cb9dd-108">The **Get-AzDataLakeAnalyticsJobPipeline** gets a specified Azure Data Lake Analytics Job pipeline or a list of pipelines.</span></span>

## <span data-ttu-id="cb9dd-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cb9dd-109">EXAMPLES</span></span>

### <span data-ttu-id="cb9dd-110">1. példa: Adott folyamat lekérte</span><span class="sxs-lookup"><span data-stu-id="cb9dd-110">Example 1: Get a specified pipeline</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -Account "contosoadla" -PipelineId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="cb9dd-111">Ez a parancs a megadott, '83cb7ad2-3523-4b82-b909-d478b0d8aea3' azonosítójú prognózist kapja a "contosoadla" fiókban.</span><span class="sxs-lookup"><span data-stu-id="cb9dd-111">This command gets the specified pipeline with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="cb9dd-112">2. példa: A fiókban található összes folyamat listájának lekérte</span><span class="sxs-lookup"><span data-stu-id="cb9dd-112">Example 2: Get a list of all pipelines in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -AccountName "contosoadla"
```

<span data-ttu-id="cb9dd-113">Ez a parancs a "contosoadla" fiók összes folyamatának listáját lekérte</span><span class="sxs-lookup"><span data-stu-id="cb9dd-113">This command gets a list of all pipelines in the account "contosoadla"</span></span>

## <span data-ttu-id="cb9dd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb9dd-114">PARAMETERS</span></span>

### <span data-ttu-id="cb9dd-115">-Account</span><span class="sxs-lookup"><span data-stu-id="cb9dd-115">-Account</span></span>
<span data-ttu-id="cb9dd-116">Annak a Data Lake Analytics-fióknak a neve, amely alatt be szeretné olvasni a feladat prognózisát.</span><span class="sxs-lookup"><span data-stu-id="cb9dd-116">Name of the Data Lake Analytics account name under which want to retrieve the job pipeline.</span></span>

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

### <span data-ttu-id="cb9dd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb9dd-117">-DefaultProfile</span></span>
<span data-ttu-id="cb9dd-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cb9dd-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb9dd-119">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="cb9dd-119">-PipelineId</span></span>
<span data-ttu-id="cb9dd-120">Annak az adott folyamatnak az azonosítója, amely adatait vissza kell visszaadni.</span><span class="sxs-lookup"><span data-stu-id="cb9dd-120">ID of the specific job pipeline to return information for.</span></span>

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

### <span data-ttu-id="cb9dd-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="cb9dd-121">-SubmittedAfter</span></span>
<span data-ttu-id="cb9dd-122">Egy választható szűrő, amely csak a megadott idő után adja vissza a feladat prognózisát.</span><span class="sxs-lookup"><span data-stu-id="cb9dd-122">An optional filter which returns job pipeline(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="cb9dd-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="cb9dd-123">-SubmittedBefore</span></span>
<span data-ttu-id="cb9dd-124">Egy választható szűrő, amely csak a megadott időpont előtt elküldve adja vissza a feladat prognózisát.</span><span class="sxs-lookup"><span data-stu-id="cb9dd-124">An optional filter which returns job pipeline(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="cb9dd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb9dd-125">CommonParameters</span></span>
<span data-ttu-id="cb9dd-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb9dd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb9dd-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb9dd-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb9dd-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cb9dd-128">INPUTS</span></span>

### <span data-ttu-id="cb9dd-129">System.String</span><span class="sxs-lookup"><span data-stu-id="cb9dd-129">System.String</span></span>

### <span data-ttu-id="cb9dd-130">System.Guid</span><span class="sxs-lookup"><span data-stu-id="cb9dd-130">System.Guid</span></span>

### <span data-ttu-id="cb9dd-131">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="cb9dd-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="cb9dd-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb9dd-132">OUTPUTS</span></span>

### <span data-ttu-id="cb9dd-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSVpPipelineInformation</span><span class="sxs-lookup"><span data-stu-id="cb9dd-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span></span>

## <span data-ttu-id="cb9dd-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cb9dd-134">NOTES</span></span>

## <span data-ttu-id="cb9dd-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb9dd-135">RELATED LINKS</span></span>
