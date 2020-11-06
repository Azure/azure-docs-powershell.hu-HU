---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/new-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 8546dbfbe8da12cd61c8b03d8aca64772d032b60
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495799"
---
# <span data-ttu-id="0329f-101">New-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="0329f-101">New-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="0329f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0329f-102">SYNOPSIS</span></span>
<span data-ttu-id="0329f-103">Új PowerBI beágyazott kapacitást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0329f-103">Creates a new PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0329f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0329f-104">SYNTAX</span></span>

```
New-AzureRmPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [-Administrator] <String[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0329f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0329f-105">DESCRIPTION</span></span>
<span data-ttu-id="0329f-106">A New-AzureRmPowerBIEmbeddedCapacity parancsmag új PowerBI beágyazott kapacitást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0329f-106">The New-AzureRmPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="0329f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0329f-107">EXAMPLES</span></span>

### <span data-ttu-id="0329f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0329f-108">Example 1</span></span>
```
PS C:\> New-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity" -Location "West Central US" -Sku "A1" -Administrator admin@microsoft.com
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

<span data-ttu-id="0329f-109">Egy testcapacity nevű kapacitást hoz létre az Azure region West Central US és az erőforrás csoport testRG.</span><span class="sxs-lookup"><span data-stu-id="0329f-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="0329f-110">A kapacitás SKU szintje a1 lesz.</span><span class="sxs-lookup"><span data-stu-id="0329f-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="0329f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0329f-111">PARAMETERS</span></span>

### <span data-ttu-id="0329f-112">-Administrator</span><span class="sxs-lookup"><span data-stu-id="0329f-112">-Administrator</span></span>
<span data-ttu-id="0329f-113">Vesszővel elválasztott kapacitási nevek a kapacitás rendszergazdaként való beállításához</span><span class="sxs-lookup"><span data-stu-id="0329f-113">A comma separated capacity names to set as administrator on the capacity</span></span>

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

### <span data-ttu-id="0329f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0329f-114">-DefaultProfile</span></span>
<span data-ttu-id="0329f-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0329f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0329f-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="0329f-116">-Location</span></span>
<span data-ttu-id="0329f-117">Az Azure-régió, ahol a PowerBI beágyazott kapacitása meg van tárolva</span><span class="sxs-lookup"><span data-stu-id="0329f-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

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

### <span data-ttu-id="0329f-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0329f-118">-Name</span></span>
<span data-ttu-id="0329f-119">A PowerBI beágyazott kapacitásának neve</span><span class="sxs-lookup"><span data-stu-id="0329f-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="0329f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0329f-120">-ResourceGroupName</span></span>
<span data-ttu-id="0329f-121">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kapacitás tartozik</span><span class="sxs-lookup"><span data-stu-id="0329f-121">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="0329f-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="0329f-122">-Sku</span></span>
<span data-ttu-id="0329f-123">A kapacitáshoz tartozó SKU neve.</span><span class="sxs-lookup"><span data-stu-id="0329f-123">The name of the Sku for the capacity.</span></span>

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

### <span data-ttu-id="0329f-124">-Címke</span><span class="sxs-lookup"><span data-stu-id="0329f-124">-Tag</span></span>
<span data-ttu-id="0329f-125">A kulcs-érték párok egy kivonatoló táblázat formájában, amely a kapacitásban címkékként van beállítva.</span><span class="sxs-lookup"><span data-stu-id="0329f-125">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

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

### <span data-ttu-id="0329f-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0329f-126">-Confirm</span></span>
<span data-ttu-id="0329f-127">Arra kéri a felhasználót, hogy erősítse meg, hogy végrehajtja-e a műveletet</span><span class="sxs-lookup"><span data-stu-id="0329f-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="0329f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0329f-128">-WhatIf</span></span>
<span data-ttu-id="0329f-129">Leírja azokat a műveleteket, amelyeket az aktuális művelet a tényleges végrehajtás nélkül fog elvégezni</span><span class="sxs-lookup"><span data-stu-id="0329f-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="0329f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0329f-130">CommonParameters</span></span>
<span data-ttu-id="0329f-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0329f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0329f-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0329f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0329f-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0329f-133">INPUTS</span></span>

### <span data-ttu-id="0329f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0329f-134">System.String</span></span>

### <span data-ttu-id="0329f-135">System. string []</span><span class="sxs-lookup"><span data-stu-id="0329f-135">System.String[]</span></span>

### <span data-ttu-id="0329f-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0329f-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0329f-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0329f-137">OUTPUTS</span></span>

### <span data-ttu-id="0329f-138">Microsoft. Azure. Command. PowerBI. models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="0329f-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="0329f-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0329f-139">NOTES</span></span>

## <span data-ttu-id="0329f-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0329f-140">RELATED LINKS</span></span>

[<span data-ttu-id="0329f-141">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="0329f-141">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="0329f-142">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="0329f-142">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
