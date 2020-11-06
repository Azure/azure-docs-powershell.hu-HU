---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 4C839730-B494-45BD-B5A1-F93B02AB4B2A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryHub.md
ms.openlocfilehash: 6788f2dea9cf46b888f729ab97640201f740e80d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499171"
---
# <span data-ttu-id="f6601-101">Remove-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="f6601-101">Remove-AzureRmDataFactoryHub</span></span>

## <span data-ttu-id="f6601-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f6601-102">SYNOPSIS</span></span>
<span data-ttu-id="f6601-103">A hub eltávolítása az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="f6601-103">Removes a hub from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6601-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f6601-104">SYNTAX</span></span>

### <span data-ttu-id="f6601-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f6601-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryHub [-Name] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f6601-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f6601-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryHub [-Name] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6601-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f6601-107">DESCRIPTION</span></span>
<span data-ttu-id="f6601-108">A **Remove-AzureRmDataFactoryHub** parancsmag eltávolítja a hubot az Azure Data Factory-től a megadott Azure-erőforrás csoportban és a megadott adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="f6601-108">The **Remove-AzureRmDataFactoryHub** cmdlet removes a hub from Azure Data Factory in the specified Azure resource group and in the specified data factory.</span></span>
<span data-ttu-id="f6601-109">Ha eltávolít egy hubot, a program a hub összes kapcsolt szolgáltatását és futószalagját is eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="f6601-109">If you remove a hub, all linked services and pipelines in the hub are also removed.</span></span>

## <span data-ttu-id="f6601-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f6601-110">EXAMPLES</span></span>

### <span data-ttu-id="f6601-111">1. példa: hub eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f6601-111">Example 1: Remove a hub</span></span>
```
PS C:\>Remove-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub"
```

<span data-ttu-id="f6601-112">Ez a parancs eltávolítja a ContosoDataHub nevű hubot a ADFResourceGroup nevű Azure Resource csoportból, valamint az ADFDataFactory nevű adatfeldolgozóból.</span><span class="sxs-lookup"><span data-stu-id="f6601-112">This command removes the hub named ContosoDataHub from the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="f6601-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f6601-113">PARAMETERS</span></span>

### <span data-ttu-id="f6601-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f6601-114">-DataFactory</span></span>
<span data-ttu-id="f6601-115">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="f6601-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="f6601-116">Ez a parancsmag eltávolítja a hub-t az adatgyárból, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6601-116">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f6601-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f6601-117">-DataFactoryName</span></span>
<span data-ttu-id="f6601-118">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6601-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f6601-119">Ez a parancsmag eltávolítja a hub-t az adatgyárból, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6601-119">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f6601-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f6601-120">-Force</span></span>
<span data-ttu-id="f6601-121">Jelzi, hogy ez a parancsmag eltávolítja a hubot a hub megerősítésének kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="f6601-121">Indicates that this cmdlet removes a hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="f6601-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f6601-122">-Name</span></span>
<span data-ttu-id="f6601-123">Az eltávolítandó hub nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6601-123">Specifies the name of the hub to remove.</span></span>

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

### <span data-ttu-id="f6601-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6601-124">-ResourceGroupName</span></span>
<span data-ttu-id="f6601-125">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6601-125">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f6601-126">Ez a parancsmag eltávolítja a csomópontot abból a csoportból, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="f6601-126">This cmdlet removes a hub from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f6601-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f6601-127">-Confirm</span></span>
<span data-ttu-id="f6601-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f6601-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6601-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6601-129">-WhatIf</span></span>
<span data-ttu-id="f6601-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f6601-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6601-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f6601-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6601-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6601-132">-DefaultProfile</span></span>
<span data-ttu-id="f6601-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f6601-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6601-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6601-134">CommonParameters</span></span>
<span data-ttu-id="f6601-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f6601-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6601-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6601-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6601-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6601-137">INPUTS</span></span>

## <span data-ttu-id="f6601-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6601-138">OUTPUTS</span></span>

### <span data-ttu-id="f6601-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f6601-139">System.Boolean</span></span>

## <span data-ttu-id="f6601-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f6601-140">NOTES</span></span>
* <span data-ttu-id="f6601-141">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="f6601-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f6601-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6601-142">RELATED LINKS</span></span>

[<span data-ttu-id="f6601-143">Get-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="f6601-143">Get-AzureRmDataFactoryHub</span></span>](./Get-AzureRmDataFactoryHub.md)

[<span data-ttu-id="f6601-144">Új – AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="f6601-144">New-AzureRmDataFactoryHub</span></span>](./New-AzureRmDataFactoryHub.md)


