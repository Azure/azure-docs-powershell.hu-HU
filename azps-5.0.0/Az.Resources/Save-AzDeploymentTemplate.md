---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
ms.openlocfilehash: dc6f7c5b66d72ae5c01ecbb8ec93fa737199d06e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195525"
---
# <span data-ttu-id="f3de5-101">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="f3de5-101">Save-AzDeploymentTemplate</span></span>

## <span data-ttu-id="f3de5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f3de5-102">SYNOPSIS</span></span>
<span data-ttu-id="f3de5-103">Egy központi telepítő sablont ment a fájlra.</span><span class="sxs-lookup"><span data-stu-id="f3de5-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="f3de5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f3de5-104">SYNTAX</span></span>

### <span data-ttu-id="f3de5-105">SaveByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f3de5-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3de5-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="f3de5-106">SaveByDeploymentObject</span></span>
```
Save-AzDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3de5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f3de5-107">DESCRIPTION</span></span>
<span data-ttu-id="f3de5-108">A **Save-AzDeploymentTemplate**  parancsmag a központi telepítő SABLONT egy JSON-fájlba menti.</span><span class="sxs-lookup"><span data-stu-id="f3de5-108">The **Save-AzDeploymentTemplate**  cmdlet saves a deployment template to a JSON file.</span></span>

## <span data-ttu-id="f3de5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f3de5-109">EXAMPLES</span></span>

### <span data-ttu-id="f3de5-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f3de5-110">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="f3de5-111">Ez a parancs beolvassa a TestDeployment a telepítő sablonból, és egy JSON-fájlként menti az aktuális könyvtárat.</span><span class="sxs-lookup"><span data-stu-id="f3de5-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="f3de5-112">2. példa: központi üzembe állítás és a sablon mentése</span><span class="sxs-lookup"><span data-stu-id="f3de5-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Save-AzDeploymentTemplate
```

<span data-ttu-id="f3de5-113">A parancs a jelenlegi előfizetési tartomány "RolesDeployment" beállítását kapja, és menti a sablont.</span><span class="sxs-lookup"><span data-stu-id="f3de5-113">This command gets the deployment "RolesDeployment" at the current subscription scope and saves its template.</span></span>

## <span data-ttu-id="f3de5-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f3de5-114">PARAMETERS</span></span>

### <span data-ttu-id="f3de5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3de5-115">-DefaultProfile</span></span>
<span data-ttu-id="f3de5-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3de5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3de5-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="f3de5-117">-DeploymentName</span></span>
<span data-ttu-id="f3de5-118">A központi telepítő neve.</span><span class="sxs-lookup"><span data-stu-id="f3de5-118">The deployment name.</span></span>

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

### <span data-ttu-id="f3de5-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="f3de5-119">-DeploymentObject</span></span>
<span data-ttu-id="f3de5-120">A központi telepítő objektum.</span><span class="sxs-lookup"><span data-stu-id="f3de5-120">The deployment object.</span></span>

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

### <span data-ttu-id="f3de5-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f3de5-121">-Force</span></span>
<span data-ttu-id="f3de5-122">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f3de5-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f3de5-123">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="f3de5-123">-Path</span></span>
<span data-ttu-id="f3de5-124">A sablonfájl kimeneti elérési útja.</span><span class="sxs-lookup"><span data-stu-id="f3de5-124">The output path of the template file.</span></span>

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

### <span data-ttu-id="f3de5-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="f3de5-125">-Pre</span></span>
<span data-ttu-id="f3de5-126">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="f3de5-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f3de5-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f3de5-127">-Confirm</span></span>
<span data-ttu-id="f3de5-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f3de5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3de5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3de5-129">-WhatIf</span></span>
<span data-ttu-id="f3de5-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f3de5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3de5-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f3de5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3de5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3de5-132">CommonParameters</span></span>
<span data-ttu-id="f3de5-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f3de5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3de5-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f3de5-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3de5-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3de5-135">INPUTS</span></span>

### <span data-ttu-id="f3de5-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="f3de5-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="f3de5-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3de5-137">OUTPUTS</span></span>

### <span data-ttu-id="f3de5-138">Microsoft. Azure. Command. ResourceManager. Parancsmags. SdkModels. PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="f3de5-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="f3de5-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f3de5-139">NOTES</span></span>

## <span data-ttu-id="f3de5-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3de5-140">RELATED LINKS</span></span>
