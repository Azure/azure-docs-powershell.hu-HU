---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B656B4C4-97DE-4F9F-937C-E115CB3F0E80
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
ms.openlocfilehash: 1155b7c0b294ac3bc5c2106b473ce1cf55a9ac82
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153491"
---
# <span data-ttu-id="969fe-101">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="969fe-101">New-AzDataFactoryHub</span></span>

## <span data-ttu-id="969fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="969fe-102">SYNOPSIS</span></span>
<span data-ttu-id="969fe-103">Létrehozza az Azure Data Factory központját.</span><span class="sxs-lookup"><span data-stu-id="969fe-103">Creates a hub for an Azure Data Factory.</span></span>

## <span data-ttu-id="969fe-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="969fe-104">SYNTAX</span></span>

### <span data-ttu-id="969fe-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="969fe-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="969fe-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="969fe-106">ByFactoryObject</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="969fe-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="969fe-107">DESCRIPTION</span></span>
<span data-ttu-id="969fe-108">A **New-AzDataFactoryHub** parancsmag létrehoz egy központot az Azure Data Factoryhoz a megadott Azure erőforráscsoportban és a megadott fájldefinícióval megadott adatüzemben.</span><span class="sxs-lookup"><span data-stu-id="969fe-108">The **New-AzDataFactoryHub** cmdlet creates a hub for Azure Data Factory in the specified Azure resource group and in the specified data factory with the specified file definition.</span></span>
<span data-ttu-id="969fe-109">Miután létrehozott egy központot, abban tárolhatja és kezelheti a csoportok csatolt szolgáltatásait, és folyamatokat adhat a központhoz.</span><span class="sxs-lookup"><span data-stu-id="969fe-109">After you create the hub, you can use it to store and manage linked services in a group, and you can add pipelines to the hub.</span></span>

## <span data-ttu-id="969fe-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="969fe-110">EXAMPLES</span></span>

### <span data-ttu-id="969fe-111">1. példa: Központ létrehozása</span><span class="sxs-lookup"><span data-stu-id="969fe-111">Example 1: Create a hub</span></span>
```
PS C:\>New-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub" -File "C:\Hub.json"
```

<span data-ttu-id="969fe-112">Ez a parancs létrehoz egy ContosoDataHub nevű központot az ADFResourceGroup erőforráscsoportban és az ADFDataFactory nevű adatüzemben.</span><span class="sxs-lookup"><span data-stu-id="969fe-112">This command creates a hub named ContosoDataHub in the resource group ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="969fe-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="969fe-113">PARAMETERS</span></span>

### <span data-ttu-id="969fe-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="969fe-114">-DataFactory</span></span>
<span data-ttu-id="969fe-115">EGY **PSDataFactory-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="969fe-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="969fe-116">Ez a parancsmag létrehoz egy központot a paraméter által megadott adatüzemelosztóhoz.</span><span class="sxs-lookup"><span data-stu-id="969fe-116">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="969fe-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="969fe-117">-DataFactoryName</span></span>
<span data-ttu-id="969fe-118">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="969fe-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="969fe-119">Ez a parancsmag létrehoz egy központot a paraméter által megadott adatüzemelosztóhoz.</span><span class="sxs-lookup"><span data-stu-id="969fe-119">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="969fe-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="969fe-120">-DefaultProfile</span></span>
<span data-ttu-id="969fe-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="969fe-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="969fe-122">-File</span><span class="sxs-lookup"><span data-stu-id="969fe-122">-File</span></span>
<span data-ttu-id="969fe-123">A központi objektum leírását tartalmazó JSON-fájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="969fe-123">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969fe-124">-Force</span><span class="sxs-lookup"><span data-stu-id="969fe-124">-Force</span></span>
<span data-ttu-id="969fe-125">Azt jelzi, hogy ez a parancsmag a megerősítés kérése nélkül lecserél egy meglévő központot.</span><span class="sxs-lookup"><span data-stu-id="969fe-125">Indicates that this cmdlet replaces an existing hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="969fe-126">-Name</span><span class="sxs-lookup"><span data-stu-id="969fe-126">-Name</span></span>
<span data-ttu-id="969fe-127">A létrehozni szükséges központ nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="969fe-127">Specifies the name of the hub to create.</span></span>

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

### <span data-ttu-id="969fe-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="969fe-128">-ResourceGroupName</span></span>
<span data-ttu-id="969fe-129">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="969fe-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="969fe-130">Ez a parancsmag létrehoz egy központot, amely a paraméter által megadott csoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="969fe-130">This cmdlet creates a hub that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="969fe-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="969fe-131">-Confirm</span></span>
<span data-ttu-id="969fe-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="969fe-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="969fe-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="969fe-133">-WhatIf</span></span>
<span data-ttu-id="969fe-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="969fe-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="969fe-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="969fe-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="969fe-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="969fe-136">CommonParameters</span></span>
<span data-ttu-id="969fe-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="969fe-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="969fe-138">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="969fe-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="969fe-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="969fe-139">INPUTS</span></span>

### <span data-ttu-id="969fe-140">System.String</span><span class="sxs-lookup"><span data-stu-id="969fe-140">System.String</span></span>

### <span data-ttu-id="969fe-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="969fe-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="969fe-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="969fe-142">OUTPUTS</span></span>

### <span data-ttu-id="969fe-143">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span><span class="sxs-lookup"><span data-stu-id="969fe-143">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="969fe-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="969fe-144">NOTES</span></span>
* <span data-ttu-id="969fe-145">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="969fe-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="969fe-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="969fe-146">RELATED LINKS</span></span>

[<span data-ttu-id="969fe-147">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="969fe-147">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="969fe-148">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="969fe-148">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)


