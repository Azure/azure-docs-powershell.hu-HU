---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: 230e443fad4740b6bf9896164f02ae9b382e3ed2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491104"
---
# <span data-ttu-id="13e4f-101">Set-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="13e4f-101">Set-AzureRmDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="13e4f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="13e4f-102">SYNOPSIS</span></span>
<span data-ttu-id="13e4f-103">Egy tárgy forrását frissíti.</span><span class="sxs-lookup"><span data-stu-id="13e4f-103">Updates an artifact source.</span></span>

## <span data-ttu-id="13e4f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="13e4f-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerArtifactSource [-ArtifactSource] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13e4f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="13e4f-105">DESCRIPTION</span></span>
<span data-ttu-id="13e4f-106">A **set-AzureRmDeploymentManagerArtifactSource** parancsmag a megadott tárgyi forrás objektummal frissíti a tárgyi forrást.</span><span class="sxs-lookup"><span data-stu-id="13e4f-106">The **Set-AzureRmDeploymentManagerArtifactSource** cmdlet updates an artifact source with the specified artifact source object.</span></span>
<span data-ttu-id="13e4f-107">A parancsmag a frissített ArtifactSource objektumot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="13e4f-107">The cmdlet returns the updated ArtifactSource object.</span></span>

## <span data-ttu-id="13e4f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="13e4f-108">EXAMPLES</span></span>

### <span data-ttu-id="13e4f-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="13e4f-109">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ArtifactSource $artifactSourceObject
```

<span data-ttu-id="13e4f-110">Ez a parancs olyan tárgyi forrást frissít, amelynek a neve és a ResourceGroup megegyezik a $artifactSourceObject neve és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="13e4f-110">This command updates an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>
<span data-ttu-id="13e4f-111">A program frissíti a tárgy forrását a $artifactSourceObjectban megadott tulajdonságokra.</span><span class="sxs-lookup"><span data-stu-id="13e4f-111">The artifact source would be updated to the properties set in the $artifactSourceObject.</span></span>

## <span data-ttu-id="13e4f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="13e4f-112">PARAMETERS</span></span>

### <span data-ttu-id="13e4f-113">-ArtifactSource</span><span class="sxs-lookup"><span data-stu-id="13e4f-113">-ArtifactSource</span></span>
<span data-ttu-id="13e4f-114">A tárgy forrás objektum.</span><span class="sxs-lookup"><span data-stu-id="13e4f-114">The artifact source object.</span></span>

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

### <span data-ttu-id="13e4f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13e4f-115">-DefaultProfile</span></span>
<span data-ttu-id="13e4f-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13e4f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13e4f-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="13e4f-117">-Confirm</span></span>
<span data-ttu-id="13e4f-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="13e4f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13e4f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13e4f-119">-WhatIf</span></span>
<span data-ttu-id="13e4f-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="13e4f-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="13e4f-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="13e4f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13e4f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13e4f-122">CommonParameters</span></span>
<span data-ttu-id="13e4f-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="13e4f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13e4f-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13e4f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13e4f-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="13e4f-125">INPUTS</span></span>

### <span data-ttu-id="13e4f-126">Microsoft. Azure. Command. DeploymentManager. models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="13e4f-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="13e4f-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13e4f-127">OUTPUTS</span></span>

### <span data-ttu-id="13e4f-128">Microsoft. Azure. Command. DeploymentManager. models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="13e4f-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="13e4f-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="13e4f-129">NOTES</span></span>

## <span data-ttu-id="13e4f-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13e4f-130">RELATED LINKS</span></span>

[<span data-ttu-id="13e4f-131">Új – AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="13e4f-131">New-AzureRmDeploymentManagerArtifactSource</span></span>](./New-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="13e4f-132">Get-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="13e4f-132">Get-AzureRmDeploymentManagerArtifactSource</span></span>](./Get-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="13e4f-133">Remove-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="13e4f-133">Remove-AzureRmDeploymentManagerArtifactSource</span></span>](./Remove-AzureRmDeploymentManagerArtifactSource.md)