---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/submit-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: fc09560bca0d825cc65d8a4f964119cd50898190
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493148"
---
# <span data-ttu-id="b58d4-101">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b58d4-101">Submit-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="b58d4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b58d4-102">SYNOPSIS</span></span>
<span data-ttu-id="b58d4-103">Feladatot küldhet el.</span><span class="sxs-lookup"><span data-stu-id="b58d4-103">Submits a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b58d4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b58d4-104">SYNTAX</span></span>

### <span data-ttu-id="b58d4-105">SubmitUSqlJobWithScriptPath</span><span class="sxs-lookup"><span data-stu-id="b58d4-105">SubmitUSqlJobWithScriptPath</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b58d4-106">SubmitUSqlJob</span><span class="sxs-lookup"><span data-stu-id="b58d4-106">SubmitUSqlJob</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b58d4-107">SubmitUSqlJobWithScriptPathAndRecurrence</span><span class="sxs-lookup"><span data-stu-id="b58d4-107">SubmitUSqlJobWithScriptPathAndRecurrence</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b58d4-108">SubmitUSqlJobWithRecurrence</span><span class="sxs-lookup"><span data-stu-id="b58d4-108">SubmitUSqlJobWithRecurrence</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b58d4-109">SubmitUSqlJobWithScriptPathAndPipeline</span><span class="sxs-lookup"><span data-stu-id="b58d4-109">SubmitUSqlJobWithScriptPathAndPipeline</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 -PipelineId <Guid> [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b58d4-110">SubmitUSqlJobWithPipeline</span><span class="sxs-lookup"><span data-stu-id="b58d4-110">SubmitUSqlJobWithPipeline</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 -PipelineId <Guid> [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b58d4-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="b58d4-111">DESCRIPTION</span></span>
<span data-ttu-id="b58d4-112">A **Submit-AzureRmDataLakeAnalyticsJob** parancsmag az Azure Data-tó Analytics-feladatát továbbítja.</span><span class="sxs-lookup"><span data-stu-id="b58d4-112">The **Submit-AzureRmDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="b58d4-113">Példák</span><span class="sxs-lookup"><span data-stu-id="b58d4-113">EXAMPLES</span></span>

