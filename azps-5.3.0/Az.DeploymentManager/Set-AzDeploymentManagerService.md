---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
ms.openlocfilehash: fb3f7ccab164370e1c55992a666ac7256b5a4a95
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469945"
---
# <span data-ttu-id="dd67a-101">Set-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="dd67a-101">Set-AzDeploymentManagerService</span></span>

## <span data-ttu-id="dd67a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd67a-102">SYNOPSIS</span></span>
<span data-ttu-id="dd67a-103">Frissíti a szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="dd67a-103">Updates the service.</span></span>

## <span data-ttu-id="dd67a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dd67a-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd67a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dd67a-105">DESCRIPTION</span></span>
<span data-ttu-id="dd67a-106">A **Set-AzDeploymentManagerService parancsmag** frissíti a szolgáltatást a megadott szolgáltatásobjektummal.</span><span class="sxs-lookup"><span data-stu-id="dd67a-106">The **Set-AzDeploymentManagerService** cmdlet updates a service with the specified service object.</span></span>
<span data-ttu-id="dd67a-107">A parancsmag a frissített szolgáltatásobjektumot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="dd67a-107">The cmdlet returns the updated service object.</span></span>

## <span data-ttu-id="dd67a-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dd67a-108">EXAMPLES</span></span>

### <span data-ttu-id="dd67a-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="dd67a-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="dd67a-110">Ez a parancs frissíti azt a szolgáltatást, amelynek a neve, a szolgáltatás topológiája és az Erőforráscsoport neve megegyezik a $serviceObject, ServiceTopologyName és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="dd67a-110">This command updates a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
<span data-ttu-id="dd67a-111">A szolgáltatás frissülni fog a $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="dd67a-111">The service would be updated to the properties set in the $serviceObject.</span></span>

## <span data-ttu-id="dd67a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd67a-112">PARAMETERS</span></span>

### <span data-ttu-id="dd67a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd67a-113">-DefaultProfile</span></span>
<span data-ttu-id="dd67a-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dd67a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd67a-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd67a-115">-InputObject</span></span>
<span data-ttu-id="dd67a-116">A szolgáltatásobjektum.</span><span class="sxs-lookup"><span data-stu-id="dd67a-116">The service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd67a-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd67a-117">-Confirm</span></span>
<span data-ttu-id="dd67a-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="dd67a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd67a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd67a-119">-WhatIf</span></span>
<span data-ttu-id="dd67a-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="dd67a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd67a-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dd67a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd67a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd67a-122">CommonParameters</span></span>
<span data-ttu-id="dd67a-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd67a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd67a-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd67a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd67a-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dd67a-125">INPUTS</span></span>

### <span data-ttu-id="dd67a-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="dd67a-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="dd67a-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd67a-127">OUTPUTS</span></span>

### <span data-ttu-id="dd67a-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="dd67a-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="dd67a-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dd67a-129">NOTES</span></span>

## <span data-ttu-id="dd67a-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd67a-130">RELATED LINKS</span></span>
