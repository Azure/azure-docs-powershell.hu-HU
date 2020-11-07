---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 4C839730-B494-45BD-B5A1-F93B02AB4B2A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
ms.openlocfilehash: 0136927eea72911e706c3e0062dbc444cf1f9b25
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667006"
---
# <span data-ttu-id="7f473-101">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="7f473-101">Remove-AzDataFactoryHub</span></span>

## <span data-ttu-id="7f473-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7f473-102">SYNOPSIS</span></span>
<span data-ttu-id="7f473-103">A hub eltávolítása az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="7f473-103">Removes a hub from Azure Data Factory.</span></span>

## <span data-ttu-id="7f473-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7f473-104">SYNTAX</span></span>

### <span data-ttu-id="7f473-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7f473-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f473-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7f473-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f473-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7f473-107">DESCRIPTION</span></span>
<span data-ttu-id="7f473-108">A **Remove-AzDataFactoryHub** parancsmag eltávolítja a hubot az Azure Data Factory-től a megadott Azure-erőforrás csoportban és a megadott adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="7f473-108">The **Remove-AzDataFactoryHub** cmdlet removes a hub from Azure Data Factory in the specified Azure resource group and in the specified data factory.</span></span>
<span data-ttu-id="7f473-109">Ha eltávolít egy hubot, a program a hub összes kapcsolt szolgáltatását és futószalagját is eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="7f473-109">If you remove a hub, all linked services and pipelines in the hub are also removed.</span></span>

## <span data-ttu-id="7f473-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7f473-110">EXAMPLES</span></span>

### <span data-ttu-id="7f473-111">1. példa: hub eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7f473-111">Example 1: Remove a hub</span></span>
```
PS C:\>Remove-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub"
```

<span data-ttu-id="7f473-112">Ez a parancs eltávolítja a ContosoDataHub nevű hubot a ADFResourceGroup nevű Azure Resource csoportból, valamint az ADFDataFactory nevű adatfeldolgozóból.</span><span class="sxs-lookup"><span data-stu-id="7f473-112">This command removes the hub named ContosoDataHub from the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="7f473-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7f473-113">PARAMETERS</span></span>

### <span data-ttu-id="7f473-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="7f473-114">-DataFactory</span></span>
<span data-ttu-id="7f473-115">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="7f473-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="7f473-116">Ez a parancsmag eltávolítja a hub-t az adatgyárból, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f473-116">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f473-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7f473-117">-DataFactoryName</span></span>
<span data-ttu-id="7f473-118">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f473-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="7f473-119">Ez a parancsmag eltávolítja a hub-t az adatgyárból, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f473-119">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7f473-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f473-120">-DefaultProfile</span></span>
<span data-ttu-id="7f473-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7f473-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f473-122">-Force</span><span class="sxs-lookup"><span data-stu-id="7f473-122">-Force</span></span>
<span data-ttu-id="7f473-123">Jelzi, hogy ez a parancsmag eltávolítja a hubot a hub megerősítésének kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="7f473-123">Indicates that this cmdlet removes a hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="7f473-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7f473-124">-Name</span></span>
<span data-ttu-id="7f473-125">Az eltávolítandó hub nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f473-125">Specifies the name of the hub to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f473-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f473-126">-ResourceGroupName</span></span>
<span data-ttu-id="7f473-127">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f473-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="7f473-128">Ez a parancsmag eltávolítja a csomópontot abból a csoportból, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="7f473-128">This cmdlet removes a hub from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7f473-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7f473-129">-Confirm</span></span>
<span data-ttu-id="7f473-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7f473-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f473-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f473-131">-WhatIf</span></span>
<span data-ttu-id="7f473-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7f473-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f473-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7f473-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f473-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f473-134">CommonParameters</span></span>
<span data-ttu-id="7f473-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7f473-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f473-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f473-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f473-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f473-137">INPUTS</span></span>

### <span data-ttu-id="7f473-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7f473-138">System.String</span></span>

### <span data-ttu-id="7f473-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="7f473-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="7f473-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f473-140">OUTPUTS</span></span>

### <span data-ttu-id="7f473-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7f473-141">System.Boolean</span></span>

## <span data-ttu-id="7f473-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7f473-142">NOTES</span></span>
* <span data-ttu-id="7f473-143">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="7f473-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="7f473-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f473-144">RELATED LINKS</span></span>

[<span data-ttu-id="7f473-145">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="7f473-145">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="7f473-146">Új – AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="7f473-146">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)


