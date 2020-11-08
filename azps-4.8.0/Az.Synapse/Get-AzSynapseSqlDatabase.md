---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlDatabase.md
ms.openlocfilehash: c203e9c80978f50bd7879627b733de2ec0c6cf7e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180724"
---
# <span data-ttu-id="243a2-101">Get-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="243a2-101">Get-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="243a2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="243a2-102">SYNOPSIS</span></span>
<span data-ttu-id="243a2-103">A szinapszis Analytics SQL-adatbázis beolvasása</span><span class="sxs-lookup"><span data-stu-id="243a2-103">Gets a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="243a2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="243a2-104">SYNTAX</span></span>

### <span data-ttu-id="243a2-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="243a2-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="243a2-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="243a2-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlDatabase [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="243a2-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="243a2-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlDatabase -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="243a2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="243a2-108">DESCRIPTION</span></span>
<span data-ttu-id="243a2-109">[Ez a funkció egy korlátozott előzetes verzió, amely eredetileg csak bizonyos előfizetésekhez érhető el.] A **Get-AzSynapseSqlDatabase** parancsmag információkat kap az Azure SZINAPSZIS Analytics SQL-adatbázisról.</span><span class="sxs-lookup"><span data-stu-id="243a2-109">[This feature is in a limited preview, initially accessible only to certain subscriptions.] The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="243a2-110">Példák</span><span class="sxs-lookup"><span data-stu-id="243a2-110">EXAMPLES</span></span>

### <span data-ttu-id="243a2-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="243a2-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="243a2-112">Ez a parancs minden SQL-adatbázist beolvas egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="243a2-112">This command gets all SQL databases under a workspace.</span></span>

### <span data-ttu-id="243a2-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="243a2-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="243a2-114">Ez a parancs az SQL-adatbázist az ContosoSqlDatabase nevű munkaterület-ContosoWorkspace kapja.</span><span class="sxs-lookup"><span data-stu-id="243a2-114">This command gets the SQL database under workspace ContosoWorkspace with name ContosoSqlDatabase.</span></span>

### <span data-ttu-id="243a2-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="243a2-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlDatabase
```

<span data-ttu-id="243a2-116">Ez a parancs a munkaterületen a csővezetéken keresztül minden SQL-adatbázishoz jut.</span><span class="sxs-lookup"><span data-stu-id="243a2-116">This command gets all the SQL databases under a workspace through pipeline.</span></span>

### <span data-ttu-id="243a2-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="243a2-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase"
```

<span data-ttu-id="243a2-118">Ez a parancs az SQL-adatbázist a megadott erőforrás-AZONOSÍTÓval kapja.</span><span class="sxs-lookup"><span data-stu-id="243a2-118">This command gets the SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="243a2-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="243a2-119">PARAMETERS</span></span>

### <span data-ttu-id="243a2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="243a2-120">-DefaultProfile</span></span>
<span data-ttu-id="243a2-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="243a2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="243a2-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="243a2-122">-Name</span></span>
<span data-ttu-id="243a2-123">A szinapszis SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="243a2-123">Name of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="243a2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="243a2-124">-ResourceGroupName</span></span>
<span data-ttu-id="243a2-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="243a2-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="243a2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="243a2-126">-ResourceId</span></span>
<span data-ttu-id="243a2-127">A szinapszis SQL-adatbázis erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="243a2-127">Resource identifier of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="243a2-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="243a2-128">-WorkspaceName</span></span>
<span data-ttu-id="243a2-129">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="243a2-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="243a2-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="243a2-130">-WorkspaceObject</span></span>
<span data-ttu-id="243a2-131">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="243a2-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="243a2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="243a2-132">CommonParameters</span></span>
<span data-ttu-id="243a2-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="243a2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="243a2-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="243a2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="243a2-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="243a2-135">INPUTS</span></span>

### <span data-ttu-id="243a2-136">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="243a2-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="243a2-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="243a2-137">OUTPUTS</span></span>

### <span data-ttu-id="243a2-138">Microsoft. Azure. commands. szinapszis. models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="243a2-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="243a2-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="243a2-139">NOTES</span></span>

## <span data-ttu-id="243a2-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="243a2-140">RELATED LINKS</span></span>
