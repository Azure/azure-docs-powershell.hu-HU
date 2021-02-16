---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: 89b9b5df2f8233254d4c1cb430a80f0a8a91c13b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162842"
---
# <span data-ttu-id="b8085-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="b8085-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="b8085-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8085-102">SYNOPSIS</span></span>
<span data-ttu-id="b8085-103">Az SQL-készlet oszlopainak ajánlott adattípusait és bizalmasság-címkéit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b8085-103">Gets the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="b8085-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b8085-104">SYNTAX</span></span>

### <span data-ttu-id="b8085-105">SqlPoolObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b8085-105">SqlPoolObjectParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8085-106">SqlPoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8085-106">SqlPoolParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8085-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b8085-107">DESCRIPTION</span></span>
<span data-ttu-id="b8085-108">A Get-AzSynapseSqlPoolSensitivityRecommendation parancsmag az SQL-készlet oszlopainak ajánlott adattípusait és bizalmasság-címkéit adja vissza.</span><span class="sxs-lookup"><span data-stu-id="b8085-108">The Get-AzSynapseSqlPoolSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="b8085-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b8085-109">EXAMPLES</span></span>

### <span data-ttu-id="b8085-110">1. példa: Az Azure Synapse SQL-készlet ajánlott adattípusai és bizalmasság-címkéinek lekértése.</span><span class="sxs-lookup"><span data-stu-id="b8085-110">Example 1: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool.</span></span>
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

### <span data-ttu-id="b8085-111">2. példa: A Piping használatával az Azure Synapse SQL-készlet ajánlott adattípusai és bizalmasság-címkéinek lekérte.</span><span class="sxs-lookup"><span data-stu-id="b8085-111">Example 2: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool using Piping.</span></span>
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

## <span data-ttu-id="b8085-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8085-112">PARAMETERS</span></span>

### <span data-ttu-id="b8085-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8085-113">-AsJob</span></span>
<span data-ttu-id="b8085-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b8085-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b8085-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8085-115">-DefaultProfile</span></span>
<span data-ttu-id="b8085-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b8085-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8085-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8085-117">-ResourceGroupName</span></span>
<span data-ttu-id="b8085-118">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b8085-118">Resource group name.</span></span>

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

### <span data-ttu-id="b8085-119">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="b8085-119">-SqlPoolName</span></span>
<span data-ttu-id="b8085-120">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="b8085-120">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="b8085-121">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="b8085-121">-SqlPoolObject</span></span>
<span data-ttu-id="b8085-122">SQL-készlet bemeneti objektuma, amely általában áthalad a folyamaton.</span><span class="sxs-lookup"><span data-stu-id="b8085-122">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b8085-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b8085-123">-WorkspaceName</span></span>
<span data-ttu-id="b8085-124">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="b8085-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b8085-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8085-125">CommonParameters</span></span>
<span data-ttu-id="b8085-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8085-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8085-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8085-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8085-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b8085-128">INPUTS</span></span>

### <span data-ttu-id="b8085-129">System.String</span><span class="sxs-lookup"><span data-stu-id="b8085-129">System.String</span></span>

### <span data-ttu-id="b8085-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="b8085-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="b8085-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8085-131">OUTPUTS</span></span>

### <span data-ttu-id="b8085-132">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="b8085-132">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

## <span data-ttu-id="b8085-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b8085-133">NOTES</span></span>

## <span data-ttu-id="b8085-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8085-134">RELATED LINKS</span></span>
