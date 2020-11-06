---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
ms.openlocfilehash: 9d7d3e3ae06d46b1ea3cb3b1e4e8db1944dc87e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499160"
---
# <span data-ttu-id="5b971-101">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="5b971-101">Remove-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="5b971-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5b971-102">SYNOPSIS</span></span>
<span data-ttu-id="5b971-103">Az adatfeldolgozó eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="5b971-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b971-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5b971-104">SYNTAX</span></span>

### <span data-ttu-id="5b971-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5b971-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b971-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="5b971-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b971-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5b971-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b971-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5b971-108">DESCRIPTION</span></span>
<span data-ttu-id="5b971-109">Az Remove-AzureRmDataFactoryV2 parancsmag eltávolítja az adatfeldolgozót.</span><span class="sxs-lookup"><span data-stu-id="5b971-109">The Remove-AzureRmDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="5b971-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5b971-110">EXAMPLES</span></span>

### <span data-ttu-id="5b971-111">1. példa: az adatfeldolgozó eltávolítása</span><span class="sxs-lookup"><span data-stu-id="5b971-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="5b971-112">Ez a parancs eltávolítja az WikiADF nevű adatfeldolgozót az ADF nevű erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="5b971-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="5b971-113">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="5b971-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="5b971-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5b971-114">PARAMETERS</span></span>

### <span data-ttu-id="5b971-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5b971-115">-Confirm</span></span>
<span data-ttu-id="5b971-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5b971-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b971-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b971-117">-InputObject</span></span>
<span data-ttu-id="5b971-118">Az eltávolítandó DataFactory-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b971-118">Specifies the DataFactory object to remove.</span></span>

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

### <span data-ttu-id="5b971-119">-Force</span><span class="sxs-lookup"><span data-stu-id="5b971-119">-Force</span></span>
<span data-ttu-id="5b971-120">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="5b971-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="5b971-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5b971-121">-Name</span></span>
<span data-ttu-id="5b971-122">Az eltávolítandó adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b971-122">Specifies the name of the data factory to remove.</span></span>

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

### <span data-ttu-id="5b971-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b971-123">-ResourceGroupName</span></span>
<span data-ttu-id="5b971-124">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b971-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="5b971-125">Ez a parancsmag eltávolítja az adatfeldolgozót abban a csoportban, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="5b971-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5b971-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b971-126">-ResourceId</span></span>
<span data-ttu-id="5b971-127">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="5b971-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5b971-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b971-128">-WhatIf</span></span>
<span data-ttu-id="5b971-129">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5b971-129">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="5b971-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b971-130">-DefaultProfile</span></span>
<span data-ttu-id="5b971-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5b971-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b971-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b971-132">CommonParameters</span></span>
<span data-ttu-id="5b971-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5b971-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b971-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b971-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b971-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b971-135">INPUTS</span></span>

### <span data-ttu-id="5b971-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="5b971-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="5b971-137">System. String</span><span class="sxs-lookup"><span data-stu-id="5b971-137">System.String</span></span>

## <span data-ttu-id="5b971-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b971-138">OUTPUTS</span></span>

### <span data-ttu-id="5b971-139">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="5b971-139">System.Object</span></span>

## <span data-ttu-id="5b971-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5b971-140">NOTES</span></span>
<span data-ttu-id="5b971-141">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="5b971-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5b971-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b971-142">RELATED LINKS</span></span>

[<span data-ttu-id="5b971-143">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="5b971-143">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="5b971-144">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="5b971-144">Set-AzureRmDataFactoryV2</span></span>]()
