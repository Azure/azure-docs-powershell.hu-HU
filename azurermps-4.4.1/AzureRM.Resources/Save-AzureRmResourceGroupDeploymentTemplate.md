---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmResourceGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmResourceGroupDeploymentTemplate.md
ms.openlocfilehash: 8f146c6516226c800f45489e1f7fa5d37173e151
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680490"
---
# <span data-ttu-id="391a7-101">Save-AzureRmResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="391a7-101">Save-AzureRmResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="391a7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="391a7-102">SYNOPSIS</span></span>
<span data-ttu-id="391a7-103">Egy erőforráscsoport-telepítő sablont ment a fájlba.</span><span class="sxs-lookup"><span data-stu-id="391a7-103">Saves a resource group deployment template to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="391a7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="391a7-104">SYNTAX</span></span>

```
Save-AzureRmResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String>
 [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="391a7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="391a7-105">DESCRIPTION</span></span>
<span data-ttu-id="391a7-106">A **Save-AzureRmResourceGroupDeploymentTemplate**  parancsmag egy erőforráscsoport-telepítő sablont JSON-fájlba menti.</span><span class="sxs-lookup"><span data-stu-id="391a7-106">The **Save-AzureRmResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="391a7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="391a7-107">EXAMPLES</span></span>

### <span data-ttu-id="391a7-108">Példa 1: központi telepítő sablon mentése</span><span class="sxs-lookup"><span data-stu-id="391a7-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzureRmResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="391a7-109">Ez a parancs beolvassa a TestDeployment a telepítő sablonból, és egy JSON-fájlként menti az aktuális könyvtárat.</span><span class="sxs-lookup"><span data-stu-id="391a7-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="391a7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="391a7-110">PARAMETERS</span></span>

### <span data-ttu-id="391a7-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="391a7-111">-ApiVersion</span></span>
<span data-ttu-id="391a7-112">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="391a7-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="391a7-113">Ha nem adja meg, akkor a program a legújabb API-verziót használja.</span><span class="sxs-lookup"><span data-stu-id="391a7-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="391a7-114">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="391a7-114">-DeploymentName</span></span>
<span data-ttu-id="391a7-115">A központi telepítő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="391a7-115">Specifies the name of the deployment.</span></span>

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

### <span data-ttu-id="391a7-116">-Force</span><span class="sxs-lookup"><span data-stu-id="391a7-116">-Force</span></span>
<span data-ttu-id="391a7-117">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="391a7-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="391a7-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="391a7-118">-InformationAction</span></span>
<span data-ttu-id="391a7-119">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="391a7-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="391a7-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="391a7-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="391a7-121">Folytassa</span><span class="sxs-lookup"><span data-stu-id="391a7-121">Continue</span></span>
- <span data-ttu-id="391a7-122">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="391a7-122">Ignore</span></span>
- <span data-ttu-id="391a7-123">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="391a7-123">Inquire</span></span>
- <span data-ttu-id="391a7-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="391a7-124">SilentlyContinue</span></span>
- <span data-ttu-id="391a7-125">állj</span><span class="sxs-lookup"><span data-stu-id="391a7-125">Stop</span></span>
- <span data-ttu-id="391a7-126">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="391a7-126">Suspend</span></span>

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

### <span data-ttu-id="391a7-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="391a7-127">-InformationVariable</span></span>
<span data-ttu-id="391a7-128">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="391a7-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="391a7-129">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="391a7-129">-Path</span></span>
<span data-ttu-id="391a7-130">A sablonfájl kimeneti elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="391a7-130">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="391a7-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="391a7-131">-Pre</span></span>
<span data-ttu-id="391a7-132">Jelzi, hogy ez a parancsmag az előzetes verziójú API-t használja, amikor automatikusan meghatározza, hogy melyik API-verziót használja.</span><span class="sxs-lookup"><span data-stu-id="391a7-132">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="391a7-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="391a7-133">-ResourceGroupName</span></span>
<span data-ttu-id="391a7-134">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="391a7-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="391a7-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="391a7-135">-Confirm</span></span>
<span data-ttu-id="391a7-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="391a7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="391a7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="391a7-137">-WhatIf</span></span>
<span data-ttu-id="391a7-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="391a7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="391a7-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="391a7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="391a7-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="391a7-140">-DefaultProfile</span></span>
<span data-ttu-id="391a7-141">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="391a7-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="391a7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="391a7-142">CommonParameters</span></span>
<span data-ttu-id="391a7-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="391a7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="391a7-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="391a7-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="391a7-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="391a7-145">INPUTS</span></span>

## <span data-ttu-id="391a7-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="391a7-146">OUTPUTS</span></span>

### <span data-ttu-id="391a7-147">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="391a7-147">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="391a7-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="391a7-148">NOTES</span></span>

## <span data-ttu-id="391a7-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="391a7-149">RELATED LINKS</span></span>

