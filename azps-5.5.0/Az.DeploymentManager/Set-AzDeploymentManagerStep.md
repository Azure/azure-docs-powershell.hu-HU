---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
ms.openlocfilehash: 2cd73cad57f36130ed11e37ad6dc2147e6c081ae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209751"
---
# <span data-ttu-id="f654f-101">Set-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="f654f-101">Set-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="f654f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f654f-102">SYNOPSIS</span></span>
<span data-ttu-id="f654f-103">Frissíti a lépést.</span><span class="sxs-lookup"><span data-stu-id="f654f-103">Updates the step.</span></span>

## <span data-ttu-id="f654f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f654f-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f654f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f654f-105">DESCRIPTION</span></span>
<span data-ttu-id="f654f-106">A **Set-AzDeploymentManagerStep** parancsmag a megadott lépésobjektummal frissíti a lépést.</span><span class="sxs-lookup"><span data-stu-id="f654f-106">The **Set-AzDeploymentManagerStep** cmdlet updates a step with the specified step object.</span></span>
<span data-ttu-id="f654f-107">A parancsmag a frissített lépésobjektumot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="f654f-107">The cmdlet returns the updated step object.</span></span>

## <span data-ttu-id="f654f-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f654f-108">EXAMPLES</span></span>

### <span data-ttu-id="f654f-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="f654f-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerStep -InputObject $stepObject
```

<span data-ttu-id="f654f-110">Ez a parancs frissíti azt a lépést, amelynek neve és ResourceGroup tulajdonsága megegyezik a $stepObject ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="f654f-110">This command updates a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>
<span data-ttu-id="f654f-111">A lépés a párbeszédpanelen beállított $stepObject.</span><span class="sxs-lookup"><span data-stu-id="f654f-111">The step would be updated to the properties set in the $stepObject.</span></span>

## <span data-ttu-id="f654f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f654f-112">PARAMETERS</span></span>

### <span data-ttu-id="f654f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f654f-113">-DefaultProfile</span></span>
<span data-ttu-id="f654f-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f654f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f654f-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f654f-115">-InputObject</span></span>
<span data-ttu-id="f654f-116">A lépésobjektum.</span><span class="sxs-lookup"><span data-stu-id="f654f-116">The step object.</span></span>

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

### <span data-ttu-id="f654f-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f654f-117">-Confirm</span></span>
<span data-ttu-id="f654f-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f654f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f654f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f654f-119">-WhatIf</span></span>
<span data-ttu-id="f654f-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f654f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f654f-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f654f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f654f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f654f-122">CommonParameters</span></span>
<span data-ttu-id="f654f-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f654f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f654f-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f654f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f654f-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f654f-125">INPUTS</span></span>

### <span data-ttu-id="f654f-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="f654f-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="f654f-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f654f-127">OUTPUTS</span></span>

### <span data-ttu-id="f654f-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="f654f-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="f654f-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f654f-129">NOTES</span></span>

## <span data-ttu-id="f654f-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f654f-130">RELATED LINKS</span></span>
