---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/suspend-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Suspend-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Suspend-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: fd50133d4919c52f314ccb7e306a022712e552c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492241"
---
# <span data-ttu-id="83d35-101">Suspend-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="83d35-101">Suspend-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="83d35-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="83d35-102">SYNOPSIS</span></span>
<span data-ttu-id="83d35-103">Felfüggeszti a PowerBI beágyazott kapacitás példányát.</span><span class="sxs-lookup"><span data-stu-id="83d35-103">Suspends an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83d35-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="83d35-104">SYNTAX</span></span>

```
Suspend-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="83d35-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="83d35-105">DESCRIPTION</span></span>
<span data-ttu-id="83d35-106">Az Suspend-AzureRmPowerBIEmbeddedCapacity parancsmag felfüggeszti a PowerBI beágyazott kapacitásának példányát</span><span class="sxs-lookup"><span data-stu-id="83d35-106">The Suspend-AzureRmPowerBIEmbeddedCapacity cmdlet suspends an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="83d35-107">Példák</span><span class="sxs-lookup"><span data-stu-id="83d35-107">EXAMPLES</span></span>

### <span data-ttu-id="83d35-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="83d35-108">Example 1</span></span>
```
PS C:\> Suspend-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Paused
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="83d35-109">Ez a parancs felfüggeszti a testcapacity nevű aktív kapacitást a resourcegroup testgroup</span><span class="sxs-lookup"><span data-stu-id="83d35-109">This command will suspend an active capacity named testcapacity in the resourcegroup testgroup</span></span>

## <span data-ttu-id="83d35-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="83d35-110">PARAMETERS</span></span>

### <span data-ttu-id="83d35-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="83d35-111">-Name</span></span>
<span data-ttu-id="83d35-112">A PowerBI beágyazott kapacitásának neve</span><span class="sxs-lookup"><span data-stu-id="83d35-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="83d35-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83d35-113">-ResourceGroupName</span></span>
<span data-ttu-id="83d35-114">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kapacitás tartozik</span><span class="sxs-lookup"><span data-stu-id="83d35-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="83d35-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83d35-115">-ResourceId</span></span>
<span data-ttu-id="83d35-116">Azure Resource ID</span><span class="sxs-lookup"><span data-stu-id="83d35-116">Azure resource ID</span></span>

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

### <span data-ttu-id="83d35-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83d35-117">-InputObject</span></span>
<span data-ttu-id="83d35-118">A csővezeték beviteli objektuma</span><span class="sxs-lookup"><span data-stu-id="83d35-118">Input object for Piping</span></span>

```yaml
Type: PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83d35-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="83d35-119">-Confirm</span></span>
<span data-ttu-id="83d35-120">Arra kéri a felhasználót, hogy erősítse meg, hogy végrehajtja-e a műveletet</span><span class="sxs-lookup"><span data-stu-id="83d35-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="83d35-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83d35-121">-WhatIf</span></span>
<span data-ttu-id="83d35-122">Leírja azokat a műveleteket, amelyeket az aktuális művelet a tényleges végrehajtás nélkül fog elvégezni</span><span class="sxs-lookup"><span data-stu-id="83d35-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="83d35-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83d35-123">CommonParameters</span></span>
<span data-ttu-id="83d35-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="83d35-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83d35-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83d35-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83d35-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="83d35-126">INPUTS</span></span>

### <span data-ttu-id="83d35-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="83d35-127">None</span></span>
<span data-ttu-id="83d35-128">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="83d35-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="83d35-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83d35-129">OUTPUTS</span></span>

### <span data-ttu-id="83d35-130">Microsoft. Azure. Command. PowerBI. models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="83d35-130">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="83d35-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="83d35-131">NOTES</span></span>

## <span data-ttu-id="83d35-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83d35-132">RELATED LINKS</span></span>

[<span data-ttu-id="83d35-133">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="83d35-133">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="83d35-134">Önéletrajz – AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="83d35-134">Resume-AzureRmPowerBIEmbeddedCapacity</span></span>](./Resume-AzureRmPowerBIEmbeddedCapacity.md)

