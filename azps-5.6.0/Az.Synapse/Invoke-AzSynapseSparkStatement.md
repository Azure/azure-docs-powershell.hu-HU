---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/invoke-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
ms.openlocfilehash: 62894b5d879febdeeb7c14360c16c66fb8a28ea0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934594"
---
# <span data-ttu-id="3d315-101">Invoke-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="3d315-101">Invoke-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="3d315-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d315-102">SYNOPSIS</span></span>
<span data-ttu-id="3d315-103">Meghívja a Synapse Analytics Spark utasítást.</span><span class="sxs-lookup"><span data-stu-id="3d315-103">Invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="3d315-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3d315-104">SYNTAX</span></span>

### <span data-ttu-id="3d315-105">RunSparkStatementByCodePathParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3d315-105">RunSparkStatementByCodePathParameterSet (Default)</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d315-106">RunSparkStatementByCodeParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d315-106">RunSparkStatementByCodeParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d315-107">RunSparkStatementByCodeAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d315-107">RunSparkStatementByCodeAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d315-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d315-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3d315-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3d315-109">DESCRIPTION</span></span>
<span data-ttu-id="3d315-110">Az **Invoke-AzSynapseSparkStatement** parancsmag meghívja a Synapse Analytics Spark utasítást.</span><span class="sxs-lookup"><span data-stu-id="3d315-110">The **Invoke-AzSynapseSparkStatement** cmdlet invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="3d315-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3d315-111">EXAMPLES</span></span>

### <span data-ttu-id="3d315-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="3d315-112">Example 1</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="3d315-113">Ezek a parancsok elindítják az Értékgörbe munkamenetet, majd elindítják a beágyazott értékgörbét a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="3d315-113">These commands start a Spark session then invoke an inline Spark statement through pipeline.</span></span>

### <span data-ttu-id="3d315-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="3d315-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSynapseSparkStatement -SessionId 324 -Language 'Spark' -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="3d315-115">Ezek a parancsok elindítják az Értékgörbe-munkamenetet, majd meghívnak egy beágyazott értékgörbét.</span><span class="sxs-lookup"><span data-stu-id="3d315-115">These commands start a Spark session then invoke an inline Spark statement.</span></span>

### <span data-ttu-id="3d315-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="3d315-116">Example 3</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -FilePath C:\path\to\code.sc
```

<span data-ttu-id="3d315-117">Ezek a parancsok elindítják a Spark munkamenetet, majd elindítják a Spark utasításokat egy fájlban.</span><span class="sxs-lookup"><span data-stu-id="3d315-117">These commands start a Spark session then invoke Spark statements in a file.</span></span>

## <span data-ttu-id="3d315-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d315-118">PARAMETERS</span></span>

### <span data-ttu-id="3d315-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d315-119">-AsJob</span></span>
<span data-ttu-id="3d315-120">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3d315-120">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d315-121">-Kód</span><span class="sxs-lookup"><span data-stu-id="3d315-121">-Code</span></span>
<span data-ttu-id="3d315-122">A végrehajtási kód.</span><span class="sxs-lookup"><span data-stu-id="3d315-122">The execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodeParameterSet, RunSparkStatementByCodeAndInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d315-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d315-123">-DefaultProfile</span></span>
<span data-ttu-id="3d315-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3d315-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d315-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="3d315-125">-FilePath</span></span>
<span data-ttu-id="3d315-126">Megadja a végrehajtási kódot tartalmazó helyi fájl elérési útját.</span><span class="sxs-lookup"><span data-stu-id="3d315-126">Specifies a local file path that contains the execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d315-127">-Language</span><span class="sxs-lookup"><span data-stu-id="3d315-127">-Language</span></span>
<span data-ttu-id="3d315-128">A végrehajtási kód nyelve.</span><span class="sxs-lookup"><span data-stu-id="3d315-128">Language of the execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp, SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodeAndInputObjectParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp, SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d315-129">-Response</span><span class="sxs-lookup"><span data-stu-id="3d315-129">-Response</span></span>
<span data-ttu-id="3d315-130">Azt jelzi, hogy a teljes válasznak vissza kell térnie.</span><span class="sxs-lookup"><span data-stu-id="3d315-130">Indicates full response should be return.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d315-131">-SessionId</span><span class="sxs-lookup"><span data-stu-id="3d315-131">-SessionId</span></span>
<span data-ttu-id="3d315-132">A Spark-munkamenet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3d315-132">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: RunSparkStatementByCodeAndInputObjectParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d315-133">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="3d315-133">-SessionObject</span></span>
<span data-ttu-id="3d315-134">Spark session input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="3d315-134">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: RunSparkStatementByCodeAndInputObjectParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d315-135">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="3d315-135">-SparkPoolName</span></span>
<span data-ttu-id="3d315-136">A Synapse spark-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="3d315-136">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d315-137">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3d315-137">-WorkspaceName</span></span>
<span data-ttu-id="3d315-138">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="3d315-138">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d315-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d315-139">-Confirm</span></span>
<span data-ttu-id="3d315-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3d315-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d315-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d315-141">-WhatIf</span></span>
<span data-ttu-id="3d315-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3d315-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d315-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3d315-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d315-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d315-144">CommonParameters</span></span>
<span data-ttu-id="3d315-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d315-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d315-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3d315-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d315-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3d315-147">INPUTS</span></span>

### <span data-ttu-id="3d315-148">System.String</span><span class="sxs-lookup"><span data-stu-id="3d315-148">System.String</span></span>

### <span data-ttu-id="3d315-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="3d315-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="3d315-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d315-150">OUTPUTS</span></span>

### <span data-ttu-id="3d315-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseExtendedSparkStatement</span><span class="sxs-lookup"><span data-stu-id="3d315-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseExtendedSparkStatement</span></span>

## <span data-ttu-id="3d315-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3d315-152">NOTES</span></span>

## <span data-ttu-id="3d315-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3d315-153">RELATED LINKS</span></span>
