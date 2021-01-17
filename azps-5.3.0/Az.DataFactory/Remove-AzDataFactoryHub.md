---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 4C839730-B494-45BD-B5A1-F93B02AB4B2A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
ms.openlocfilehash: 12a18c62d3cc3412726df323bd48acd86ed7b1fd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477106"
---
# <span data-ttu-id="121f8-101">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="121f8-101">Remove-AzDataFactoryHub</span></span>

## <span data-ttu-id="121f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="121f8-102">SYNOPSIS</span></span>
<span data-ttu-id="121f8-103">Eltávolít egy központot az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="121f8-103">Removes a hub from Azure Data Factory.</span></span>

## <span data-ttu-id="121f8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="121f8-104">SYNTAX</span></span>

### <span data-ttu-id="121f8-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="121f8-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="121f8-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="121f8-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="121f8-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="121f8-107">DESCRIPTION</span></span>
<span data-ttu-id="121f8-108">A **Remove-AzDataFactoryHub** parancsmag eltávolít egy központot az Azure Data Factoryból a megadott Azure-erőforráscsoportban és a megadott adat factoryban.</span><span class="sxs-lookup"><span data-stu-id="121f8-108">The **Remove-AzDataFactoryHub** cmdlet removes a hub from Azure Data Factory in the specified Azure resource group and in the specified data factory.</span></span>
<span data-ttu-id="121f8-109">Ha eltávolít egy központot, a központ összes csatolt szolgáltatása és prognózisa is törlődik.</span><span class="sxs-lookup"><span data-stu-id="121f8-109">If you remove a hub, all linked services and pipelines in the hub are also removed.</span></span>

## <span data-ttu-id="121f8-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="121f8-110">EXAMPLES</span></span>

### <span data-ttu-id="121f8-111">1. példa: Központ eltávolítása</span><span class="sxs-lookup"><span data-stu-id="121f8-111">Example 1: Remove a hub</span></span>
```
PS C:\>Remove-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub"
```

<span data-ttu-id="121f8-112">Ez a parancs eltávolítja a ContosoDataHub nevű központot az ADFResourceGroup nevű Azure erőforráscsoportból és az ADFDataFactory nevű adatüzemből.</span><span class="sxs-lookup"><span data-stu-id="121f8-112">This command removes the hub named ContosoDataHub from the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="121f8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="121f8-113">PARAMETERS</span></span>

### <span data-ttu-id="121f8-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="121f8-114">-DataFactory</span></span>
<span data-ttu-id="121f8-115">EGY **PSDataFactory-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="121f8-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="121f8-116">Ez a parancsmag eltávolít egy központot a paraméter által megadott adatüzemelosztóból.</span><span class="sxs-lookup"><span data-stu-id="121f8-116">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="121f8-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="121f8-117">-DataFactoryName</span></span>
<span data-ttu-id="121f8-118">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="121f8-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="121f8-119">Ez a parancsmag eltávolít egy központot a paraméter által megadott adatüzemelosztóból.</span><span class="sxs-lookup"><span data-stu-id="121f8-119">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="121f8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="121f8-120">-DefaultProfile</span></span>
<span data-ttu-id="121f8-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="121f8-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="121f8-122">-Force</span><span class="sxs-lookup"><span data-stu-id="121f8-122">-Force</span></span>
<span data-ttu-id="121f8-123">Azt jelzi, hogy ez a parancsmag anélkül távolítja el a központot, hogy megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="121f8-123">Indicates that this cmdlet removes a hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="121f8-124">-Name</span><span class="sxs-lookup"><span data-stu-id="121f8-124">-Name</span></span>
<span data-ttu-id="121f8-125">Az eltávolítható központ nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="121f8-125">Specifies the name of the hub to remove.</span></span>

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

### <span data-ttu-id="121f8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="121f8-126">-ResourceGroupName</span></span>
<span data-ttu-id="121f8-127">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="121f8-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="121f8-128">Ez a parancsmag eltávolít egy központot a paraméter által megadott csoportból.</span><span class="sxs-lookup"><span data-stu-id="121f8-128">This cmdlet removes a hub from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="121f8-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="121f8-129">-Confirm</span></span>
<span data-ttu-id="121f8-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="121f8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="121f8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="121f8-131">-WhatIf</span></span>
<span data-ttu-id="121f8-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="121f8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="121f8-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="121f8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="121f8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="121f8-134">CommonParameters</span></span>
<span data-ttu-id="121f8-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="121f8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="121f8-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="121f8-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="121f8-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="121f8-137">INPUTS</span></span>

### <span data-ttu-id="121f8-138">System.String</span><span class="sxs-lookup"><span data-stu-id="121f8-138">System.String</span></span>

### <span data-ttu-id="121f8-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="121f8-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="121f8-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="121f8-140">OUTPUTS</span></span>

### <span data-ttu-id="121f8-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="121f8-141">System.Boolean</span></span>

## <span data-ttu-id="121f8-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="121f8-142">NOTES</span></span>
* <span data-ttu-id="121f8-143">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="121f8-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="121f8-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="121f8-144">RELATED LINKS</span></span>

[<span data-ttu-id="121f8-145">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="121f8-145">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="121f8-146">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="121f8-146">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)


