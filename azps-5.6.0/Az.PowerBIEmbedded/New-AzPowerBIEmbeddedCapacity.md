---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/new-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 86531beb13ef70f8c35de7f4921277b0f9fa0bf2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919345"
---
# <span data-ttu-id="883af-101">New-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="883af-101">New-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="883af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="883af-102">SYNOPSIS</span></span>
<span data-ttu-id="883af-103">Új beágyazott PowerBI-kapacitást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="883af-103">Creates a new PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="883af-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="883af-104">SYNTAX</span></span>

```
New-AzPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [-Administrator] <String[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="883af-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="883af-105">DESCRIPTION</span></span>
<span data-ttu-id="883af-106">A New-AzPowerBIEmbeddedCapacity parancsmag létrehoz egy új Beágyazott PowerBI-kapacitást</span><span class="sxs-lookup"><span data-stu-id="883af-106">The New-AzPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="883af-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="883af-107">EXAMPLES</span></span>

### <span data-ttu-id="883af-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="883af-108">Example 1</span></span>
```
PS C:\> New-AzPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity" -Location "West Central US" -Sku "A1" -Administrator admin@microsoft.com
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="883af-109">Létrehoz egy tesztkapacitás nevű kapacitást az Azure régió nyugati részén, az Egyesült Államok nyugati részén és az erőforráscsoport tesztRG-ében.</span><span class="sxs-lookup"><span data-stu-id="883af-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="883af-110">A kapacitás termékváltozatának szintje A1 lesz.</span><span class="sxs-lookup"><span data-stu-id="883af-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="883af-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="883af-111">PARAMETERS</span></span>

### <span data-ttu-id="883af-112">- Rendszergazda</span><span class="sxs-lookup"><span data-stu-id="883af-112">-Administrator</span></span>
<span data-ttu-id="883af-113">Vesszővel elválasztott nevek beállítása rendszergazdaként a kapacitáson</span><span class="sxs-lookup"><span data-stu-id="883af-113">A comma separated names to set as administrator on the capacity</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="883af-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="883af-114">-DefaultProfile</span></span>
<span data-ttu-id="883af-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="883af-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="883af-116">-Location</span><span class="sxs-lookup"><span data-stu-id="883af-116">-Location</span></span>
<span data-ttu-id="883af-117">Az Azure-régió, ahol a PowerBI beágyazott kapacitást üzemeltet</span><span class="sxs-lookup"><span data-stu-id="883af-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

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

### <span data-ttu-id="883af-118">-Name</span><span class="sxs-lookup"><span data-stu-id="883af-118">-Name</span></span>
<span data-ttu-id="883af-119">A Beágyazott PowerBI-kapacitás neve</span><span class="sxs-lookup"><span data-stu-id="883af-119">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="883af-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="883af-120">-ResourceGroupName</span></span>
<span data-ttu-id="883af-121">Annak az Azure-erőforráscsoportnak a neve, amelyhez a kapacitás tartozik</span><span class="sxs-lookup"><span data-stu-id="883af-121">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="883af-122">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="883af-122">-Sku</span></span>
<span data-ttu-id="883af-123">A kapacitás termékváltozatának neve.</span><span class="sxs-lookup"><span data-stu-id="883af-123">The name of the Sku for the capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: A1, A2, A3, A4, A5, A6

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="883af-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="883af-124">-Tag</span></span>
<span data-ttu-id="883af-125">Kulcsérték-párok a kapacitás címkéiként beállított kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="883af-125">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="883af-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="883af-126">-Confirm</span></span>
<span data-ttu-id="883af-127">Arra kéri a felhasználót, hogy erősítse meg a művelet elvégzését</span><span class="sxs-lookup"><span data-stu-id="883af-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="883af-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="883af-128">-WhatIf</span></span>
<span data-ttu-id="883af-129">Az aktuális művelet által ténylegesen végrehajtott műveleteket ismerteti anélkül, hogy végrehajtaná őket.</span><span class="sxs-lookup"><span data-stu-id="883af-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="883af-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="883af-130">CommonParameters</span></span>
<span data-ttu-id="883af-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="883af-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="883af-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="883af-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="883af-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="883af-133">INPUTS</span></span>

### <span data-ttu-id="883af-134">System.String</span><span class="sxs-lookup"><span data-stu-id="883af-134">System.String</span></span>

### <span data-ttu-id="883af-135">System.String[]</span><span class="sxs-lookup"><span data-stu-id="883af-135">System.String[]</span></span>

### <span data-ttu-id="883af-136">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="883af-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="883af-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="883af-137">OUTPUTS</span></span>

### <span data-ttu-id="883af-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="883af-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="883af-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="883af-139">NOTES</span></span>

## <span data-ttu-id="883af-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="883af-140">RELATED LINKS</span></span>

[<span data-ttu-id="883af-141">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="883af-141">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="883af-142">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="883af-142">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