### <span data-ttu-id="b58d4-114">1. példa: feladat elvégzése</span><span class="sxs-lookup"><span data-stu-id="b58d4-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32
```

<span data-ttu-id="b58d4-115">Ez a parancs egy adattói Analytics-feladatot küldött.</span><span class="sxs-lookup"><span data-stu-id="b58d4-115">This command submits a Data Lake Analytics job.</span></span>

### <span data-ttu-id="b58d4-116">2. példa: feladatok elvégzése parancsfájl-paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="b58d4-116">Example 2: Submit a job with script parameters</span></span>
```
PS C:\>$parameters = [ordered]@{}
$parameters["Department"] = "Sales"
$parameters["NumRecords"] = 1000
$parameters["StartDateTime"] = (Get-Date).AddDays(-14)
Submit-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32 -ScriptParameter $parameters
```

<span data-ttu-id="b58d4-117">Az U-SQL-parancsfájlok paramétereinek egységprefixumokat a fő parancsfájlok tartalma fölött, például:</span><span class="sxs-lookup"><span data-stu-id="b58d4-117">U-SQL script parameters are prepended above the main script contents, e.g.:</span></span>

<span data-ttu-id="b58d4-118">DEKLARÁLjon @Department karakterlánc = "Sales"; ÁLLAPÍTSA meg az @NumRecords int = 1000; A @StartDateTime datetime = New datetime (2017; 12; 6; 0; 0; 0; 0) deklarálása;</span><span class="sxs-lookup"><span data-stu-id="b58d4-118">DECLARE @Department string = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = new DateTime(2017, 12, 6, 0, 0, 0, 0);</span></span>

## <span data-ttu-id="b58d4-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b58d4-119">PARAMETERS</span></span>

### <span data-ttu-id="b58d4-120">-Fiók</span><span class="sxs-lookup"><span data-stu-id="b58d4-120">-Account</span></span>
<span data-ttu-id="b58d4-121">Az adattó-fiók neve, amelybe a feladatot be fogja nyújtani.</span><span class="sxs-lookup"><span data-stu-id="b58d4-121">Name of Data Lake Analytics account under which the job will be submitted.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b58d4-122">-CompileMode</span><span class="sxs-lookup"><span data-stu-id="b58d4-122">-CompileMode</span></span>
<span data-ttu-id="b58d4-123">A feladat során elvégzendő összeállítás típusa.</span><span class="sxs-lookup"><span data-stu-id="b58d4-123">The type of compilation to be done on this job.</span></span> <span data-ttu-id="b58d4-124">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="b58d4-124">Valid values:</span></span> 

- <span data-ttu-id="b58d4-125">Szemantikai (csak szemantikai vizsgálatokkal és a szükséges józan ellenőrzésekkel végezhető el)</span><span class="sxs-lookup"><span data-stu-id="b58d4-125">Semantic (Only performs semantic checks and necessary sanity checks)</span></span>
- <span data-ttu-id="b58d4-126">Teljes (teljes összeállítás)</span><span class="sxs-lookup"><span data-stu-id="b58d4-126">Full (Full compilation)</span></span>
- <span data-ttu-id="b58d4-127">SingleBox (teljes összeállítás helyben végzett)</span><span class="sxs-lookup"><span data-stu-id="b58d4-127">SingleBox (Full compilation performed locally)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Semantic, Full, SingleBox

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b58d4-128">-CompileOnly</span><span class="sxs-lookup"><span data-stu-id="b58d4-128">-CompileOnly</span></span>
<span data-ttu-id="b58d4-129">Jelzi, hogy a beküldésnek csak a feladatot kell kiépítenie, és nem kell végrehajtania, ha igaz értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="b58d4-129">Indicates that the submission should only build the job and not execute if set to true.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b58d4-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b58d4-130">-DefaultProfile</span></span>
<span data-ttu-id="b58d4-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b58d4-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b58d4-132">-AnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="b58d4-132">-AnalyticsUnits</span></span>
<span data-ttu-id="b58d4-133">A projekthez használandó Analytics-egységek.</span><span class="sxs-lookup"><span data-stu-id="b58d4-133">The analytics units to use for this job.</span></span> <span data-ttu-id="b58d4-134">A parancsfájlokhoz tartozó további elemzési egységek általában gyorsabban futtathatják a parancsfájl-végrehajtási időt.</span><span class="sxs-lookup"><span data-stu-id="b58d4-134">Typically, more analytics units dedicated to a script results in faster script execution time.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: DegreeOfParallelism

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b58d4-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b58d4-135">-Name</span></span>
<span data-ttu-id="b58d4-136">A elküldeni kívánt feladat rövid neve.</span><span class="sxs-lookup"><span data-stu-id="b58d4-136">The friendly name of the job to submit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b58d4-137">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="b58d4-137">-PipelineId</span></span>
<span data-ttu-id="b58d4-138">A feladat beküldését jelző azonosító a munkafolyamathoz kapcsolódó ismétlődő feladatok, valamint a munkafolyamathoz kapcsolódó munka része.</span><span class="sxs-lookup"><span data-stu-id="b58d4-138">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

```yaml
Type: Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b58d4-139">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="b58d4-139">-PipelineName</span></span>
<span data-ttu-id="b58d4-140">A projekthez társított pipeline számára választható felhasználóbarát név.</span><span class="sxs-lookup"><span data-stu-id="b58d4-140">An optional friendly name for the pipeline associated with this job.</span></span>

```yaml
Type: String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b58d4-141">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="b58d4-141">-PipelineUri</span></span>
<span data-ttu-id="b58d4-142">Egy opcionális URI, amely a csővezetékhez társított származó szolgáltatásra hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="b58d4-142">An optional uri that links to the originating service associated with this pipeline.</span></span>

```yaml
Type: String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b58d4-143">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="b58d4-143">-Priority</span></span>
<span data-ttu-id="b58d4-144">A feladat prioritása.</span><span class="sxs-lookup"><span data-stu-id="b58d4-144">The priority of the job.</span></span> <span data-ttu-id="b58d4-145">Ha nincs megadva, a prioritás a 1000.</span><span class="sxs-lookup"><span data-stu-id="b58d4-145">If not specified, the priority is 1000.</span></span> <span data-ttu-id="b58d4-146">Az alacsonyabb számok magasabb prioritást jeleznek.</span><span class="sxs-lookup"><span data-stu-id="b58d4-146">A lower number indicates a higher job priority.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b58d4-147">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="b58d4-147">-RecurrenceId</span></span>
<span data-ttu-id="b58d4-148">A feladat beküldését jelző azonosító egy olyan ismétlődő feladat része, amely ugyanazzal az ismétlődési AZONOSÍTÓval rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="b58d4-148">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

