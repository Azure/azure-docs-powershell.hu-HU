---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 7d2a7916e73b20e4c4e7a3602dc23bc10a67c744
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467921"
---
# <span data-ttu-id="df6fc-101">Set-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="df6fc-101">Set-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="df6fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df6fc-102">SYNOPSIS</span></span>
<span data-ttu-id="df6fc-103">Frissíti a szervizegységet.</span><span class="sxs-lookup"><span data-stu-id="df6fc-103">Updates the service unit.</span></span>

## <span data-ttu-id="df6fc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="df6fc-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df6fc-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="df6fc-105">DESCRIPTION</span></span>
<span data-ttu-id="df6fc-106">A **Set-AzDeploymentManagerServiceUnit** parancsmag frissíti a szolgáltatási egységet a megadott szolgáltatásiegység-objektummal.</span><span class="sxs-lookup"><span data-stu-id="df6fc-106">The **Set-AzDeploymentManagerServiceUnit** cmdlet updates a service unit with the specified service unit object.</span></span>
<span data-ttu-id="df6fc-107">A parancsmag a frissített szolgáltatásiegység-objektumot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="df6fc-107">The cmdlet returns the updated service unit object.</span></span>

## <span data-ttu-id="df6fc-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="df6fc-108">EXAMPLES</span></span>

### <span data-ttu-id="df6fc-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="df6fc-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="df6fc-110">Ez a parancs frissíti a szolgáltatásegységet, amelynek neve, szolgáltatásneve, szolgáltatás topológiája és Erőforráscsoportneve megegyezik a $serviceUnitObject, ServiceName, ServiceTopologyName és ResourceGroupName tulajdonságának nevével.</span><span class="sxs-lookup"><span data-stu-id="df6fc-110">This command updates a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>
<span data-ttu-id="df6fc-111">A parancs a frissített szolgáltatásegység-objektumot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="df6fc-111">The command returns the updated service unit object.</span></span>

## <span data-ttu-id="df6fc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df6fc-112">PARAMETERS</span></span>

### <span data-ttu-id="df6fc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df6fc-113">-DefaultProfile</span></span>
<span data-ttu-id="df6fc-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="df6fc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df6fc-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df6fc-115">-InputObject</span></span>
<span data-ttu-id="df6fc-116">A szolgáltatásiegység-objektum.</span><span class="sxs-lookup"><span data-stu-id="df6fc-116">The service unit object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df6fc-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df6fc-117">-Confirm</span></span>
<span data-ttu-id="df6fc-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="df6fc-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df6fc-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df6fc-119">-WhatIf</span></span>
<span data-ttu-id="df6fc-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="df6fc-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df6fc-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="df6fc-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df6fc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df6fc-122">CommonParameters</span></span>
<span data-ttu-id="df6fc-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df6fc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df6fc-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df6fc-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df6fc-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="df6fc-125">INPUTS</span></span>

### <span data-ttu-id="df6fc-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="df6fc-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="df6fc-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df6fc-127">OUTPUTS</span></span>

### <span data-ttu-id="df6fc-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="df6fc-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="df6fc-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="df6fc-129">NOTES</span></span>

## <span data-ttu-id="df6fc-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df6fc-130">RELATED LINKS</span></span>
