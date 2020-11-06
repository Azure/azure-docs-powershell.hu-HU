---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: E1461540-DEAE-43C3-83DF-7DF3FE8D4EC0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryGateway.md
ms.openlocfilehash: d9ae03325afbfe81c47847cb27df75973221667b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497828"
---
# <span data-ttu-id="90a88-101">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="90a88-101">Remove-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="90a88-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="90a88-102">SYNOPSIS</span></span>
<span data-ttu-id="90a88-103">Átjáró eltávolítása az Azure Data Factory programból.</span><span class="sxs-lookup"><span data-stu-id="90a88-103">Removes a gateway from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90a88-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="90a88-104">SYNTAX</span></span>

### <span data-ttu-id="90a88-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="90a88-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="90a88-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="90a88-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90a88-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="90a88-107">DESCRIPTION</span></span>
<span data-ttu-id="90a88-108">A **Remove-AzureRmDataFactoryGateway** parancsmag eltávolítja a megadott átjárót az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="90a88-108">The **Remove-AzureRmDataFactoryGateway** cmdlet removes the specified gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="90a88-109">Példák</span><span class="sxs-lookup"><span data-stu-id="90a88-109">EXAMPLES</span></span>

### <span data-ttu-id="90a88-110">1. példa: átjáró eltávolítása</span><span class="sxs-lookup"><span data-stu-id="90a88-110">Example 1: Remove a gateway</span></span>
```
PS C:\>Remove-AzureRmDataFactoryGateway -Name "ContosoGateway" -DataFactoryName "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove gateway 'ContosoGateway' in data factory 'WikiADF'? 
 [Y] Yes  [N] No  [S] Suspend  [?] Help (default is Y): Y
True
```

<span data-ttu-id="90a88-111">Ez a parancs eltávolítja a ContosoGateway nevű átjárót a WikiADF nevű adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="90a88-111">This command removes the gateway named ContosoGateway from the data factory named WikiADF.</span></span>

## <span data-ttu-id="90a88-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="90a88-112">PARAMETERS</span></span>

### <span data-ttu-id="90a88-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="90a88-113">-DataFactory</span></span>
<span data-ttu-id="90a88-114">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="90a88-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="90a88-115">Ez a parancsmag eltávolítja az adatgyárból az átjárót, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="90a88-115">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="90a88-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="90a88-116">-DataFactoryName</span></span>
<span data-ttu-id="90a88-117">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="90a88-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="90a88-118">Ez a parancsmag eltávolítja az adatgyárból az átjárót, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="90a88-118">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="90a88-119">-Force</span><span class="sxs-lookup"><span data-stu-id="90a88-119">-Force</span></span>
<span data-ttu-id="90a88-120">Jelzi, hogy ez a parancsmag eltávolítja az átjárót anélkül, hogy megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="90a88-120">Indicates that this cmdlet removes a gateway without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="90a88-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="90a88-121">-Name</span></span>
<span data-ttu-id="90a88-122">Az eltávolítandó átjáró nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="90a88-122">Specifies the name of the gateway to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90a88-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90a88-123">-ResourceGroupName</span></span>
<span data-ttu-id="90a88-124">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="90a88-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="90a88-125">Ez a parancsmag eltávolítja azt az átjárót, amely a paraméter által megadott csoportba tartozik.</span><span class="sxs-lookup"><span data-stu-id="90a88-125">This cmdlet removes a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="90a88-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="90a88-126">-Confirm</span></span>
<span data-ttu-id="90a88-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="90a88-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90a88-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90a88-128">-WhatIf</span></span>
<span data-ttu-id="90a88-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="90a88-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90a88-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="90a88-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90a88-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90a88-131">-DefaultProfile</span></span>
<span data-ttu-id="90a88-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="90a88-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90a88-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90a88-133">CommonParameters</span></span>
<span data-ttu-id="90a88-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="90a88-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90a88-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90a88-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90a88-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="90a88-136">INPUTS</span></span>

## <span data-ttu-id="90a88-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="90a88-137">OUTPUTS</span></span>

### <span data-ttu-id="90a88-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="90a88-138">System.Boolean</span></span>

## <span data-ttu-id="90a88-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="90a88-139">NOTES</span></span>
* <span data-ttu-id="90a88-140">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="90a88-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="90a88-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="90a88-141">RELATED LINKS</span></span>

[<span data-ttu-id="90a88-142">Get-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="90a88-142">Get-AzureRmDataFactoryGateway</span></span>](./Get-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="90a88-143">Új – AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="90a88-143">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="90a88-144">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="90a88-144">Set-AzureRmDataFactoryGateway</span></span>](./Set-AzureRmDataFactoryGateway.md)


