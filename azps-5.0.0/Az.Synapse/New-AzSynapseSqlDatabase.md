---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
ms.openlocfilehash: 16f2df5900fcc522f0ff3afb7b9f5b14ea5f0b64
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195003"
---
# <span data-ttu-id="6e62b-101">New-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6e62b-101">New-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="6e62b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6e62b-102">SYNOPSIS</span></span>
<span data-ttu-id="6e62b-103">A szinapszis Analytics SQL-adatbázis létrehozása.</span><span class="sxs-lookup"><span data-stu-id="6e62b-103">Creates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="6e62b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6e62b-104">SYNTAX</span></span>

### <span data-ttu-id="6e62b-105">CreateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6e62b-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e62b-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e62b-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlDatabase -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e62b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6e62b-107">DESCRIPTION</span></span>
<span data-ttu-id="6e62b-108">A **Get-AzSynapseSqlDatabase** parancsmag információkat kap az Azure SZINAPSZIS Analytics SQL-adatbázisról.</span><span class="sxs-lookup"><span data-stu-id="6e62b-108">The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>


## <span data-ttu-id="6e62b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6e62b-109">EXAMPLES</span></span>

### <span data-ttu-id="6e62b-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6e62b-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase 
```

<span data-ttu-id="6e62b-111">Ez a parancs az Azure szinapszis Analytics SQL-adatbázisát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="6e62b-111">This command creates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="6e62b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6e62b-112">PARAMETERS</span></span>

### <span data-ttu-id="6e62b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e62b-113">-AsJob</span></span>
<span data-ttu-id="6e62b-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6e62b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6e62b-115">-Szétválogatás</span><span class="sxs-lookup"><span data-stu-id="6e62b-115">-Collation</span></span>
<span data-ttu-id="6e62b-116">A szétválogatás az adatrendezési és-összehasonlító szabályokat határozza meg, az SQL-készlet létrehozása után azonban nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="6e62b-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="6e62b-117">Az alapértelmezett rendezési sorrend SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="6e62b-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

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

### <span data-ttu-id="6e62b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e62b-118">-DefaultProfile</span></span>
<span data-ttu-id="6e62b-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6e62b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e62b-120">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="6e62b-120">-MaxSizeInBytes</span></span>
<span data-ttu-id="6e62b-121">Az adatbázis maximális méretét adja meg bájtban.</span><span class="sxs-lookup"><span data-stu-id="6e62b-121">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e62b-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6e62b-122">-Name</span></span>
<span data-ttu-id="6e62b-123">A szinapszis SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="6e62b-123">Name of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e62b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e62b-124">-ResourceGroupName</span></span>
<span data-ttu-id="6e62b-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="6e62b-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e62b-126">-Címke</span><span class="sxs-lookup"><span data-stu-id="6e62b-126">-Tag</span></span>
<span data-ttu-id="6e62b-127">Az erőforráshoz társított címkék karakterlánca, karakterláncok szótára</span><span class="sxs-lookup"><span data-stu-id="6e62b-127">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e62b-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6e62b-128">-WorkspaceName</span></span>
<span data-ttu-id="6e62b-129">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="6e62b-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e62b-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6e62b-130">-WorkspaceObject</span></span>
<span data-ttu-id="6e62b-131">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="6e62b-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e62b-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6e62b-132">-Confirm</span></span>
<span data-ttu-id="6e62b-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6e62b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e62b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e62b-134">-WhatIf</span></span>
<span data-ttu-id="6e62b-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6e62b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e62b-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6e62b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e62b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e62b-137">CommonParameters</span></span>
<span data-ttu-id="6e62b-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6e62b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e62b-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6e62b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e62b-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e62b-140">INPUTS</span></span>

### <span data-ttu-id="6e62b-141">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6e62b-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="6e62b-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e62b-142">OUTPUTS</span></span>

### <span data-ttu-id="6e62b-143">Microsoft. Azure. commands. szinapszis. models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6e62b-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="6e62b-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6e62b-144">NOTES</span></span>

## <span data-ttu-id="6e62b-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e62b-145">RELATED LINKS</span></span>
