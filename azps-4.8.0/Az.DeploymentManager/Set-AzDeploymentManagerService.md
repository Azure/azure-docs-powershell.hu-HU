---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
ms.openlocfilehash: fb3f7ccab164370e1c55992a666ac7256b5a4a95
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182806"
---
# <span data-ttu-id="45034-101">Set-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="45034-101">Set-AzDeploymentManagerService</span></span>

## <span data-ttu-id="45034-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="45034-102">SYNOPSIS</span></span>
<span data-ttu-id="45034-103">Frissíti a szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="45034-103">Updates the service.</span></span>

## <span data-ttu-id="45034-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="45034-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45034-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="45034-105">DESCRIPTION</span></span>
<span data-ttu-id="45034-106">A **set-AzDeploymentManagerService** parancsmag a megadott szolgáltatási objektummal frissíti a szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="45034-106">The **Set-AzDeploymentManagerService** cmdlet updates a service with the specified service object.</span></span>
<span data-ttu-id="45034-107">A parancsmag a frissített szolgáltatási objektumot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="45034-107">The cmdlet returns the updated service object.</span></span>

## <span data-ttu-id="45034-108">Példák</span><span class="sxs-lookup"><span data-stu-id="45034-108">EXAMPLES</span></span>

### <span data-ttu-id="45034-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="45034-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="45034-110">Ez a parancs frissíti azt a szolgáltatást, amelynek a neve, a szolgáltatás topológiájának neve és a ResourceGroup megegyezik a $serviceObject neve, a ServiceTopologyName és a ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="45034-110">This command updates a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
<span data-ttu-id="45034-111">A szolgáltatás frissült a $serviceObjectban beállított tulajdonságokra.</span><span class="sxs-lookup"><span data-stu-id="45034-111">The service would be updated to the properties set in the $serviceObject.</span></span>

## <span data-ttu-id="45034-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="45034-112">PARAMETERS</span></span>

### <span data-ttu-id="45034-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45034-113">-DefaultProfile</span></span>
<span data-ttu-id="45034-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="45034-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45034-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45034-115">-InputObject</span></span>
<span data-ttu-id="45034-116">A szolgáltatás objektuma.</span><span class="sxs-lookup"><span data-stu-id="45034-116">The service object.</span></span>

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

### <span data-ttu-id="45034-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="45034-117">-Confirm</span></span>
<span data-ttu-id="45034-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="45034-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45034-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45034-119">-WhatIf</span></span>
<span data-ttu-id="45034-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="45034-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45034-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="45034-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45034-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45034-122">CommonParameters</span></span>
<span data-ttu-id="45034-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="45034-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45034-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="45034-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45034-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="45034-125">INPUTS</span></span>

### <span data-ttu-id="45034-126">Microsoft. Azure. Command. DeploymentManager. models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="45034-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="45034-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45034-127">OUTPUTS</span></span>

### <span data-ttu-id="45034-128">Microsoft. Azure. Command. DeploymentManager. models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="45034-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="45034-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="45034-129">NOTES</span></span>

## <span data-ttu-id="45034-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45034-130">RELATED LINKS</span></span>
