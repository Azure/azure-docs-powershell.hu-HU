---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 4a9f785519710b7a6653b1ece27d7b526fceab31
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479241"
---
# <span data-ttu-id="c958c-101">Set-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="c958c-101">Set-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="c958c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c958c-102">SYNOPSIS</span></span>
<span data-ttu-id="c958c-103">Frissíti a szolgáltatás topológiáját.</span><span class="sxs-lookup"><span data-stu-id="c958c-103">Updates the service topology.</span></span>

## <span data-ttu-id="c958c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c958c-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c958c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c958c-105">DESCRIPTION</span></span>
<span data-ttu-id="c958c-106">A **Set-AzDeploymentManagerServiceTopology** parancsmag frissíti a szolgáltatás topológiáját a megadott szolgáltatás topológiaobjektummal.</span><span class="sxs-lookup"><span data-stu-id="c958c-106">The **Set-AzDeploymentManagerServiceTopology** cmdlet updates a service topology with the specified service topology object.</span></span>
<span data-ttu-id="c958c-107">A parancsmag visszaadja a frissített szolgáltatás topológiaobjektumot.</span><span class="sxs-lookup"><span data-stu-id="c958c-107">The cmdlet returns the updated service topology object.</span></span>

## <span data-ttu-id="c958c-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c958c-108">EXAMPLES</span></span>

### <span data-ttu-id="c958c-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="c958c-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="c958c-110">Ez a parancs frissíti a szolgáltatás topológiáját, amelynek neve és ResourceGroup tulajdonsága megegyezik a $serviceTopologyObject ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="c958c-110">This command updates a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>
<span data-ttu-id="c958c-111">A parancs a frissített szolgáltatás topológiaobjektumot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="c958c-111">The command returns the updated service topology object.</span></span>

## <span data-ttu-id="c958c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c958c-112">PARAMETERS</span></span>

### <span data-ttu-id="c958c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c958c-113">-DefaultProfile</span></span>
<span data-ttu-id="c958c-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c958c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c958c-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c958c-115">-InputObject</span></span>
<span data-ttu-id="c958c-116">A szolgáltatás topológia objektuma.</span><span class="sxs-lookup"><span data-stu-id="c958c-116">The service topology object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c958c-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c958c-117">-Confirm</span></span>
<span data-ttu-id="c958c-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c958c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c958c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c958c-119">-WhatIf</span></span>
<span data-ttu-id="c958c-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c958c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c958c-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c958c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c958c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c958c-122">CommonParameters</span></span>
<span data-ttu-id="c958c-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c958c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c958c-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c958c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c958c-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c958c-125">INPUTS</span></span>

### <span data-ttu-id="c958c-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="c958c-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="c958c-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c958c-127">OUTPUTS</span></span>

### <span data-ttu-id="c958c-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="c958c-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="c958c-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c958c-129">NOTES</span></span>

## <span data-ttu-id="c958c-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c958c-130">RELATED LINKS</span></span>
