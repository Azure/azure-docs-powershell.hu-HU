---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/submit-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 429b0a6cec9c7a3f27019e950e5497eac961c81f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935809"
---
# <span data-ttu-id="ca146-101">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ca146-101">Submit-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="ca146-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca146-102">SYNOPSIS</span></span>
<span data-ttu-id="ca146-103">Feladatot küld.</span><span class="sxs-lookup"><span data-stu-id="ca146-103">Submits a job.</span></span>

## <span data-ttu-id="ca146-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ca146-104">SYNTAX</span></span>

### <span data-ttu-id="ca146-105">SubmitUSqlWithScriptPath</span><span class="sxs-lookup"><span data-stu-id="ca146-105">SubmitUSqlJobWithScriptPath</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca146-106">SubmitUSqlJob</span><span class="sxs-lookup"><span data-stu-id="ca146-106">SubmitUSqlJob</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca146-107">SubmitUSqlSqlWithScriptPathAndRecurrence</span><span class="sxs-lookup"><span data-stu-id="ca146-107">SubmitUSqlJobWithScriptPathAndRecurrence</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca146-108">SubmitUSqlWithRecurrence</span><span class="sxs-lookup"><span data-stu-id="ca146-108">SubmitUSqlJobWithRecurrence</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca146-109">SubmitUSqlWithScriptPathAndPipeline</span><span class="sxs-lookup"><span data-stu-id="ca146-109">SubmitUSqlJobWithScriptPathAndPipeline</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ca146-110">SubmitUSqlWithPipeline</span><span class="sxs-lookup"><span data-stu-id="ca146-110">SubmitUSqlJobWithPipeline</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ca146-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ca146-111">DESCRIPTION</span></span>
<span data-ttu-id="ca146-112">A **Submit-AzDataLakeAnalytics Job** parancsmag elküld egy Azure Data Lake Analytics-feladatot.</span><span class="sxs-lookup"><span data-stu-id="ca146-112">The **Submit-AzDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="ca146-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ca146-113">EXAMPLES</span></span>

