---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
ms.openlocfilehash: 57c0a05c5b0f279fa7c9f06cd561385de87698bf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183668"
---
# <span data-ttu-id="0a8e0-101">Update-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0a8e0-101">Update-AzDataFactoryV2</span></span>

## <span data-ttu-id="0a8e0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0a8e0-102">SYNOPSIS</span></span>
<span data-ttu-id="0a8e0-103">Frissíti az adattípusok tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="0a8e0-103">Updates the properties of a data factory.</span></span>

## <span data-ttu-id="0a8e0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0a8e0-104">SYNTAX</span></span>

### <span data-ttu-id="0a8e0-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0a8e0-105">ByFactoryName (Default)</span></span>
```
Update-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a8e0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0a8e0-106">ByFactoryObject</span></span>
```
Update-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a8e0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0a8e0-107">ByResourceId</span></span>
```
Update-AzDataFactoryV2 [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a8e0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0a8e0-108">DESCRIPTION</span></span>
<span data-ttu-id="0a8e0-109">Az **Update-AzDataFactoryV2** parancsmag frissíti az adatfeldolgozó címkéit vagy azonossági tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="0a8e0-109">The **Update-AzDataFactoryV2** cmdlet updates tags or identity properties of a data factory.</span></span>

## <span data-ttu-id="0a8e0-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0a8e0-110">EXAMPLES</span></span>

### <span data-ttu-id="0a8e0-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0a8e0-111">Example 1</span></span>
```
PS C:\> Update-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Tag @{myNewTagName = "myTagValue"}

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

<span data-ttu-id="0a8e0-112">Ez a parancs frissíti a gyári WikiADF a myNewTagName nevű címkét tartalmazó szótár címkéit a myTagValue értékkel.</span><span class="sxs-lookup"><span data-stu-id="0a8e0-112">This command updates the tags for the factory WikiADF to a dictionary containing a tag named myNewTagName with value myTagValue.</span></span>

## <span data-ttu-id="0a8e0-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0a8e0-113">PARAMETERS</span></span>

### <span data-ttu-id="0a8e0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a8e0-114">-DefaultProfile</span></span>
<span data-ttu-id="0a8e0-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0a8e0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a8e0-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a8e0-116">-InputObject</span></span>
<span data-ttu-id="0a8e0-117">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="0a8e0-117">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a8e0-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0a8e0-118">-Name</span></span>
<span data-ttu-id="0a8e0-119">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="0a8e0-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a8e0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a8e0-120">-ResourceGroupName</span></span>
<span data-ttu-id="0a8e0-121">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="0a8e0-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a8e0-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a8e0-122">-ResourceId</span></span>
<span data-ttu-id="0a8e0-123">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="0a8e0-123">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a8e0-124">-Címke</span><span class="sxs-lookup"><span data-stu-id="0a8e0-124">-Tag</span></span>
<span data-ttu-id="0a8e0-125">Az adatfeldolgozó címkéi.</span><span class="sxs-lookup"><span data-stu-id="0a8e0-125">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a8e0-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0a8e0-126">-Confirm</span></span>
<span data-ttu-id="0a8e0-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0a8e0-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a8e0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a8e0-128">-WhatIf</span></span>
<span data-ttu-id="0a8e0-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0a8e0-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a8e0-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0a8e0-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a8e0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a8e0-131">CommonParameters</span></span>
<span data-ttu-id="0a8e0-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0a8e0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a8e0-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a8e0-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a8e0-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a8e0-134">INPUTS</span></span>

### <span data-ttu-id="0a8e0-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0a8e0-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="0a8e0-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0a8e0-136">System.String</span></span>

## <span data-ttu-id="0a8e0-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a8e0-137">OUTPUTS</span></span>

### <span data-ttu-id="0a8e0-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0a8e0-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="0a8e0-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0a8e0-139">NOTES</span></span>

## <span data-ttu-id="0a8e0-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a8e0-140">RELATED LINKS</span></span>
