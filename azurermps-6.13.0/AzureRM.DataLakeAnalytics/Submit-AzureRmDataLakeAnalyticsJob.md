---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/submit-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: acd61ac9da39a56cf03499d0a2a4fcd25d321525
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499607"
---
# <span data-ttu-id="c0c03-101">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c0c03-101">Submit-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="c0c03-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c0c03-102">SYNOPSIS</span></span>
<span data-ttu-id="c0c03-103">Feladatot küldhet el.</span><span class="sxs-lookup"><span data-stu-id="c0c03-103">Submits a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0c03-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c0c03-104">SYNTAX</span></span>

### <span data-ttu-id="c0c03-105">SubmitUSqlJobWithScriptPath</span><span class="sxs-lookup"><span data-stu-id="c0c03-105">SubmitUSqlJobWithScriptPath</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0c03-106">SubmitUSqlJob</span><span class="sxs-lookup"><span data-stu-id="c0c03-106">SubmitUSqlJob</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0c03-107">SubmitUSqlJobWithScriptPathAndRecurrence</span><span class="sxs-lookup"><span data-stu-id="c0c03-107">SubmitUSqlJobWithScriptPathAndRecurrence</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0c03-108">SubmitUSqlJobWithRecurrence</span><span class="sxs-lookup"><span data-stu-id="c0c03-108">SubmitUSqlJobWithRecurrence</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0c03-109">SubmitUSqlJobWithScriptPathAndPipeline</span><span class="sxs-lookup"><span data-stu-id="c0c03-109">SubmitUSqlJobWithScriptPathAndPipeline</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 -PipelineId <Guid> [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0c03-110">SubmitUSqlJobWithPipeline</span><span class="sxs-lookup"><span data-stu-id="c0c03-110">SubmitUSqlJobWithPipeline</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 -PipelineId <Guid> [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0c03-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="c0c03-111">DESCRIPTION</span></span>
<span data-ttu-id="c0c03-112">A **Submit-AzureRmDataLakeAnalyticsJob** parancsmag az Azure Data-tó Analytics-feladatát továbbítja.</span><span class="sxs-lookup"><span data-stu-id="c0c03-112">The **Submit-AzureRmDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="c0c03-113">Példák</span><span class="sxs-lookup"><span data-stu-id="c0c03-113">EXAMPLES</span></span>

