---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/submit-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 23c8f8baa2753382ef2ee91f62199966a4fb9c2d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666886"
---
# <span data-ttu-id="62c52-101">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="62c52-101">Submit-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="62c52-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="62c52-102">SYNOPSIS</span></span>
<span data-ttu-id="62c52-103">Feladatot küldhet el.</span><span class="sxs-lookup"><span data-stu-id="62c52-103">Submits a job.</span></span>

## <span data-ttu-id="62c52-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="62c52-104">SYNTAX</span></span>

### <span data-ttu-id="62c52-105">SubmitUSqlJobWithScriptPath</span><span class="sxs-lookup"><span data-stu-id="62c52-105">SubmitUSqlJobWithScriptPath</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62c52-106">SubmitUSqlJob</span><span class="sxs-lookup"><span data-stu-id="62c52-106">SubmitUSqlJob</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62c52-107">SubmitUSqlJobWithScriptPathAndRecurrence</span><span class="sxs-lookup"><span data-stu-id="62c52-107">SubmitUSqlJobWithScriptPathAndRecurrence</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62c52-108">SubmitUSqlJobWithRecurrence</span><span class="sxs-lookup"><span data-stu-id="62c52-108">SubmitUSqlJobWithRecurrence</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62c52-109">SubmitUSqlJobWithScriptPathAndPipeline</span><span class="sxs-lookup"><span data-stu-id="62c52-109">SubmitUSqlJobWithScriptPathAndPipeline</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="62c52-110">SubmitUSqlJobWithPipeline</span><span class="sxs-lookup"><span data-stu-id="62c52-110">SubmitUSqlJobWithPipeline</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="62c52-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="62c52-111">DESCRIPTION</span></span>
<span data-ttu-id="62c52-112">A **Submit-AzDataLakeAnalyticsJob** parancsmag az Azure Data-tó Analytics-feladatát továbbítja.</span><span class="sxs-lookup"><span data-stu-id="62c52-112">The **Submit-AzDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="62c52-113">Példák</span><span class="sxs-lookup"><span data-stu-id="62c52-113">EXAMPLES</span></span>

