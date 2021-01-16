---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: acd3fadd45dfc32c745af943013f4c0f00b663ad
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341178"
---
# <span data-ttu-id="0f6fb-101">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="0f6fb-101">Remove-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="0f6fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f6fb-102">SYNOPSIS</span></span>
<span data-ttu-id="0f6fb-103">Eltávolít egy csatolt szolgáltatást a Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-103">Removes a linked service from Data Factory.</span></span>

## <span data-ttu-id="0f6fb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0f6fb-104">SYNTAX</span></span>

### <span data-ttu-id="0f6fb-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0f6fb-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f6fb-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0f6fb-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f6fb-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0f6fb-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2LinkedService [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f6fb-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0f6fb-108">DESCRIPTION</span></span>
<span data-ttu-id="0f6fb-109">A Remove-AzDataFactoryV2LinkedService parancsmag eltávolítja a csatolt szolgáltatásokat az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-109">The Remove-AzDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="0f6fb-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0f6fb-110">EXAMPLES</span></span>

### <span data-ttu-id="0f6fb-111">1. példa: Csatolt szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0f6fb-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="0f6fb-112">Ez a parancs eltávolítja a LinkedServiceTest nevű csatolt szolgáltatást a WikiADF nevű adatüzemből.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="0f6fb-113">Ez a parancs egy számértéket ad $True.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="0f6fb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f6fb-114">PARAMETERS</span></span>

### <span data-ttu-id="0f6fb-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0f6fb-115">-DataFactoryName</span></span>
<span data-ttu-id="0f6fb-116">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="0f6fb-117">Ez a parancsmag eltávolít egy csatolt szolgáltatást a paraméter által megadott adatüzemből.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-117">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f6fb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f6fb-118">-DefaultProfile</span></span>
<span data-ttu-id="0f6fb-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f6fb-120">-Force</span><span class="sxs-lookup"><span data-stu-id="0f6fb-120">-Force</span></span>
<span data-ttu-id="0f6fb-121">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="0f6fb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f6fb-122">-InputObject</span></span>
<span data-ttu-id="0f6fb-123">Az eltávolítható LinkedService-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-123">Specifies the LinkedService object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f6fb-124">-Name</span><span class="sxs-lookup"><span data-stu-id="0f6fb-124">-Name</span></span>
<span data-ttu-id="0f6fb-125">Az eltávolítható csatolt szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="0f6fb-126">A csatolt szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-126">Name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f6fb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f6fb-127">-ResourceGroupName</span></span>
<span data-ttu-id="0f6fb-128">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0f6fb-129">Ez a parancsmag eltávolít egy csatolt szolgáltatást a paraméter által megadott csoportból.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f6fb-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f6fb-130">-ResourceId</span></span>
<span data-ttu-id="0f6fb-131">Az eltávolítható csatolt szolgáltatás Azure-erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-131">The Azure resource ID of the linked service to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f6fb-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f6fb-132">-Confirm</span></span>
<span data-ttu-id="0f6fb-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f6fb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f6fb-134">-WhatIf</span></span>
<span data-ttu-id="0f6fb-135">Azt mutatja, mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="0f6fb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f6fb-136">CommonParameters</span></span>
<span data-ttu-id="0f6fb-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f6fb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f6fb-138">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f6fb-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f6fb-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0f6fb-139">INPUTS</span></span>

### <span data-ttu-id="0f6fb-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="0f6fb-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

### <span data-ttu-id="0f6fb-141">System.String</span><span class="sxs-lookup"><span data-stu-id="0f6fb-141">System.String</span></span>

## <span data-ttu-id="0f6fb-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f6fb-142">OUTPUTS</span></span>

### <span data-ttu-id="0f6fb-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="0f6fb-143">System.Void</span></span>

## <span data-ttu-id="0f6fb-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0f6fb-144">NOTES</span></span>
<span data-ttu-id="0f6fb-145">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="0f6fb-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0f6fb-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f6fb-146">RELATED LINKS</span></span>

[<span data-ttu-id="0f6fb-147">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="0f6fb-147">Get-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="0f6fb-148">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="0f6fb-148">Set-AzDataFactoryV2LinkedService</span></span>]()

