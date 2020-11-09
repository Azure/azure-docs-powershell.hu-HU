---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azmanagementgroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
ms.openlocfilehash: f45602ad2515a90e39e45edb80ca1cb0bf051f00
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301004"
---
# <span data-ttu-id="7b243-101">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="7b243-101">Save-AzManagementGroupDeploymentTemplate</span></span>

## <span data-ttu-id="7b243-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7b243-102">SYNOPSIS</span></span>
<span data-ttu-id="7b243-103">Egy központi telepítő sablont ment a fájlra.</span><span class="sxs-lookup"><span data-stu-id="7b243-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="7b243-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7b243-104">SYNTAX</span></span>

### <span data-ttu-id="7b243-105">SaveByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7b243-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzManagementGroupDeploymentTemplate -ManagementGroupId <String> -DeploymentName <String> [-Path <String>]
 [-Force] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b243-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="7b243-106">SaveByDeploymentObject</span></span>
```
Save-AzManagementGroupDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b243-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7b243-107">DESCRIPTION</span></span>
<span data-ttu-id="7b243-108">A **Save-AzManagementGroupDeploymentTemplate**  parancsmag egy, a felügyeleti csoportba való bevezetésre szolgáló telepítő sablont JSON-fájlba menti.</span><span class="sxs-lookup"><span data-stu-id="7b243-108">The **Save-AzManagementGroupDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at a management group.</span></span>

## <span data-ttu-id="7b243-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7b243-109">EXAMPLES</span></span>

### <span data-ttu-id="7b243-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7b243-110">Example 1</span></span>
```powershell
PS C:\> Save-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -DeploymentName "TestDeployment"
```

<span data-ttu-id="7b243-111">Ez a parancs beolvassa a TestDeployment a telepítő sablonból, és egy JSON-fájlként menti az aktuális könyvtárat.</span><span class="sxs-lookup"><span data-stu-id="7b243-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="7b243-112">2. példa: központi üzembe állítás és a sablon mentése</span><span class="sxs-lookup"><span data-stu-id="7b243-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -Name "RolesDeployment" | Save-AzManagementGroupDeploymentTemplate
```

<span data-ttu-id="7b243-113">Ez a parancs a "RolesDeployment" ("myMG") felügyeleti csoport "" üzembe állítását, majd a sablon mentését kapja.</span><span class="sxs-lookup"><span data-stu-id="7b243-113">This command gets the deployment "RolesDeployment" at the management group "myMG" and saves its template.</span></span>

## <span data-ttu-id="7b243-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7b243-114">PARAMETERS</span></span>

### <span data-ttu-id="7b243-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b243-115">-DefaultProfile</span></span>
<span data-ttu-id="7b243-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7b243-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b243-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="7b243-117">-DeploymentName</span></span>
<span data-ttu-id="7b243-118">A központi telepítő neve.</span><span class="sxs-lookup"><span data-stu-id="7b243-118">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveByDeploymentName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b243-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="7b243-119">-DeploymentObject</span></span>
<span data-ttu-id="7b243-120">A központi telepítő objektum.</span><span class="sxs-lookup"><span data-stu-id="7b243-120">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: SaveByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b243-121">-Force</span><span class="sxs-lookup"><span data-stu-id="7b243-121">-Force</span></span>
<span data-ttu-id="7b243-122">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7b243-122">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b243-123">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="7b243-123">-ManagementGroupId</span></span>
<span data-ttu-id="7b243-124">A kezelési csoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7b243-124">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b243-125">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="7b243-125">-Path</span></span>
<span data-ttu-id="7b243-126">A sablonfájl kimeneti elérési útja.</span><span class="sxs-lookup"><span data-stu-id="7b243-126">The output path of the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b243-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="7b243-127">-Pre</span></span>
<span data-ttu-id="7b243-128">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="7b243-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b243-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7b243-129">-Confirm</span></span>
<span data-ttu-id="7b243-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7b243-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b243-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b243-131">-WhatIf</span></span>
<span data-ttu-id="7b243-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7b243-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b243-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7b243-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b243-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b243-134">CommonParameters</span></span>
<span data-ttu-id="7b243-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7b243-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b243-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7b243-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b243-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b243-137">INPUTS</span></span>

### <span data-ttu-id="7b243-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="7b243-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="7b243-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b243-139">OUTPUTS</span></span>

### <span data-ttu-id="7b243-140">Microsoft. Azure. Command. ResourceManager. Parancsmags. SdkModels. PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="7b243-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="7b243-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7b243-141">NOTES</span></span>

## <span data-ttu-id="7b243-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7b243-142">RELATED LINKS</span></span>
