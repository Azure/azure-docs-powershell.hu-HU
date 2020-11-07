---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/remove-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Remove-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Remove-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: bbdfe43b4f6cad72432c85876c71bcd34a9a371c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93678964"
---
# <span data-ttu-id="8e958-101">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="8e958-101">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="8e958-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8e958-102">SYNOPSIS</span></span>
<span data-ttu-id="8e958-103">A PowerBI beágyazott kapacitás példányának törlése</span><span class="sxs-lookup"><span data-stu-id="8e958-103">Deletes an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e958-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8e958-104">SYNTAX</span></span>

```
Remove-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="8e958-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8e958-105">DESCRIPTION</span></span>
<span data-ttu-id="8e958-106">A Remove-AzureRmPowerBIEmbeddedCapacity parancsmag törli a PowerBI beágyazott kapacitású példányát</span><span class="sxs-lookup"><span data-stu-id="8e958-106">The Remove-AzureRmPowerBIEmbeddedCapacity cmdlet deletes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="8e958-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8e958-107">EXAMPLES</span></span>

### <span data-ttu-id="8e958-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8e958-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG"
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

<span data-ttu-id="8e958-109">Ez a parancs eltávolítja a testcapacity nevű kapacitást a resourcegroup testRG</span><span class="sxs-lookup"><span data-stu-id="8e958-109">This command will remove the capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="8e958-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8e958-110">PARAMETERS</span></span>

### <span data-ttu-id="8e958-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e958-111">-ResourceGroupName</span></span>
<span data-ttu-id="8e958-112">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kapacitás tartozik</span><span class="sxs-lookup"><span data-stu-id="8e958-112">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="8e958-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8e958-113">-Name</span></span>
<span data-ttu-id="8e958-114">A PowerBI beágyazott kapacitásának neve</span><span class="sxs-lookup"><span data-stu-id="8e958-114">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="8e958-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e958-115">-ResourceId</span></span>
<span data-ttu-id="8e958-116">Azure Resource ID</span><span class="sxs-lookup"><span data-stu-id="8e958-116">Azure resource ID</span></span>

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

### <span data-ttu-id="8e958-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e958-117">-InputObject</span></span>
<span data-ttu-id="8e958-118">A csővezeték beviteli objektuma</span><span class="sxs-lookup"><span data-stu-id="8e958-118">Input object for Piping</span></span>

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

### <span data-ttu-id="8e958-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e958-119">-PassThru</span></span>
<span data-ttu-id="8e958-120">Visszaadja a törölt kapacitás adatait, ha a művelet sikeresen befejeződött</span><span class="sxs-lookup"><span data-stu-id="8e958-120">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="8e958-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8e958-121">-Confirm</span></span>
<span data-ttu-id="8e958-122">Arra kéri a felhasználót, hogy erősítse meg, hogy végrehajtja-e a műveletet</span><span class="sxs-lookup"><span data-stu-id="8e958-122">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="8e958-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e958-123">-WhatIf</span></span>
<span data-ttu-id="8e958-124">Leírja azokat a műveleteket, amelyeket az aktuális művelet a tényleges végrehajtás nélkül fog elvégezni</span><span class="sxs-lookup"><span data-stu-id="8e958-124">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="8e958-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e958-125">CommonParameters</span></span>
<span data-ttu-id="8e958-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8e958-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e958-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e958-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e958-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e958-128">INPUTS</span></span>

### <span data-ttu-id="8e958-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="8e958-129">None</span></span>
<span data-ttu-id="8e958-130">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="8e958-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8e958-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e958-131">OUTPUTS</span></span>

### <span data-ttu-id="8e958-132">Microsoft. Azure. Command. PowerBI. models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="8e958-132">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="8e958-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8e958-133">NOTES</span></span>

## <span data-ttu-id="8e958-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e958-134">RELATED LINKS</span></span>

[<span data-ttu-id="8e958-135">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="8e958-135">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="8e958-136">Új – AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="8e958-136">New-AzureRmPowerBIEmbeddedCapacity</span></span>](./New-AzureRmPowerBIEmbeddedCapacity.md)
