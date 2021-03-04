---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1461540-DEAE-43C3-83DF-7DF3FE8D4EC0
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
ms.openlocfilehash: eb9100bf4843d7213d2fbb89ac1827ba7ee1e509
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921313"
---
# <span data-ttu-id="d3771-101">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="d3771-101">Remove-AzDataFactoryGateway</span></span>

## <span data-ttu-id="d3771-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3771-102">SYNOPSIS</span></span>
<span data-ttu-id="d3771-103">Eltávolít egy átjárót az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="d3771-103">Removes a gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="d3771-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d3771-104">SYNTAX</span></span>

### <span data-ttu-id="d3771-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d3771-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3771-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d3771-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3771-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d3771-107">DESCRIPTION</span></span>
<span data-ttu-id="d3771-108">A **Remove-AzDataFactoryGateway** parancsmag eltávolítja a megadott átjárót az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="d3771-108">The **Remove-AzDataFactoryGateway** cmdlet removes the specified gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="d3771-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d3771-109">EXAMPLES</span></span>

### <span data-ttu-id="d3771-110">1. példa: Átjáró eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d3771-110">Example 1: Remove a gateway</span></span>
```
PS C:\>Remove-AzDataFactoryGateway -Name "ContosoGateway" -DataFactoryName "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove gateway 'ContosoGateway' in data factory 'WikiADF'? 
 [Y] Yes  [N] No  [S] Suspend  [?] Help (default is Y): Y
True
```

<span data-ttu-id="d3771-111">Ez a parancs eltávolítja a ContosoGateway nevű átjárót a WikiADF nevű adatüzemből.</span><span class="sxs-lookup"><span data-stu-id="d3771-111">This command removes the gateway named ContosoGateway from the data factory named WikiADF.</span></span>

## <span data-ttu-id="d3771-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3771-112">PARAMETERS</span></span>

### <span data-ttu-id="d3771-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d3771-113">-DataFactory</span></span>
<span data-ttu-id="d3771-114">EGY **PSDataFactory-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="d3771-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="d3771-115">Ez a parancsmag eltávolít egy átjárót a paraméter által megadott adatüzemből.</span><span class="sxs-lookup"><span data-stu-id="d3771-115">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d3771-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d3771-116">-DataFactoryName</span></span>
<span data-ttu-id="d3771-117">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d3771-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d3771-118">Ez a parancsmag eltávolít egy átjárót a paraméter által megadott adatüzemből.</span><span class="sxs-lookup"><span data-stu-id="d3771-118">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d3771-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3771-119">-DefaultProfile</span></span>
<span data-ttu-id="d3771-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d3771-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3771-121">-Force</span><span class="sxs-lookup"><span data-stu-id="d3771-121">-Force</span></span>
<span data-ttu-id="d3771-122">Azt jelzi, hogy ez a parancsmag anélkül távolítja el az átjárót, hogy megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d3771-122">Indicates that this cmdlet removes a gateway without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="d3771-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d3771-123">-Name</span></span>
<span data-ttu-id="d3771-124">Az eltávolítható átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="d3771-124">Specifies the name of the gateway to remove.</span></span>

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

### <span data-ttu-id="d3771-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3771-125">-ResourceGroupName</span></span>
<span data-ttu-id="d3771-126">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d3771-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d3771-127">Ez a parancsmag eltávolít egy átjárót, amely a paraméter által megadott csoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="d3771-127">This cmdlet removes a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d3771-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3771-128">-Confirm</span></span>
<span data-ttu-id="d3771-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d3771-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3771-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3771-130">-WhatIf</span></span>
<span data-ttu-id="d3771-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d3771-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3771-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d3771-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3771-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3771-133">CommonParameters</span></span>
<span data-ttu-id="d3771-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3771-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3771-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3771-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3771-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3771-136">INPUTS</span></span>

### <span data-ttu-id="d3771-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d3771-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="d3771-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d3771-138">System.String</span></span>

## <span data-ttu-id="d3771-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3771-139">OUTPUTS</span></span>

### <span data-ttu-id="d3771-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d3771-140">System.Boolean</span></span>

## <span data-ttu-id="d3771-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d3771-141">NOTES</span></span>
* <span data-ttu-id="d3771-142">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="d3771-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d3771-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3771-143">RELATED LINKS</span></span>

[<span data-ttu-id="d3771-144">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="d3771-144">Get-AzDataFactoryGateway</span></span>](./Get-AzDataFactoryGateway.md)

[<span data-ttu-id="d3771-145">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="d3771-145">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="d3771-146">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="d3771-146">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


