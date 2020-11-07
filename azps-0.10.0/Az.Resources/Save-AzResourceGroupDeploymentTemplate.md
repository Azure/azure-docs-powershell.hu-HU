---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-Azresourcegroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
ms.openlocfilehash: 1ffdcef1bb27ec06873c12f64a135adc0e433929
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843210"
---
# <span data-ttu-id="1e77d-101">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="1e77d-101">Save-AzResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="1e77d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1e77d-102">SYNOPSIS</span></span>
<span data-ttu-id="1e77d-103">Egy erőforráscsoport-telepítő sablont ment a fájlba.</span><span class="sxs-lookup"><span data-stu-id="1e77d-103">Saves a resource group deployment template to a file.</span></span>

## <span data-ttu-id="1e77d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1e77d-104">SYNTAX</span></span>

```
Save-AzResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String>
 [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1e77d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1e77d-105">DESCRIPTION</span></span>
<span data-ttu-id="1e77d-106">A **Save-AzResourceGroupDeploymentTemplate**  parancsmag egy erőforráscsoport-telepítő sablont JSON-fájlba menti.</span><span class="sxs-lookup"><span data-stu-id="1e77d-106">The **Save-AzResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="1e77d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1e77d-107">EXAMPLES</span></span>

### <span data-ttu-id="1e77d-108">Példa 1: központi telepítő sablon mentése</span><span class="sxs-lookup"><span data-stu-id="1e77d-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="1e77d-109">Ez a parancs beolvassa a TestDeployment a telepítő sablonból, és egy JSON-fájlként menti az aktuális könyvtárat.</span><span class="sxs-lookup"><span data-stu-id="1e77d-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="1e77d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1e77d-110">PARAMETERS</span></span>

### <span data-ttu-id="1e77d-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1e77d-111">-ApiVersion</span></span>
<span data-ttu-id="1e77d-112">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1e77d-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="1e77d-113">Ha nem adja meg, akkor a program a legújabb API-verziót használja.</span><span class="sxs-lookup"><span data-stu-id="1e77d-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="1e77d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e77d-114">-DefaultProfile</span></span>
<span data-ttu-id="1e77d-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1e77d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e77d-116">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="1e77d-116">-DeploymentName</span></span>
<span data-ttu-id="1e77d-117">A központi telepítő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1e77d-117">Specifies the name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e77d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1e77d-118">-Force</span></span>
<span data-ttu-id="1e77d-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="1e77d-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1e77d-120">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1e77d-120">-InformationAction</span></span>
<span data-ttu-id="1e77d-121">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="1e77d-121">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="1e77d-122">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="1e77d-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1e77d-123">Folytassa</span><span class="sxs-lookup"><span data-stu-id="1e77d-123">Continue</span></span>
- <span data-ttu-id="1e77d-124">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="1e77d-124">Ignore</span></span>
- <span data-ttu-id="1e77d-125">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="1e77d-125">Inquire</span></span>
- <span data-ttu-id="1e77d-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1e77d-126">SilentlyContinue</span></span>
- <span data-ttu-id="1e77d-127">állj</span><span class="sxs-lookup"><span data-stu-id="1e77d-127">Stop</span></span>
- <span data-ttu-id="1e77d-128">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="1e77d-128">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e77d-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1e77d-129">-InformationVariable</span></span>
<span data-ttu-id="1e77d-130">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="1e77d-130">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e77d-131">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="1e77d-131">-Path</span></span>
<span data-ttu-id="1e77d-132">A sablonfájl kimeneti elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1e77d-132">Specifies the output path of the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e77d-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="1e77d-133">-Pre</span></span>
<span data-ttu-id="1e77d-134">Jelzi, hogy ez a parancsmag az előzetes verziójú API-t használja, amikor automatikusan meghatározza, hogy melyik API-verziót használja.</span><span class="sxs-lookup"><span data-stu-id="1e77d-134">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="1e77d-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e77d-135">-ResourceGroupName</span></span>
<span data-ttu-id="1e77d-136">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1e77d-136">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e77d-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1e77d-137">-Confirm</span></span>
<span data-ttu-id="1e77d-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1e77d-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e77d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e77d-139">-WhatIf</span></span>
<span data-ttu-id="1e77d-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1e77d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e77d-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1e77d-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e77d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e77d-142">CommonParameters</span></span>
<span data-ttu-id="1e77d-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1e77d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e77d-144">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e77d-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e77d-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e77d-145">INPUTS</span></span>

## <span data-ttu-id="1e77d-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e77d-146">OUTPUTS</span></span>

## <span data-ttu-id="1e77d-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1e77d-147">NOTES</span></span>

## <span data-ttu-id="1e77d-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e77d-148">RELATED LINKS</span></span>
