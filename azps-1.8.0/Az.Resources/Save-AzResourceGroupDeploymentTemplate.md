---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azresourcegroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
ms.openlocfilehash: f9532ebaffaaae6a1429cb7ce8680283572c1775
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669319"
---
# <span data-ttu-id="41af4-101">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="41af4-101">Save-AzResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="41af4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="41af4-102">SYNOPSIS</span></span>
<span data-ttu-id="41af4-103">Egy erőforráscsoport-telepítő sablont ment a fájlba.</span><span class="sxs-lookup"><span data-stu-id="41af4-103">Saves a resource group deployment template to a file.</span></span>

## <span data-ttu-id="41af4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="41af4-104">SYNTAX</span></span>

```
Save-AzResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String> [-Path <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="41af4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="41af4-105">DESCRIPTION</span></span>
<span data-ttu-id="41af4-106">A **Save-AzResourceGroupDeploymentTemplate**  parancsmag egy erőforráscsoport-telepítő sablont JSON-fájlba menti.</span><span class="sxs-lookup"><span data-stu-id="41af4-106">The **Save-AzResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="41af4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="41af4-107">EXAMPLES</span></span>

### <span data-ttu-id="41af4-108">Példa 1: központi telepítő sablon mentése</span><span class="sxs-lookup"><span data-stu-id="41af4-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="41af4-109">Ez a parancs beolvassa a TestDeployment a telepítő sablonból, és egy JSON-fájlként menti az aktuális könyvtárat.</span><span class="sxs-lookup"><span data-stu-id="41af4-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="41af4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="41af4-110">PARAMETERS</span></span>

### <span data-ttu-id="41af4-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="41af4-111">-ApiVersion</span></span>
<span data-ttu-id="41af4-112">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="41af4-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="41af4-113">Ha nem adja meg, akkor a program a legújabb API-verziót használja.</span><span class="sxs-lookup"><span data-stu-id="41af4-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="41af4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41af4-114">-DefaultProfile</span></span>
<span data-ttu-id="41af4-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="41af4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41af4-116">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="41af4-116">-DeploymentName</span></span>
<span data-ttu-id="41af4-117">A központi telepítő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="41af4-117">Specifies the name of the deployment.</span></span>

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

### <span data-ttu-id="41af4-118">-Force</span><span class="sxs-lookup"><span data-stu-id="41af4-118">-Force</span></span>
<span data-ttu-id="41af4-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="41af4-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="41af4-120">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="41af4-120">-Path</span></span>
<span data-ttu-id="41af4-121">A sablonfájl kimeneti elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="41af4-121">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="41af4-122">-Pre</span><span class="sxs-lookup"><span data-stu-id="41af4-122">-Pre</span></span>
<span data-ttu-id="41af4-123">Jelzi, hogy ez a parancsmag az előzetes verziójú API-t használja, amikor automatikusan meghatározza, hogy melyik API-verziót használja.</span><span class="sxs-lookup"><span data-stu-id="41af4-123">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="41af4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41af4-124">-ResourceGroupName</span></span>
<span data-ttu-id="41af4-125">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="41af4-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="41af4-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="41af4-126">-Confirm</span></span>
<span data-ttu-id="41af4-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="41af4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41af4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41af4-128">-WhatIf</span></span>
<span data-ttu-id="41af4-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="41af4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41af4-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="41af4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41af4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41af4-131">CommonParameters</span></span>
<span data-ttu-id="41af4-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="41af4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41af4-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41af4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41af4-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="41af4-134">INPUTS</span></span>

### <span data-ttu-id="41af4-135">System. String</span><span class="sxs-lookup"><span data-stu-id="41af4-135">System.String</span></span>

## <span data-ttu-id="41af4-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41af4-136">OUTPUTS</span></span>

### <span data-ttu-id="41af4-137">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="41af4-137">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="41af4-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="41af4-138">NOTES</span></span>

## <span data-ttu-id="41af4-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41af4-139">RELATED LINKS</span></span>