### <span data-ttu-id="c0c03-114">1. példa: feladat elvégzése</span><span class="sxs-lookup"><span data-stu-id="c0c03-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32
```

<span data-ttu-id="c0c03-115">Ez a parancs egy adattói Analytics-feladatot küldött.</span><span class="sxs-lookup"><span data-stu-id="c0c03-115">This command submits a Data Lake Analytics job.</span></span>

### <span data-ttu-id="c0c03-116">2. példa: feladatok elvégzése parancsfájl-paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="c0c03-116">Example 2: Submit a job with script parameters</span></span>
```
PS C:\>$parameters = [ordered]@{}
$parameters["Department"] = "Sales"
$parameters["NumRecords"] = 1000
$parameters["StartDateTime"] = (Get-Date).AddDays(-14)
Submit-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32 -ScriptParameter $parameters
```

<span data-ttu-id="c0c03-117">Az U-SQL-parancsfájlok paraméterei a fő egységprefixumokat felett jelennek meg, például: DEKLARÁLja a @Department String = "Sales" nevet. ÁLLAPÍTSA meg az @NumRecords int = 1000; A @StartDateTime datetime = New datetime (2017; 12; 6; 0; 0; 0; 0) deklarálása;</span><span class="sxs-lookup"><span data-stu-id="c0c03-117">U-SQL script parameters are prepended above the main script contents, e.g.: DECLARE @Department string = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = new DateTime(2017, 12, 6, 0, 0, 0, 0);</span></span>

## <span data-ttu-id="c0c03-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c0c03-118">PARAMETERS</span></span>

### <span data-ttu-id="c0c03-119">-Fiók</span><span class="sxs-lookup"><span data-stu-id="c0c03-119">-Account</span></span>
<span data-ttu-id="c0c03-120">Az adattó-fiók neve, amelybe a feladatot be fogja nyújtani.</span><span class="sxs-lookup"><span data-stu-id="c0c03-120">Name of Data Lake Analytics account under which the job will be submitted.</span></span>

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

### <span data-ttu-id="c0c03-121">-AnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="c0c03-121">-AnalyticsUnits</span></span>
<span data-ttu-id="c0c03-122">A projekthez használandó Analytics-egységek.</span><span class="sxs-lookup"><span data-stu-id="c0c03-122">The analytics units to use for this job.</span></span> <span data-ttu-id="c0c03-123">A parancsfájlokhoz tartozó további elemzési egységek általában gyorsabban futtathatják a parancsfájl-végrehajtási időt.</span><span class="sxs-lookup"><span data-stu-id="c0c03-123">Typically, more analytics units dedicated to a script results in faster script execution time.</span></span>

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

### <span data-ttu-id="c0c03-124">-CompileMode</span><span class="sxs-lookup"><span data-stu-id="c0c03-124">-CompileMode</span></span>
<span data-ttu-id="c0c03-125">A feladat során elvégzendő összeállítás típusa.</span><span class="sxs-lookup"><span data-stu-id="c0c03-125">The type of compilation to be done on this job.</span></span> <span data-ttu-id="c0c03-126">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="c0c03-126">Valid values:</span></span> 
- <span data-ttu-id="c0c03-127">Szemantikai (csak szemantikai vizsgálatokkal és a szükséges józan ellenőrzésekkel végezhető el)</span><span class="sxs-lookup"><span data-stu-id="c0c03-127">Semantic (Only performs semantic checks and necessary sanity checks)</span></span>
- <span data-ttu-id="c0c03-128">Teljes (teljes összeállítás)</span><span class="sxs-lookup"><span data-stu-id="c0c03-128">Full (Full compilation)</span></span>
- <span data-ttu-id="c0c03-129">SingleBox (teljes összeállítás helyben végzett)</span><span class="sxs-lookup"><span data-stu-id="c0c03-129">SingleBox (Full compilation performed locally)</span></span>

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

### <span data-ttu-id="c0c03-130">-CompileOnly</span><span class="sxs-lookup"><span data-stu-id="c0c03-130">-CompileOnly</span></span>
<span data-ttu-id="c0c03-131">Jelzi, hogy a beküldésnek csak a feladatot kell kiépítenie, és nem kell végrehajtania, ha igaz értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="c0c03-131">Indicates that the submission should only build the job and not execute if set to true.</span></span>

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

### <span data-ttu-id="c0c03-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0c03-132">-DefaultProfile</span></span>
<span data-ttu-id="c0c03-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c0c03-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0c03-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c0c03-134">-Name</span></span>
<span data-ttu-id="c0c03-135">A elküldeni kívánt feladat rövid neve.</span><span class="sxs-lookup"><span data-stu-id="c0c03-135">The friendly name of the job to submit.</span></span>

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

### <span data-ttu-id="c0c03-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="c0c03-136">-PipelineId</span></span>
<span data-ttu-id="c0c03-137">A feladat beküldését jelző azonosító a munkafolyamathoz kapcsolódó ismétlődő feladatok, valamint a munkafolyamathoz kapcsolódó munka része.</span><span class="sxs-lookup"><span data-stu-id="c0c03-137">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

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

### <span data-ttu-id="c0c03-138">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="c0c03-138">-PipelineName</span></span>
<span data-ttu-id="c0c03-139">A projekthez társított pipeline számára választható felhasználóbarát név.</span><span class="sxs-lookup"><span data-stu-id="c0c03-139">An optional friendly name for the pipeline associated with this job.</span></span>

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

### <span data-ttu-id="c0c03-140">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="c0c03-140">-PipelineUri</span></span>
<span data-ttu-id="c0c03-141">Egy opcionális URI, amely a csővezetékhez társított származó szolgáltatásra hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="c0c03-141">An optional uri that links to the originating service associated with this pipeline.</span></span>

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

### <span data-ttu-id="c0c03-142">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="c0c03-142">-Priority</span></span>
<span data-ttu-id="c0c03-143">A feladat prioritása.</span><span class="sxs-lookup"><span data-stu-id="c0c03-143">The priority of the job.</span></span> <span data-ttu-id="c0c03-144">Ha nincs megadva, a prioritás a 1000.</span><span class="sxs-lookup"><span data-stu-id="c0c03-144">If not specified, the priority is 1000.</span></span> <span data-ttu-id="c0c03-145">Az alacsonyabb számok magasabb prioritást jeleznek.</span><span class="sxs-lookup"><span data-stu-id="c0c03-145">A lower number indicates a higher job priority.</span></span>

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

### <span data-ttu-id="c0c03-146">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="c0c03-146">-RecurrenceId</span></span>
<span data-ttu-id="c0c03-147">A feladat beküldését jelző azonosító egy olyan ismétlődő feladat része, amely ugyanazzal az ismétlődési AZONOSÍTÓval rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="c0c03-147">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

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

### <span data-ttu-id="c0c03-148">-RecurrenceName</span><span class="sxs-lookup"><span data-stu-id="c0c03-148">-RecurrenceName</span></span>
<span data-ttu-id="c0c03-149">Választható rövid név a feladatok közötti ismétlődési korrelációhoz.</span><span class="sxs-lookup"><span data-stu-id="c0c03-149">An optional friendly name for the recurrence correlation between jobs.</span></span>

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

### <span data-ttu-id="c0c03-150">-RunId</span><span class="sxs-lookup"><span data-stu-id="c0c03-150">-RunId</span></span>
<span data-ttu-id="c0c03-151">Egy azonosító, amely azonosítja a folyamat adott futási közelítését.</span><span class="sxs-lookup"><span data-stu-id="c0c03-151">An ID that identifies this specific run iteration of the pipeline.</span></span>

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

### <span data-ttu-id="c0c03-152">-Futtatókörnyezet</span><span class="sxs-lookup"><span data-stu-id="c0c03-152">-Runtime</span></span>
<span data-ttu-id="c0c03-153">Tetszés szerint állítsa be a projekthez használni kívánt futásidejű verziót.</span><span class="sxs-lookup"><span data-stu-id="c0c03-153">Optionally set the version of the runtime to use for the job.</span></span> <span data-ttu-id="c0c03-154">Ha nincs bekapcsolva, az alapértelmezett futásidejű érték van használatban.</span><span class="sxs-lookup"><span data-stu-id="c0c03-154">If left unset, the default runtime is used.</span></span>

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

### <span data-ttu-id="c0c03-155">-Script</span><span class="sxs-lookup"><span data-stu-id="c0c03-155">-Script</span></span>
<span data-ttu-id="c0c03-156">Parancsfájl végrehajtása (írt sor).</span><span class="sxs-lookup"><span data-stu-id="c0c03-156">Script to execute (written inline).</span></span>

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

### <span data-ttu-id="c0c03-157">-ScriptParameter</span><span class="sxs-lookup"><span data-stu-id="c0c03-157">-ScriptParameter</span></span>
<span data-ttu-id="c0c03-158">A projekthez tartozó parancsfájlok paraméterei (karakterlánc) az értékekhez (a bájtok, a sbyte, az int, a uint (vagy a UInt32), a Long, a ulong (vagy a UInt64), az float, a Double, a decimális, a short (vagy a Int16), a karakter, a karakterlánc, a DateTime, a bool, a GUID vagy a byte [] függvény</span><span class="sxs-lookup"><span data-stu-id="c0c03-158">The script parameters for this job, as a dictionary of parameter names (string) to values (any combination of byte, sbyte, int, uint (or uint32), long, ulong (or uint64), float, double, decimal, short (or int16), ushort (or uint16), char, string, DateTime, bool, Guid, or byte[]).</span></span>

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

### <span data-ttu-id="c0c03-159">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="c0c03-159">-ScriptPath</span></span>
<span data-ttu-id="c0c03-160">A küldeni kívánt parancsfájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="c0c03-160">Path to the script file to submit.</span></span>

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

### <span data-ttu-id="c0c03-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0c03-161">CommonParameters</span></span>
<span data-ttu-id="c0c03-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c0c03-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0c03-163">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0c03-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0c03-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0c03-164">INPUTS</span></span>

### <span data-ttu-id="c0c03-165">System. String</span><span class="sxs-lookup"><span data-stu-id="c0c03-165">System.String</span></span>

### <span data-ttu-id="c0c03-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c0c03-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="c0c03-167">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c0c03-167">System.Int32</span></span>

### <span data-ttu-id="c0c03-168">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="c0c03-168">System.Collections.IDictionary</span></span>

### <span data-ttu-id="c0c03-169">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c0c03-169">System.Guid</span></span>

### <span data-ttu-id="c0c03-170">System. null ' 1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c0c03-170">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="c0c03-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0c03-171">OUTPUTS</span></span>

### <span data-ttu-id="c0c03-172">Microsoft. Azure. Management. DataLake. Analytics. models. JobInformation</span><span class="sxs-lookup"><span data-stu-id="c0c03-172">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="c0c03-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c0c03-173">NOTES</span></span>

## <span data-ttu-id="c0c03-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0c03-174">RELATED LINKS</span></span>

[<span data-ttu-id="c0c03-175">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c0c03-175">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="c0c03-176">Stop-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c0c03-176">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="c0c03-177">Várjon-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c0c03-177">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


