---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqladvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedDataSecurityPolicy.md
ms.openlocfilehash: b0d21c8d59d2a33671fead2e88d402779f99fb7f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165627"
---
# <span data-ttu-id="54767-101">Get-AzSynapseSqlAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="54767-101">Get-AzSynapseSqlAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="54767-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54767-102">SYNOPSIS</span></span>
<span data-ttu-id="54767-103">A munkaterület speciális adatbiztonsági házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="54767-103">Gets Advanced Data Security policy of a workspace.</span></span>

## <span data-ttu-id="54767-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="54767-104">SYNTAX</span></span>

### <span data-ttu-id="54767-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="54767-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54767-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54767-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54767-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="54767-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="54767-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="54767-108">DESCRIPTION</span></span>
<span data-ttu-id="54767-109">A **Get-AzSynapseSqlAdvancedDataSecurityPolicy** parancsmag beolvassa egy munkaterület speciális adatbiztonsági házirendjét.</span><span class="sxs-lookup"><span data-stu-id="54767-109">The **Get-AzSynapseSqlAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a workspace.</span></span>

## <span data-ttu-id="54767-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="54767-110">EXAMPLES</span></span>

### <span data-ttu-id="54767-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="54767-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedDataSecurityPolicy -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="54767-112">Ez a parancs a Speciális adatbiztonság parancsot kapja a ContosoWorkspace nevű munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="54767-112">This command gets Advanced Data Security on the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="54767-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="54767-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Get-AzSynapseSqlAdvancedDataSecurityPolicy
```

<span data-ttu-id="54767-114">Ez a parancs a Speciális adatbiztonság parancsot kapja a ContosoWorkspace nevű munkaterületen a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="54767-114">This command gets Advanced Data Security on the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="54767-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54767-115">PARAMETERS</span></span>

### <span data-ttu-id="54767-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54767-116">-DefaultProfile</span></span>
<span data-ttu-id="54767-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="54767-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54767-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54767-118">-InputObject</span></span>
<span data-ttu-id="54767-119">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="54767-119">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="54767-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54767-120">-ResourceGroupName</span></span>
<span data-ttu-id="54767-121">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="54767-121">Resource group name.</span></span>

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

### <span data-ttu-id="54767-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54767-122">-ResourceId</span></span>
<span data-ttu-id="54767-123">A Synapse-munkaterület erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="54767-123">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="54767-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="54767-124">-WorkspaceName</span></span>
<span data-ttu-id="54767-125">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="54767-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="54767-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54767-126">CommonParameters</span></span>
<span data-ttu-id="54767-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54767-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54767-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54767-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54767-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="54767-129">INPUTS</span></span>

### <span data-ttu-id="54767-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="54767-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="54767-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="54767-131">OUTPUTS</span></span>

### <span data-ttu-id="54767-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="54767-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="54767-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="54767-133">NOTES</span></span>

## <span data-ttu-id="54767-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="54767-134">RELATED LINKS</span></span>