```yaml
Type: Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b58d4-149">-RecurrenceName</span><span class="sxs-lookup"><span data-stu-id="b58d4-149">-RecurrenceName</span></span>
<span data-ttu-id="b58d4-150">Választható rövid név a feladatok közötti ismétlődési korrelációhoz.</span><span class="sxs-lookup"><span data-stu-id="b58d4-150">An optional friendly name for the recurrence correlation between jobs.</span></span>

```yaml
Type: String
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b58d4-151">-RunId</span><span class="sxs-lookup"><span data-stu-id="b58d4-151">-RunId</span></span>
<span data-ttu-id="b58d4-152">Egy azonosító, amely azonosítja a folyamat adott futási közelítését.</span><span class="sxs-lookup"><span data-stu-id="b58d4-152">An ID that identifies this specific run iteration of the pipeline.</span></span>

```yaml
Type: Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b58d4-153">-Futtatókörnyezet</span><span class="sxs-lookup"><span data-stu-id="b58d4-153">-Runtime</span></span>
<span data-ttu-id="b58d4-154">Tetszés szerint állítsa be a projekthez használni kívánt futásidejű verziót.</span><span class="sxs-lookup"><span data-stu-id="b58d4-154">Optionally set the version of the runtime to use for the job.</span></span> <span data-ttu-id="b58d4-155">Ha nincs bekapcsolva, az alapértelmezett futásidejű érték van használatban.</span><span class="sxs-lookup"><span data-stu-id="b58d4-155">If left unset, the default runtime is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b58d4-156">-Script</span><span class="sxs-lookup"><span data-stu-id="b58d4-156">-Script</span></span>
<span data-ttu-id="b58d4-157">Parancsfájl végrehajtása (írt sor).</span><span class="sxs-lookup"><span data-stu-id="b58d4-157">Script to execute (written inline).</span></span>

```yaml
Type: String
Parameter Sets: SubmitUSqlJob, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithPipeline
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b58d4-158">-ScriptParameter</span><span class="sxs-lookup"><span data-stu-id="b58d4-158">-ScriptParameter</span></span>
<span data-ttu-id="b58d4-159">A projekthez tartozó parancsfájlok paraméterei (karakterlánc) az értékekhez (a bájtok, a sbyte, az int, a uint (vagy a UInt32), a Long, a ulong (vagy a UInt64), az float, a Double, a decimális, a short (vagy a Int16), a karakter, a karakterlánc, a DateTime, a bool, a GUID vagy a byte [] függvény</span><span class="sxs-lookup"><span data-stu-id="b58d4-159">The script parameters for this job, as a dictionary of parameter names (string) to values (any combination of byte, sbyte, int, uint (or uint32), long, ulong (or uint64), float, double, decimal, short (or int16), ushort (or uint16), char, string, DateTime, bool, Guid, or byte[]).</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b58d4-160">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="b58d4-160">-ScriptPath</span></span>
<span data-ttu-id="b58d4-161">A küldeni kívánt parancsfájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="b58d4-161">Path to the script file to submit.</span></span>

```yaml
Type: String
Parameter Sets: SubmitUSqlJobWithScriptPath, SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithScriptPathAndPipeline
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b58d4-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b58d4-162">CommonParameters</span></span>
<span data-ttu-id="b58d4-163">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b58d4-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b58d4-164">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b58d4-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b58d4-165">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b58d4-165">INPUTS</span></span>

### <span data-ttu-id="b58d4-166">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="b58d4-166">String</span></span>
<span data-ttu-id="b58d4-167">A ' script ' paraméter a pipeline "string" típusú értékét fogadja el.</span><span class="sxs-lookup"><span data-stu-id="b58d4-167">Parameter 'Script' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="b58d4-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b58d4-168">OUTPUTS</span></span>

### <span data-ttu-id="b58d4-169">JobInformation</span><span class="sxs-lookup"><span data-stu-id="b58d4-169">JobInformation</span></span>
<span data-ttu-id="b58d4-170">Az elküldött feladat kezdeti munkarészletei.</span><span class="sxs-lookup"><span data-stu-id="b58d4-170">The initial job details for the submitted job.</span></span>

## <span data-ttu-id="b58d4-171">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b58d4-171">NOTES</span></span>

## <span data-ttu-id="b58d4-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b58d4-172">RELATED LINKS</span></span>

[<span data-ttu-id="b58d4-173">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b58d4-173">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="b58d4-174">Stop-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b58d4-174">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="b58d4-175">Várjon-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b58d4-175">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


