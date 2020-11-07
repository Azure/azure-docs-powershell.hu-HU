---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 3509212801aaeda9926b7f441e0aae7e17f8cbb2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670969"
---
# <span data-ttu-id="8bfed-101">Set-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="8bfed-101">Set-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="8bfed-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8bfed-102">SYNOPSIS</span></span>
<span data-ttu-id="8bfed-103">Frissíti a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="8bfed-103">Updates the service unit.</span></span>

## <span data-ttu-id="8bfed-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8bfed-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bfed-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8bfed-105">DESCRIPTION</span></span>
<span data-ttu-id="8bfed-106">A **set-AzDeploymentManagerServiceUnit** parancsmag a megadott szervizcikksor-objektummal frissíti a szolgáltatási egységet.</span><span class="sxs-lookup"><span data-stu-id="8bfed-106">The **Set-AzDeploymentManagerServiceUnit** cmdlet updates a service unit with the specified service unit object.</span></span>
<span data-ttu-id="8bfed-107">A parancsmag a frissített Service Unit objektum értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="8bfed-107">The cmdlet returns the updated service unit object.</span></span>

## <span data-ttu-id="8bfed-108">Példák</span><span class="sxs-lookup"><span data-stu-id="8bfed-108">EXAMPLES</span></span>

### <span data-ttu-id="8bfed-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8bfed-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="8bfed-110">A parancs frissíti azt a szolgáltatási egységet, amelynek a neve, a szolgáltatásnév, a szolgáltatás topológiájának neve és a ResourceGroup megegyezik a $serviceUnitObject, a szolgáltatásnév, a ServiceTopologyName és a ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="8bfed-110">This command updates a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>
<span data-ttu-id="8bfed-111">A parancs a frissített szervizcikk-objektumot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="8bfed-111">The command returns the updated service unit object.</span></span>

## <span data-ttu-id="8bfed-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8bfed-112">PARAMETERS</span></span>

### <span data-ttu-id="8bfed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bfed-113">-DefaultProfile</span></span>
<span data-ttu-id="8bfed-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8bfed-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bfed-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8bfed-115">-InputObject</span></span>
<span data-ttu-id="8bfed-116">A Service Unit objektum.</span><span class="sxs-lookup"><span data-stu-id="8bfed-116">The service unit object.</span></span>

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

### <span data-ttu-id="8bfed-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8bfed-117">-Confirm</span></span>
<span data-ttu-id="8bfed-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8bfed-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bfed-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bfed-119">-WhatIf</span></span>
<span data-ttu-id="8bfed-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8bfed-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bfed-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8bfed-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bfed-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bfed-122">CommonParameters</span></span>
<span data-ttu-id="8bfed-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8bfed-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bfed-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bfed-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bfed-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8bfed-125">INPUTS</span></span>

### <span data-ttu-id="8bfed-126">Microsoft. Azure. Command. DeploymentManager. models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="8bfed-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="8bfed-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8bfed-127">OUTPUTS</span></span>

### <span data-ttu-id="8bfed-128">Microsoft. Azure. Command. DeploymentManager. models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="8bfed-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="8bfed-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8bfed-129">NOTES</span></span>

## <span data-ttu-id="8bfed-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8bfed-130">RELATED LINKS</span></span>
