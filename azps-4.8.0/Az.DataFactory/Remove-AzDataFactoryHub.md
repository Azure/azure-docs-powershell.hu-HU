---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 4C839730-B494-45BD-B5A1-F93B02AB4B2A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
ms.openlocfilehash: 12a18c62d3cc3412726df323bd48acd86ed7b1fd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017879"
---
# <span data-ttu-id="f391a-101">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="f391a-101">Remove-AzDataFactoryHub</span></span>

## <span data-ttu-id="f391a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f391a-102">SYNOPSIS</span></span>
<span data-ttu-id="f391a-103">A hub eltávolítása az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="f391a-103">Removes a hub from Azure Data Factory.</span></span>

## <span data-ttu-id="f391a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f391a-104">SYNTAX</span></span>

### <span data-ttu-id="f391a-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f391a-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f391a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f391a-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f391a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f391a-107">DESCRIPTION</span></span>
<span data-ttu-id="f391a-108">A **Remove-AzDataFactoryHub** parancsmag eltávolítja a hubot az Azure Data Factory-től a megadott Azure-erőforrás csoportban és a megadott adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="f391a-108">The **Remove-AzDataFactoryHub** cmdlet removes a hub from Azure Data Factory in the specified Azure resource group and in the specified data factory.</span></span>
<span data-ttu-id="f391a-109">Ha eltávolít egy hubot, a program a hub összes kapcsolt szolgáltatását és futószalagját is eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="f391a-109">If you remove a hub, all linked services and pipelines in the hub are also removed.</span></span>

## <span data-ttu-id="f391a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f391a-110">EXAMPLES</span></span>

### <span data-ttu-id="f391a-111">1. példa: hub eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f391a-111">Example 1: Remove a hub</span></span>
```
PS C:\>Remove-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub"
```

<span data-ttu-id="f391a-112">Ez a parancs eltávolítja a ContosoDataHub nevű hubot a ADFResourceGroup nevű Azure Resource csoportból, valamint az ADFDataFactory nevű adatfeldolgozóból.</span><span class="sxs-lookup"><span data-stu-id="f391a-112">This command removes the hub named ContosoDataHub from the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="f391a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f391a-113">PARAMETERS</span></span>

### <span data-ttu-id="f391a-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f391a-114">-DataFactory</span></span>
<span data-ttu-id="f391a-115">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="f391a-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="f391a-116">Ez a parancsmag eltávolítja a hub-t az adatgyárból, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="f391a-116">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f391a-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f391a-117">-DataFactoryName</span></span>
<span data-ttu-id="f391a-118">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f391a-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f391a-119">Ez a parancsmag eltávolítja a hub-t az adatgyárból, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="f391a-119">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f391a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f391a-120">-DefaultProfile</span></span>
<span data-ttu-id="f391a-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f391a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f391a-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f391a-122">-Force</span></span>
<span data-ttu-id="f391a-123">Jelzi, hogy ez a parancsmag eltávolítja a hubot a hub megerősítésének kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="f391a-123">Indicates that this cmdlet removes a hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="f391a-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f391a-124">-Name</span></span>
<span data-ttu-id="f391a-125">Az eltávolítandó hub nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f391a-125">Specifies the name of the hub to remove.</span></span>

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

### <span data-ttu-id="f391a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f391a-126">-ResourceGroupName</span></span>
<span data-ttu-id="f391a-127">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f391a-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f391a-128">Ez a parancsmag eltávolítja a csomópontot abból a csoportból, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="f391a-128">This cmdlet removes a hub from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f391a-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f391a-129">-Confirm</span></span>
<span data-ttu-id="f391a-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f391a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f391a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f391a-131">-WhatIf</span></span>
<span data-ttu-id="f391a-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f391a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f391a-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f391a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f391a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f391a-134">CommonParameters</span></span>
<span data-ttu-id="f391a-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f391a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f391a-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f391a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f391a-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f391a-137">INPUTS</span></span>

### <span data-ttu-id="f391a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f391a-138">System.String</span></span>

### <span data-ttu-id="f391a-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f391a-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="f391a-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f391a-140">OUTPUTS</span></span>

### <span data-ttu-id="f391a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f391a-141">System.Boolean</span></span>

## <span data-ttu-id="f391a-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f391a-142">NOTES</span></span>
* <span data-ttu-id="f391a-143">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="f391a-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f391a-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f391a-144">RELATED LINKS</span></span>

[<span data-ttu-id="f391a-145">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="f391a-145">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="f391a-146">Új – AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="f391a-146">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)


