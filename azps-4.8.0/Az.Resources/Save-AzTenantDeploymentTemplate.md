---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-aztenantdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
ms.openlocfilehash: 79a60294126a990d191e4838a91c0f6554bea43b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180927"
---
# <span data-ttu-id="3b97e-101">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="3b97e-101">Save-AzTenantDeploymentTemplate</span></span>

## <span data-ttu-id="3b97e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3b97e-102">SYNOPSIS</span></span>
<span data-ttu-id="3b97e-103">Egy központi telepítő sablont ment a fájlra.</span><span class="sxs-lookup"><span data-stu-id="3b97e-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="3b97e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3b97e-104">SYNTAX</span></span>

### <span data-ttu-id="3b97e-105">SaveByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3b97e-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b97e-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="3b97e-106">SaveByDeploymentObject</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3b97e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3b97e-107">DESCRIPTION</span></span>
<span data-ttu-id="3b97e-108">A **Save-AzTenantDeploymentTemplate**  parancsmag egy telepítő sablont JSON-fájlba menti a bérlői hatókörben.</span><span class="sxs-lookup"><span data-stu-id="3b97e-108">The **Save-AzTenantDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at tenant scope.</span></span>

## <span data-ttu-id="3b97e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3b97e-109">EXAMPLES</span></span>

### <span data-ttu-id="3b97e-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3b97e-110">Example 1</span></span>
```powershell
PS C:\> Save-AzTenantDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="3b97e-111">Ez a parancs beolvassa a TestDeployment a telepítő sablonból, és egy JSON-fájlként menti az aktuális könyvtárat.</span><span class="sxs-lookup"><span data-stu-id="3b97e-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="3b97e-112">2. példa: központi üzembe állítás és a sablon mentése</span><span class="sxs-lookup"><span data-stu-id="3b97e-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzTenantDeploymentTemplate -Name "RolesDeployment" | Save-AzTenantDeploymentTemplate
```

<span data-ttu-id="3b97e-113">Ez a parancs a "RolesDeployment" üzembe állítását a bérlői hatókörben kapja, és menti a sablont.</span><span class="sxs-lookup"><span data-stu-id="3b97e-113">This command gets the deployment "RolesDeployment" at the current tenant scope and saves its template.</span></span>

## <span data-ttu-id="3b97e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3b97e-114">PARAMETERS</span></span>

### <span data-ttu-id="3b97e-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3b97e-115">-ApiVersion</span></span>
<span data-ttu-id="3b97e-116">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b97e-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="3b97e-117">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="3b97e-117">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b97e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b97e-118">-DefaultProfile</span></span>
<span data-ttu-id="3b97e-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3b97e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b97e-120">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="3b97e-120">-DeploymentName</span></span>
<span data-ttu-id="3b97e-121">A központi telepítő neve.</span><span class="sxs-lookup"><span data-stu-id="3b97e-121">The deployment name.</span></span>

```yaml
Type: String
Parameter Sets: SaveByDeploymentName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b97e-122">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="3b97e-122">-DeploymentObject</span></span>
<span data-ttu-id="3b97e-123">A központi telepítő objektum.</span><span class="sxs-lookup"><span data-stu-id="3b97e-123">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: SaveByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b97e-124">-Force</span><span class="sxs-lookup"><span data-stu-id="3b97e-124">-Force</span></span>
<span data-ttu-id="3b97e-125">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3b97e-125">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b97e-126">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="3b97e-126">-Path</span></span>
<span data-ttu-id="3b97e-127">A sablonfájl kimeneti elérési útja.</span><span class="sxs-lookup"><span data-stu-id="3b97e-127">The output path of the template file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b97e-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="3b97e-128">-Pre</span></span>
<span data-ttu-id="3b97e-129">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="3b97e-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b97e-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3b97e-130">-Confirm</span></span>
<span data-ttu-id="3b97e-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3b97e-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b97e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b97e-132">-WhatIf</span></span>
<span data-ttu-id="3b97e-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3b97e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b97e-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3b97e-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b97e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b97e-135">CommonParameters</span></span>
<span data-ttu-id="3b97e-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3b97e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b97e-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3b97e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b97e-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b97e-138">INPUTS</span></span>

### <span data-ttu-id="3b97e-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="3b97e-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="3b97e-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b97e-140">OUTPUTS</span></span>

### <span data-ttu-id="3b97e-141">Microsoft. Azure. Command. ResourceManager. Parancsmags. SdkModels. PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="3b97e-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="3b97e-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3b97e-142">NOTES</span></span>

## <span data-ttu-id="3b97e-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b97e-143">RELATED LINKS</span></span>
