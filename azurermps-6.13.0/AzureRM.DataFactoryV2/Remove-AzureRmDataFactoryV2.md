---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
ms.openlocfilehash: a4446fb64ed8d279e24b3cf3d6c82701b48ab754
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491964"
---
# <span data-ttu-id="373da-101">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="373da-101">Remove-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="373da-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="373da-102">SYNOPSIS</span></span>
<span data-ttu-id="373da-103">Az adatfeldolgozó eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="373da-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="373da-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="373da-104">SYNTAX</span></span>

### <span data-ttu-id="373da-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="373da-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="373da-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="373da-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="373da-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="373da-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="373da-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="373da-108">DESCRIPTION</span></span>
<span data-ttu-id="373da-109">Az Remove-AzureRmDataFactoryV2 parancsmag eltávolítja az adatfeldolgozót.</span><span class="sxs-lookup"><span data-stu-id="373da-109">The Remove-AzureRmDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="373da-110">Példák</span><span class="sxs-lookup"><span data-stu-id="373da-110">EXAMPLES</span></span>

### <span data-ttu-id="373da-111">1. példa: az adatfeldolgozó eltávolítása</span><span class="sxs-lookup"><span data-stu-id="373da-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="373da-112">Ez a parancs eltávolítja az WikiADF nevű adatfeldolgozót az ADF nevű erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="373da-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="373da-113">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="373da-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="373da-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="373da-114">PARAMETERS</span></span>

### <span data-ttu-id="373da-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="373da-115">-DefaultProfile</span></span>
<span data-ttu-id="373da-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="373da-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="373da-117">-Force</span><span class="sxs-lookup"><span data-stu-id="373da-117">-Force</span></span>
<span data-ttu-id="373da-118">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="373da-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="373da-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="373da-119">-InputObject</span></span>
<span data-ttu-id="373da-120">Az eltávolítandó DataFactory-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="373da-120">Specifies the DataFactory object to remove.</span></span>

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

### <span data-ttu-id="373da-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="373da-121">-Name</span></span>
<span data-ttu-id="373da-122">Az eltávolítandó adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="373da-122">Specifies the name of the data factory to remove.</span></span>

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

### <span data-ttu-id="373da-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="373da-123">-ResourceGroupName</span></span>
<span data-ttu-id="373da-124">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="373da-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="373da-125">Ez a parancsmag eltávolítja az adatfeldolgozót abban a csoportban, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="373da-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="373da-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="373da-126">-ResourceId</span></span>
<span data-ttu-id="373da-127">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="373da-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="373da-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="373da-128">-Confirm</span></span>
<span data-ttu-id="373da-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="373da-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="373da-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="373da-130">-WhatIf</span></span>
<span data-ttu-id="373da-131">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="373da-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="373da-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="373da-132">CommonParameters</span></span>
<span data-ttu-id="373da-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="373da-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="373da-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="373da-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="373da-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="373da-135">INPUTS</span></span>

### <span data-ttu-id="373da-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="373da-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="373da-137">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="373da-137">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="373da-138">System. String</span><span class="sxs-lookup"><span data-stu-id="373da-138">System.String</span></span>

## <span data-ttu-id="373da-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="373da-139">OUTPUTS</span></span>

### <span data-ttu-id="373da-140">System. Void</span><span class="sxs-lookup"><span data-stu-id="373da-140">System.Void</span></span>

## <span data-ttu-id="373da-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="373da-141">NOTES</span></span>
<span data-ttu-id="373da-142">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="373da-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="373da-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="373da-143">RELATED LINKS</span></span>

[<span data-ttu-id="373da-144">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="373da-144">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="373da-145">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="373da-145">Set-AzureRmDataFactoryV2</span></span>]()
