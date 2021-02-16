---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
ms.openlocfilehash: fb3f7ccab164370e1c55992a666ac7256b5a4a95
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163739"
---
# <span data-ttu-id="04201-101">Set-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="04201-101">Set-AzDeploymentManagerService</span></span>

## <span data-ttu-id="04201-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04201-102">SYNOPSIS</span></span>
<span data-ttu-id="04201-103">Frissíti a szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="04201-103">Updates the service.</span></span>

## <span data-ttu-id="04201-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="04201-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04201-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="04201-105">DESCRIPTION</span></span>
<span data-ttu-id="04201-106">A **Set-AzDeploymentManagerService parancsmag** frissíti a szolgáltatást a megadott szolgáltatásobjektummal.</span><span class="sxs-lookup"><span data-stu-id="04201-106">The **Set-AzDeploymentManagerService** cmdlet updates a service with the specified service object.</span></span>
<span data-ttu-id="04201-107">A parancsmag a frissített szolgáltatásobjektumot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="04201-107">The cmdlet returns the updated service object.</span></span>

## <span data-ttu-id="04201-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="04201-108">EXAMPLES</span></span>

### <span data-ttu-id="04201-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="04201-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="04201-110">Ez a parancs frissíti azt a szolgáltatást, amelynek a neve, a szolgáltatás topológiája és az Erőforráscsoport neve megegyezik a $serviceObject, ServiceTopologyName és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="04201-110">This command updates a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
<span data-ttu-id="04201-111">A szolgáltatás frissülni fog a $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="04201-111">The service would be updated to the properties set in the $serviceObject.</span></span>

## <span data-ttu-id="04201-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04201-112">PARAMETERS</span></span>

### <span data-ttu-id="04201-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04201-113">-DefaultProfile</span></span>
<span data-ttu-id="04201-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="04201-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04201-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04201-115">-InputObject</span></span>
<span data-ttu-id="04201-116">A szolgáltatásobjektum.</span><span class="sxs-lookup"><span data-stu-id="04201-116">The service object.</span></span>

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

### <span data-ttu-id="04201-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04201-117">-Confirm</span></span>
<span data-ttu-id="04201-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="04201-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04201-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04201-119">-WhatIf</span></span>
<span data-ttu-id="04201-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="04201-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04201-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="04201-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04201-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04201-122">CommonParameters</span></span>
<span data-ttu-id="04201-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04201-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04201-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04201-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04201-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="04201-125">INPUTS</span></span>

### <span data-ttu-id="04201-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="04201-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="04201-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04201-127">OUTPUTS</span></span>

### <span data-ttu-id="04201-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="04201-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="04201-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="04201-129">NOTES</span></span>

## <span data-ttu-id="04201-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04201-130">RELATED LINKS</span></span>