### <span data-ttu-id="ca146-114">1. példa: Feladat elküldése</span><span class="sxs-lookup"><span data-stu-id="ca146-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32
```

<span data-ttu-id="ca146-115">Ez a parancs egy Data Lake Analytics-feladatot küld.</span><span class="sxs-lookup"><span data-stu-id="ca146-115">This command submits a Data Lake Analytics job.</span></span>

### <span data-ttu-id="ca146-116">2. példa: Feladat elküldése parancsprogram-paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="ca146-116">Example 2: Submit a job with script parameters</span></span>
```
PS C:\>$parameters = [ordered]@{}
$parameters["Department"] = "Sales"
$parameters["NumRecords"] = 1000
$parameters["StartDateTime"] = (Get-Date).AddDays(-14)
Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32 -ScriptParameter $parameters
```

<span data-ttu-id="ca146-117">Az U-SQL-parancsprogram paramétereit a fő parancsfájl tartalma fölé kell írni, például: DECLARE @Department string = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = new DateTime(2017;12;6;0;0;0;0;0);</span><span class="sxs-lookup"><span data-stu-id="ca146-117">U-SQL script parameters are prepended above the main script contents, e.g.: DECLARE @Department string = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = new DateTime(2017, 12, 6, 0, 0, 0, 0);</span></span>

## <span data-ttu-id="ca146-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca146-118">PARAMETERS</span></span>

### <span data-ttu-id="ca146-119">-Account</span><span class="sxs-lookup"><span data-stu-id="ca146-119">-Account</span></span>
<span data-ttu-id="ca146-120">Annak a Data Lake Analytics-fióknak a neve, amelybe a feladatot be fogják nyújtani.</span><span class="sxs-lookup"><span data-stu-id="ca146-120">Name of Data Lake Analytics account under which the job will be submitted.</span></span>

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

### <span data-ttu-id="ca146-121">-AnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="ca146-121">-AnalyticsUnits</span></span>
<span data-ttu-id="ca146-122">Az ehhez a feladathoz használható elemzési egységek.</span><span class="sxs-lookup"><span data-stu-id="ca146-122">The analytics units to use for this job.</span></span> <span data-ttu-id="ca146-123">A parancsfájlhoz dedikált több elemzési egység általában gyorsabb parancsfájlvégrehajtási időt biztosít.</span><span class="sxs-lookup"><span data-stu-id="ca146-123">Typically, more analytics units dedicated to a script results in faster script execution time.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: DegreeOfParallelism

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca146-124">-CompileMode</span><span class="sxs-lookup"><span data-stu-id="ca146-124">-CompileMode</span></span>
<span data-ttu-id="ca146-125">Az ezen a feladaton el kell végezni az összeállítás típusát.</span><span class="sxs-lookup"><span data-stu-id="ca146-125">The type of compilation to be done on this job.</span></span> <span data-ttu-id="ca146-126">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="ca146-126">Valid values:</span></span> 
- <span data-ttu-id="ca146-127">Szemantikus (Csak szemantikus és szükséges sanitás-ellenőrzéseket végez)</span><span class="sxs-lookup"><span data-stu-id="ca146-127">Semantic (Only performs semantic checks and necessary sanity checks)</span></span>
- <span data-ttu-id="ca146-128">Teljes (teljes összeállítás)</span><span class="sxs-lookup"><span data-stu-id="ca146-128">Full (Full compilation)</span></span>
- <span data-ttu-id="ca146-129">SingleBox (A teljes fordítás helyileg történik)</span><span class="sxs-lookup"><span data-stu-id="ca146-129">SingleBox (Full compilation performed locally)</span></span>

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

### <span data-ttu-id="ca146-130">-CompileOnly</span><span class="sxs-lookup"><span data-stu-id="ca146-130">-CompileOnly</span></span>
<span data-ttu-id="ca146-131">Azt jelzi, hogy a beküldésnek csak a feladatot kell felépítenie, és igaz érték esetén nem kell végrehajtania.</span><span class="sxs-lookup"><span data-stu-id="ca146-131">Indicates that the submission should only build the job and not execute if set to true.</span></span>

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

### <span data-ttu-id="ca146-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca146-132">-DefaultProfile</span></span>
<span data-ttu-id="ca146-133">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ca146-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca146-134">-Name</span><span class="sxs-lookup"><span data-stu-id="ca146-134">-Name</span></span>
<span data-ttu-id="ca146-135">A beküldő feladat rövid neve.</span><span class="sxs-lookup"><span data-stu-id="ca146-135">The friendly name of the job to submit.</span></span>

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

### <span data-ttu-id="ca146-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="ca146-136">-PipelineId</span></span>
<span data-ttu-id="ca146-137">A feladat beküldését jelző azonosító az ismétlődő feladatok része, és egy feladat prognózishoz is társítva van.</span><span class="sxs-lookup"><span data-stu-id="ca146-137">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca146-138">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="ca146-138">-PipelineName</span></span>
<span data-ttu-id="ca146-139">A feladathoz társított folyamat opcionális rövid neve.</span><span class="sxs-lookup"><span data-stu-id="ca146-139">An optional friendly name for the pipeline associated with this job.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca146-140">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="ca146-140">-PipelineUri</span></span>
<span data-ttu-id="ca146-141">Egy opcionális uri, amely a prognózissal társított, az eredeti szolgáltatáshoz kapcsolódik.</span><span class="sxs-lookup"><span data-stu-id="ca146-141">An optional uri that links to the originating service associated with this pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca146-142">-Priority</span><span class="sxs-lookup"><span data-stu-id="ca146-142">-Priority</span></span>
<span data-ttu-id="ca146-143">A feladat prioritása.</span><span class="sxs-lookup"><span data-stu-id="ca146-143">The priority of the job.</span></span> <span data-ttu-id="ca146-144">Ha nincs megadva, a prioritás 1000.</span><span class="sxs-lookup"><span data-stu-id="ca146-144">If not specified, the priority is 1000.</span></span> <span data-ttu-id="ca146-145">Az alacsonyabb szám magasabb prioritást jelez.</span><span class="sxs-lookup"><span data-stu-id="ca146-145">A lower number indicates a higher job priority.</span></span>

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

### <span data-ttu-id="ca146-146">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="ca146-146">-RecurrenceId</span></span>
<span data-ttu-id="ca146-147">A feladat beküldését jelző azonosító egy ismétlődő feladat része ugyanazokkal az ismétlődő azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="ca146-147">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca146-148">-RecurrenceName</span><span class="sxs-lookup"><span data-stu-id="ca146-148">-RecurrenceName</span></span>
<span data-ttu-id="ca146-149">A feladatok közötti ismétlődési korreláció opcionális rövid neve.</span><span class="sxs-lookup"><span data-stu-id="ca146-149">An optional friendly name for the recurrence correlation between jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca146-150">-RunId</span><span class="sxs-lookup"><span data-stu-id="ca146-150">-RunId</span></span>
<span data-ttu-id="ca146-151">A folyamat adott futási iterációját azonosító azonosító.</span><span class="sxs-lookup"><span data-stu-id="ca146-151">An ID that identifies this specific run iteration of the pipeline.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca146-152">-Runtime</span><span class="sxs-lookup"><span data-stu-id="ca146-152">-Runtime</span></span>
<span data-ttu-id="ca146-153">Szükség esetén állítsa be a feladathoz használni szükséges futásidejű verziót.</span><span class="sxs-lookup"><span data-stu-id="ca146-153">Optionally set the version of the runtime to use for the job.</span></span> <span data-ttu-id="ca146-154">Ha nincs beállítva, a program az alapértelmezett futásidejű futásiidőt használja.</span><span class="sxs-lookup"><span data-stu-id="ca146-154">If left unset, the default runtime is used.</span></span>

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

### <span data-ttu-id="ca146-155">-Script</span><span class="sxs-lookup"><span data-stu-id="ca146-155">-Script</span></span>
<span data-ttu-id="ca146-156">Végrehajtható parancsfájl (szövegbe írt).</span><span class="sxs-lookup"><span data-stu-id="ca146-156">Script to execute (written inline).</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJob, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithPipeline
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca146-157">-ScriptParameter</span><span class="sxs-lookup"><span data-stu-id="ca146-157">-ScriptParameter</span></span>
<span data-ttu-id="ca146-158">A feladat parancsfájl-paraméterei, paraméternevek (karakterlánc) szótára értékekre (bájt, sbyte, int, uint32), hosszú, ulong (vagy uint64), lebegés, dupla, tizedes, rövid (vagy int16), karakter, karakterlánc, DateTime, bool, Guid vagy bájt[]).</span><span class="sxs-lookup"><span data-stu-id="ca146-158">The script parameters for this job, as a dictionary of parameter names (string) to values (any combination of byte, sbyte, int, uint (or uint32), long, ulong (or uint64), float, double, decimal, short (or int16), ushort (or uint16), char, string, DateTime, bool, Guid, or byte[]).</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca146-159">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="ca146-159">-ScriptPath</span></span>
<span data-ttu-id="ca146-160">A elküldni kívánt parancsfájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="ca146-160">Path to the script file to submit.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPath, SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithScriptPathAndPipeline
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca146-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca146-161">CommonParameters</span></span>
<span data-ttu-id="ca146-162">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca146-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca146-163">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca146-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca146-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ca146-164">INPUTS</span></span>

### <span data-ttu-id="ca146-165">System.String</span><span class="sxs-lookup"><span data-stu-id="ca146-165">System.String</span></span>

### <span data-ttu-id="ca146-166">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ca146-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ca146-167">System.Int32</span><span class="sxs-lookup"><span data-stu-id="ca146-167">System.Int32</span></span>

### <span data-ttu-id="ca146-168">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="ca146-168">System.Collections.IDictionary</span></span>

### <span data-ttu-id="ca146-169">System.Guid</span><span class="sxs-lookup"><span data-stu-id="ca146-169">System.Guid</span></span>

### <span data-ttu-id="ca146-170">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ca146-170">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ca146-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca146-171">OUTPUTS</span></span>

### <span data-ttu-id="ca146-172">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span><span class="sxs-lookup"><span data-stu-id="ca146-172">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="ca146-173">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ca146-173">NOTES</span></span>

## <span data-ttu-id="ca146-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ca146-174">RELATED LINKS</span></span>

[<span data-ttu-id="ca146-175">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ca146-175">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="ca146-176">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ca146-176">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="ca146-177">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ca146-177">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


