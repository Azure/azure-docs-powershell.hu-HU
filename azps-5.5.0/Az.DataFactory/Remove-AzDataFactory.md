---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 3D2E9FAE-FE34-457A-BE95-BC61D025B07A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactory.md
ms.openlocfilehash: 36c22a432d4e281600a1b718c1ac58a851fb7069
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148259"
---
# <span data-ttu-id="1e39f-101">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="1e39f-101">Remove-AzDataFactory</span></span>

## <span data-ttu-id="1e39f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e39f-102">SYNOPSIS</span></span>
<span data-ttu-id="1e39f-103">Adat factory eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="1e39f-103">Removes a data factory.</span></span>

## <span data-ttu-id="1e39f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1e39f-104">SYNTAX</span></span>

### <span data-ttu-id="1e39f-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1e39f-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactory [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e39f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1e39f-106">ByFactoryObject</span></span>
```
Remove-AzDataFactory [-DataFactory] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e39f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1e39f-107">DESCRIPTION</span></span>
<span data-ttu-id="1e39f-108">A **Remove-AzDataFactory** parancsmag eltávolít egy adatüzemet.</span><span class="sxs-lookup"><span data-stu-id="1e39f-108">The **Remove-AzDataFactory** cmdlet removes a data factory.</span></span>

## <span data-ttu-id="1e39f-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1e39f-109">EXAMPLES</span></span>

### <span data-ttu-id="1e39f-110">1. példa: Adat factory eltávolítása</span><span class="sxs-lookup"><span data-stu-id="1e39f-110">Example 1: Remove a data factory</span></span>
```
PS C:\>Remove-AzDataFactory -Name "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="1e39f-111">Ez a parancs eltávolítja a WikiADF nevű adatüzemet az ADF nevű erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="1e39f-111">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="1e39f-112">Ez a parancs egy számértéket ad $True.</span><span class="sxs-lookup"><span data-stu-id="1e39f-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="1e39f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e39f-113">PARAMETERS</span></span>

### <span data-ttu-id="1e39f-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1e39f-114">-DataFactory</span></span>
<span data-ttu-id="1e39f-115">Az eltávolítható **PSDataFactory-objektumot** adja meg.</span><span class="sxs-lookup"><span data-stu-id="1e39f-115">Specifies the **PSDataFactory** object to remove.</span></span>

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

### <span data-ttu-id="1e39f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e39f-116">-DefaultProfile</span></span>
<span data-ttu-id="1e39f-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1e39f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e39f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1e39f-118">-Force</span></span>
<span data-ttu-id="1e39f-119">Azt jelzi, hogy ez a parancsmag a megerősítés kérése nélkül eltávolítja az adatüzemet.</span><span class="sxs-lookup"><span data-stu-id="1e39f-119">Indicates that this cmdlet removes a data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="1e39f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1e39f-120">-Name</span></span>
<span data-ttu-id="1e39f-121">Az eltávolítható adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1e39f-121">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e39f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e39f-122">-ResourceGroupName</span></span>
<span data-ttu-id="1e39f-123">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1e39f-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1e39f-124">Ez a parancsmag eltávolít egy adat factoryt a paraméter által megadott csoportból.</span><span class="sxs-lookup"><span data-stu-id="1e39f-124">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1e39f-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e39f-125">-Confirm</span></span>
<span data-ttu-id="1e39f-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1e39f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e39f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e39f-127">-WhatIf</span></span>
<span data-ttu-id="1e39f-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1e39f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e39f-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1e39f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e39f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e39f-130">CommonParameters</span></span>
<span data-ttu-id="1e39f-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e39f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e39f-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e39f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e39f-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1e39f-133">INPUTS</span></span>

### <span data-ttu-id="1e39f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="1e39f-134">System.String</span></span>

### <span data-ttu-id="1e39f-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1e39f-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="1e39f-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e39f-136">OUTPUTS</span></span>

### <span data-ttu-id="1e39f-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="1e39f-137">System.Void</span></span>

## <span data-ttu-id="1e39f-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1e39f-138">NOTES</span></span>
* <span data-ttu-id="1e39f-139">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="1e39f-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1e39f-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e39f-140">RELATED LINKS</span></span>

[<span data-ttu-id="1e39f-141">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="1e39f-141">Get-AzDataFactory</span></span>](./Get-AzDataFactory.md)

[<span data-ttu-id="1e39f-142">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="1e39f-142">New-AzDataFactory</span></span>](./New-AzDataFactory.md)


