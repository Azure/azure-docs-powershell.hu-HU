---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlDatabase.md
ms.openlocfilehash: c203e9c80978f50bd7879627b733de2ec0c6cf7e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359405"
---
# <span data-ttu-id="aca2d-101">Get-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="aca2d-101">Get-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="aca2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aca2d-102">SYNOPSIS</span></span>
<span data-ttu-id="aca2d-103">Synapse Analytics SQL-adatbázist kap.</span><span class="sxs-lookup"><span data-stu-id="aca2d-103">Gets a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="aca2d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="aca2d-104">SYNTAX</span></span>

### <span data-ttu-id="aca2d-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aca2d-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aca2d-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aca2d-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlDatabase [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aca2d-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aca2d-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlDatabase -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aca2d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="aca2d-108">DESCRIPTION</span></span>
<span data-ttu-id="aca2d-109">[Ez a funkció korlátozott előzetes verzióban érhető el, kezdetben csak bizonyos előfizetések számára érhető el.] A **Get-AzSynapseSqlDatabase** parancsmag információkat kap egy Azure Synapse Analytics SQL-adatbázisról.</span><span class="sxs-lookup"><span data-stu-id="aca2d-109">[This feature is in a limited preview, initially accessible only to certain subscriptions.] The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="aca2d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="aca2d-110">EXAMPLES</span></span>

### <span data-ttu-id="aca2d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="aca2d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="aca2d-112">Ez a parancs munkaterület alatt tárolja az összes SQL-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="aca2d-112">This command gets all SQL databases under a workspace.</span></span>

### <span data-ttu-id="aca2d-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="aca2d-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="aca2d-114">Ez a parancs a ContosoWorkspace munkaterületre beszúrja az SQL-adatbázist ContosoSqlDatabase néven.</span><span class="sxs-lookup"><span data-stu-id="aca2d-114">This command gets the SQL database under workspace ContosoWorkspace with name ContosoSqlDatabase.</span></span>

### <span data-ttu-id="aca2d-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="aca2d-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlDatabase
```

<span data-ttu-id="aca2d-116">Ez a parancs az összes SQL-adatbázist egy munkaterület alá beszúrja egy folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="aca2d-116">This command gets all the SQL databases under a workspace through pipeline.</span></span>

### <span data-ttu-id="aca2d-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="aca2d-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase"
```

<span data-ttu-id="aca2d-118">Ez a parancs a megadott erőforrás-azonosítójú SQL-adatbázist kapja meg.</span><span class="sxs-lookup"><span data-stu-id="aca2d-118">This command gets the SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="aca2d-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aca2d-119">PARAMETERS</span></span>

### <span data-ttu-id="aca2d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aca2d-120">-DefaultProfile</span></span>
<span data-ttu-id="aca2d-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aca2d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aca2d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="aca2d-122">-Name</span></span>
<span data-ttu-id="aca2d-123">A Synapse SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="aca2d-123">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="aca2d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aca2d-124">-ResourceGroupName</span></span>
<span data-ttu-id="aca2d-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="aca2d-125">Resource group name.</span></span>

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

### <span data-ttu-id="aca2d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aca2d-126">-ResourceId</span></span>
<span data-ttu-id="aca2d-127">A Synapse SQL-adatbázis erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="aca2d-127">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="aca2d-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="aca2d-128">-WorkspaceName</span></span>
<span data-ttu-id="aca2d-129">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="aca2d-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="aca2d-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="aca2d-130">-WorkspaceObject</span></span>
<span data-ttu-id="aca2d-131">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="aca2d-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="aca2d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aca2d-132">CommonParameters</span></span>
<span data-ttu-id="aca2d-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aca2d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aca2d-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aca2d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aca2d-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aca2d-135">INPUTS</span></span>

### <span data-ttu-id="aca2d-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="aca2d-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="aca2d-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aca2d-137">OUTPUTS</span></span>

### <span data-ttu-id="aca2d-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="aca2d-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="aca2d-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="aca2d-139">NOTES</span></span>

## <span data-ttu-id="aca2d-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aca2d-140">RELATED LINKS</span></span>
