---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2.md
ms.openlocfilehash: c396455804f6bb501fa6439fceffb0eb45875516
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183674"
---
# <span data-ttu-id="dfe76-101">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="dfe76-101">Remove-AzDataFactoryV2</span></span>

## <span data-ttu-id="dfe76-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dfe76-102">SYNOPSIS</span></span>
<span data-ttu-id="dfe76-103">Az adatfeldolgozó eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="dfe76-103">Removes a data factory.</span></span>

## <span data-ttu-id="dfe76-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dfe76-104">SYNTAX</span></span>

### <span data-ttu-id="dfe76-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dfe76-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfe76-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="dfe76-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfe76-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="dfe76-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2 [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfe76-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="dfe76-108">DESCRIPTION</span></span>
<span data-ttu-id="dfe76-109">Az Remove-AzDataFactoryV2 parancsmag eltávolítja az adatfeldolgozót.</span><span class="sxs-lookup"><span data-stu-id="dfe76-109">The Remove-AzDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="dfe76-110">Példák</span><span class="sxs-lookup"><span data-stu-id="dfe76-110">EXAMPLES</span></span>

### <span data-ttu-id="dfe76-111">1. példa: az adatfeldolgozó eltávolítása</span><span class="sxs-lookup"><span data-stu-id="dfe76-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="dfe76-112">Ez a parancs eltávolítja az WikiADF nevű adatfeldolgozót az ADF nevű erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="dfe76-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="dfe76-113">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="dfe76-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="dfe76-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dfe76-114">PARAMETERS</span></span>

### <span data-ttu-id="dfe76-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfe76-115">-DefaultProfile</span></span>
<span data-ttu-id="dfe76-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dfe76-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfe76-117">-Force</span><span class="sxs-lookup"><span data-stu-id="dfe76-117">-Force</span></span>
<span data-ttu-id="dfe76-118">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="dfe76-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="dfe76-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dfe76-119">-InputObject</span></span>
<span data-ttu-id="dfe76-120">Az eltávolítandó DataFactory-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="dfe76-120">Specifies the DataFactory object to remove.</span></span>

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

### <span data-ttu-id="dfe76-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dfe76-121">-Name</span></span>
<span data-ttu-id="dfe76-122">Az eltávolítandó adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dfe76-122">Specifies the name of the data factory to remove.</span></span>

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

### <span data-ttu-id="dfe76-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfe76-123">-ResourceGroupName</span></span>
<span data-ttu-id="dfe76-124">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dfe76-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="dfe76-125">Ez a parancsmag eltávolítja az adatfeldolgozót abban a csoportban, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="dfe76-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="dfe76-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dfe76-126">-ResourceId</span></span>
<span data-ttu-id="dfe76-127">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="dfe76-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="dfe76-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dfe76-128">-Confirm</span></span>
<span data-ttu-id="dfe76-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dfe76-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfe76-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfe76-130">-WhatIf</span></span>
<span data-ttu-id="dfe76-131">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="dfe76-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="dfe76-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfe76-132">CommonParameters</span></span>
<span data-ttu-id="dfe76-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dfe76-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfe76-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfe76-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfe76-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dfe76-135">INPUTS</span></span>

### <span data-ttu-id="dfe76-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="dfe76-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="dfe76-137">System. String</span><span class="sxs-lookup"><span data-stu-id="dfe76-137">System.String</span></span>

## <span data-ttu-id="dfe76-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dfe76-138">OUTPUTS</span></span>

### <span data-ttu-id="dfe76-139">System. Void</span><span class="sxs-lookup"><span data-stu-id="dfe76-139">System.Void</span></span>

## <span data-ttu-id="dfe76-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dfe76-140">NOTES</span></span>
<span data-ttu-id="dfe76-141">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="dfe76-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="dfe76-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dfe76-142">RELATED LINKS</span></span>

[<span data-ttu-id="dfe76-143">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="dfe76-143">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="dfe76-144">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="dfe76-144">Set-AzDataFactoryV2</span></span>]()
