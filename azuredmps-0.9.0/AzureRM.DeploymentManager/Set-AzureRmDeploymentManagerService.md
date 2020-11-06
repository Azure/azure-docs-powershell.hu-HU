---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 2f4cab266cf63e1c33c35c051e9cc2b838f5b066
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490808"
---
# <span data-ttu-id="48d45-101">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="48d45-101">Set-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="48d45-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="48d45-102">SYNOPSIS</span></span>
<span data-ttu-id="48d45-103">A szolgáltatás topológiájában frissíti a szolgáltatásokat.</span><span class="sxs-lookup"><span data-stu-id="48d45-103">Updates a service in service topology.</span></span>

## <span data-ttu-id="48d45-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="48d45-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48d45-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="48d45-105">DESCRIPTION</span></span>
<span data-ttu-id="48d45-106">A **set-AzureRmDeploymentManagerService** parancsmag a megadott szolgáltatási objektummal frissíti a szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="48d45-106">The **Set-AzureRmDeploymentManagerService** cmdlet updates a service with the specified service object.</span></span>
<span data-ttu-id="48d45-107">A parancsmag a frissített szolgáltatási objektumot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="48d45-107">The cmdlet returns the updated service object.</span></span>

## <span data-ttu-id="48d45-108">Példák</span><span class="sxs-lookup"><span data-stu-id="48d45-108">EXAMPLES</span></span>

### <span data-ttu-id="48d45-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="48d45-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="48d45-110">Ez a parancs frissíti azt a szolgáltatást, amelynek a neve, a szolgáltatás topológiájának neve és a ResourceGroup megegyezik a $serviceObject neve, a ServiceTopologyName és a ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="48d45-110">This command updates a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
<span data-ttu-id="48d45-111">A szolgáltatás frissült a $serviceObjectban beállított tulajdonságokra.</span><span class="sxs-lookup"><span data-stu-id="48d45-111">The service would be updated to the properties set in the $serviceObject.</span></span>

## <span data-ttu-id="48d45-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="48d45-112">PARAMETERS</span></span>

### <span data-ttu-id="48d45-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48d45-113">-DefaultProfile</span></span>
<span data-ttu-id="48d45-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="48d45-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48d45-115">-Szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="48d45-115">-Service</span></span>
<span data-ttu-id="48d45-116">A szolgáltatás objektuma.</span><span class="sxs-lookup"><span data-stu-id="48d45-116">The service object.</span></span>

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

### <span data-ttu-id="48d45-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="48d45-117">-Confirm</span></span>
<span data-ttu-id="48d45-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="48d45-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48d45-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48d45-119">-WhatIf</span></span>
<span data-ttu-id="48d45-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="48d45-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48d45-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="48d45-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48d45-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48d45-122">CommonParameters</span></span>
<span data-ttu-id="48d45-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="48d45-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48d45-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48d45-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48d45-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="48d45-125">INPUTS</span></span>

### <span data-ttu-id="48d45-126">Microsoft. Azure. Command. DeploymentManager. models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="48d45-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="48d45-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48d45-127">OUTPUTS</span></span>

### <span data-ttu-id="48d45-128">Microsoft. Azure. Command. DeploymentManager. models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="48d45-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="48d45-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="48d45-129">NOTES</span></span>

## <span data-ttu-id="48d45-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48d45-130">RELATED LINKS</span></span>

[<span data-ttu-id="48d45-131">Új – AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="48d45-131">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="48d45-132">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="48d45-132">Get-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="48d45-133">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="48d45-133">Remove-AzureRmDeploymentManagerService</span></span>](./Remove-AzureRmDeploymentManagerService.md)