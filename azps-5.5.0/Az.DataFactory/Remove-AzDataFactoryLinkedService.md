---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 9425D38D-5978-421F-A438-4463068C4628
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
ms.openlocfilehash: a8731b075ff5df71aa368fa0c1a3c94ade9ef9e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148235"
---
# <span data-ttu-id="e4b09-101">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="e4b09-101">Remove-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="e4b09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4b09-102">SYNOPSIS</span></span>
<span data-ttu-id="e4b09-103">Eltávolít egy csatolt szolgáltatást az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="e4b09-103">Removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="e4b09-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e4b09-104">SYNTAX</span></span>

### <span data-ttu-id="e4b09-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e4b09-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e4b09-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e4b09-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4b09-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e4b09-107">DESCRIPTION</span></span>
<span data-ttu-id="e4b09-108">A **Remove-AzDataFactoryLinkedService** parancsmag eltávolít egy csatolt szolgáltatást az Azure Data Factoryból.</span><span class="sxs-lookup"><span data-stu-id="e4b09-108">The **Remove-AzDataFactoryLinkedService** cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="e4b09-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e4b09-109">EXAMPLES</span></span>

### <span data-ttu-id="e4b09-110">1. példa: Csatolt szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e4b09-110">Example 1: Remove a linked service</span></span>
```
PS C:\>Remove-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
Confirm
Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="e4b09-111">Ez a parancs eltávolítja a LinkedServiceTest nevű csatolt szolgáltatást a WikiADF nevű adatüzemből.</span><span class="sxs-lookup"><span data-stu-id="e4b09-111">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="e4b09-112">Ez a parancs egy számértéket ad $True.</span><span class="sxs-lookup"><span data-stu-id="e4b09-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="e4b09-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4b09-113">PARAMETERS</span></span>

### <span data-ttu-id="e4b09-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="e4b09-114">-DataFactory</span></span>
<span data-ttu-id="e4b09-115">EGY **PSDataFactory-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="e4b09-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="e4b09-116">Ez a parancsmag eltávolít egy csatolt szolgáltatást a paraméter által megadott adatüzemből.</span><span class="sxs-lookup"><span data-stu-id="e4b09-116">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e4b09-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e4b09-117">-DataFactoryName</span></span>
<span data-ttu-id="e4b09-118">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4b09-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="e4b09-119">Ez a parancsmag eltávolít egy csatolt szolgáltatást a paraméter által megadott adatüzemből.</span><span class="sxs-lookup"><span data-stu-id="e4b09-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e4b09-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4b09-120">-DefaultProfile</span></span>
<span data-ttu-id="e4b09-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e4b09-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4b09-122">-Force</span><span class="sxs-lookup"><span data-stu-id="e4b09-122">-Force</span></span>
<span data-ttu-id="e4b09-123">Azt jelzi, hogy ez a parancsmag a megerősítés kérése nélkül eltávolít egy csatolt szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="e4b09-123">Indicates that this cmdlet removes a linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="e4b09-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e4b09-124">-Name</span></span>
<span data-ttu-id="e4b09-125">Az eltávolítható csatolt szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="e4b09-125">Specifies the name of the linked service to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4b09-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4b09-126">-ResourceGroupName</span></span>
<span data-ttu-id="e4b09-127">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4b09-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e4b09-128">Ez a parancsmag eltávolít egy csatolt szolgáltatást a paraméter által megadott csoportból.</span><span class="sxs-lookup"><span data-stu-id="e4b09-128">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e4b09-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4b09-129">-Confirm</span></span>
<span data-ttu-id="e4b09-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e4b09-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4b09-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4b09-131">-WhatIf</span></span>
<span data-ttu-id="e4b09-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e4b09-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4b09-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e4b09-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4b09-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4b09-134">CommonParameters</span></span>
<span data-ttu-id="e4b09-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4b09-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4b09-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4b09-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4b09-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e4b09-137">INPUTS</span></span>

### <span data-ttu-id="e4b09-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e4b09-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="e4b09-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e4b09-139">System.String</span></span>

## <span data-ttu-id="e4b09-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4b09-140">OUTPUTS</span></span>

### <span data-ttu-id="e4b09-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="e4b09-141">System.Void</span></span>

## <span data-ttu-id="e4b09-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e4b09-142">NOTES</span></span>
* <span data-ttu-id="e4b09-143">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="e4b09-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e4b09-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4b09-144">RELATED LINKS</span></span>

[<span data-ttu-id="e4b09-145">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="e4b09-145">Get-AzDataFactoryLinkedService</span></span>](./Get-AzDataFactoryLinkedService.md)

[<span data-ttu-id="e4b09-146">New-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="e4b09-146">New-AzDataFactoryLinkedService</span></span>](./New-AzDataFactoryLinkedService.md)


