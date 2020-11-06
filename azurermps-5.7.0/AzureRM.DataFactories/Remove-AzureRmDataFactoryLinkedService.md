---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 9425D38D-5978-421F-A438-4463068C4628
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryLinkedService.md
ms.openlocfilehash: 94321cc8f9d42cd4ef26e617426f844b9774b5b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496611"
---
# <span data-ttu-id="69b2b-101">Remove-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="69b2b-101">Remove-AzureRmDataFactoryLinkedService</span></span>

## <span data-ttu-id="69b2b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="69b2b-102">SYNOPSIS</span></span>
<span data-ttu-id="69b2b-103">Egy kapcsolt szolgáltatás eltávolítása az Azure Data Factory alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="69b2b-103">Removes a linked service from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69b2b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="69b2b-104">SYNTAX</span></span>

### <span data-ttu-id="69b2b-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="69b2b-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryLinkedService [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69b2b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="69b2b-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryLinkedService [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69b2b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="69b2b-107">DESCRIPTION</span></span>
<span data-ttu-id="69b2b-108">A **Remove-AzureRmDataFactoryLinkedService** parancsmag egy kapcsolt szolgáltatást távolít el az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="69b2b-108">The **Remove-AzureRmDataFactoryLinkedService** cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="69b2b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="69b2b-109">EXAMPLES</span></span>

### <span data-ttu-id="69b2b-110">1. példa: kapcsolt szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="69b2b-110">Example 1: Remove a linked service</span></span>
```
PS C:\>Remove-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
Confirm
Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="69b2b-111">Ez a parancs eltávolítja a LinkedServiceTest nevű kapcsolt szolgáltatást a WikiADF nevű adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="69b2b-111">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="69b2b-112">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="69b2b-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="69b2b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="69b2b-113">PARAMETERS</span></span>

### <span data-ttu-id="69b2b-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="69b2b-114">-DataFactory</span></span>
<span data-ttu-id="69b2b-115">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="69b2b-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="69b2b-116">Ez a parancsmag eltávolítja a kapcsolt szolgáltatást az adatgyárból, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="69b2b-116">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69b2b-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="69b2b-117">-DataFactoryName</span></span>
<span data-ttu-id="69b2b-118">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="69b2b-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="69b2b-119">Ez a parancsmag eltávolítja a kapcsolt szolgáltatást az adatgyárból, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="69b2b-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69b2b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69b2b-120">-DefaultProfile</span></span>
<span data-ttu-id="69b2b-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="69b2b-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69b2b-122">-Force</span><span class="sxs-lookup"><span data-stu-id="69b2b-122">-Force</span></span>
<span data-ttu-id="69b2b-123">Azt jelzi, hogy ez a parancsmag egy kapcsolt szolgáltatás eltávolítását követően nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="69b2b-123">Indicates that this cmdlet removes a linked service without prompting you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69b2b-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="69b2b-124">-Name</span></span>
<span data-ttu-id="69b2b-125">Az eltávolítandó kapcsolt szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="69b2b-125">Specifies the name of the linked service to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69b2b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69b2b-126">-ResourceGroupName</span></span>
<span data-ttu-id="69b2b-127">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="69b2b-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="69b2b-128">Ez a parancsmag eltávolítja a kapcsolt szolgáltatást abból a csoportból, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="69b2b-128">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69b2b-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="69b2b-129">-Confirm</span></span>
<span data-ttu-id="69b2b-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="69b2b-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69b2b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69b2b-131">-WhatIf</span></span>
<span data-ttu-id="69b2b-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="69b2b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69b2b-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="69b2b-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69b2b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69b2b-134">CommonParameters</span></span>
<span data-ttu-id="69b2b-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="69b2b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69b2b-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69b2b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69b2b-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="69b2b-137">INPUTS</span></span>

### <span data-ttu-id="69b2b-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="69b2b-138">None</span></span>
<span data-ttu-id="69b2b-139">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="69b2b-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="69b2b-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69b2b-140">OUTPUTS</span></span>

### <span data-ttu-id="69b2b-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="69b2b-141">System.Boolean</span></span>

## <span data-ttu-id="69b2b-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="69b2b-142">NOTES</span></span>
* <span data-ttu-id="69b2b-143">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="69b2b-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="69b2b-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69b2b-144">RELATED LINKS</span></span>

[<span data-ttu-id="69b2b-145">Get-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="69b2b-145">Get-AzureRmDataFactoryLinkedService</span></span>](./Get-AzureRmDataFactoryLinkedService.md)

[<span data-ttu-id="69b2b-146">Új – AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="69b2b-146">New-AzureRmDataFactoryLinkedService</span></span>](./New-AzureRmDataFactoryLinkedService.md)


