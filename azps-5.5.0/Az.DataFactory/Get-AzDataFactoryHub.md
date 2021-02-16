---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
ms.openlocfilehash: 292a288850371a834f938143cf2ec4380504091b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166122"
---
# <span data-ttu-id="cccd6-101">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="cccd6-101">Get-AzDataFactoryHub</span></span>

## <span data-ttu-id="cccd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cccd6-102">SYNOPSIS</span></span>
<span data-ttu-id="cccd6-103">Információkat kap az Azure Data Factoryban található központokkal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="cccd6-103">Gets information about hubs in Azure Data Factory.</span></span>

## <span data-ttu-id="cccd6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cccd6-104">SYNTAX</span></span>

### <span data-ttu-id="cccd6-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cccd6-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cccd6-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="cccd6-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cccd6-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cccd6-107">DESCRIPTION</span></span>
<span data-ttu-id="cccd6-108">A **Get-AzDataFactoryHub** parancsmag információkat kap az Azure Data Factoryban található központokkal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="cccd6-108">The **Get-AzDataFactoryHub** cmdlet gets information about hubs in Azure Data Factory.</span></span>
<span data-ttu-id="cccd6-109">Ha megadja egy központ nevét, ez a parancsmag információt kap erről a központról.</span><span class="sxs-lookup"><span data-stu-id="cccd6-109">If you specify the name of a hub, this cmdlet gets information about that hub.</span></span>
<span data-ttu-id="cccd6-110">Ha nem ad meg nevet, ez a parancsmag információt kap egy adatüzemelosztó központról.</span><span class="sxs-lookup"><span data-stu-id="cccd6-110">If you do not specify a name, this cmdlet gets information about all of the hubs in a data factory.</span></span>

## <span data-ttu-id="cccd6-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cccd6-111">EXAMPLES</span></span>

### <span data-ttu-id="cccd6-112">1. példa: Az összes adatközpont lekérte</span><span class="sxs-lookup"><span data-stu-id="cccd6-112">Example 1: Get all data hubs</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

<span data-ttu-id="cccd6-113">Ez a parancs az ADFResourceGroup nevű Azure-erőforráscsoport és az ADFDataFactory nevű adatüzem összes adatközpontját begyűjte.</span><span class="sxs-lookup"><span data-stu-id="cccd6-113">This command gets all data hubs in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

### <span data-ttu-id="cccd6-114">2. példa: Adott adatközpont lekérte</span><span class="sxs-lookup"><span data-stu-id="cccd6-114">Example 2: Get a specific data hub</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

<span data-ttu-id="cccd6-115">Ez a parancs információkat kap a MyDataHub nevű központról az ADFResourceGroup nevű Azure erőforráscsoportban és az ADFDataFactory nevű adatüzemben.</span><span class="sxs-lookup"><span data-stu-id="cccd6-115">This command gets information about the hub named MyDataHub in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="cccd6-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cccd6-116">PARAMETERS</span></span>

### <span data-ttu-id="cccd6-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="cccd6-117">-DataFactory</span></span>
<span data-ttu-id="cccd6-118">EGY **PSDataFactory-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="cccd6-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="cccd6-119">Ez a parancsmag információt kap a paraméter által megadott adatközpontokkal kapcsolatban az adat factoryban.</span><span class="sxs-lookup"><span data-stu-id="cccd6-119">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="cccd6-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="cccd6-120">-DataFactoryName</span></span>
<span data-ttu-id="cccd6-121">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cccd6-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="cccd6-122">Ez a parancsmag információt kap a paraméter által megadott adatközpontokkal kapcsolatban az adat factoryban.</span><span class="sxs-lookup"><span data-stu-id="cccd6-122">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="cccd6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cccd6-123">-DefaultProfile</span></span>
<span data-ttu-id="cccd6-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cccd6-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cccd6-125">-Name</span><span class="sxs-lookup"><span data-stu-id="cccd6-125">-Name</span></span>
<span data-ttu-id="cccd6-126">Annak a központnak a nevét adja meg, amelyről információt kell kapni.</span><span class="sxs-lookup"><span data-stu-id="cccd6-126">Specifies the name of the hub about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cccd6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cccd6-127">-ResourceGroupName</span></span>
<span data-ttu-id="cccd6-128">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cccd6-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="cccd6-129">Ez a parancsmag információt kap a paraméter által megadott csoporthoz tartozó központokról.</span><span class="sxs-lookup"><span data-stu-id="cccd6-129">This cmdlet gets information about hubs that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="cccd6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cccd6-130">CommonParameters</span></span>
<span data-ttu-id="cccd6-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cccd6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cccd6-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cccd6-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cccd6-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cccd6-133">INPUTS</span></span>

### <span data-ttu-id="cccd6-134">System.String</span><span class="sxs-lookup"><span data-stu-id="cccd6-134">System.String</span></span>

### <span data-ttu-id="cccd6-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="cccd6-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="cccd6-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cccd6-136">OUTPUTS</span></span>

### <span data-ttu-id="cccd6-137">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span><span class="sxs-lookup"><span data-stu-id="cccd6-137">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="cccd6-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cccd6-138">NOTES</span></span>
* <span data-ttu-id="cccd6-139">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="cccd6-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="cccd6-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cccd6-140">RELATED LINKS</span></span>

[<span data-ttu-id="cccd6-141">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="cccd6-141">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)

[<span data-ttu-id="cccd6-142">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="cccd6-142">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)


