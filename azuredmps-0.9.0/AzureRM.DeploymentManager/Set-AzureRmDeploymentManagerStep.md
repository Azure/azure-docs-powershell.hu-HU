---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: 7241e072109583b7afc24fc3f69746599bd67c53
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491276"
---
# <span data-ttu-id="4dedf-101">Set-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="4dedf-101">Set-AzureRmDeploymentManagerStep</span></span>

## <span data-ttu-id="4dedf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4dedf-102">SYNOPSIS</span></span>
<span data-ttu-id="4dedf-103">Lépés frissítése</span><span class="sxs-lookup"><span data-stu-id="4dedf-103">Updates a step.</span></span>

## <span data-ttu-id="4dedf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4dedf-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerStep [-Step] <PSStepResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dedf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4dedf-105">DESCRIPTION</span></span>
<span data-ttu-id="4dedf-106">A **set-AzureRmDeploymentManagerStep** parancsmag egy lépéssel frissíti a megadott lépés objektummal.</span><span class="sxs-lookup"><span data-stu-id="4dedf-106">The **Set-AzureRmDeploymentManagerStep** cmdlet updates a step with the specified step object.</span></span>
<span data-ttu-id="4dedf-107">A parancsmag a frissített lépés objektumot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="4dedf-107">The cmdlet returns the updated step object.</span></span>

## <span data-ttu-id="4dedf-108">Példák</span><span class="sxs-lookup"><span data-stu-id="4dedf-108">EXAMPLES</span></span>

### <span data-ttu-id="4dedf-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4dedf-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDeploymentManagerStep -Step $stepObject
```

<span data-ttu-id="4dedf-110">A parancs frissíti azt a lépést, amelynek a neve és a ResourceGroup meg kell egyeznie az $stepObject neve és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="4dedf-110">This command updates a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>
<span data-ttu-id="4dedf-111">A lépést a program frissíti a $stepObjectban megadott tulajdonságokra.</span><span class="sxs-lookup"><span data-stu-id="4dedf-111">The step would be updated to the properties set in the $stepObject.</span></span>

## <span data-ttu-id="4dedf-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4dedf-112">PARAMETERS</span></span>

### <span data-ttu-id="4dedf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dedf-113">-DefaultProfile</span></span>
<span data-ttu-id="4dedf-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4dedf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dedf-115">Lépés</span><span class="sxs-lookup"><span data-stu-id="4dedf-115">-Step</span></span>
<span data-ttu-id="4dedf-116">A Step objektum.</span><span class="sxs-lookup"><span data-stu-id="4dedf-116">The step object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4dedf-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4dedf-117">-Confirm</span></span>
<span data-ttu-id="4dedf-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4dedf-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dedf-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dedf-119">-WhatIf</span></span>
<span data-ttu-id="4dedf-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4dedf-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dedf-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4dedf-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dedf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dedf-122">CommonParameters</span></span>
<span data-ttu-id="4dedf-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4dedf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4dedf-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dedf-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dedf-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4dedf-125">INPUTS</span></span>

### <span data-ttu-id="4dedf-126">Microsoft. Azure. Command. DeploymentManager. models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="4dedf-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="4dedf-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4dedf-127">OUTPUTS</span></span>

### <span data-ttu-id="4dedf-128">Microsoft. Azure. Command. DeploymentManager. models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="4dedf-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="4dedf-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4dedf-129">NOTES</span></span>

## <span data-ttu-id="4dedf-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4dedf-130">RELATED LINKS</span></span>
