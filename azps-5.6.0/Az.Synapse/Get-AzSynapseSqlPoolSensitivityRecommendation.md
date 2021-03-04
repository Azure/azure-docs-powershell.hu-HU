---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: d2949bf2d366dc64b0e55b82d0c90979042ea294
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935449"
---
# <span data-ttu-id="e6935-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="e6935-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="e6935-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6935-102">SYNOPSIS</span></span>
<span data-ttu-id="e6935-103">Az SQL-készlet oszlopainak ajánlott adattípusait és bizalmasság-címkéit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e6935-103">Gets the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="e6935-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e6935-104">SYNTAX</span></span>

### <span data-ttu-id="e6935-105">SqlPoolObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e6935-105">SqlPoolObjectParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6935-106">SqlPoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6935-106">SqlPoolParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6935-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e6935-107">DESCRIPTION</span></span>
<span data-ttu-id="e6935-108">A Get-AzSynapseSqlPoolSensitivityRecommendation parancsmag az SQL-készlet oszlopainak ajánlott adattípusait és bizalmasság-címkéit adja vissza.</span><span class="sxs-lookup"><span data-stu-id="e6935-108">The Get-AzSynapseSqlPoolSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="e6935-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e6935-109">EXAMPLES</span></span>

### <span data-ttu-id="e6935-110">1. példa: Az Azure Synapse SQL-készlet ajánlott adattípusai és bizalmasság-címkéinek lekértése.</span><span class="sxs-lookup"><span data-stu-id="e6935-110">Example 1: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="e6935-111">2. példa: Egy Azure Synapse SQL-készlet ajánlott adattípusai és bizalmasság-címkéinek lekértése a Piping használatával.</span><span class="sxs-lookup"><span data-stu-id="e6935-111">Example 2: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolSensitivityRecommendation

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

## <span data-ttu-id="e6935-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6935-112">PARAMETERS</span></span>

### <span data-ttu-id="e6935-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6935-113">-AsJob</span></span>
<span data-ttu-id="e6935-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e6935-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e6935-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6935-115">-DefaultProfile</span></span>
<span data-ttu-id="e6935-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6935-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6935-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6935-117">-ResourceGroupName</span></span>
<span data-ttu-id="e6935-118">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e6935-118">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6935-119">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="e6935-119">-SqlPoolName</span></span>
<span data-ttu-id="e6935-120">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="e6935-120">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6935-121">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="e6935-121">-SqlPoolObject</span></span>
<span data-ttu-id="e6935-122">SQL-készlet bemeneti objektuma, amely általában a folyamaton keresztül áthalad.</span><span class="sxs-lookup"><span data-stu-id="e6935-122">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SqlPoolObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6935-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e6935-123">-WorkspaceName</span></span>
<span data-ttu-id="e6935-124">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="e6935-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6935-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6935-125">CommonParameters</span></span>
<span data-ttu-id="e6935-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6935-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6935-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6935-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6935-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e6935-128">INPUTS</span></span>

### <span data-ttu-id="e6935-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e6935-129">System.String</span></span>

### <span data-ttu-id="e6935-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e6935-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="e6935-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6935-131">OUTPUTS</span></span>

### <span data-ttu-id="e6935-132">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="e6935-132">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

## <span data-ttu-id="e6935-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e6935-133">NOTES</span></span>

## <span data-ttu-id="e6935-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6935-134">RELATED LINKS</span></span>
