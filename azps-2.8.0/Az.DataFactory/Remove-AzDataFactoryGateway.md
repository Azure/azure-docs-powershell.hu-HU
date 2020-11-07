---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1461540-DEAE-43C3-83DF-7DF3FE8D4EC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
ms.openlocfilehash: 0f8bd59f6215a2f9cc2bdbcc993da0cb373f70af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667007"
---
# <span data-ttu-id="33259-101">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="33259-101">Remove-AzDataFactoryGateway</span></span>

## <span data-ttu-id="33259-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="33259-102">SYNOPSIS</span></span>
<span data-ttu-id="33259-103">Átjáró eltávolítása az Azure Data Factory programból.</span><span class="sxs-lookup"><span data-stu-id="33259-103">Removes a gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="33259-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="33259-104">SYNTAX</span></span>

### <span data-ttu-id="33259-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="33259-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33259-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="33259-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33259-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="33259-107">DESCRIPTION</span></span>
<span data-ttu-id="33259-108">A **Remove-AzDataFactoryGateway** parancsmag eltávolítja a megadott átjárót az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="33259-108">The **Remove-AzDataFactoryGateway** cmdlet removes the specified gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="33259-109">Példák</span><span class="sxs-lookup"><span data-stu-id="33259-109">EXAMPLES</span></span>

### <span data-ttu-id="33259-110">1. példa: átjáró eltávolítása</span><span class="sxs-lookup"><span data-stu-id="33259-110">Example 1: Remove a gateway</span></span>
```
PS C:\>Remove-AzDataFactoryGateway -Name "ContosoGateway" -DataFactoryName "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove gateway 'ContosoGateway' in data factory 'WikiADF'? 
 [Y] Yes  [N] No  [S] Suspend  [?] Help (default is Y): Y
True
```

<span data-ttu-id="33259-111">Ez a parancs eltávolítja a ContosoGateway nevű átjárót a WikiADF nevű adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="33259-111">This command removes the gateway named ContosoGateway from the data factory named WikiADF.</span></span>

## <span data-ttu-id="33259-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="33259-112">PARAMETERS</span></span>

### <span data-ttu-id="33259-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="33259-113">-DataFactory</span></span>
<span data-ttu-id="33259-114">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="33259-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="33259-115">Ez a parancsmag eltávolítja az adatgyárból az átjárót, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="33259-115">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="33259-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="33259-116">-DataFactoryName</span></span>
<span data-ttu-id="33259-117">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="33259-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="33259-118">Ez a parancsmag eltávolítja az adatgyárból az átjárót, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="33259-118">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="33259-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33259-119">-DefaultProfile</span></span>
<span data-ttu-id="33259-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="33259-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33259-121">-Force</span><span class="sxs-lookup"><span data-stu-id="33259-121">-Force</span></span>
<span data-ttu-id="33259-122">Jelzi, hogy ez a parancsmag eltávolítja az átjárót anélkül, hogy megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="33259-122">Indicates that this cmdlet removes a gateway without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="33259-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="33259-123">-Name</span></span>
<span data-ttu-id="33259-124">Az eltávolítandó átjáró nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="33259-124">Specifies the name of the gateway to remove.</span></span>

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

### <span data-ttu-id="33259-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33259-125">-ResourceGroupName</span></span>
<span data-ttu-id="33259-126">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="33259-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="33259-127">Ez a parancsmag eltávolítja azt az átjárót, amely a paraméter által megadott csoportba tartozik.</span><span class="sxs-lookup"><span data-stu-id="33259-127">This cmdlet removes a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="33259-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="33259-128">-Confirm</span></span>
<span data-ttu-id="33259-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="33259-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33259-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33259-130">-WhatIf</span></span>
<span data-ttu-id="33259-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="33259-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33259-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="33259-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33259-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33259-133">CommonParameters</span></span>
<span data-ttu-id="33259-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="33259-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33259-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33259-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33259-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="33259-136">INPUTS</span></span>

### <span data-ttu-id="33259-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="33259-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="33259-138">System. String</span><span class="sxs-lookup"><span data-stu-id="33259-138">System.String</span></span>

## <span data-ttu-id="33259-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="33259-139">OUTPUTS</span></span>

### <span data-ttu-id="33259-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="33259-140">System.Boolean</span></span>

## <span data-ttu-id="33259-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="33259-141">NOTES</span></span>
* <span data-ttu-id="33259-142">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="33259-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="33259-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="33259-143">RELATED LINKS</span></span>

[<span data-ttu-id="33259-144">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="33259-144">Get-AzDataFactoryGateway</span></span>](./Get-AzDataFactoryGateway.md)

[<span data-ttu-id="33259-145">Új – AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="33259-145">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="33259-146">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="33259-146">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


