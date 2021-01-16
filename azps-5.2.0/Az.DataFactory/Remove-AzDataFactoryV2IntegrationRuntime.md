---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 0c24f77b51bcfc50ec11e211fc7f11b60e348221
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329332"
---
# <span data-ttu-id="1e30a-101">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1e30a-101">Remove-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="1e30a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e30a-102">SYNOPSIS</span></span>
<span data-ttu-id="1e30a-103">Eltávolítja az integrációs futásiidőt.</span><span class="sxs-lookup"><span data-stu-id="1e30a-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="1e30a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1e30a-104">SYNTAX</span></span>

### <span data-ttu-id="1e30a-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1e30a-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e30a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1e30a-106">ByResourceId</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e30a-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="1e30a-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1e30a-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1e30a-108">DESCRIPTION</span></span>
<span data-ttu-id="1e30a-109">A Remove-AzDataFactoryV2IntegrationRuntime parancsmag eltávolítja az integrációs futásiidőt.</span><span class="sxs-lookup"><span data-stu-id="1e30a-109">The Remove-AzDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="1e30a-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1e30a-110">EXAMPLES</span></span>

### <span data-ttu-id="1e30a-111">1. példa: Integrációs futási idő eltávolítása</span><span class="sxs-lookup"><span data-stu-id="1e30a-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="1e30a-112">Ez a parancs eltávolítja a "test-reserved-ir" nevű integrációs futásiidőt a "test-df" adatüzemből.</span><span class="sxs-lookup"><span data-stu-id="1e30a-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="1e30a-113">Ez a parancs egy számértéket ad $True.</span><span class="sxs-lookup"><span data-stu-id="1e30a-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="1e30a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e30a-114">PARAMETERS</span></span>

### <span data-ttu-id="1e30a-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1e30a-115">-DataFactoryName</span></span>
<span data-ttu-id="1e30a-116">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="1e30a-116">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e30a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e30a-117">-DefaultProfile</span></span>
<span data-ttu-id="1e30a-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1e30a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e30a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="1e30a-119">-Force</span></span>
<span data-ttu-id="1e30a-120">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="1e30a-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="1e30a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e30a-121">-InputObject</span></span>
<span data-ttu-id="1e30a-122">Az integráció futásidejű objektuma.</span><span class="sxs-lookup"><span data-stu-id="1e30a-122">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e30a-123">-LinkedDataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1e30a-123">-LinkedDataFactoryName</span></span>
<span data-ttu-id="1e30a-124">A csatolt adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="1e30a-124">The linked data factory name.</span></span>

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

### <span data-ttu-id="1e30a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="1e30a-125">-Name</span></span>
<span data-ttu-id="1e30a-126">Az integráció futásidejű neve.</span><span class="sxs-lookup"><span data-stu-id="1e30a-126">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e30a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e30a-127">-ResourceGroupName</span></span>
<span data-ttu-id="1e30a-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1e30a-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e30a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e30a-129">-ResourceId</span></span>
<span data-ttu-id="1e30a-130">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="1e30a-130">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e30a-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e30a-131">-Confirm</span></span>
<span data-ttu-id="1e30a-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1e30a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e30a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e30a-133">-WhatIf</span></span>
<span data-ttu-id="1e30a-134">Azt mutatja, mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1e30a-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="1e30a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e30a-135">CommonParameters</span></span>
<span data-ttu-id="1e30a-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e30a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e30a-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e30a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e30a-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1e30a-138">INPUTS</span></span>

### <span data-ttu-id="1e30a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="1e30a-139">System.String</span></span>

### <span data-ttu-id="1e30a-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1e30a-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="1e30a-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e30a-141">OUTPUTS</span></span>

### <span data-ttu-id="1e30a-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="1e30a-142">System.Void</span></span>

## <span data-ttu-id="1e30a-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1e30a-143">NOTES</span></span>
<span data-ttu-id="1e30a-144">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, kezelő, adatok, faktorok, másolás, tevékenységek, integráció futásideje</span><span class="sxs-lookup"><span data-stu-id="1e30a-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="1e30a-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e30a-145">RELATED LINKS</span></span>

[<span data-ttu-id="1e30a-146">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1e30a-146">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="1e30a-147">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1e30a-147">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