### <span data-ttu-id="62c52-114">1. példa: feladat elvégzése</span><span class="sxs-lookup"><span data-stu-id="62c52-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32
```

<span data-ttu-id="62c52-115">Ez a parancs egy adattói Analytics-feladatot küldött.</span><span class="sxs-lookup"><span data-stu-id="62c52-115">This command submits a Data Lake Analytics job.</span></span>

### <span data-ttu-id="62c52-116">2. példa: feladatok elvégzése parancsfájl-paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="62c52-116">Example 2: Submit a job with script parameters</span></span>
```
PS C:\>$parameters = [ordered]@{}
$parameters["Department"] = "Sales"
$parameters["NumRecords"] = 1000
$parameters["StartDateTime"] = (Get-Date).AddDays(-14)
Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32 -ScriptParameter $parameters
```

<span data-ttu-id="62c52-117">Az U-SQL-parancsfájlok paraméterei a fő egységprefixumokat felett jelennek meg, például: DEKLARÁLja a @Department String = "Sales" nevet. ÁLLAPÍTSA meg az @NumRecords int = 1000; A @StartDateTime datetime = New datetime (2017; 12; 6; 0; 0; 0; 0) deklarálása;</span><span class="sxs-lookup"><span data-stu-id="62c52-117">U-SQL script parameters are prepended above the main script contents, e.g.: DECLARE @Department string = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = new DateTime(2017, 12, 6, 0, 0, 0, 0);</span></span>

## <span data-ttu-id="62c52-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="62c52-118">PARAMETERS</span></span>

### <span data-ttu-id="62c52-119">-Fiók</span><span class="sxs-lookup"><span data-stu-id="62c52-119">-Account</span></span>
<span data-ttu-id="62c52-120">Az adattó-fiók neve, amelybe a feladatot be fogja nyújtani.</span><span class="sxs-lookup"><span data-stu-id="62c52-120">Name of Data Lake Analytics account under which the job will be submitted.</span></span>

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

### <span data-ttu-id="62c52-121">-AnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="62c52-121">-AnalyticsUnits</span></span>
<span data-ttu-id="62c52-122">A projekthez használandó Analytics-egységek.</span><span class="sxs-lookup"><span data-stu-id="62c52-122">The analytics units to use for this job.</span></span> <span data-ttu-id="62c52-123">A parancsfájlokhoz tartozó további elemzési egységek általában gyorsabban futtathatják a parancsfájl-végrehajtási időt.</span><span class="sxs-lookup"><span data-stu-id="62c52-123">Typically, more analytics units dedicated to a script results in faster script execution time.</span></span>

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

### <span data-ttu-id="62c52-124">-CompileMode</span><span class="sxs-lookup"><span data-stu-id="62c52-124">-CompileMode</span></span>
<span data-ttu-id="62c52-125">A feladat során elvégzendő összeállítás típusa.</span><span class="sxs-lookup"><span data-stu-id="62c52-125">The type of compilation to be done on this job.</span></span> <span data-ttu-id="62c52-126">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="62c52-126">Valid values:</span></span> 
- <span data-ttu-id="62c52-127">Szemantikai (csak szemantikai vizsgálatokkal és a szükséges józan ellenőrzésekkel végezhető el)</span><span class="sxs-lookup"><span data-stu-id="62c52-127">Semantic (Only performs semantic checks and necessary sanity checks)</span></span>
- <span data-ttu-id="62c52-128">Teljes (teljes összeállítás)</span><span class="sxs-lookup"><span data-stu-id="62c52-128">Full (Full compilation)</span></span>
- <span data-ttu-id="62c52-129">SingleBox (teljes összeállítás helyben végzett)</span><span class="sxs-lookup"><span data-stu-id="62c52-129">SingleBox (Full compilation performed locally)</span></span>

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

### <span data-ttu-id="62c52-130">-CompileOnly</span><span class="sxs-lookup"><span data-stu-id="62c52-130">-CompileOnly</span></span>
<span data-ttu-id="62c52-131">Jelzi, hogy a beküldésnek csak a feladatot kell kiépítenie, és nem kell végrehajtania, ha igaz értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="62c52-131">Indicates that the submission should only build the job and not execute if set to true.</span></span>

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

### <span data-ttu-id="62c52-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62c52-132">-DefaultProfile</span></span>
<span data-ttu-id="62c52-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="62c52-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62c52-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="62c52-134">-Name</span></span>
<span data-ttu-id="62c52-135">A elküldeni kívánt feladat rövid neve.</span><span class="sxs-lookup"><span data-stu-id="62c52-135">The friendly name of the job to submit.</span></span>

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

### <span data-ttu-id="62c52-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="62c52-136">-PipelineId</span></span>
<span data-ttu-id="62c52-137">A feladat beküldését jelző azonosító a munkafolyamathoz kapcsolódó ismétlődő feladatok, valamint a munkafolyamathoz kapcsolódó munka része.</span><span class="sxs-lookup"><span data-stu-id="62c52-137">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

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

### <span data-ttu-id="62c52-138">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="62c52-138">-PipelineName</span></span>
<span data-ttu-id="62c52-139">A projekthez társított pipeline számára választható felhasználóbarát név.</span><span class="sxs-lookup"><span data-stu-id="62c52-139">An optional friendly name for the pipeline associated with this job.</span></span>

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

### <span data-ttu-id="62c52-140">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="62c52-140">-PipelineUri</span></span>
<span data-ttu-id="62c52-141">Egy opcionális URI, amely a csővezetékhez társított származó szolgáltatásra hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="62c52-141">An optional uri that links to the originating service associated with this pipeline.</span></span>

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

### <span data-ttu-id="62c52-142">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="62c52-142">-Priority</span></span>
<span data-ttu-id="62c52-143">A feladat prioritása.</span><span class="sxs-lookup"><span data-stu-id="62c52-143">The priority of the job.</span></span> <span data-ttu-id="62c52-144">Ha nincs megadva, a prioritás a 1000.</span><span class="sxs-lookup"><span data-stu-id="62c52-144">If not specified, the priority is 1000.</span></span> <span data-ttu-id="62c52-145">Az alacsonyabb számok magasabb prioritást jeleznek.</span><span class="sxs-lookup"><span data-stu-id="62c52-145">A lower number indicates a higher job priority.</span></span>

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

### <span data-ttu-id="62c52-146">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="62c52-146">-RecurrenceId</span></span>
<span data-ttu-id="62c52-147">A feladat beküldését jelző azonosító egy olyan ismétlődő feladat része, amely ugyanazzal az ismétlődési AZONOSÍTÓval rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="62c52-147">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

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

### <span data-ttu-id="62c52-148">-RecurrenceName</span><span class="sxs-lookup"><span data-stu-id="62c52-148">-RecurrenceName</span></span>
<span data-ttu-id="62c52-149">Választható rövid név a feladatok közötti ismétlődési korrelációhoz.</span><span class="sxs-lookup"><span data-stu-id="62c52-149">An optional friendly name for the recurrence correlation between jobs.</span></span>

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

### <span data-ttu-id="62c52-150">-RunId</span><span class="sxs-lookup"><span data-stu-id="62c52-150">-RunId</span></span>
<span data-ttu-id="62c52-151">Egy azonosító, amely azonosítja a folyamat adott futási közelítését.</span><span class="sxs-lookup"><span data-stu-id="62c52-151">An ID that identifies this specific run iteration of the pipeline.</span></span>

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

### <span data-ttu-id="62c52-152">-Futtatókörnyezet</span><span class="sxs-lookup"><span data-stu-id="62c52-152">-Runtime</span></span>
<span data-ttu-id="62c52-153">Tetszés szerint állítsa be a projekthez használni kívánt futásidejű verziót.</span><span class="sxs-lookup"><span data-stu-id="62c52-153">Optionally set the version of the runtime to use for the job.</span></span> <span data-ttu-id="62c52-154">Ha nincs bekapcsolva, az alapértelmezett futásidejű érték van használatban.</span><span class="sxs-lookup"><span data-stu-id="62c52-154">If left unset, the default runtime is used.</span></span>

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

### <span data-ttu-id="62c52-155">-Script</span><span class="sxs-lookup"><span data-stu-id="62c52-155">-Script</span></span>
<span data-ttu-id="62c52-156">Parancsfájl végrehajtása (írt sor).</span><span class="sxs-lookup"><span data-stu-id="62c52-156">Script to execute (written inline).</span></span>

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

### <span data-ttu-id="62c52-157">-ScriptParameter</span><span class="sxs-lookup"><span data-stu-id="62c52-157">-ScriptParameter</span></span>
<span data-ttu-id="62c52-158">A projekthez tartozó parancsfájlok paraméterei (karakterlánc) az értékekhez (a bájtok, a sbyte, az int, a uint (vagy a UInt32), a Long, a ulong (vagy a UInt64), az float, a Double, a decimális, a short (vagy a Int16), a karakter, a karakterlánc, a DateTime, a bool, a GUID vagy a byte [] függvény</span><span class="sxs-lookup"><span data-stu-id="62c52-158">The script parameters for this job, as a dictionary of parameter names (string) to values (any combination of byte, sbyte, int, uint (or uint32), long, ulong (or uint64), float, double, decimal, short (or int16), ushort (or uint16), char, string, DateTime, bool, Guid, or byte[]).</span></span>

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

### <span data-ttu-id="62c52-159">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="62c52-159">-ScriptPath</span></span>
<span data-ttu-id="62c52-160">A küldeni kívánt parancsfájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="62c52-160">Path to the script file to submit.</span></span>

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

### <span data-ttu-id="62c52-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62c52-161">CommonParameters</span></span>
<span data-ttu-id="62c52-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="62c52-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62c52-163">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62c52-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62c52-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="62c52-164">INPUTS</span></span>

### <span data-ttu-id="62c52-165">System. String</span><span class="sxs-lookup"><span data-stu-id="62c52-165">System.String</span></span>

### <span data-ttu-id="62c52-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="62c52-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="62c52-167">System. Int32</span><span class="sxs-lookup"><span data-stu-id="62c52-167">System.Int32</span></span>

### <span data-ttu-id="62c52-168">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="62c52-168">System.Collections.IDictionary</span></span>

### <span data-ttu-id="62c52-169">System. GUID</span><span class="sxs-lookup"><span data-stu-id="62c52-169">System.Guid</span></span>

### <span data-ttu-id="62c52-170">System. null ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="62c52-170">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="62c52-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62c52-171">OUTPUTS</span></span>

### <span data-ttu-id="62c52-172">Microsoft. Azure. Management. DataLake. Analytics. models. JobInformation</span><span class="sxs-lookup"><span data-stu-id="62c52-172">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="62c52-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="62c52-173">NOTES</span></span>

## <span data-ttu-id="62c52-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62c52-174">RELATED LINKS</span></span>

[<span data-ttu-id="62c52-175">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="62c52-175">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="62c52-176">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="62c52-176">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="62c52-177">Várjon-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="62c52-177">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


