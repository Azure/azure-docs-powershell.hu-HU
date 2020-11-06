---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/resume-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Resume-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Resume-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: fe660d200c578d15fe8e23e7bfffc9a249651ae2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492248"
---
# <span data-ttu-id="208ad-101">Resume-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="208ad-101">Resume-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="208ad-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="208ad-102">SYNOPSIS</span></span>
<span data-ttu-id="208ad-103">Folytatja a PowerBI beágyazott kapacitások példányát.</span><span class="sxs-lookup"><span data-stu-id="208ad-103">Resumes an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="208ad-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="208ad-104">SYNTAX</span></span>

```
Resume-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="208ad-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="208ad-105">DESCRIPTION</span></span>
<span data-ttu-id="208ad-106">Az Resume-AzureRmPowerBIEmbeddedCapacity parancsmag a PowerBI beágyazott kapacitásának egy példányát folytatja.</span><span class="sxs-lookup"><span data-stu-id="208ad-106">The Resume-AzureRmPowerBIEmbeddedCapacity cmdlet resumes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="208ad-107">Példák</span><span class="sxs-lookup"><span data-stu-id="208ad-107">EXAMPLES</span></span>

### <span data-ttu-id="208ad-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="208ad-108">Example 1</span></span>
```
PS C:\> Resume-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
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

<span data-ttu-id="208ad-109">Ez a parancs folytatja a testcapacity nevű felfüggesztett kapacitást a resourcegroup testRG</span><span class="sxs-lookup"><span data-stu-id="208ad-109">This command will resume a paused capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="208ad-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="208ad-110">PARAMETERS</span></span>

### <span data-ttu-id="208ad-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="208ad-111">-Name</span></span>
<span data-ttu-id="208ad-112">A PowerBI beágyazott kapacitásának neve</span><span class="sxs-lookup"><span data-stu-id="208ad-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="208ad-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="208ad-113">-ResourceGroupName</span></span>
<span data-ttu-id="208ad-114">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kapacitás tartozik</span><span class="sxs-lookup"><span data-stu-id="208ad-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="208ad-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="208ad-115">-ResourceId</span></span>
<span data-ttu-id="208ad-116">Azure Resource ID</span><span class="sxs-lookup"><span data-stu-id="208ad-116">Azure resource ID</span></span>

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

### <span data-ttu-id="208ad-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="208ad-117">-InputObject</span></span>
<span data-ttu-id="208ad-118">A csővezeték beviteli objektuma</span><span class="sxs-lookup"><span data-stu-id="208ad-118">Input object for Piping</span></span>

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

### <span data-ttu-id="208ad-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="208ad-119">-Confirm</span></span>
<span data-ttu-id="208ad-120">Arra kéri a felhasználót, hogy erősítse meg, hogy végrehajtja-e a műveletet</span><span class="sxs-lookup"><span data-stu-id="208ad-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="208ad-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="208ad-121">-WhatIf</span></span>
<span data-ttu-id="208ad-122">Leírja azokat a műveleteket, amelyeket az aktuális művelet a tényleges végrehajtás nélkül fog elvégezni</span><span class="sxs-lookup"><span data-stu-id="208ad-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="208ad-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="208ad-123">CommonParameters</span></span>
<span data-ttu-id="208ad-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="208ad-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="208ad-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="208ad-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="208ad-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="208ad-126">INPUTS</span></span>

### <span data-ttu-id="208ad-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="208ad-127">None</span></span>
<span data-ttu-id="208ad-128">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="208ad-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="208ad-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="208ad-129">OUTPUTS</span></span>

### <span data-ttu-id="208ad-130">Microsoft. Azure. Command. PowerBI. models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="208ad-130">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="208ad-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="208ad-131">NOTES</span></span>

## <span data-ttu-id="208ad-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="208ad-132">RELATED LINKS</span></span>

[<span data-ttu-id="208ad-133">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="208ad-133">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="208ad-134">Felfüggesztés – AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="208ad-134">Suspend-AzureRmPowerBIEmbeddedCapacity</span></span>](./Suspend-AzureRmPowerBIEmbeddedCapacity.md)
