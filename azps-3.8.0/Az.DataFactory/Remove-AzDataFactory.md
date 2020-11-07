---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 3D2E9FAE-FE34-457A-BE95-BC61D025B07A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactory.md
ms.openlocfilehash: 36c22a432d4e281600a1b718c1ac58a851fb7069
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847197"
---
# <span data-ttu-id="54919-101">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="54919-101">Remove-AzDataFactory</span></span>

## <span data-ttu-id="54919-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="54919-102">SYNOPSIS</span></span>
<span data-ttu-id="54919-103">Az adatfeldolgozó eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="54919-103">Removes a data factory.</span></span>

## <span data-ttu-id="54919-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="54919-104">SYNTAX</span></span>

### <span data-ttu-id="54919-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="54919-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactory [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54919-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="54919-106">ByFactoryObject</span></span>
```
Remove-AzDataFactory [-DataFactory] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54919-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="54919-107">DESCRIPTION</span></span>
<span data-ttu-id="54919-108">A **Remove-AzDataFactory** parancsmag eltávolítja az adatfeldolgozót.</span><span class="sxs-lookup"><span data-stu-id="54919-108">The **Remove-AzDataFactory** cmdlet removes a data factory.</span></span>

## <span data-ttu-id="54919-109">Példák</span><span class="sxs-lookup"><span data-stu-id="54919-109">EXAMPLES</span></span>

### <span data-ttu-id="54919-110">1. példa: az adatfeldolgozó eltávolítása</span><span class="sxs-lookup"><span data-stu-id="54919-110">Example 1: Remove a data factory</span></span>
```
PS C:\>Remove-AzDataFactory -Name "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="54919-111">Ez a parancs eltávolítja az WikiADF nevű adatfeldolgozót az ADF nevű erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="54919-111">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="54919-112">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="54919-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="54919-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="54919-113">PARAMETERS</span></span>

### <span data-ttu-id="54919-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="54919-114">-DataFactory</span></span>
<span data-ttu-id="54919-115">Az eltávolítandó **PSDataFactory** -objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="54919-115">Specifies the **PSDataFactory** object to remove.</span></span>

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

### <span data-ttu-id="54919-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54919-116">-DefaultProfile</span></span>
<span data-ttu-id="54919-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="54919-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54919-118">-Force</span><span class="sxs-lookup"><span data-stu-id="54919-118">-Force</span></span>
<span data-ttu-id="54919-119">Jelzi, hogy ez a parancsmag eltávolítja az adatfeldolgozót, ha nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="54919-119">Indicates that this cmdlet removes a data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="54919-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="54919-120">-Name</span></span>
<span data-ttu-id="54919-121">Az eltávolítandó adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="54919-121">Specifies the name of the data factory to remove.</span></span>

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

### <span data-ttu-id="54919-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54919-122">-ResourceGroupName</span></span>
<span data-ttu-id="54919-123">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="54919-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="54919-124">Ez a parancsmag eltávolítja az adatfeldolgozót abban a csoportban, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="54919-124">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="54919-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="54919-125">-Confirm</span></span>
<span data-ttu-id="54919-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="54919-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54919-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54919-127">-WhatIf</span></span>
<span data-ttu-id="54919-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="54919-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54919-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="54919-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54919-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54919-130">CommonParameters</span></span>
<span data-ttu-id="54919-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="54919-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54919-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54919-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54919-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="54919-133">INPUTS</span></span>

### <span data-ttu-id="54919-134">System. String</span><span class="sxs-lookup"><span data-stu-id="54919-134">System.String</span></span>

### <span data-ttu-id="54919-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="54919-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="54919-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="54919-136">OUTPUTS</span></span>

### <span data-ttu-id="54919-137">System. Void</span><span class="sxs-lookup"><span data-stu-id="54919-137">System.Void</span></span>

## <span data-ttu-id="54919-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="54919-138">NOTES</span></span>
* <span data-ttu-id="54919-139">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="54919-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="54919-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="54919-140">RELATED LINKS</span></span>

[<span data-ttu-id="54919-141">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="54919-141">Get-AzDataFactory</span></span>](./Get-AzDataFactory.md)

[<span data-ttu-id="54919-142">Új – AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="54919-142">New-AzDataFactory</span></span>](./New-AzDataFactory.md)

