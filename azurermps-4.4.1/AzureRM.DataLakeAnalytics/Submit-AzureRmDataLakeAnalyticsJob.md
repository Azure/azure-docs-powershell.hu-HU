---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: bb0ad536d738facdfe50bc7983517f4505ab4ef2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500072"
---
# <span data-ttu-id="5d1f9-101">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5d1f9-101">Submit-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="5d1f9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5d1f9-102">SYNOPSIS</span></span>
<span data-ttu-id="5d1f9-103">Feladatot küldhet el.</span><span class="sxs-lookup"><span data-stu-id="5d1f9-103">Submits a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d1f9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5d1f9-104">SYNTAX</span></span>

### <span data-ttu-id="5d1f9-105">Feladat elvégzése az U-SQL parancsfájl elérési útján</span><span class="sxs-lookup"><span data-stu-id="5d1f9-105">Submit job with script path for U-SQL</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d1f9-106">U-SQL-feladat beadása</span><span class="sxs-lookup"><span data-stu-id="5d1f9-106">Submit U-SQL Job</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d1f9-107">Az reucurrence-adatokkal rendelkező U-SQL parancsfájl-elérési útjának elvégzése</span><span class="sxs-lookup"><span data-stu-id="5d1f9-107">Submit job with script path for U-SQL with reucurrence information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d1f9-108">E-SQL-feladat beadása ismétlődési adatokkal</span><span class="sxs-lookup"><span data-stu-id="5d1f9-108">Submit U-SQL Job with recurrence information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d1f9-109">Az U-SQL parancsfájl-elérési útjának elvégzése a reucurrence és a pipeline-adatokkal</span><span class="sxs-lookup"><span data-stu-id="5d1f9-109">Submit job with script path for U-SQL with reucurrence and pipeline information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5d1f9-110">U-SQL-feladat beadása ismétlődési és pipeline-adatokkal</span><span class="sxs-lookup"><span data-stu-id="5d1f9-110">Submit U-SQL Job with recurrence and pipeline information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d1f9-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="5d1f9-111">DESCRIPTION</span></span>
<span data-ttu-id="5d1f9-112">A **Submit-AzureRmDataLakeAnalyticsJob** parancsmag az Azure Data-tó Analytics-feladatát továbbítja.</span><span class="sxs-lookup"><span data-stu-id="5d1f9-112">The **Submit-AzureRmDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="5d1f9-113">Példák</span><span class="sxs-lookup"><span data-stu-id="5d1f9-113">EXAMPLES</span></span>

