---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
ms.openlocfilehash: a553f5e1e6b4929997cbd850ca199e6fd7acef08
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359447"
---
# <span data-ttu-id="c92c5-101">Get-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="c92c5-101">Get-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="c92c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c92c5-102">SYNOPSIS</span></span>
<span data-ttu-id="c92c5-103">Synapse Analytics Spark utasítást kap.</span><span class="sxs-lookup"><span data-stu-id="c92c5-103">Gets a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="c92c5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c92c5-104">SYNTAX</span></span>

### <span data-ttu-id="c92c5-105">GetSparkStatementsByIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c92c5-105">GetSparkStatementsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>]
 -SessionId <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c92c5-106">GetSparkStatementsByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c92c5-106">GetSparkStatementsByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> [-LivyId <Int32>] [-SessionId <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c92c5-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c92c5-107">DESCRIPTION</span></span>
<span data-ttu-id="c92c5-108">A **Get-AzSynapseSparkStatement** parancsmag információkat kap az Azure Synapse Analytics Spark utasításról.</span><span class="sxs-lookup"><span data-stu-id="c92c5-108">The **Get-AzSynapseSparkStatement** cmdlet gets information about an Azure Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="c92c5-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c92c5-109">EXAMPLES</span></span>

### <span data-ttu-id="c92c5-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="c92c5-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120
```

<span data-ttu-id="c92c5-111">Ez a parancs az összes Spark-utasításhoz spark-munkamenetet kap.</span><span class="sxs-lookup"><span data-stu-id="c92c5-111">This command gets all the Spark statements under a Spark session.</span></span>

### <span data-ttu-id="c92c5-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="c92c5-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120 -LivyId 0
```

<span data-ttu-id="c92c5-113">Ez a parancs a Spark utasítást kapja meg a megadott y azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="c92c5-113">This command gets the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="c92c5-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="c92c5-114">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 107
PS C:\> $session | Get-AzSynapseSparkStatement
```

<span data-ttu-id="c92c5-115">Ez a parancs az összes Spark-utasítást egy Spark-munkamenet alatt kapja meg a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="c92c5-115">This command gets all the Spark statements under a Spark session through pipeline.</span></span>

## <span data-ttu-id="c92c5-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c92c5-116">PARAMETERS</span></span>

### <span data-ttu-id="c92c5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c92c5-117">-DefaultProfile</span></span>
<span data-ttu-id="c92c5-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c92c5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c92c5-119">-SiyId</span><span class="sxs-lookup"><span data-stu-id="c92c5-119">-LivyId</span></span>
<span data-ttu-id="c92c5-120">Az Értékgörbe utasítás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c92c5-120">Identifier of Spark statement.</span></span>

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

### <span data-ttu-id="c92c5-121">-SessionId</span><span class="sxs-lookup"><span data-stu-id="c92c5-121">-SessionId</span></span>
<span data-ttu-id="c92c5-122">A Spark-munkamenet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c92c5-122">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: GetSparkStatementsByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c92c5-123">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="c92c5-123">-SessionObject</span></span>
<span data-ttu-id="c92c5-124">Spark pool input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="c92c5-124">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: GetSparkStatementsByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c92c5-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="c92c5-125">-SparkPoolName</span></span>
<span data-ttu-id="c92c5-126">A Synapse spark-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="c92c5-126">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c92c5-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c92c5-127">-WorkspaceName</span></span>
<span data-ttu-id="c92c5-128">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="c92c5-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c92c5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c92c5-129">CommonParameters</span></span>
<span data-ttu-id="c92c5-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c92c5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c92c5-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c92c5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c92c5-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c92c5-132">INPUTS</span></span>

### <span data-ttu-id="c92c5-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="c92c5-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="c92c5-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c92c5-134">OUTPUTS</span></span>

### <span data-ttu-id="c92c5-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="c92c5-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkStatement</span></span>

## <span data-ttu-id="c92c5-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c92c5-136">NOTES</span></span>

## <span data-ttu-id="c92c5-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c92c5-137">RELATED LINKS</span></span>
