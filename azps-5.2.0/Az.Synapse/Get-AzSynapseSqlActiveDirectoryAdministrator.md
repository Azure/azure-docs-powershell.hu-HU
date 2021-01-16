---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: d3ea1a67d8afa15549c19d6099dc727aab43adc5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334073"
---
# <span data-ttu-id="73af4-101">Get-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="73af4-101">Get-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="73af4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73af4-102">SYNOPSIS</span></span>
<span data-ttu-id="73af4-103">Információkat kap egy Azure AD-rendszergazdáról a Synapse Analytics Workspace-hez.</span><span class="sxs-lookup"><span data-stu-id="73af4-103">Gets information about an Azure AD administrator for Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="73af4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="73af4-104">SYNTAX</span></span>

### <span data-ttu-id="73af4-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="73af4-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73af4-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73af4-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73af4-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73af4-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="73af4-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="73af4-108">DESCRIPTION</span></span>
<span data-ttu-id="73af4-109">A **Get-AzSynapseSqlActiveDirectoryAdministrator** parancsmag információt kap egy Azure Active Directory (Azure AD) rendszergazdáról egy Azure Synapse Analytics Workspace-hez az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="73af4-109">The **Get-AzSynapseSqlActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an Azure Synapse Analytics Workspace in the current subscription.</span></span>

## <span data-ttu-id="73af4-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="73af4-110">EXAMPLES</span></span>

### <span data-ttu-id="73af4-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="73af4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="73af4-112">Ez a parancs információkat kap egy ContosoWorkspace nevű munkaterület Azure AD-rendszergazdájának adatairól.</span><span class="sxs-lookup"><span data-stu-id="73af4-112">This command gets information about an Azure AD administrator for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="73af4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73af4-113">PARAMETERS</span></span>

### <span data-ttu-id="73af4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73af4-114">-DefaultProfile</span></span>
<span data-ttu-id="73af4-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="73af4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73af4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73af4-116">-InputObject</span></span>
<span data-ttu-id="73af4-117">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="73af4-117">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73af4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73af4-118">-ResourceGroupName</span></span>
<span data-ttu-id="73af4-119">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="73af4-119">Resource group name.</span></span>

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

### <span data-ttu-id="73af4-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73af4-120">-ResourceId</span></span>
<span data-ttu-id="73af4-121">A Synapse-munkaterület erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="73af4-121">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="73af4-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="73af4-122">-WorkspaceName</span></span>
<span data-ttu-id="73af4-123">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="73af4-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="73af4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73af4-124">CommonParameters</span></span>
<span data-ttu-id="73af4-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73af4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73af4-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73af4-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73af4-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73af4-127">INPUTS</span></span>

### <span data-ttu-id="73af4-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="73af4-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="73af4-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="73af4-129">OUTPUTS</span></span>

### <span data-ttu-id="73af4-130">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span><span class="sxs-lookup"><span data-stu-id="73af4-130">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span></span>

## <span data-ttu-id="73af4-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="73af4-131">NOTES</span></span>

## <span data-ttu-id="73af4-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="73af4-132">RELATED LINKS</span></span>