### <span data-ttu-id="5d1f9-114">1. példa: feladat elvégzése</span><span class="sxs-lookup"><span data-stu-id="5d1f9-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -DegreeOfParallelism 32
```

<span data-ttu-id="5d1f9-115">Ez a parancs egy adattói Analytics-feladatot küldött.</span><span class="sxs-lookup"><span data-stu-id="5d1f9-115">This command submits a Data Lake Analytics job.</span></span>

## <span data-ttu-id="5d1f9-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5d1f9-116">PARAMETERS</span></span>

### <span data-ttu-id="5d1f9-117">-Fiók</span><span class="sxs-lookup"><span data-stu-id="5d1f9-117">-Account</span></span>
<span data-ttu-id="5d1f9-118">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d1f9-118">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="5d1f9-119">-CompileMode</span><span class="sxs-lookup"><span data-stu-id="5d1f9-119">-CompileMode</span></span>
<span data-ttu-id="5d1f9-120">A feladat fordítási módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d1f9-120">Specifies the compilation mode of the job.</span></span>
<span data-ttu-id="5d1f9-121">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="5d1f9-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5d1f9-122">Szemantikai</span><span class="sxs-lookup"><span data-stu-id="5d1f9-122">Semantic</span></span>
- <span data-ttu-id="5d1f9-123">Teljes</span><span class="sxs-lookup"><span data-stu-id="5d1f9-123">Full</span></span>
- <span data-ttu-id="5d1f9-124">SingleBox</span><span class="sxs-lookup"><span data-stu-id="5d1f9-124">SingleBox</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Semantic, Full, SingleBox

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d1f9-125">-CompileOnly</span><span class="sxs-lookup"><span data-stu-id="5d1f9-125">-CompileOnly</span></span>
<span data-ttu-id="5d1f9-126">Jelzi, hogy ez a parancsmag a feladatot a Futtatás nélkül fordítja le.</span><span class="sxs-lookup"><span data-stu-id="5d1f9-126">Indicates that this cmdlet compiles the job without running it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d1f9-127">-DegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="5d1f9-127">-DegreeOfParallelism</span></span>
<span data-ttu-id="5d1f9-128">A projekt adattó-elemzési egységeit (DLAU) adja meg, amely a feladat maximálisan megengedhető párhuzamosságát jelzi.</span><span class="sxs-lookup"><span data-stu-id="5d1f9-128">Specifies the Data Lake Analytics Units (DLAU) of the job, which indicates the maximum allowable parallelism of the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d1f9-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5d1f9-129">-Name</span></span>
<span data-ttu-id="5d1f9-130">A feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d1f9-130">Specifies the job name.</span></span>

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

### <span data-ttu-id="5d1f9-131">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="5d1f9-131">-PipelineId</span></span>
<span data-ttu-id="5d1f9-132">A feladat beküldését jelző azonosító a munkafolyamathoz kapcsolódó ismétlődő feladatok, valamint a munkafolyamathoz kapcsolódó munka része.</span><span class="sxs-lookup"><span data-stu-id="5d1f9-132">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d1f9-133">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="5d1f9-133">-PipelineName</span></span>
<span data-ttu-id="5d1f9-134">A projekthez társított pipeline számára választható felhasználóbarát név.</span><span class="sxs-lookup"><span data-stu-id="5d1f9-134">An optional friendly name for the pipeline associated with this job.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d1f9-135">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="5d1f9-135">-PipelineUri</span></span>
<span data-ttu-id="5d1f9-136">Egy opcionális URI, amely a csővezetékhez társított származó szolgáltatásra hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="5d1f9-136">An optional uri that links to the originating service associated with this pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d1f9-137">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="5d1f9-137">-Priority</span></span>
<span data-ttu-id="5d1f9-138">A feladat prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d1f9-138">Specifies the priority of the job.</span></span>
<span data-ttu-id="5d1f9-139">Ha nincs megadva, a prioritás a 1000.</span><span class="sxs-lookup"><span data-stu-id="5d1f9-139">If not specified, the priority is 1000.</span></span>
<span data-ttu-id="5d1f9-140">A kis szám magasabb prioritást jelez.</span><span class="sxs-lookup"><span data-stu-id="5d1f9-140">A low number indicates a higher job priority.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d1f9-141">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="5d1f9-141">-RecurrenceId</span></span>
<span data-ttu-id="5d1f9-142">A feladat beküldését jelző azonosító egy olyan ismétlődő feladat része, amely ugyanazzal az ismétlődési AZONOSÍTÓval rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="5d1f9-142">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Submit job with script path for U-SQL with reucurrence information, Submit U-SQL Job with recurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d1f9-143">-RecurrenceName</span><span class="sxs-lookup"><span data-stu-id="5d1f9-143">-RecurrenceName</span></span>
<span data-ttu-id="5d1f9-144">Választható rövid név a feladatok közötti ismétlődési korrelációhoz.</span><span class="sxs-lookup"><span data-stu-id="5d1f9-144">An optional friendly name for the recurrence correlation between jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence information, Submit U-SQL Job with recurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d1f9-145">-RunId</span><span class="sxs-lookup"><span data-stu-id="5d1f9-145">-RunId</span></span>
<span data-ttu-id="5d1f9-146">Egy azonosító, amely azonosítja a folyamat adott futási közelítését.</span><span class="sxs-lookup"><span data-stu-id="5d1f9-146">An ID that identifies this specific run iteration of the pipeline.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d1f9-147">-Futtatókörnyezet</span><span class="sxs-lookup"><span data-stu-id="5d1f9-147">-Runtime</span></span>
<span data-ttu-id="5d1f9-148">A feladat futásidejű verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d1f9-148">Specifies the runtime version of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d1f9-149">-Script</span><span class="sxs-lookup"><span data-stu-id="5d1f9-149">-Script</span></span>
<span data-ttu-id="5d1f9-150">A futtatandó parancsfájl tartalmát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d1f9-150">Specifies the contents of the script to run.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit U-SQL Job, Submit U-SQL Job with recurrence information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d1f9-151">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="5d1f9-151">-ScriptPath</span></span>
<span data-ttu-id="5d1f9-152">A futtatandó parancsfájl helyi fájlelérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d1f9-152">Specifies the local file path to the script to run.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL, Submit job with script path for U-SQL with reucurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d1f9-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d1f9-153">-DefaultProfile</span></span>
<span data-ttu-id="5d1f9-154">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5d1f9-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d1f9-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d1f9-155">CommonParameters</span></span>
<span data-ttu-id="5d1f9-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5d1f9-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d1f9-157">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d1f9-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d1f9-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d1f9-158">INPUTS</span></span>

### <span data-ttu-id="5d1f9-159">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="5d1f9-159">String</span></span>
<span data-ttu-id="5d1f9-160">A ' script ' paraméter a pipeline "string" típusú értékét fogadja el.</span><span class="sxs-lookup"><span data-stu-id="5d1f9-160">Parameter 'Script' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="5d1f9-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d1f9-161">OUTPUTS</span></span>

### <span data-ttu-id="5d1f9-162">JobInformation</span><span class="sxs-lookup"><span data-stu-id="5d1f9-162">JobInformation</span></span>
<span data-ttu-id="5d1f9-163">Az elküldött feladat kezdeti munkarészletei.</span><span class="sxs-lookup"><span data-stu-id="5d1f9-163">The initial job details for the submitted job.</span></span>

## <span data-ttu-id="5d1f9-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5d1f9-164">NOTES</span></span>

## <span data-ttu-id="5d1f9-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d1f9-165">RELATED LINKS</span></span>

[<span data-ttu-id="5d1f9-166">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5d1f9-166">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="5d1f9-167">Stop-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5d1f9-167">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="5d1f9-168">Várjon-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5d1f9-168">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


