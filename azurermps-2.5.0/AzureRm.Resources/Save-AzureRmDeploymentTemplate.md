---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/save-azurermdeploymenttemplate
schema: 2.0.0
ms.openlocfilehash: d8adaee3e6dacafb4391f350ef567117dc3442c2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850213"
---
# <span data-ttu-id="0425b-101">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="0425b-101">Save-AzureRmDeploymentTemplate</span></span>

## <span data-ttu-id="0425b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0425b-102">SYNOPSIS</span></span>
<span data-ttu-id="0425b-103">Egy központi telepítő sablont ment a fájlra.</span><span class="sxs-lookup"><span data-stu-id="0425b-103">Saves a deployment template to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0425b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0425b-104">SYNTAX</span></span>

### <span data-ttu-id="0425b-105">SaveByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0425b-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzureRmDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0425b-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="0425b-106">SaveByDeploymentObject</span></span>
```
Save-AzureRmDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0425b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0425b-107">DESCRIPTION</span></span>
<span data-ttu-id="0425b-108">A **Save-AzureRmDeploymentTemplate**  parancsmag a központi telepítő SABLONT egy JSON-fájlba menti.</span><span class="sxs-lookup"><span data-stu-id="0425b-108">The **Save-AzureRmDeploymentTemplate**  cmdlet saves a deployment template to a JSON file.</span></span>

## <span data-ttu-id="0425b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0425b-109">EXAMPLES</span></span>

### <span data-ttu-id="0425b-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0425b-110">Example 1</span></span>
```powershell
PS C:\> Save-AzureRmDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="0425b-111">Ez a parancs beolvassa a TestDeployment a telepítő sablonból, és egy JSON-fájlként menti az aktuális könyvtárat.</span><span class="sxs-lookup"><span data-stu-id="0425b-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="0425b-112">2. példa: központi üzembe állítás és a sablon mentése</span><span class="sxs-lookup"><span data-stu-id="0425b-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "RolesDeployment" | Save-AzureRmDeploymentTemplate
```

<span data-ttu-id="0425b-113">A parancs a jelenlegi előfizetési tartomány "RolesDeployment" beállítását kapja, és menti a sablont.</span><span class="sxs-lookup"><span data-stu-id="0425b-113">This command gets the deployment "RolesDeployment" at the current subscription scope and saves its template.</span></span>

## <span data-ttu-id="0425b-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0425b-114">PARAMETERS</span></span>

### <span data-ttu-id="0425b-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0425b-115">-ApiVersion</span></span>
<span data-ttu-id="0425b-116">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0425b-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="0425b-117">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="0425b-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="0425b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0425b-118">-DefaultProfile</span></span>
<span data-ttu-id="0425b-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0425b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0425b-120">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="0425b-120">-DeploymentName</span></span>
<span data-ttu-id="0425b-121">A központi telepítő neve.</span><span class="sxs-lookup"><span data-stu-id="0425b-121">The deployment name.</span></span>

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

### <span data-ttu-id="0425b-122">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="0425b-122">-DeploymentObject</span></span>
<span data-ttu-id="0425b-123">A központi telepítő objektum.</span><span class="sxs-lookup"><span data-stu-id="0425b-123">The deployment object.</span></span>

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

### <span data-ttu-id="0425b-124">-Force</span><span class="sxs-lookup"><span data-stu-id="0425b-124">-Force</span></span>
<span data-ttu-id="0425b-125">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0425b-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0425b-126">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="0425b-126">-Path</span></span>
<span data-ttu-id="0425b-127">A sablonfájl kimeneti elérési útja.</span><span class="sxs-lookup"><span data-stu-id="0425b-127">The output path of the template file.</span></span>

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

### <span data-ttu-id="0425b-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="0425b-128">-Pre</span></span>
<span data-ttu-id="0425b-129">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="0425b-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0425b-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0425b-130">-Confirm</span></span>
<span data-ttu-id="0425b-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0425b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0425b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0425b-132">-WhatIf</span></span>
<span data-ttu-id="0425b-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0425b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0425b-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0425b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0425b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0425b-135">CommonParameters</span></span>
<span data-ttu-id="0425b-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0425b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0425b-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0425b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0425b-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0425b-138">INPUTS</span></span>

### <span data-ttu-id="0425b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0425b-139">System.String</span></span>

## <span data-ttu-id="0425b-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0425b-140">OUTPUTS</span></span>

### <span data-ttu-id="0425b-141">Microsoft. Azure. Command. ResourceManager. Parancsmags. SdkModels</span><span class="sxs-lookup"><span data-stu-id="0425b-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels</span></span>

## <span data-ttu-id="0425b-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0425b-142">NOTES</span></span>

## <span data-ttu-id="0425b-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0425b-143">RELATED LINKS</span></span>
