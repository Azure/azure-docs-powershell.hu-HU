---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: 6387e5a2938bdef99e4aea5e93248a0ecf8e8da7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491810"
---
# <span data-ttu-id="15a31-101">Set-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="15a31-101">Set-AzureRmDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="15a31-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="15a31-102">SYNOPSIS</span></span>
<span data-ttu-id="15a31-103">Frissíti a szolgáltatási topológiát.</span><span class="sxs-lookup"><span data-stu-id="15a31-103">Updates the service topology.</span></span>

## <span data-ttu-id="15a31-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="15a31-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerServiceTopology [-ServiceTopology] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15a31-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="15a31-105">DESCRIPTION</span></span>
<span data-ttu-id="15a31-106">A **set-AzureRmDeploymentManagerServiceTopology** parancsmag a megadott szolgáltatási topológia objektummal frissíti a szolgáltatási topológiát.</span><span class="sxs-lookup"><span data-stu-id="15a31-106">The **Set-AzureRmDeploymentManagerServiceTopology** cmdlet updates a service topology with the specified service topology object.</span></span>
<span data-ttu-id="15a31-107">A parancsmag a frissített szolgáltatási topológia objektumot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="15a31-107">The cmdlet returns the updated service topology object.</span></span>

## <span data-ttu-id="15a31-108">Példák</span><span class="sxs-lookup"><span data-stu-id="15a31-108">EXAMPLES</span></span>

### <span data-ttu-id="15a31-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="15a31-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDeploymentManagerService -ServiceTopology $serviceTopologyObject
```

<span data-ttu-id="15a31-110">Ez a parancs frissíti a szolgáltatási topológiát, amelynek a neve és a ResourceGroup megegyeznek a $serviceTopologyObject neve és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="15a31-110">This command updates a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>
<span data-ttu-id="15a31-111">A parancs a frissített szolgáltatás topológiája objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="15a31-111">The command returns the updated service topology object.</span></span>

## <span data-ttu-id="15a31-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="15a31-112">PARAMETERS</span></span>

### <span data-ttu-id="15a31-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15a31-113">-DefaultProfile</span></span>
<span data-ttu-id="15a31-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="15a31-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a31-115">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="15a31-115">-ServiceTopology</span></span>
<span data-ttu-id="15a31-116">A szolgáltatás topológiája objektum.</span><span class="sxs-lookup"><span data-stu-id="15a31-116">The service topology object.</span></span>

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

### <span data-ttu-id="15a31-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="15a31-117">-Confirm</span></span>
<span data-ttu-id="15a31-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="15a31-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15a31-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15a31-119">-WhatIf</span></span>
<span data-ttu-id="15a31-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="15a31-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15a31-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="15a31-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15a31-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15a31-122">CommonParameters</span></span>
<span data-ttu-id="15a31-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="15a31-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15a31-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15a31-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15a31-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="15a31-125">INPUTS</span></span>

### <span data-ttu-id="15a31-126">Microsoft. Azure. Command. DeploymentManager. models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="15a31-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="15a31-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15a31-127">OUTPUTS</span></span>

### <span data-ttu-id="15a31-128">Microsoft. Azure. Command. DeploymentManager. models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="15a31-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="15a31-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="15a31-129">NOTES</span></span>

## <span data-ttu-id="15a31-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15a31-130">RELATED LINKS</span></span>

[<span data-ttu-id="15a31-131">Új – AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="15a31-131">New-AzureRmDeploymentManagerServiceTopology</span></span>](./New-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="15a31-132">Get-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="15a31-132">Get-AzureRmDeploymentManagerServiceTopology</span></span>](./Set-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="15a31-133">Remove-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="15a31-133">Remove-AzureRmDeploymentManagerServiceTopology</span></span>](./Remove-AzureRmDeploymentManagerServiceTopology.md)