---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsjobpipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobPipeline.md
ms.openlocfilehash: c17a58cee2b5f13345997b97ce00792a8b9c9a0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502136"
---
# <span data-ttu-id="30d72-101">Get-AzureRmDataLakeAnalyticsJobPipeline</span><span class="sxs-lookup"><span data-stu-id="30d72-101">Get-AzureRmDataLakeAnalyticsJobPipeline</span></span>

## <span data-ttu-id="30d72-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="30d72-102">SYNOPSIS</span></span>
<span data-ttu-id="30d72-103">Adatforrást kap az adattó-munkafolyamatok és a csővezetékek között.</span><span class="sxs-lookup"><span data-stu-id="30d72-103">Gets a Data Lake Analytics Job pipeline or pipelines.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30d72-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="30d72-104">SYNTAX</span></span>

### <span data-ttu-id="30d72-105">GetAllInAccount (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="30d72-105">GetAllInAccount (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJobPipeline [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30d72-106">GetBySpecificJobPipeline</span><span class="sxs-lookup"><span data-stu-id="30d72-106">GetBySpecificJobPipeline</span></span>
```
Get-AzureRmDataLakeAnalyticsJobPipeline [-Account] <String> [-PipelineId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30d72-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="30d72-107">DESCRIPTION</span></span>
<span data-ttu-id="30d72-108">A **Get-AzureRmDataLakeAnalyticsJobPipeline** megkapja a megadott Azure Data Lake Analytics-munkafolyamatot vagy a csővezetékek listáját.</span><span class="sxs-lookup"><span data-stu-id="30d72-108">The **Get-AzureRmDataLakeAnalyticsJobPipeline** gets a specified Azure Data Lake Analytics Job pipeline or a list of pipelines.</span></span>

## <span data-ttu-id="30d72-109">Példák</span><span class="sxs-lookup"><span data-stu-id="30d72-109">EXAMPLES</span></span>

### <span data-ttu-id="30d72-110">1. példa: megadott csővezeték beszerzése</span><span class="sxs-lookup"><span data-stu-id="30d72-110">Example 1: Get a specified pipeline</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobPipeline -Account "contosoadla" -PipelineId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="30d72-111">Ez a parancs a "83cb7ad2-3523-4b82-b909-d478b0d8aea3" azonosítójú "contosoadla" azonosítójú megadott csővezetéket kapja.</span><span class="sxs-lookup"><span data-stu-id="30d72-111">This command gets the specified pipeline with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="30d72-112">2. példa: a fiók összes futószalagjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="30d72-112">Example 2: Get a list of all pipelines in the account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobPipeline -AccountName "contosoadla"
```

<span data-ttu-id="30d72-113">Ez a parancs a "contosoadla" fiók összes futószalagjának listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="30d72-113">This command gets a list of all pipelines in the account "contosoadla"</span></span>

## <span data-ttu-id="30d72-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="30d72-114">PARAMETERS</span></span>

### <span data-ttu-id="30d72-115">-Fiók</span><span class="sxs-lookup"><span data-stu-id="30d72-115">-Account</span></span>
<span data-ttu-id="30d72-116">Annak az adattó-fióknak a neve, amely alatt a munkafolyamatot le szeretné olvasni.</span><span class="sxs-lookup"><span data-stu-id="30d72-116">Name of the Data Lake Analytics account name under which want to retrieve the job pipeline.</span></span>

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

### <span data-ttu-id="30d72-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30d72-117">-DefaultProfile</span></span>
<span data-ttu-id="30d72-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="30d72-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30d72-119">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="30d72-119">-PipelineId</span></span>
<span data-ttu-id="30d72-120">Annak az adott projekt-csővezetéknek az azonosítója, amelybe az adatokat vissza szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="30d72-120">ID of the specific job pipeline to return information for.</span></span>

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

### <span data-ttu-id="30d72-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="30d72-121">-SubmittedAfter</span></span>
<span data-ttu-id="30d72-122">Egy opcionális szűrő, amely csak a megadott idő után küldi el a munkafolyamatot (ka) t.</span><span class="sxs-lookup"><span data-stu-id="30d72-122">An optional filter which returns job pipeline(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="30d72-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="30d72-123">-SubmittedBefore</span></span>
<span data-ttu-id="30d72-124">Egy opcionális szűrő, amely csak a megadott idő előtt küldi el a munkafolyamatot (ka) t.</span><span class="sxs-lookup"><span data-stu-id="30d72-124">An optional filter which returns job pipeline(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="30d72-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30d72-125">CommonParameters</span></span>
<span data-ttu-id="30d72-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="30d72-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30d72-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30d72-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30d72-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="30d72-128">INPUTS</span></span>

### <span data-ttu-id="30d72-129">System. String</span><span class="sxs-lookup"><span data-stu-id="30d72-129">System.String</span></span>

### <span data-ttu-id="30d72-130">System. GUID</span><span class="sxs-lookup"><span data-stu-id="30d72-130">System.Guid</span></span>

### <span data-ttu-id="30d72-131">System. null ' 1 [[System. DateTimeOffset, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="30d72-131">System.Nullable\`1[[System.DateTimeOffset, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="30d72-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30d72-132">OUTPUTS</span></span>

### <span data-ttu-id="30d72-133">Microsoft. Azure. Command. DataLakeAnalytics. models. PSJobPipelineInformation</span><span class="sxs-lookup"><span data-stu-id="30d72-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span></span>

## <span data-ttu-id="30d72-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="30d72-134">NOTES</span></span>

## <span data-ttu-id="30d72-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30d72-135">RELATED LINKS</span></span>