---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/update-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2.md
ms.openlocfilehash: d7173b75d9796eeab974973f9f997d5b7cb72b49
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672868"
---
# <span data-ttu-id="02e5e-101">Update-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="02e5e-101">Update-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="02e5e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="02e5e-102">SYNOPSIS</span></span>
<span data-ttu-id="02e5e-103">Frissíti az adattípusok tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="02e5e-103">Updates the properties of a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02e5e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="02e5e-104">SYNTAX</span></span>

### <span data-ttu-id="02e5e-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="02e5e-105">ByFactoryName (Default)</span></span>
```
Update-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02e5e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="02e5e-106">ByFactoryObject</span></span>
```
Update-AzureRmDataFactoryV2 [-InputObject] <PSDataFactory> [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02e5e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="02e5e-107">ByResourceId</span></span>
```
Update-AzureRmDataFactoryV2 [-ResourceId] <String> [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02e5e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="02e5e-108">DESCRIPTION</span></span>
<span data-ttu-id="02e5e-109">Az **Update-AzureRmDataFactoryV2** parancsmag frissíti az adatfeldolgozó címkéit vagy azonossági tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="02e5e-109">The **Update-AzureRmDataFactoryV2** cmdlet updates tags or identity properties of a data factory.</span></span>

## <span data-ttu-id="02e5e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="02e5e-110">EXAMPLES</span></span>

### <span data-ttu-id="02e5e-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="02e5e-111">Example 1</span></span>
```
PS C:\> Update-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Tag @{myNewTagName = "myTagValue"}

Confirm
Are you sure you want to update properties of the data factory 'WikiADF' in resource group 'ADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y


DataFactoryName   : WikiADF
DataFactoryId     : /subscriptions/1e42591f-1f0c-4c5a-b7f2-a268f6105ec5/resourceGroups/adf/providers/Microsoft.DataF
                    actory/factories/wikiadf
ResourceGroupName : ADF
Location          : EastUS
Tags              : {[myNewTagName, myTagValue]}
Identity          :
ProvisioningState : Succeeded
```

<span data-ttu-id="02e5e-112">Ez a parancs frissíti a gyári WikiADF a myNewTagName nevű címkét tartalmazó szótár címkéit a myTagValue értékkel.</span><span class="sxs-lookup"><span data-stu-id="02e5e-112">This command updates the tags for the factory WikiADF to a dictionary containing a tag named myNewTagName with value myTagValue.</span></span>

## <span data-ttu-id="02e5e-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="02e5e-113">PARAMETERS</span></span>

### <span data-ttu-id="02e5e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02e5e-114">-DefaultProfile</span></span>
<span data-ttu-id="02e5e-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="02e5e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02e5e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02e5e-116">-InputObject</span></span>
<span data-ttu-id="02e5e-117">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="02e5e-117">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02e5e-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="02e5e-118">-Name</span></span>
<span data-ttu-id="02e5e-119">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="02e5e-119">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02e5e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02e5e-120">-ResourceGroupName</span></span>
<span data-ttu-id="02e5e-121">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="02e5e-121">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02e5e-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02e5e-122">-ResourceId</span></span>
<span data-ttu-id="02e5e-123">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="02e5e-123">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02e5e-124">-Címke</span><span class="sxs-lookup"><span data-stu-id="02e5e-124">-Tag</span></span>
<span data-ttu-id="02e5e-125">Az adatfeldolgozó címkéi.</span><span class="sxs-lookup"><span data-stu-id="02e5e-125">The tags of the data factory.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02e5e-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="02e5e-126">-Confirm</span></span>
<span data-ttu-id="02e5e-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="02e5e-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02e5e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02e5e-128">-WhatIf</span></span>
<span data-ttu-id="02e5e-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="02e5e-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="02e5e-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="02e5e-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02e5e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02e5e-131">CommonParameters</span></span>
<span data-ttu-id="02e5e-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="02e5e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02e5e-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02e5e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02e5e-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="02e5e-134">INPUTS</span></span>

### <span data-ttu-id="02e5e-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="02e5e-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="02e5e-136">System. String Microsoft. Azure. Management. DataFactory. models. FactoryIdentity</span><span class="sxs-lookup"><span data-stu-id="02e5e-136">System.String Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity</span></span>

## <span data-ttu-id="02e5e-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02e5e-137">OUTPUTS</span></span>

### <span data-ttu-id="02e5e-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="02e5e-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="02e5e-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="02e5e-139">NOTES</span></span>

## <span data-ttu-id="02e5e-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02e5e-140">RELATED LINKS</span></span>

