---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: 0942373dc3ad741f10d5a87d7b4713413f9db4f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010134"
---
# <span data-ttu-id="27b89-101">Get-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="27b89-101">Get-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="27b89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27b89-102">SYNOPSIS</span></span>
<span data-ttu-id="27b89-103">Az SQL-készlet oszlopainak aktuális adattípusait és bizalmasság-címkéit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="27b89-103">Gets the current information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="27b89-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="27b89-104">SYNTAX</span></span>

### <span data-ttu-id="27b89-105">SqlPoolObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="27b89-105">SqlPoolObjectParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27b89-106">SqlPoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="27b89-106">SqlPoolParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27b89-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="27b89-107">ColumnParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27b89-108">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="27b89-108">SqlPoolObjectColumnParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="27b89-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="27b89-109">DESCRIPTION</span></span>
<span data-ttu-id="27b89-110">A Get-AzSynapseSqlPoolSensitivityClassification parancsmag az Azure Synapse SQL-készlet oszlopainak aktuális adattípusait és bizalmasság-címkéit adja vissza.</span><span class="sxs-lookup"><span data-stu-id="27b89-110">The Get-AzSynapseSqlPoolSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure Synapse SQL pool.</span></span>

## <span data-ttu-id="27b89-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="27b89-111">EXAMPLES</span></span>

### <span data-ttu-id="27b89-112">1. példa: Az Azure Synapse SQL-készlet aktuális adattípusai és bizalmasság-címkéinek be szereznie.</span><span class="sxs-lookup"><span data-stu-id="27b89-112">Example 1: Get current information types and sensitivity labels of an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool

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

### <span data-ttu-id="27b89-113">2. példa: A Pipinget futtató Azure Synapse SQL-készlet aktuális adattípusai és bizalmasság-címkéinek begyűjtse.</span><span class="sxs-lookup"><span data-stu-id="27b89-113">Example 2: Get current information types and sensitivity labels of an Azure Synapse SQL pool with Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool | Get-AzSynapseSqlPoolSensitivityClassification

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

### <span data-ttu-id="27b89-114">3. példa: Az Azure Synapse SQL-készlet adott oszlopának aktuális adattípus- és bizalmasság-címkéje.</span><span class="sxs-lookup"><span data-stu-id="27b89-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="27b89-115">4. példa: Az Azure Synapse SQL-készlet egy adott oszlopának aktuális adattípus- és bizalmasság-címkéje a Piping használatával.</span><span class="sxs-lookup"><span data-stu-id="27b89-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolSensitivityClassification -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

## <span data-ttu-id="27b89-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27b89-116">PARAMETERS</span></span>

### <span data-ttu-id="27b89-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27b89-117">-AsJob</span></span>
<span data-ttu-id="27b89-118">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="27b89-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="27b89-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="27b89-119">-ColumnName</span></span>
<span data-ttu-id="27b89-120">Az oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="27b89-120">Name of column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27b89-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27b89-121">-DefaultProfile</span></span>
<span data-ttu-id="27b89-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="27b89-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27b89-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27b89-123">-ResourceGroupName</span></span>
<span data-ttu-id="27b89-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="27b89-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27b89-125">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="27b89-125">-SchemaName</span></span>
<span data-ttu-id="27b89-126">A séma neve.</span><span class="sxs-lookup"><span data-stu-id="27b89-126">Name of schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27b89-127">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="27b89-127">-SqlPoolName</span></span>
<span data-ttu-id="27b89-128">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="27b89-128">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27b89-129">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="27b89-129">-SqlPoolObject</span></span>
<span data-ttu-id="27b89-130">SQL-készlet bemeneti objektuma, amely általában a folyamaton keresztül áthalad.</span><span class="sxs-lookup"><span data-stu-id="27b89-130">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SqlPoolObjectParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27b89-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="27b89-131">-TableName</span></span>
<span data-ttu-id="27b89-132">A tábla neve.</span><span class="sxs-lookup"><span data-stu-id="27b89-132">Name of table.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27b89-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="27b89-133">-WorkspaceName</span></span>
<span data-ttu-id="27b89-134">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="27b89-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27b89-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27b89-135">CommonParameters</span></span>
<span data-ttu-id="27b89-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27b89-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27b89-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27b89-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27b89-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="27b89-138">INPUTS</span></span>

### <span data-ttu-id="27b89-139">System.String</span><span class="sxs-lookup"><span data-stu-id="27b89-139">System.String</span></span>

### <span data-ttu-id="27b89-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="27b89-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="27b89-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27b89-141">OUTPUTS</span></span>

### <span data-ttu-id="27b89-142">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="27b89-142">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

## <span data-ttu-id="27b89-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="27b89-143">NOTES</span></span>

## <span data-ttu-id="27b89-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27b89-144">RELATED LINKS</span></span>
