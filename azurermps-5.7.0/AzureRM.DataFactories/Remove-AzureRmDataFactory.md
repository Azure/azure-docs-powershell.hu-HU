---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 3D2E9FAE-FE34-457A-BE95-BC61D025B07A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactory.md
ms.openlocfilehash: 212e0c2ee4863c6d18873a717ff25f6940c34a15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494537"
---
# <span data-ttu-id="4adec-101">Remove-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="4adec-101">Remove-AzureRmDataFactory</span></span>

## <span data-ttu-id="4adec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4adec-102">SYNOPSIS</span></span>
<span data-ttu-id="4adec-103">Az adatfeldolgozó eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="4adec-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4adec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4adec-104">SYNTAX</span></span>

### <span data-ttu-id="4adec-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4adec-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactory [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4adec-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4adec-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactory [-DataFactory] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4adec-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4adec-107">DESCRIPTION</span></span>
<span data-ttu-id="4adec-108">A **Remove-AzureRmDataFactory** parancsmag eltávolítja az adatfeldolgozót.</span><span class="sxs-lookup"><span data-stu-id="4adec-108">The **Remove-AzureRmDataFactory** cmdlet removes a data factory.</span></span>

## <span data-ttu-id="4adec-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4adec-109">EXAMPLES</span></span>

### <span data-ttu-id="4adec-110">1. példa: az adatfeldolgozó eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4adec-110">Example 1: Remove a data factory</span></span>
```
PS C:\>Remove-AzureRmDataFactory -Name "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="4adec-111">Ez a parancs eltávolítja az WikiADF nevű adatfeldolgozót az ADF nevű erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="4adec-111">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="4adec-112">A parancs a $True értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="4adec-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="4adec-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4adec-113">PARAMETERS</span></span>

### <span data-ttu-id="4adec-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="4adec-114">-DataFactory</span></span>
<span data-ttu-id="4adec-115">Az eltávolítandó **PSDataFactory** -objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="4adec-115">Specifies the **PSDataFactory** object to remove.</span></span>

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

### <span data-ttu-id="4adec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4adec-116">-DefaultProfile</span></span>
<span data-ttu-id="4adec-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4adec-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4adec-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4adec-118">-Force</span></span>
<span data-ttu-id="4adec-119">Jelzi, hogy ez a parancsmag eltávolítja az adatfeldolgozót, ha nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4adec-119">Indicates that this cmdlet removes a data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="4adec-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4adec-120">-Name</span></span>
<span data-ttu-id="4adec-121">Az eltávolítandó adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4adec-121">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4adec-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4adec-122">-ResourceGroupName</span></span>
<span data-ttu-id="4adec-123">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4adec-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4adec-124">Ez a parancsmag eltávolítja az adatfeldolgozót abban a csoportban, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="4adec-124">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4adec-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4adec-125">-Confirm</span></span>
<span data-ttu-id="4adec-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4adec-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4adec-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4adec-127">-WhatIf</span></span>
<span data-ttu-id="4adec-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4adec-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4adec-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4adec-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4adec-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4adec-130">CommonParameters</span></span>
<span data-ttu-id="4adec-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4adec-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4adec-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4adec-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4adec-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4adec-133">INPUTS</span></span>

### <span data-ttu-id="4adec-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="4adec-134">None</span></span>
<span data-ttu-id="4adec-135">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="4adec-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4adec-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4adec-136">OUTPUTS</span></span>

### <span data-ttu-id="4adec-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4adec-137">System.Boolean</span></span>

## <span data-ttu-id="4adec-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4adec-138">NOTES</span></span>
* <span data-ttu-id="4adec-139">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="4adec-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4adec-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4adec-140">RELATED LINKS</span></span>

[<span data-ttu-id="4adec-141">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="4adec-141">Get-AzureRmDataFactory</span></span>](./Get-AzureRmDataFactory.md)

[<span data-ttu-id="4adec-142">Új – AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="4adec-142">New-AzureRmDataFactory</span></span>](./New-AzureRmDataFactory.md)


