---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/remove-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Remove-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Remove-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: c2dc0333d2e991b21ac1a921465971f2131f5c3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500156"
---
# <span data-ttu-id="25429-101">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="25429-101">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="25429-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="25429-102">SYNOPSIS</span></span>
<span data-ttu-id="25429-103">A PowerBI beágyazott kapacitás példányának törlése</span><span class="sxs-lookup"><span data-stu-id="25429-103">Deletes an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25429-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="25429-104">SYNTAX</span></span>

### <span data-ttu-id="25429-105">ByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="25429-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25429-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="25429-106">ByResourceId</span></span>
```
Remove-AzureRmPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25429-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="25429-107">ByInputObject</span></span>
```
Remove-AzureRmPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25429-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="25429-108">DESCRIPTION</span></span>
<span data-ttu-id="25429-109">A Remove-AzureRmPowerBIEmbeddedCapacity parancsmag törli a PowerBI beágyazott kapacitású példányát</span><span class="sxs-lookup"><span data-stu-id="25429-109">The Remove-AzureRmPowerBIEmbeddedCapacity cmdlet deletes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="25429-110">Példák</span><span class="sxs-lookup"><span data-stu-id="25429-110">EXAMPLES</span></span>

### <span data-ttu-id="25429-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="25429-111">Example 1</span></span>
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

<span data-ttu-id="25429-112">Ez a parancs eltávolítja a testcapacity nevű kapacitást a resourcegroup testRG</span><span class="sxs-lookup"><span data-stu-id="25429-112">This command will remove the capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="25429-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="25429-113">PARAMETERS</span></span>

### <span data-ttu-id="25429-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25429-114">-DefaultProfile</span></span>
<span data-ttu-id="25429-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="25429-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25429-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25429-116">-InputObject</span></span>
<span data-ttu-id="25429-117">A csővezeték beviteli objektuma</span><span class="sxs-lookup"><span data-stu-id="25429-117">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25429-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="25429-118">-Name</span></span>
<span data-ttu-id="25429-119">A PowerBI beágyazott kapacitásának neve</span><span class="sxs-lookup"><span data-stu-id="25429-119">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25429-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25429-120">-PassThru</span></span>
<span data-ttu-id="25429-121">Visszaadja a törölt kapacitás adatait, ha a művelet sikeresen befejeződött</span><span class="sxs-lookup"><span data-stu-id="25429-121">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="25429-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25429-122">-ResourceGroupName</span></span>
<span data-ttu-id="25429-123">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kapacitás tartozik</span><span class="sxs-lookup"><span data-stu-id="25429-123">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25429-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25429-124">-ResourceId</span></span>
<span data-ttu-id="25429-125">Azure Resource ID</span><span class="sxs-lookup"><span data-stu-id="25429-125">Azure resource ID</span></span>

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

### <span data-ttu-id="25429-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="25429-126">-Confirm</span></span>
<span data-ttu-id="25429-127">Arra kéri a felhasználót, hogy erősítse meg, hogy végrehajtja-e a műveletet</span><span class="sxs-lookup"><span data-stu-id="25429-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="25429-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25429-128">-WhatIf</span></span>
<span data-ttu-id="25429-129">Leírja azokat a műveleteket, amelyeket az aktuális művelet a tényleges végrehajtás nélkül fog elvégezni</span><span class="sxs-lookup"><span data-stu-id="25429-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="25429-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25429-130">CommonParameters</span></span>
<span data-ttu-id="25429-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="25429-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25429-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25429-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25429-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="25429-133">INPUTS</span></span>

### <span data-ttu-id="25429-134">System. String</span><span class="sxs-lookup"><span data-stu-id="25429-134">System.String</span></span>

### <span data-ttu-id="25429-135">Microsoft. Azure. Command. PowerBI. models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="25429-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>
<span data-ttu-id="25429-136">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="25429-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="25429-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25429-137">OUTPUTS</span></span>

### <span data-ttu-id="25429-138">Microsoft. Azure. Command. PowerBI. models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="25429-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="25429-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="25429-139">NOTES</span></span>

## <span data-ttu-id="25429-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25429-140">RELATED LINKS</span></span>

[<span data-ttu-id="25429-141">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="25429-141">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="25429-142">Új – AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="25429-142">New-AzureRmPowerBIEmbeddedCapacity</span></span>](./New-AzureRmPowerBIEmbeddedCapacity.md)
