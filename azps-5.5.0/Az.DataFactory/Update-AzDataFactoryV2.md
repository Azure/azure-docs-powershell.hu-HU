---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
ms.openlocfilehash: 57c0a05c5b0f279fa7c9f06cd561385de87698bf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153458"
---
# <span data-ttu-id="1fcf9-101">Update-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1fcf9-101">Update-AzDataFactoryV2</span></span>

## <span data-ttu-id="1fcf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fcf9-102">SYNOPSIS</span></span>
<span data-ttu-id="1fcf9-103">Frissíti egy adatüzem tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="1fcf9-103">Updates the properties of a data factory.</span></span>

## <span data-ttu-id="1fcf9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1fcf9-104">SYNTAX</span></span>

### <span data-ttu-id="1fcf9-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1fcf9-105">ByFactoryName (Default)</span></span>
```
Update-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fcf9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1fcf9-106">ByFactoryObject</span></span>
```
Update-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fcf9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1fcf9-107">ByResourceId</span></span>
```
Update-AzDataFactoryV2 [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fcf9-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1fcf9-108">DESCRIPTION</span></span>
<span data-ttu-id="1fcf9-109">Az **Update-AzDataFactoryV2** parancsmag frissíti egy adatüzem címkéit vagy identitástulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="1fcf9-109">The **Update-AzDataFactoryV2** cmdlet updates tags or identity properties of a data factory.</span></span>

## <span data-ttu-id="1fcf9-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1fcf9-110">EXAMPLES</span></span>

### <span data-ttu-id="1fcf9-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="1fcf9-111">Example 1</span></span>
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

<span data-ttu-id="1fcf9-112">Ez a parancs frissíti a gyári WikiADF címkéit egy olyan szótárra, amely tartalmaz egy MyNewTagName nevű címkét myTagValue értékkel.</span><span class="sxs-lookup"><span data-stu-id="1fcf9-112">This command updates the tags for the factory WikiADF to a dictionary containing a tag named myNewTagName with value myTagValue.</span></span>

## <span data-ttu-id="1fcf9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1fcf9-113">PARAMETERS</span></span>

### <span data-ttu-id="1fcf9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fcf9-114">-DefaultProfile</span></span>
<span data-ttu-id="1fcf9-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1fcf9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fcf9-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1fcf9-116">-InputObject</span></span>
<span data-ttu-id="1fcf9-117">A data factory objektum.</span><span class="sxs-lookup"><span data-stu-id="1fcf9-117">The data factory object.</span></span>

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

### <span data-ttu-id="1fcf9-118">-Name</span><span class="sxs-lookup"><span data-stu-id="1fcf9-118">-Name</span></span>
<span data-ttu-id="1fcf9-119">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="1fcf9-119">The data factory name.</span></span>

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

### <span data-ttu-id="1fcf9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fcf9-120">-ResourceGroupName</span></span>
<span data-ttu-id="1fcf9-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1fcf9-121">The resource group name.</span></span>

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

### <span data-ttu-id="1fcf9-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1fcf9-122">-ResourceId</span></span>
<span data-ttu-id="1fcf9-123">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="1fcf9-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="1fcf9-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="1fcf9-124">-Tag</span></span>
<span data-ttu-id="1fcf9-125">Az adatüzem címkéi.</span><span class="sxs-lookup"><span data-stu-id="1fcf9-125">The tags of the data factory.</span></span>

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

### <span data-ttu-id="1fcf9-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1fcf9-126">-Confirm</span></span>
<span data-ttu-id="1fcf9-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1fcf9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fcf9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fcf9-128">-WhatIf</span></span>
<span data-ttu-id="1fcf9-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1fcf9-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1fcf9-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1fcf9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fcf9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fcf9-131">CommonParameters</span></span>
<span data-ttu-id="1fcf9-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fcf9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fcf9-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fcf9-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fcf9-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1fcf9-134">INPUTS</span></span>

### <span data-ttu-id="1fcf9-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1fcf9-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="1fcf9-136">System.String</span><span class="sxs-lookup"><span data-stu-id="1fcf9-136">System.String</span></span>

## <span data-ttu-id="1fcf9-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1fcf9-137">OUTPUTS</span></span>

### <span data-ttu-id="1fcf9-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1fcf9-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="1fcf9-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1fcf9-139">NOTES</span></span>

## <span data-ttu-id="1fcf9-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1fcf9-140">RELATED LINKS</span></span>
