---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2.md
ms.openlocfilehash: 99033646aac6f41397a7097afc8d78626d905a95
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010645"
---
# <span data-ttu-id="7715a-101">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="7715a-101">Remove-AzDataFactoryV2</span></span>

## <span data-ttu-id="7715a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7715a-102">SYNOPSIS</span></span>
<span data-ttu-id="7715a-103">Adat factory eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="7715a-103">Removes a data factory.</span></span>

## <span data-ttu-id="7715a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7715a-104">SYNTAX</span></span>

### <span data-ttu-id="7715a-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7715a-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7715a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7715a-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7715a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7715a-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2 [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7715a-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7715a-108">DESCRIPTION</span></span>
<span data-ttu-id="7715a-109">A Remove-AzDataFactoryV2 parancsmag eltávolítja az adatüzemet.</span><span class="sxs-lookup"><span data-stu-id="7715a-109">The Remove-AzDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="7715a-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7715a-110">EXAMPLES</span></span>

### <span data-ttu-id="7715a-111">1. példa: Adat factory eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7715a-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="7715a-112">Ez a parancs eltávolítja a WikiADF nevű adatüzemet az ADF nevű erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="7715a-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="7715a-113">Ez a parancs egy számértéket ad $True.</span><span class="sxs-lookup"><span data-stu-id="7715a-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="7715a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7715a-114">PARAMETERS</span></span>

### <span data-ttu-id="7715a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7715a-115">-DefaultProfile</span></span>
<span data-ttu-id="7715a-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7715a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7715a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7715a-117">-Force</span></span>
<span data-ttu-id="7715a-118">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="7715a-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="7715a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7715a-119">-InputObject</span></span>
<span data-ttu-id="7715a-120">Az eltávolítható DataFactory-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="7715a-120">Specifies the DataFactory object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7715a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7715a-121">-Name</span></span>
<span data-ttu-id="7715a-122">Az eltávolítható adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7715a-122">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7715a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7715a-123">-ResourceGroupName</span></span>
<span data-ttu-id="7715a-124">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7715a-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="7715a-125">Ez a parancsmag eltávolít egy adat factoryt a paraméter által megadott csoportból.</span><span class="sxs-lookup"><span data-stu-id="7715a-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7715a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7715a-126">-ResourceId</span></span>
<span data-ttu-id="7715a-127">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="7715a-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="7715a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7715a-128">-Confirm</span></span>
<span data-ttu-id="7715a-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7715a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7715a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7715a-130">-WhatIf</span></span>
<span data-ttu-id="7715a-131">Azt mutatja, mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7715a-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="7715a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7715a-132">CommonParameters</span></span>
<span data-ttu-id="7715a-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7715a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7715a-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7715a-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7715a-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7715a-135">INPUTS</span></span>

### <span data-ttu-id="7715a-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="7715a-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="7715a-137">System.String</span><span class="sxs-lookup"><span data-stu-id="7715a-137">System.String</span></span>

## <span data-ttu-id="7715a-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7715a-138">OUTPUTS</span></span>

### <span data-ttu-id="7715a-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="7715a-139">System.Void</span></span>

## <span data-ttu-id="7715a-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7715a-140">NOTES</span></span>
<span data-ttu-id="7715a-141">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="7715a-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="7715a-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7715a-142">RELATED LINKS</span></span>

[<span data-ttu-id="7715a-143">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="7715a-143">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="7715a-144">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="7715a-144">Set-AzDataFactoryV2</span></span>]()
