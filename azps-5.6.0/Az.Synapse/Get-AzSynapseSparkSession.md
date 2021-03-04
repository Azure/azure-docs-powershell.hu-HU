---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
ms.openlocfilehash: efe733250c43d79aa8296db380ac453d44231c01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011317"
---
# <span data-ttu-id="6fe2f-101">Get-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="6fe2f-101">Get-AzSynapseSparkSession</span></span>

## <span data-ttu-id="6fe2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fe2f-102">SYNOPSIS</span></span>
<span data-ttu-id="6fe2f-103">Synapse Analytics Spark munkamenetet kap.</span><span class="sxs-lookup"><span data-stu-id="6fe2f-103">Gets a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="6fe2f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6fe2f-104">SYNTAX</span></span>

### <span data-ttu-id="6fe2f-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6fe2f-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fe2f-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fe2f-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fe2f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6fe2f-107">DESCRIPTION</span></span>
<span data-ttu-id="6fe2f-108">A **Get-AzSynapseSparkSession** parancsmag információt kap egy Azure Synapse Analytics Spark-munkamenetről.</span><span class="sxs-lookup"><span data-stu-id="6fe2f-108">The **Get-AzSynapseSparkSession** cmdlet gets information about an Azure Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="6fe2f-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6fe2f-109">EXAMPLES</span></span>

### <span data-ttu-id="6fe2f-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="6fe2f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="6fe2f-111">Ez a parancs a megadott Értékgörbe alatti összes Spark-munkamenetet lekérte.</span><span class="sxs-lookup"><span data-stu-id="6fe2f-111">This command gets all the Spark sessions under the specified Spark pool.</span></span>

### <span data-ttu-id="6fe2f-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="6fe2f-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 1
```

<span data-ttu-id="6fe2f-113">Ez a parancs a spark-munkamenetet a megadott y azonosítóval kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6fe2f-113">This command gets the Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="6fe2f-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="6fe2f-114">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkSession
```

<span data-ttu-id="6fe2f-115">Ez a parancs a megadott Értékgörbe-készleten keresztüli összes Spark-munkamenetet lekérte.</span><span class="sxs-lookup"><span data-stu-id="6fe2f-115">This command gets all the Spark sessions under the specified Spark pool through pipeline.</span></span>

## <span data-ttu-id="6fe2f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6fe2f-116">PARAMETERS</span></span>

### <span data-ttu-id="6fe2f-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="6fe2f-117">-ApplicationId</span></span>
<span data-ttu-id="6fe2f-118">A munkamenet alkalmazásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="6fe2f-118">The Application identifier of the session.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe2f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fe2f-119">-DefaultProfile</span></span>
<span data-ttu-id="6fe2f-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6fe2f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fe2f-121">-SiyId</span><span class="sxs-lookup"><span data-stu-id="6fe2f-121">-LivyId</span></span>
<span data-ttu-id="6fe2f-122">A Spark-munkamenet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6fe2f-122">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe2f-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6fe2f-123">-Name</span></span>
<span data-ttu-id="6fe2f-124">A Synapse spark-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="6fe2f-124">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe2f-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="6fe2f-125">-SparkPoolName</span></span>
<span data-ttu-id="6fe2f-126">A Synapse spark-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="6fe2f-126">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe2f-127">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="6fe2f-127">-SparkPoolObject</span></span>
<span data-ttu-id="6fe2f-128">Spark pool input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="6fe2f-128">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe2f-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6fe2f-129">-WorkspaceName</span></span>
<span data-ttu-id="6fe2f-130">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="6fe2f-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe2f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fe2f-131">CommonParameters</span></span>
<span data-ttu-id="6fe2f-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fe2f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fe2f-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6fe2f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fe2f-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6fe2f-134">INPUTS</span></span>

### <span data-ttu-id="6fe2f-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="6fe2f-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="6fe2f-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6fe2f-136">OUTPUTS</span></span>

### <span data-ttu-id="6fe2f-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="6fe2f-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="6fe2f-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6fe2f-138">NOTES</span></span>

## <span data-ttu-id="6fe2f-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6fe2f-139">RELATED LINKS</span></span>
