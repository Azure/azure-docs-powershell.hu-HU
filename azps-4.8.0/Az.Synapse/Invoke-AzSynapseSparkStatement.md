---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
ms.openlocfilehash: 64677ac73fecbaeaaaa327f21bc8e67e2a933d97
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017475"
---
# <span data-ttu-id="9cf8b-101">Invoke-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="9cf8b-101">Invoke-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="9cf8b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9cf8b-102">SYNOPSIS</span></span>
<span data-ttu-id="9cf8b-103">A szinapszis-elemző szikra utasítását hívja fel.</span><span class="sxs-lookup"><span data-stu-id="9cf8b-103">Invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="9cf8b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9cf8b-104">SYNTAX</span></span>

### <span data-ttu-id="9cf8b-105">RunSparkStatementByCodePathParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9cf8b-105">RunSparkStatementByCodePathParameterSet (Default)</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cf8b-106">RunSparkStatementByCodeParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cf8b-106">RunSparkStatementByCodeParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cf8b-107">RunSparkStatementByCodeAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cf8b-107">RunSparkStatementByCodeAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9cf8b-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cf8b-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9cf8b-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="9cf8b-109">DESCRIPTION</span></span>
<span data-ttu-id="9cf8b-110">A **meghívó-AzSynapseSparkStatement** parancsmag a szinapszis-elemző szikra utasítását hívja fel.</span><span class="sxs-lookup"><span data-stu-id="9cf8b-110">The **Invoke-AzSynapseSparkStatement** cmdlet invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="9cf8b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="9cf8b-111">EXAMPLES</span></span>

### <span data-ttu-id="9cf8b-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9cf8b-112">Example 1</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="9cf8b-113">Ezek a parancsok olyan szikra-munkamenetet indítanak, amely egy szövegközi külső bejelentést hoz létre a csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="9cf8b-113">These commands start a Spark session then invoke an inline Spark statement through pipeline.</span></span>

### <span data-ttu-id="9cf8b-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="9cf8b-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSynapseSparkStatement -SessionId 324 -Language 'Spark' -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="9cf8b-115">Ezekkel a parancsokkal egy szikra-munkamenetet indíthat, majd hivatkozhat egy szövegközi szikra utasításra.</span><span class="sxs-lookup"><span data-stu-id="9cf8b-115">These commands start a Spark session then invoke an inline Spark statement.</span></span>

### <span data-ttu-id="9cf8b-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="9cf8b-116">Example 3</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -FilePath C:\path\to\code.sc
```

<span data-ttu-id="9cf8b-117">Ezek a parancsok olyan szikra-munkamenetet indítanak, amely egy fájlban a szikra kijelentéseit hívja fel.</span><span class="sxs-lookup"><span data-stu-id="9cf8b-117">These commands start a Spark session then invoke Spark statements in a file.</span></span>

## <span data-ttu-id="9cf8b-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9cf8b-118">PARAMETERS</span></span>

### <span data-ttu-id="9cf8b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9cf8b-119">-AsJob</span></span>
<span data-ttu-id="9cf8b-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9cf8b-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9cf8b-121">-Kód</span><span class="sxs-lookup"><span data-stu-id="9cf8b-121">-Code</span></span>
<span data-ttu-id="9cf8b-122">A végrehajtási kód.</span><span class="sxs-lookup"><span data-stu-id="9cf8b-122">The execution code.</span></span>

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

### <span data-ttu-id="9cf8b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cf8b-123">-DefaultProfile</span></span>
<span data-ttu-id="9cf8b-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9cf8b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cf8b-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="9cf8b-125">-FilePath</span></span>
<span data-ttu-id="9cf8b-126">A végrehajtási kódot tartalmazó helyi fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9cf8b-126">Specifies a local file path that contains the execution code.</span></span>

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

### <span data-ttu-id="9cf8b-127">-Nyelv</span><span class="sxs-lookup"><span data-stu-id="9cf8b-127">-Language</span></span>
<span data-ttu-id="9cf8b-128">A végrehajtási kód nyelve.</span><span class="sxs-lookup"><span data-stu-id="9cf8b-128">Language of the execution code.</span></span>

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

### <span data-ttu-id="9cf8b-129">– Válasz</span><span class="sxs-lookup"><span data-stu-id="9cf8b-129">-Response</span></span>
<span data-ttu-id="9cf8b-130">A teljes választ adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="9cf8b-130">Indicates full response should be return.</span></span>

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

### <span data-ttu-id="9cf8b-131">-Munkamenet</span><span class="sxs-lookup"><span data-stu-id="9cf8b-131">-SessionId</span></span>
<span data-ttu-id="9cf8b-132">A szikra munkamenet azonosítója</span><span class="sxs-lookup"><span data-stu-id="9cf8b-132">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="9cf8b-133">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="9cf8b-133">-SessionObject</span></span>
<span data-ttu-id="9cf8b-134">A szikra-munkamenet bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="9cf8b-134">Spark session input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9cf8b-135">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="9cf8b-135">-SparkPoolName</span></span>
<span data-ttu-id="9cf8b-136">A szinapszis Spark Pool neve.</span><span class="sxs-lookup"><span data-stu-id="9cf8b-136">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="9cf8b-137">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9cf8b-137">-WorkspaceName</span></span>
<span data-ttu-id="9cf8b-138">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="9cf8b-138">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9cf8b-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9cf8b-139">-Confirm</span></span>
<span data-ttu-id="9cf8b-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9cf8b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cf8b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cf8b-141">-WhatIf</span></span>
<span data-ttu-id="9cf8b-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9cf8b-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9cf8b-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9cf8b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cf8b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cf8b-144">CommonParameters</span></span>
<span data-ttu-id="9cf8b-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9cf8b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cf8b-146">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9cf8b-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cf8b-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9cf8b-147">INPUTS</span></span>

### <span data-ttu-id="9cf8b-148">System. String</span><span class="sxs-lookup"><span data-stu-id="9cf8b-148">System.String</span></span>

### <span data-ttu-id="9cf8b-149">Microsoft. Azure. commands. szinapszis. models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="9cf8b-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="9cf8b-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9cf8b-150">OUTPUTS</span></span>

### <span data-ttu-id="9cf8b-151">Microsoft. Azure. commands. szinapszis. models. PSSynapseExtendedSparkStatement</span><span class="sxs-lookup"><span data-stu-id="9cf8b-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseExtendedSparkStatement</span></span>

## <span data-ttu-id="9cf8b-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9cf8b-152">NOTES</span></span>

## <span data-ttu-id="9cf8b-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9cf8b-153">RELATED LINKS</span></span>
