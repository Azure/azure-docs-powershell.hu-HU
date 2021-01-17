---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: ee69c178d48775a870b229e652a1584c413bd7ca
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467922"
---
# <span data-ttu-id="0b4b8-101">Set-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="0b4b8-101">Set-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="0b4b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b4b8-102">SYNOPSIS</span></span>
<span data-ttu-id="0b4b8-103">Frissíti az összetevők forrását.</span><span class="sxs-lookup"><span data-stu-id="0b4b8-103">Updates the artifacts source.</span></span>

## <span data-ttu-id="0b4b8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0b4b8-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b4b8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0b4b8-105">DESCRIPTION</span></span>
<span data-ttu-id="0b4b8-106">A **Set-AzDeploymentManagerArtifactSource** parancsmag frissíti az objektumforrást a megadott objektumforrás-objektummal.</span><span class="sxs-lookup"><span data-stu-id="0b4b8-106">The **Set-AzDeploymentManagerArtifactSource** cmdlet updates an artifact source with the specified artifact source object.</span></span>
<span data-ttu-id="0b4b8-107">A parancsmag visszaadja a frissített ObjectSource objektumot.</span><span class="sxs-lookup"><span data-stu-id="0b4b8-107">The cmdlet returns the updated ArtifactSource object.</span></span>

## <span data-ttu-id="0b4b8-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0b4b8-108">EXAMPLES</span></span>

### <span data-ttu-id="0b4b8-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="0b4b8-109">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="0b4b8-110">Ez a parancs frissíti azt az összetevőforrást, amelynek a neve és az Erőforráscsoport tulajdonsága megegyezik a $artifactSourceObject ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="0b4b8-110">This command updates an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>
<span data-ttu-id="0b4b8-111">Az összetevőforrást a rendszer frissíti a $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="0b4b8-111">The artifact source would be updated to the properties set in the $artifactSourceObject.</span></span>

## <span data-ttu-id="0b4b8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b4b8-112">PARAMETERS</span></span>

### <span data-ttu-id="0b4b8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b4b8-113">-DefaultProfile</span></span>
<span data-ttu-id="0b4b8-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0b4b8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b4b8-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b4b8-115">-InputObject</span></span>
<span data-ttu-id="0b4b8-116">Az objektumforrás-objektum.</span><span class="sxs-lookup"><span data-stu-id="0b4b8-116">The artifact source object.</span></span>

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

### <span data-ttu-id="0b4b8-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b4b8-117">-Confirm</span></span>
<span data-ttu-id="0b4b8-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0b4b8-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b4b8-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b4b8-119">-WhatIf</span></span>
<span data-ttu-id="0b4b8-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0b4b8-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b4b8-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0b4b8-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b4b8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b4b8-122">CommonParameters</span></span>
<span data-ttu-id="0b4b8-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b4b8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b4b8-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b4b8-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b4b8-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0b4b8-125">INPUTS</span></span>

### <span data-ttu-id="0b4b8-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="0b4b8-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="0b4b8-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b4b8-127">OUTPUTS</span></span>

### <span data-ttu-id="0b4b8-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="0b4b8-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="0b4b8-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0b4b8-129">NOTES</span></span>

## <span data-ttu-id="0b4b8-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0b4b8-130">RELATED LINKS</span></span>
