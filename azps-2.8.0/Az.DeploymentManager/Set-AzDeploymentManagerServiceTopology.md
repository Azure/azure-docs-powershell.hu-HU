---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: ff3cdb549835ceb4689ee5be8569b61ffa89538d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666634"
---
# <span data-ttu-id="d46de-101">Set-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="d46de-101">Set-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="d46de-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d46de-102">SYNOPSIS</span></span>
<span data-ttu-id="d46de-103">Frissíti a szolgáltatási topológiát.</span><span class="sxs-lookup"><span data-stu-id="d46de-103">Updates the service topology.</span></span>

## <span data-ttu-id="d46de-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d46de-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d46de-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d46de-105">DESCRIPTION</span></span>
<span data-ttu-id="d46de-106">A **set-AzDeploymentManagerServiceTopology** parancsmag a megadott szolgáltatási topológia objektummal frissíti a szolgáltatási topológiát.</span><span class="sxs-lookup"><span data-stu-id="d46de-106">The **Set-AzDeploymentManagerServiceTopology** cmdlet updates a service topology with the specified service topology object.</span></span>
<span data-ttu-id="d46de-107">A parancsmag a frissített szolgáltatási topológia objektumot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="d46de-107">The cmdlet returns the updated service topology object.</span></span>

## <span data-ttu-id="d46de-108">Példák</span><span class="sxs-lookup"><span data-stu-id="d46de-108">EXAMPLES</span></span>

### <span data-ttu-id="d46de-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d46de-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="d46de-110">Ez a parancs frissíti a szolgáltatási topológiát, amelynek a neve és a ResourceGroup megegyeznek a $serviceTopologyObject neve és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="d46de-110">This command updates a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>
<span data-ttu-id="d46de-111">A parancs a frissített szolgáltatás topológiája objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="d46de-111">The command returns the updated service topology object.</span></span>

## <span data-ttu-id="d46de-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d46de-112">PARAMETERS</span></span>

### <span data-ttu-id="d46de-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d46de-113">-DefaultProfile</span></span>
<span data-ttu-id="d46de-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d46de-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d46de-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d46de-115">-InputObject</span></span>
<span data-ttu-id="d46de-116">A szolgáltatás topológiája objektum.</span><span class="sxs-lookup"><span data-stu-id="d46de-116">The service topology object.</span></span>

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

### <span data-ttu-id="d46de-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d46de-117">-Confirm</span></span>
<span data-ttu-id="d46de-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d46de-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d46de-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d46de-119">-WhatIf</span></span>
<span data-ttu-id="d46de-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d46de-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d46de-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d46de-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d46de-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d46de-122">CommonParameters</span></span>
<span data-ttu-id="d46de-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d46de-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d46de-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d46de-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d46de-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d46de-125">INPUTS</span></span>

### <span data-ttu-id="d46de-126">Microsoft. Azure. Command. DeploymentManager. models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="d46de-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="d46de-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d46de-127">OUTPUTS</span></span>

### <span data-ttu-id="d46de-128">Microsoft. Azure. Command. DeploymentManager. models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="d46de-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="d46de-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d46de-129">NOTES</span></span>

## <span data-ttu-id="d46de-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d46de-130">RELATED LINKS</span></span>
