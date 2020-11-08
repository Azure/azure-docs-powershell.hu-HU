---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
ms.openlocfilehash: 587183d72c6fdeec965f1ec1aa6aa88f5d6f36f9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182029"
---
# <span data-ttu-id="d8ea6-101">Get-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="d8ea6-101">Get-AzSynapseSparkSession</span></span>

## <span data-ttu-id="d8ea6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d8ea6-102">SYNOPSIS</span></span>
<span data-ttu-id="d8ea6-103">A szinapszis-elemző Spark-munkamenetet kapja.</span><span class="sxs-lookup"><span data-stu-id="d8ea6-103">Gets a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="d8ea6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d8ea6-104">SYNTAX</span></span>

### <span data-ttu-id="d8ea6-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d8ea6-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8ea6-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8ea6-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8ea6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d8ea6-107">DESCRIPTION</span></span>
<span data-ttu-id="d8ea6-108">A **Get-AzSynapseSparkSession** parancsmag információkat kap az Azure szinapszis Analytics Spark-munkamenetről.</span><span class="sxs-lookup"><span data-stu-id="d8ea6-108">The **Get-AzSynapseSparkSession** cmdlet gets information about an Azure Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="d8ea6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d8ea6-109">EXAMPLES</span></span>

### <span data-ttu-id="d8ea6-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d8ea6-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="d8ea6-111">Ez a parancs a megadott Spark-készlet alatti összes szikra-munkamenetet megkapja.</span><span class="sxs-lookup"><span data-stu-id="d8ea6-111">This command gets all the Spark sessions under the specified Spark pool.</span></span>

### <span data-ttu-id="d8ea6-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="d8ea6-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 1
```

<span data-ttu-id="d8ea6-113">Ez a parancs a megadott Livius-AZONOSÍTÓJÚ Spark-munkamenetet kapja.</span><span class="sxs-lookup"><span data-stu-id="d8ea6-113">This command gets the Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="d8ea6-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="d8ea6-114">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkSession
```

<span data-ttu-id="d8ea6-115">Ez a parancs a megadott Spark-kapcsolat alatti összes szikra-munkamenetet a csővezetéken keresztül kapja.</span><span class="sxs-lookup"><span data-stu-id="d8ea6-115">This command gets all the Spark sessions under the specified Spark pool through pipeline.</span></span>

## <span data-ttu-id="d8ea6-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d8ea6-116">PARAMETERS</span></span>

### <span data-ttu-id="d8ea6-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d8ea6-117">-ApplicationId</span></span>
<span data-ttu-id="d8ea6-118">A munkamenet alkalmazásspecifikus azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d8ea6-118">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="d8ea6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8ea6-119">-DefaultProfile</span></span>
<span data-ttu-id="d8ea6-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d8ea6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8ea6-121">-LivyId</span><span class="sxs-lookup"><span data-stu-id="d8ea6-121">-LivyId</span></span>
<span data-ttu-id="d8ea6-122">A szikra munkamenet azonosítója</span><span class="sxs-lookup"><span data-stu-id="d8ea6-122">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="d8ea6-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d8ea6-123">-Name</span></span>
<span data-ttu-id="d8ea6-124">A szinapszis Spark Pool neve.</span><span class="sxs-lookup"><span data-stu-id="d8ea6-124">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="d8ea6-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="d8ea6-125">-SparkPoolName</span></span>
<span data-ttu-id="d8ea6-126">A szinapszis Spark Pool neve.</span><span class="sxs-lookup"><span data-stu-id="d8ea6-126">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="d8ea6-127">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="d8ea6-127">-SparkPoolObject</span></span>
<span data-ttu-id="d8ea6-128">A szikra medence bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="d8ea6-128">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d8ea6-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d8ea6-129">-WorkspaceName</span></span>
<span data-ttu-id="d8ea6-130">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="d8ea6-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d8ea6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8ea6-131">CommonParameters</span></span>
<span data-ttu-id="d8ea6-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d8ea6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8ea6-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d8ea6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8ea6-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8ea6-134">INPUTS</span></span>

### <span data-ttu-id="d8ea6-135">Microsoft. Azure. commands. szinapszis. models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="d8ea6-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="d8ea6-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8ea6-136">OUTPUTS</span></span>

### <span data-ttu-id="d8ea6-137">Microsoft. Azure. commands. szinapszis. models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="d8ea6-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="d8ea6-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d8ea6-138">NOTES</span></span>

## <span data-ttu-id="d8ea6-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8ea6-139">RELATED LINKS</span></span>
