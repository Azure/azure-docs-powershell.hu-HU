---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: ee69c178d48775a870b229e652a1584c413bd7ca
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297146"
---
# <span data-ttu-id="cbdfc-101">Set-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="cbdfc-101">Set-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="cbdfc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cbdfc-102">SYNOPSIS</span></span>
<span data-ttu-id="cbdfc-103">Frissíti a leletek forrását.</span><span class="sxs-lookup"><span data-stu-id="cbdfc-103">Updates the artifacts source.</span></span>

## <span data-ttu-id="cbdfc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cbdfc-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbdfc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cbdfc-105">DESCRIPTION</span></span>
<span data-ttu-id="cbdfc-106">A **set-AzDeploymentManagerArtifactSource** parancsmag a megadott tárgyi forrás objektummal frissíti a tárgyi forrást.</span><span class="sxs-lookup"><span data-stu-id="cbdfc-106">The **Set-AzDeploymentManagerArtifactSource** cmdlet updates an artifact source with the specified artifact source object.</span></span>
<span data-ttu-id="cbdfc-107">A parancsmag a frissített ArtifactSource objektumot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="cbdfc-107">The cmdlet returns the updated ArtifactSource object.</span></span>

## <span data-ttu-id="cbdfc-108">Példák</span><span class="sxs-lookup"><span data-stu-id="cbdfc-108">EXAMPLES</span></span>

### <span data-ttu-id="cbdfc-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cbdfc-109">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="cbdfc-110">Ez a parancs olyan tárgyi forrást frissít, amelynek a neve és a ResourceGroup megegyezik a $artifactSourceObject neve és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="cbdfc-110">This command updates an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>
<span data-ttu-id="cbdfc-111">A program frissíti a tárgy forrását a $artifactSourceObjectban megadott tulajdonságokra.</span><span class="sxs-lookup"><span data-stu-id="cbdfc-111">The artifact source would be updated to the properties set in the $artifactSourceObject.</span></span>

## <span data-ttu-id="cbdfc-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cbdfc-112">PARAMETERS</span></span>

### <span data-ttu-id="cbdfc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbdfc-113">-DefaultProfile</span></span>
<span data-ttu-id="cbdfc-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cbdfc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbdfc-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbdfc-115">-InputObject</span></span>
<span data-ttu-id="cbdfc-116">A tárgy forrás objektum.</span><span class="sxs-lookup"><span data-stu-id="cbdfc-116">The artifact source object.</span></span>

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

### <span data-ttu-id="cbdfc-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cbdfc-117">-Confirm</span></span>
<span data-ttu-id="cbdfc-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cbdfc-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbdfc-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbdfc-119">-WhatIf</span></span>
<span data-ttu-id="cbdfc-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cbdfc-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbdfc-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cbdfc-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbdfc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbdfc-122">CommonParameters</span></span>
<span data-ttu-id="cbdfc-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cbdfc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbdfc-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cbdfc-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbdfc-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbdfc-125">INPUTS</span></span>

### <span data-ttu-id="cbdfc-126">Microsoft. Azure. Command. DeploymentManager. models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="cbdfc-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="cbdfc-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbdfc-127">OUTPUTS</span></span>

### <span data-ttu-id="cbdfc-128">Microsoft. Azure. Command. DeploymentManager. models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="cbdfc-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="cbdfc-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cbdfc-129">NOTES</span></span>

## <span data-ttu-id="cbdfc-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cbdfc-130">RELATED LINKS</span></span>
