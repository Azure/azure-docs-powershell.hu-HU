---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
ms.openlocfilehash: a553f5e1e6b4929997cbd850ca199e6fd7acef08
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302321"
---
# <span data-ttu-id="579ac-101">Get-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="579ac-101">Get-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="579ac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="579ac-102">SYNOPSIS</span></span>
<span data-ttu-id="579ac-103">Beolvassa a szinapszis-elemző szikra nyilatkozatát.</span><span class="sxs-lookup"><span data-stu-id="579ac-103">Gets a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="579ac-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="579ac-104">SYNTAX</span></span>

### <span data-ttu-id="579ac-105">GetSparkStatementsByIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="579ac-105">GetSparkStatementsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>]
 -SessionId <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="579ac-106">GetSparkStatementsByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="579ac-106">GetSparkStatementsByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> [-LivyId <Int32>] [-SessionId <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="579ac-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="579ac-107">DESCRIPTION</span></span>
<span data-ttu-id="579ac-108">A **Get-AzSynapseSparkStatement** parancsmag információkat kap az Azure szinapszis Analytics Spark utasításról.</span><span class="sxs-lookup"><span data-stu-id="579ac-108">The **Get-AzSynapseSparkStatement** cmdlet gets information about an Azure Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="579ac-109">Példák</span><span class="sxs-lookup"><span data-stu-id="579ac-109">EXAMPLES</span></span>

### <span data-ttu-id="579ac-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="579ac-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120
```

<span data-ttu-id="579ac-111">Ez a parancs a szikra-munkamenet alatt minden szikra kijelentést megkapja.</span><span class="sxs-lookup"><span data-stu-id="579ac-111">This command gets all the Spark statements under a Spark session.</span></span>

### <span data-ttu-id="579ac-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="579ac-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120 -LivyId 0
```

<span data-ttu-id="579ac-113">Ez a parancs a megadott Livius-AZONOSÍTÓval kapja meg a szikra utasítását.</span><span class="sxs-lookup"><span data-stu-id="579ac-113">This command gets the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="579ac-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="579ac-114">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 107
PS C:\> $session | Get-AzSynapseSparkStatement
```

<span data-ttu-id="579ac-115">Ez a parancs az összes szikra kijelentését beilleszti a folyamaton keresztül egy szikra fázisba.</span><span class="sxs-lookup"><span data-stu-id="579ac-115">This command gets all the Spark statements under a Spark session through pipeline.</span></span>

## <span data-ttu-id="579ac-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="579ac-116">PARAMETERS</span></span>

### <span data-ttu-id="579ac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="579ac-117">-DefaultProfile</span></span>
<span data-ttu-id="579ac-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="579ac-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="579ac-119">-LivyId</span><span class="sxs-lookup"><span data-stu-id="579ac-119">-LivyId</span></span>
<span data-ttu-id="579ac-120">A szikra-utasítás azonosítója</span><span class="sxs-lookup"><span data-stu-id="579ac-120">Identifier of Spark statement.</span></span>

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

### <span data-ttu-id="579ac-121">-Munkamenet</span><span class="sxs-lookup"><span data-stu-id="579ac-121">-SessionId</span></span>
<span data-ttu-id="579ac-122">A szikra munkamenet azonosítója</span><span class="sxs-lookup"><span data-stu-id="579ac-122">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="579ac-123">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="579ac-123">-SessionObject</span></span>
<span data-ttu-id="579ac-124">A szikra medence bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="579ac-124">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="579ac-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="579ac-125">-SparkPoolName</span></span>
<span data-ttu-id="579ac-126">A szinapszis Spark Pool neve.</span><span class="sxs-lookup"><span data-stu-id="579ac-126">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="579ac-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="579ac-127">-WorkspaceName</span></span>
<span data-ttu-id="579ac-128">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="579ac-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="579ac-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="579ac-129">CommonParameters</span></span>
<span data-ttu-id="579ac-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="579ac-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="579ac-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="579ac-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="579ac-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="579ac-132">INPUTS</span></span>

### <span data-ttu-id="579ac-133">Microsoft. Azure. commands. szinapszis. models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="579ac-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="579ac-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="579ac-134">OUTPUTS</span></span>

### <span data-ttu-id="579ac-135">Microsoft. Azure. commands. szinapszis. models. PSSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="579ac-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkStatement</span></span>

## <span data-ttu-id="579ac-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="579ac-136">NOTES</span></span>

## <span data-ttu-id="579ac-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="579ac-137">RELATED LINKS</span></span>
