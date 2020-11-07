---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/export-azurermresourcegroup
schema: 2.0.0
ms.openlocfilehash: a5390cd66e97f05e80f52685af6e43135ed64141
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849057"
---
# <span data-ttu-id="ae47e-101">Export-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ae47e-101">Export-AzureRmResourceGroup</span></span>

## <span data-ttu-id="ae47e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ae47e-102">SYNOPSIS</span></span>
<span data-ttu-id="ae47e-103">Egy erőforráscsoportot sablonként rögzít, és egy fájlba menti.</span><span class="sxs-lookup"><span data-stu-id="ae47e-103">Captures a resource group as a template and saves it to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae47e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ae47e-104">SYNTAX</span></span>

```
Export-AzureRmResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ae47e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ae47e-105">DESCRIPTION</span></span>
<span data-ttu-id="ae47e-106">Az **export-AzureRmResourceGroup** parancsmag sablonként rögzíti a megadott erőforráscsoportot, és egy JSON-fájlba menti. Ez olyan esetekben lehet hasznos, amikor már létrehozott néhány erőforrást az erőforráscsoport-ban, és ki szeretné használni a sablonon alapuló telepített példányok használatának előnyeit.</span><span class="sxs-lookup"><span data-stu-id="ae47e-106">The **Export-AzureRmResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="ae47e-107">Ezzel a parancsmaggal megkönnyítheti a meglévő erőforrások sablonjának generálását az erőforrás csoportban.</span><span class="sxs-lookup"><span data-stu-id="ae47e-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>
<span data-ttu-id="ae47e-108">Bizonyos esetekben előfordulhat, hogy ez a parancsmag nem hoz létre a sablon bizonyos részeit.</span><span class="sxs-lookup"><span data-stu-id="ae47e-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="ae47e-109">A figyelmeztető üzenetek tájékoztatni fogják a sikertelen erőforrásokról.</span><span class="sxs-lookup"><span data-stu-id="ae47e-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="ae47e-110">A sablon továbbra is létrejön a sikeres részekhez.</span><span class="sxs-lookup"><span data-stu-id="ae47e-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="ae47e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ae47e-111">EXAMPLES</span></span>

### <span data-ttu-id="ae47e-112">1. példa: erőforráscsoport exportálása</span><span class="sxs-lookup"><span data-stu-id="ae47e-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzureRmResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="ae47e-113">Ez a parancs rögzíti az TestGroup nevű erőforráscsoportot sablonként, és egy JSON-fájlba menti az aktuális címtárban.</span><span class="sxs-lookup"><span data-stu-id="ae47e-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

## <span data-ttu-id="ae47e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ae47e-114">PARAMETERS</span></span>

### <span data-ttu-id="ae47e-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ae47e-115">-ApiVersion</span></span>
<span data-ttu-id="ae47e-116">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae47e-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ae47e-117">Ha nem adja meg, akkor a program a legújabb API-verziót használja.</span><span class="sxs-lookup"><span data-stu-id="ae47e-117">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="ae47e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae47e-118">-DefaultProfile</span></span>
<span data-ttu-id="ae47e-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ae47e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae47e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ae47e-120">-Force</span></span>
<span data-ttu-id="ae47e-121">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="ae47e-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ae47e-122">-IncludeComments</span><span class="sxs-lookup"><span data-stu-id="ae47e-122">-IncludeComments</span></span>
<span data-ttu-id="ae47e-123">Jelzi, hogy a művelet a megjegyzésekkel exportálja a sablont.</span><span class="sxs-lookup"><span data-stu-id="ae47e-123">Indicates that this operation exports the template with comments.</span></span>

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

### <span data-ttu-id="ae47e-124">-IncludeParameterDefaultValue</span><span class="sxs-lookup"><span data-stu-id="ae47e-124">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="ae47e-125">Azt jelzi, hogy a művelet az alapértelmezett értékkel exportálja a Template paramétert.</span><span class="sxs-lookup"><span data-stu-id="ae47e-125">Indicates that this operation exports the template parameter with the default value.</span></span>

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

### <span data-ttu-id="ae47e-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ae47e-126">-InformationAction</span></span>
<span data-ttu-id="ae47e-127">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="ae47e-127">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="ae47e-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ae47e-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ae47e-129">Folytassa</span><span class="sxs-lookup"><span data-stu-id="ae47e-129">Continue</span></span>
- <span data-ttu-id="ae47e-130">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="ae47e-130">Ignore</span></span>
- <span data-ttu-id="ae47e-131">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="ae47e-131">Inquire</span></span>
- <span data-ttu-id="ae47e-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ae47e-132">SilentlyContinue</span></span>
- <span data-ttu-id="ae47e-133">állj</span><span class="sxs-lookup"><span data-stu-id="ae47e-133">Stop</span></span>
- <span data-ttu-id="ae47e-134">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="ae47e-134">Suspend</span></span>

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

### <span data-ttu-id="ae47e-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ae47e-135">-InformationVariable</span></span>
<span data-ttu-id="ae47e-136">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="ae47e-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ae47e-137">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="ae47e-137">-Path</span></span>
<span data-ttu-id="ae47e-138">A sablonfájl kimeneti elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae47e-138">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="ae47e-139">-Pre</span><span class="sxs-lookup"><span data-stu-id="ae47e-139">-Pre</span></span>
<span data-ttu-id="ae47e-140">Jelzi, hogy ez a parancsmag az előzetes verziójú API-t használja, amikor automatikusan meghatározza, hogy melyik API-verziót használja.</span><span class="sxs-lookup"><span data-stu-id="ae47e-140">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="ae47e-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae47e-141">-ResourceGroupName</span></span>
<span data-ttu-id="ae47e-142">Az exportálandó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae47e-142">Specifies the name of the resource group to export.</span></span>

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

### <span data-ttu-id="ae47e-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ae47e-143">-Confirm</span></span>
<span data-ttu-id="ae47e-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ae47e-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae47e-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae47e-145">-WhatIf</span></span>
<span data-ttu-id="ae47e-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ae47e-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae47e-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ae47e-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae47e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae47e-148">CommonParameters</span></span>
<span data-ttu-id="ae47e-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ae47e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae47e-150">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae47e-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae47e-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae47e-151">INPUTS</span></span>

## <span data-ttu-id="ae47e-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae47e-152">OUTPUTS</span></span>

## <span data-ttu-id="ae47e-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ae47e-153">NOTES</span></span>

## <span data-ttu-id="ae47e-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae47e-154">RELATED LINKS</span></span>




