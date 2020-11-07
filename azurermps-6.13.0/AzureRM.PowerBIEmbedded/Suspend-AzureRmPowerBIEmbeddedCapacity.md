---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/suspend-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Suspend-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Suspend-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: c95019c253a4ecb6c442c9f88262f536c4590a83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672588"
---
# <span data-ttu-id="e7825-101">Suspend-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e7825-101">Suspend-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="e7825-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e7825-102">SYNOPSIS</span></span>
<span data-ttu-id="e7825-103">Felfüggeszti a PowerBI beágyazott kapacitás példányát.</span><span class="sxs-lookup"><span data-stu-id="e7825-103">Suspends an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7825-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e7825-104">SYNTAX</span></span>

### <span data-ttu-id="e7825-105">ByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e7825-105">ByNameAndResourceGroup (Default)</span></span>
```
Suspend-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7825-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e7825-106">ByResourceId</span></span>
```
Suspend-AzureRmPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7825-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e7825-107">ByInputObject</span></span>
```
Suspend-AzureRmPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7825-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e7825-108">DESCRIPTION</span></span>
<span data-ttu-id="e7825-109">Az Suspend-AzureRmPowerBIEmbeddedCapacity parancsmag felfüggeszti a PowerBI beágyazott kapacitásának példányát</span><span class="sxs-lookup"><span data-stu-id="e7825-109">The Suspend-AzureRmPowerBIEmbeddedCapacity cmdlet suspends an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="e7825-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e7825-110">EXAMPLES</span></span>

### <span data-ttu-id="e7825-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e7825-111">Example 1</span></span>
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

<span data-ttu-id="e7825-112">Ez a parancs felfüggeszti a testcapacity nevű aktív kapacitást a resourcegroup testgroup</span><span class="sxs-lookup"><span data-stu-id="e7825-112">This command will suspend an active capacity named testcapacity in the resourcegroup testgroup</span></span>

## <span data-ttu-id="e7825-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e7825-113">PARAMETERS</span></span>

### <span data-ttu-id="e7825-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7825-114">-DefaultProfile</span></span>
<span data-ttu-id="e7825-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e7825-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7825-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7825-116">-InputObject</span></span>
<span data-ttu-id="e7825-117">A csővezeték beviteli objektuma</span><span class="sxs-lookup"><span data-stu-id="e7825-117">Input object for Piping</span></span>

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

### <span data-ttu-id="e7825-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e7825-118">-Name</span></span>
<span data-ttu-id="e7825-119">A PowerBI beágyazott kapacitásának neve</span><span class="sxs-lookup"><span data-stu-id="e7825-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="e7825-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7825-120">-PassThru</span></span>
<span data-ttu-id="e7825-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="e7825-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e7825-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7825-122">-ResourceGroupName</span></span>
<span data-ttu-id="e7825-123">Annak az Azure-erőforrás-csoportnak a neve, amelyhez a kapacitás tartozik</span><span class="sxs-lookup"><span data-stu-id="e7825-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="e7825-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7825-124">-ResourceId</span></span>
<span data-ttu-id="e7825-125">Azure Resource ID</span><span class="sxs-lookup"><span data-stu-id="e7825-125">Azure resource ID</span></span>

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

### <span data-ttu-id="e7825-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e7825-126">-Confirm</span></span>
<span data-ttu-id="e7825-127">Arra kéri a felhasználót, hogy erősítse meg, hogy végrehajtja-e a műveletet</span><span class="sxs-lookup"><span data-stu-id="e7825-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="e7825-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7825-128">-WhatIf</span></span>
<span data-ttu-id="e7825-129">Leírja azokat a műveleteket, amelyeket az aktuális művelet a tényleges végrehajtás nélkül fog elvégezni</span><span class="sxs-lookup"><span data-stu-id="e7825-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="e7825-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7825-130">CommonParameters</span></span>
<span data-ttu-id="e7825-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e7825-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7825-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7825-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7825-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7825-133">INPUTS</span></span>

### <span data-ttu-id="e7825-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e7825-134">System.String</span></span>

### <span data-ttu-id="e7825-135">Microsoft. Azure. Command. PowerBI. models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e7825-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>
<span data-ttu-id="e7825-136">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e7825-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="e7825-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7825-137">OUTPUTS</span></span>

### <span data-ttu-id="e7825-138">Microsoft. Azure. Command. PowerBI. models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e7825-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="e7825-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e7825-139">NOTES</span></span>

## <span data-ttu-id="e7825-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7825-140">RELATED LINKS</span></span>

[<span data-ttu-id="e7825-141">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e7825-141">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="e7825-142">Önéletrajz – AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e7825-142">Resume-AzureRmPowerBIEmbeddedCapacity</span></span>](./Resume-AzureRmPowerBIEmbeddedCapacity.md)

