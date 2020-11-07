---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-Azdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
ms.openlocfilehash: 82fd6ba15a240be208445493810551154e188e92
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843209"
---
# <span data-ttu-id="4bacd-101">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="4bacd-101">Save-AzDeploymentTemplate</span></span>

## <span data-ttu-id="4bacd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4bacd-102">SYNOPSIS</span></span>
<span data-ttu-id="4bacd-103">Egy központi telepítő sablont ment a fájlra.</span><span class="sxs-lookup"><span data-stu-id="4bacd-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="4bacd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4bacd-104">SYNTAX</span></span>

### <span data-ttu-id="4bacd-105">SaveByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4bacd-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bacd-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="4bacd-106">SaveByDeploymentObject</span></span>
```
Save-AzDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4bacd-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4bacd-107">DESCRIPTION</span></span>
<span data-ttu-id="4bacd-108">A **Save-AzDeploymentTemplate**  parancsmag a központi telepítő SABLONT egy JSON-fájlba menti.</span><span class="sxs-lookup"><span data-stu-id="4bacd-108">The **Save-AzDeploymentTemplate**  cmdlet saves a deployment template to a JSON file.</span></span>

## <span data-ttu-id="4bacd-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4bacd-109">EXAMPLES</span></span>

### <span data-ttu-id="4bacd-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4bacd-110">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="4bacd-111">Ez a parancs beolvassa a TestDeployment a telepítő sablonból, és egy JSON-fájlként menti az aktuális könyvtárat.</span><span class="sxs-lookup"><span data-stu-id="4bacd-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="4bacd-112">2. példa: központi üzembe állítás és a sablon mentése</span><span class="sxs-lookup"><span data-stu-id="4bacd-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Save-AzDeploymentTemplate
```

<span data-ttu-id="4bacd-113">A parancs a jelenlegi előfizetési tartomány "RolesDeployment" beállítását kapja, és menti a sablont.</span><span class="sxs-lookup"><span data-stu-id="4bacd-113">This command gets the deployment "RolesDeployment" at the current subscription scope and saves its template.</span></span>

## <span data-ttu-id="4bacd-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4bacd-114">PARAMETERS</span></span>

### <span data-ttu-id="4bacd-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4bacd-115">-ApiVersion</span></span>
<span data-ttu-id="4bacd-116">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4bacd-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="4bacd-117">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="4bacd-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="4bacd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bacd-118">-DefaultProfile</span></span>
<span data-ttu-id="4bacd-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4bacd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bacd-120">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="4bacd-120">-DeploymentName</span></span>
<span data-ttu-id="4bacd-121">A központi telepítő neve.</span><span class="sxs-lookup"><span data-stu-id="4bacd-121">The deployment name.</span></span>

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

### <span data-ttu-id="4bacd-122">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="4bacd-122">-DeploymentObject</span></span>
<span data-ttu-id="4bacd-123">A központi telepítő objektum.</span><span class="sxs-lookup"><span data-stu-id="4bacd-123">The deployment object.</span></span>

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

### <span data-ttu-id="4bacd-124">-Force</span><span class="sxs-lookup"><span data-stu-id="4bacd-124">-Force</span></span>
<span data-ttu-id="4bacd-125">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4bacd-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4bacd-126">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="4bacd-126">-Path</span></span>
<span data-ttu-id="4bacd-127">A sablonfájl kimeneti elérési útja.</span><span class="sxs-lookup"><span data-stu-id="4bacd-127">The output path of the template file.</span></span>

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

### <span data-ttu-id="4bacd-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="4bacd-128">-Pre</span></span>
<span data-ttu-id="4bacd-129">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="4bacd-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4bacd-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4bacd-130">-Confirm</span></span>
<span data-ttu-id="4bacd-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4bacd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bacd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bacd-132">-WhatIf</span></span>
<span data-ttu-id="4bacd-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4bacd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bacd-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4bacd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bacd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bacd-135">CommonParameters</span></span>
<span data-ttu-id="4bacd-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4bacd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bacd-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bacd-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bacd-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4bacd-138">INPUTS</span></span>

### <span data-ttu-id="4bacd-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4bacd-139">System.String</span></span>

## <span data-ttu-id="4bacd-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4bacd-140">OUTPUTS</span></span>

### <span data-ttu-id="4bacd-141">Microsoft. Azure. Command. ResourceManager. Parancsmags. SdkModels</span><span class="sxs-lookup"><span data-stu-id="4bacd-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels</span></span>

## <span data-ttu-id="4bacd-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4bacd-142">NOTES</span></span>

## <span data-ttu-id="4bacd-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4bacd-143">RELATED LINKS</span></span>
