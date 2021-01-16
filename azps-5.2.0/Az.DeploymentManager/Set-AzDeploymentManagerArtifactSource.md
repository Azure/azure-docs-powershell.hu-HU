---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: ee69c178d48775a870b229e652a1584c413bd7ca
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333618"
---
# <span data-ttu-id="17b8e-101">Set-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="17b8e-101">Set-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="17b8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17b8e-102">SYNOPSIS</span></span>
<span data-ttu-id="17b8e-103">Frissíti az összetevők forrását.</span><span class="sxs-lookup"><span data-stu-id="17b8e-103">Updates the artifacts source.</span></span>

## <span data-ttu-id="17b8e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="17b8e-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17b8e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="17b8e-105">DESCRIPTION</span></span>
<span data-ttu-id="17b8e-106">A **Set-AzDeploymentManagerArtifactSource** parancsmag frissíti az objektumforrást a megadott objektumforrás-objektummal.</span><span class="sxs-lookup"><span data-stu-id="17b8e-106">The **Set-AzDeploymentManagerArtifactSource** cmdlet updates an artifact source with the specified artifact source object.</span></span>
<span data-ttu-id="17b8e-107">A parancsmag visszaadja a frissített ObjectSource objektumot.</span><span class="sxs-lookup"><span data-stu-id="17b8e-107">The cmdlet returns the updated ArtifactSource object.</span></span>

## <span data-ttu-id="17b8e-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="17b8e-108">EXAMPLES</span></span>

### <span data-ttu-id="17b8e-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="17b8e-109">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="17b8e-110">Ez a parancs frissíti azt az összetevőforrást, amelynek a neve és az Erőforráscsoport tulajdonsága megegyezik a $artifactSourceObject ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="17b8e-110">This command updates an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>
<span data-ttu-id="17b8e-111">Az összetevőforrást a rendszer frissíti a $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="17b8e-111">The artifact source would be updated to the properties set in the $artifactSourceObject.</span></span>

## <span data-ttu-id="17b8e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17b8e-112">PARAMETERS</span></span>

### <span data-ttu-id="17b8e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17b8e-113">-DefaultProfile</span></span>
<span data-ttu-id="17b8e-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="17b8e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17b8e-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17b8e-115">-InputObject</span></span>
<span data-ttu-id="17b8e-116">Az objektumforrás-objektum.</span><span class="sxs-lookup"><span data-stu-id="17b8e-116">The artifact source object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17b8e-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17b8e-117">-Confirm</span></span>
<span data-ttu-id="17b8e-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="17b8e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17b8e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17b8e-119">-WhatIf</span></span>
<span data-ttu-id="17b8e-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="17b8e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17b8e-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="17b8e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17b8e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17b8e-122">CommonParameters</span></span>
<span data-ttu-id="17b8e-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17b8e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17b8e-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17b8e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17b8e-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="17b8e-125">INPUTS</span></span>

### <span data-ttu-id="17b8e-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="17b8e-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="17b8e-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="17b8e-127">OUTPUTS</span></span>

### <span data-ttu-id="17b8e-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="17b8e-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="17b8e-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="17b8e-129">NOTES</span></span>

## <span data-ttu-id="17b8e-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="17b8e-130">RELATED LINKS</span></span>
